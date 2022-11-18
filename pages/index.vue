

<script setup lang="ts">
import { ref, computed } from 'vue'

  
    
useHead({
  title: 'Slaid - Arhiveerimine & Digitaliseerimine',
  meta: [
    { name: 'og:title', content: 'Slaid - Arhiveerimine & Digitaliseerimine' },
    { name: 'og:site_name', content: 'Slaid.ee' },
    { name: 'og:locale', content: 'et_EE' },
    // { name: 'og:locale:alternative', content: '' },
    { name: 'og:url', content: 'https://slaid.ee' },
    { name: 'og:type', content: 'article' }, // website
    { name: 'og:description', content: 'Slaid.ee pakub professionaalsel tasemel videokonversiooni, digitaliseerimise ja arhiveerimise teenuseid.' },
    { name: 'description', content: '' },
    { name: 'og:image', content: '' },
    { name: 'og:image:secure_url', content: '' },
    { name: 'og:image:type', content: '' },
    { name: 'og:image:width', content: '1200' },
    { name: 'og:image:height', content: '627' },
    { name: 'article:published_time', content: '' },
    { name: 'article:author', content: '' },
    { name: 'article:section', content: '' },
    { name: 'article:tag', content: '' },
    { name: 'google-site-verification', content: '' },
    { name: 'robots', content: 'nofollow,noindex' }, //TBR ---
    { name: 'rating', content: '' },
  ],
  bodyAttrs: {
    class: 'test'
  },
  //script: [ { children: 'console.log(\'Hello world\')' } ]
})


  const client = useSupabaseClient()
  async function createOrder() {
    const { data, error } = await client
      .from("orders")
      .insert([{ 
        source: "website", 
        name: customer.value.name,
        phone: customer.value.phone,
        email: customer.value.email,
        reference: paymentReference
      }]);
    if (error) return error;
    return { id: data[0].id, error };
  }

    /* ref() and computed() are auto-imported */
    const date = ref(new Date().getFullYear())
    const randomString = Math.random().toString(36).slice(3, 9);
    const randomTime = Math.random()*1000
    const paymentReference = (randomString+randomTime).replaceAll(".","").slice(1, 10)

    const notification = ref({
      tag: "Oi?!",
      description: "Veendu, et kõik sisestatud andmed oleksid korrektsed.",
      ref: "#order",
      show: false
    })

    let questions = ref([
      {
        question: "Kas meil on kvaliteedigarantii?",
        answer: "Paraku sõltub töö tulemuslikkus suurel määral materjali kvaliteedist, mille üle meil otsest kontrolli pole. Digitaliseerimisega enamasti probleeme ei esine, aga kui materjali sisu pole loetav, siis selgitame välja, mis võiks olla põhjuseks ning anname endast parima, et selle loetavust parandada."
      },
      {
        question: "Mida kujutab endast kingitus?",
        answer: "Kui soovite teha kingitust endale või lähedastele, siis aitame teid pakendamise, soovi korral kirjakese või õnnitluskaardiga. Soovi korral saab kinkida ka kinkekaardi. Lähtume eelkõige teie soovidest ja leiame lahenduse."
      },
      {
        question: "Mis siis, kui saadetud andmed on autoriõigustega kaitstud?",
        answer: "Autoriõigus paragraaf ? lg ? kohaselt on ostetud teose omanikul õigus teha tootest koopiaid isiklikuks kasutamiseks, sh. lindistada telekanalitel näidatavaid filme, juhul kui neil on olnud teose autorilt või lubatud edasimüüjalt ostetud/saadud koopia. Meie, Slaid, teostame kvaliteedikontrolli väikeste videolõikude põhjal (kui ei ole palutud teisiti) ning ei säilita koopiaid tehtud töödest. Teie materjal, teie asi."
      },
      {
        question: "Kui kiiresti oma digitaliseeritud materjali kätte saan?",
        answer: "Kolme kuni kümne tööpäeva jooksul sõltuvalt töö mahust ning transpordivõrgustiku koormusest."
      },
    ])

    let products = ref([
      {
        name: "Kaks parimat",
        description: "2 eset*",
        quantity: 2,
        price: 30,
        visible: true
      },
      {
        name: "Kümme parimat",
        description: "10 eset*",
        quantity: 10,
        price: 135,
        visible: true
      },
      {
        name: "Riiulitäis",
        description: "20 eset*",
        quantity: 20,
        price: 250,
        visible: true
      },
      {
        name: "Kogu arhiiv",
        description: "40 eset*",
        quantity: 40,
        price: 500,
        selected: true
      },
      {
        name: "Konsultatsioon",
        description: "kuni 15min",
        quantity: 1,
        price: 0,
        visible: true
      },
      {
        name: "Konsultatsioon",
        description: "kuni 15min",
        quantity: 1,
        price: 0,
        visible: false
      }
    ])

    interface Provider {
      region: string,
      country: string,
      locale: string,
      company: string
    }
    const cart = ref({
      ids: [],
      items: [],
      sum: 0
    });

    // watch works directly on a ref
    watch(() => cart.value.ids, async (newList, oldList) => {
      cart.value.items = [];
      cart.value.sum = 0;
      if (newList.length > 0) {
        cart.value.ids.forEach(id => {
          let product = products.value[id];
          console.log(product)
          cart.value.items.push(product)
          cart.value.sum += product.price
        });
      }
    })
    const customer = ref({
      name: "",
      email: "",
      phone: ""
    })

    function sleep (time) {
      return new Promise((resolve) => setTimeout(resolve, time));
    }

    function sendNotification(description:string) {
      notification.value.description = description;
      notification.value.show = true;
      sleep(2900).then(() => {
        notification.value.show = false;
      })
    }

    function placeOrder() {
      if(cart.value.items.length < 1) return sendNotification("Tundub, et teie ostukorv on tühi.");
      if(customer.value.email.length < 10) return sendNotification("Tundub, et teie e-posti aadress on vigane.");
      if(customer.value.name.length < 1) return sendNotification("Nimi on kohustuslik väli, et teaksime kellega edaspidi vestleme.");
      if(customer.value.phone.length < 7) return sendNotification("Tundub, et teie telefoninumber on vigane.");
      if(cart.value.sum > 0) {
        createOrder();
        let url = `https://payment.test.maksekeskus.ee/pay/1/link.html?shop=f7741ab2-7445-45f9-9af4-0d0408ef1e4c&amount=${ cart.value.sum }&reference=${ paymentReference }&country=ee&locale=et`;
        window.open(url);
      }
    }
</script>

<template>
  <div>
    <div v-show="notification.show" class="text-center py-4 lg:px-4 fixed translate-y-1/2 -translate-x-1/2 left-1/2">
      <div class="p-2 bg-red-800 items-center text-red-100 leading-none lg:rounded-full flex lg:inline-flex" role="alert">
        <span class="flex rounded-full bg-red-500 uppercase px-2 py-1 text-xs font-bold mr-3">{{ notification.tag }}</span>
        <span class="font-semibold mr-2 text-left flex-auto">{{ notification.description }}</span>
        <svg class="fill-current opacity-75 h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M12.95 10.707l.707-.707L8 4.343 6.586 5.757 10.828 10l-4.242 4.243L8 15.657l4.95-4.95z"/></svg>
      </div>
    </div>
    <Navigation />
  <section class="text-gray-600 body-font">
  <div class="container mx-auto flex px-5 py-6 md:py-24 md:flex-row flex-col-reverse items-center">
    <div class="lg:flex-grow md:w-1/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center">
      <h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-gray-900">Päästame oma
        <br class="hidden lg:inline-block">tuhmuvad mälestused
      </h1>
      <p class="mb-8 leading-relaxed">Kas teadsid, et VHS kassettide elueaks lubatakse tootjate poolt 10-15 aastat? Ajaga kahjustuvad kassettide magnetribad, mille tulemusena videokvaliteet langeb. Esimesi fotosid suudeti teha juba peaaegu 200 aastat tagasi, mis tähendab, et majapidamistes võib olla fotonegatiive, -positiive, slaide, paberfotosid ja muid andmekandjaid, millele on jäädvustatud meie esivanemate nooruspõlve hetki. Digitaliseerimine ja korrektne arhiveerimine suudab need mälestused igaveseks jäädvustada. Tee kingitus endale, oma lastele ja lähedastele, ning veendu, et mälestused saaksid korralikult arhiveeritud.</p>
      <div class="flex justify-center">
        <a href="#order">
          <button  class="flex ml-auto h-fit text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded">
            <p>Tellima</p>
          </button>
        </a>
        <button class="ml-4 flex h-fit text-gray-700 bg-gray-100 border-0 py-2 px-6 focus:outline-none hover:bg-gray-200 rounded">
          <p>Kliendid</p>
        </button>
      </div>
    </div>
    <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6">
      <img class="object-cover object-center rounded" alt="hero" :src="`img/${'hero-1440x1200'}.png`">
    </div>
  </div>
</section>

<section id="order" class="text-gray-600 body-font">
  <div class="container px-5 py-24 mx-auto">
    <div class="flex flex-col text-center w-full mb-10">
      <h1 class="sm:text-4xl text-3xl font-medium title-font mb-2 text-gray-900">Hinnakiri</h1>
      <p class="lg:w-2/3 mx-auto leading-relaxed text-base">Teame, et Teie mälestused on teie jaoks hindamatud, mis tõttu kasutame me oma töös parimaid võimalikke töövahendeid ja tehnoloogiaid. Meie eesmärk ja südamesoov on, et teie mälestused jääksid teid alatiseks saatma!</p>
    </div>
    <div class="lg:w-2/3 w-full mx-auto overflow-auto">
      <table class="table-auto w-full text-left whitespace-no-wrap">
        <thead>
          <tr>
            <th class="px-4 py-3 title-font tracking-wider font-medium text-gray-900 text-sm bg-gray-100 rounded-tl rounded-bl">Pakett</th>
            <th class="px-4 py-3 title-font tracking-wider font-medium text-gray-900 text-sm bg-gray-100">Kogus</th>
            <th class="px-4 py-3 title-font tracking-wider font-medium text-gray-900 text-sm bg-gray-100">
              Hind €
            </th>
            <th class="w-10 title-font tracking-wider font-medium text-gray-900 text-sm bg-gray-100 rounded-tr rounded-br"></th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(item, i) in products" :key="i">
            <td class="border-t-2 border-gray-200 px-4 py-3">{{ item.name }}</td>
            <td class="border-t-2 border-gray-200 px-4 py-3">{{ item.description }}</td>
            <td v-if="item.price == 0" class="border-t-2 border-gray-200 px-4 py-3 text-lg text-gray-900"><p style="font-size: 0.95rem;">TASUTA</p></td>
            <td v-else class="border-t-2 border-gray-200 px-4 py-3 text-lg text-gray-900"><p style="font-size: 0.95rem;">{{ item.price }}</p></td>
            <td class="border-t-2 border-gray-200 w-10 text-center">
              <input :id="item.name" type="checkbox" v-model="cart.ids" :value="i">
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="pt-2">
      <div v-if="cart.ids.length > 0" class="relative lg:w-2/3 w-full mx-auto">
        <label for="email" class="leading-7 text-sm text-gray-500">E-posti aadress</label>
        <input required v-model="customer.email" type="email" id="email" name="email" class="w-full bg-gray-100 rounded border border-gray-700 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-900 text-base outline-none text-gray-800 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out">
      </div>
      <div v-if="customer.email.length > 0 && cart.ids.length > 0" class="flex gap-4 relative lg:w-2/3 w-full mx-auto">
        <div class="w-1/2">
          <label for="name" class="leading-7 text-sm text-gray-500">Nimi</label>
          <input required v-model="customer.name" type="text" id="name" name="name" class="w-full bg-gray-100 rounded border border-gray-700 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-900 text-base outline-none text-gray-800 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out">
        </div>
        <div class="w-1/2">
          <label for="phone" class="leading-7 text-sm text-gray-500">Telefoninumber</label>
          <input required v-model="customer.phone" type="text" id="phone" name="phone" class="w-full bg-gray-100 rounded border border-gray-700 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-900 text-base outline-none text-gray-800 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out">
        </div>
      </div>
    </div>
    <div class="flex pl-4 mt-4 lg:w-2/3 w-full mx-auto">
      <div>
        <p>* ese ehk 1x videokassett, 2x audiokassett või 20x pilt</p>
        <a class="text-indigo-500 inline-flex items-center md:mb-2 lg:mb-0">Loe lisaks
          <svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 ml-2" viewBox="0 0 24 24" data-darkreader-inline-stroke="" style="--darkreader-inline-stroke:currentColor;">
            <path d="M5 12h14M12 5l7 7-7 7"></path>
          </svg>
        </a>
      </div>
      <button @click="placeOrder()" class="flex ml-auto h-fit text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded">
        <p>Telli</p>
      </button>
    </div>
  </div>
</section>

<section id="testimonials" class="text-gray-600 body-font">
  <div class="container px-5 py-24 mx-auto">
    <h1 class="text-3xl font-medium title-font text-gray-900 mb-12 text-center">Klientide tagasiside</h1>
    <div class="flex flex-wrap -m-4">
      <div class="p-4 md:w-1/2 w-full">
        <div class="h-full bg-gray-100 p-8 rounded">
          <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="block w-5 h-5 text-gray-400 mb-4" viewBox="0 0 975.036 975.036" data-darkreader-inline-fill="" style="--darkreader-inline-fill:currentColor;">
            <path d="M925.036 57.197h-304c-27.6 0-50 22.4-50 50v304c0 27.601 22.4 50 50 50h145.5c-1.9 79.601-20.4 143.3-55.4 191.2-27.6 37.8-69.399 69.1-125.3 93.8-25.7 11.3-36.8 41.7-24.8 67.101l36 76c11.6 24.399 40.3 35.1 65.1 24.399 66.2-28.6 122.101-64.8 167.7-108.8 55.601-53.7 93.7-114.3 114.3-181.9 20.601-67.6 30.9-159.8 30.9-276.8v-239c0-27.599-22.401-50-50-50zM106.036 913.497c65.4-28.5 121-64.699 166.9-108.6 56.1-53.7 94.4-114.1 115-181.2 20.6-67.1 30.899-159.6 30.899-277.5v-239c0-27.6-22.399-50-50-50h-304c-27.6 0-50 22.4-50 50v304c0 27.601 22.4 50 50 50h145.5c-1.9 79.601-20.4 143.3-55.4 191.2-27.6 37.8-69.4 69.1-125.3 93.8-25.7 11.3-36.8 41.7-24.8 67.101l35.9 75.8c11.601 24.399 40.501 35.2 65.301 24.399z"></path>
          </svg>
          <p class="leading-relaxed mb-6">Synth chartreuse iPhone lomo cray raw denim brunch everyday carry neutra before they sold out fixie 90's microdosing. Tacos pinterest fanny pack venmo, post-ironic heirloom try-hard pabst authentic iceland.</p>
          <a class="inline-flex items-center">
            <img alt="testimonial" :src="`img/${'Merli-156x156'}.png`" class="w-12 h-12 rounded-full flex-shrink-0 object-cover object-center">
            <span class="flex-grow flex flex-col pl-4">
              <span class="title-font font-medium text-gray-900">Merli Mirk</span>
              <span class="text-gray-500 text-sm">Vaimne tervendaja</span>
            </span>
          </a>
        </div>
      </div>
      <div class="p-4 md:w-1/2 w-full">
        <div class="h-full bg-gray-100 p-8 rounded">
          <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="block w-5 h-5 text-gray-400 mb-4" viewBox="0 0 975.036 975.036" data-darkreader-inline-fill="" style="--darkreader-inline-fill:currentColor;">
            <path d="M925.036 57.197h-304c-27.6 0-50 22.4-50 50v304c0 27.601 22.4 50 50 50h145.5c-1.9 79.601-20.4 143.3-55.4 191.2-27.6 37.8-69.399 69.1-125.3 93.8-25.7 11.3-36.8 41.7-24.8 67.101l36 76c11.6 24.399 40.3 35.1 65.1 24.399 66.2-28.6 122.101-64.8 167.7-108.8 55.601-53.7 93.7-114.3 114.3-181.9 20.601-67.6 30.9-159.8 30.9-276.8v-239c0-27.599-22.401-50-50-50zM106.036 913.497c65.4-28.5 121-64.699 166.9-108.6 56.1-53.7 94.4-114.1 115-181.2 20.6-67.1 30.899-159.6 30.899-277.5v-239c0-27.6-22.399-50-50-50h-304c-27.6 0-50 22.4-50 50v304c0 27.601 22.4 50 50 50h145.5c-1.9 79.601-20.4 143.3-55.4 191.2-27.6 37.8-69.4 69.1-125.3 93.8-25.7 11.3-36.8 41.7-24.8 67.101l35.9 75.8c11.601 24.399 40.501 35.2 65.301 24.399z"></path>
          </svg>
          <p class="leading-relaxed mb-6">Synth chartreuse iPhone lomo cray raw denim brunch everyday carry neutra before they sold out fixie 90's microdosing. Tacos pinterest fanny pack venmo, post-ironic heirloom try-hard pabst authentic iceland.</p>
          <a class="inline-flex items-center">
            <img alt="testimonial" :src="`img/${'s2m-156x156'}.png`" class="w-12 h-12 rounded-full flex-shrink-0 object-cover object-center">
            <span class="flex-grow flex flex-col pl-4">
              <span class="title-font font-medium text-gray-900">säm</span>
              <span class="text-gray-500 text-sm">Muusik & suunamudija</span>
            </span>
          </a>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="">
  <div class="py-8 px-4 mx-auto max-w-screen-xl sm:py-16 lg:px-6">
    <h1 class="text-3xl font-medium title-font text-gray-900 mb-12 text-center">Levinud küsimused</h1>
      <div class="flex flex-wrap pt-8 text-left border-t border-gray-200">
        <div v-for="(faq, i) in questions" :key="i" class="mb-10 w-1/2">
          <div class="mx-4">
            <h3 class="flex items-center mb-4 text-lg font-medium text-gray-900 dark:text-white">
                <svg class="mr-2 w-5 h-5 text-gray-500" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-8-3a1 1 0 00-.867.5 1 1 0 11-1.731-1A3 3 0 0113 8a3.001 3.001 0 01-2 2.83V11a1 1 0 11-2 0v-1a1 1 0 011-1 1 1 0 100-2zm0 8a1 1 0 100-2 1 1 0 000 2z" clip-rule="evenodd"></path></svg>
                
                <span class="title-font font-medium text-gray-900">{{ faq.question }}</span>
            </h3>
            <p class="text-gray-500">{{ faq. answer }}</p>
          </div>
        </div>
      </div>
  </div>
</section>

<BlogPostCta />

<section class="text-gray-600 body-font">
  <div class="container px-5 py-24 mx-auto">
    <div class="lg:w-2/3 flex flex-col sm:flex-row sm:items-center items-start mx-auto">
      <h1 class="flex-grow sm:pr-16 text-2xl font-medium title-font text-gray-900">Veendu, et väärt mälestused saavad talletatud, sest noorus ei tule iial tagasi.</h1>
      <a href="#order">
        <button class="flex ml-auto h-fit text-white bg-indigo-500 border-0 mt-6 sm:mt-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded">
          <p>Tellima</p>
        </button>
      </a>
    </div>
  </div>
</section>

<BottomNavigation />

</div>
</template>
