<script setup lang="ts">

let articles = ref([
    {
        tags: [
            {
                name: "Slaidid"
            },
            {
                name: "Negatiivid"
            },
            {
                name: "Positiivid"
            },
        ],
        title: "Kuidas organiseerida pildiarhiivi?",
        description: "Meile kõigile meeldib pildistada ja pildistamine oli võimalik juba enne nutitelefonide teket. Paraku jäävad tehtud pildid tihtipeale vanasse seadmesse, pildistamisäppi, kastidesse, albumitesse, ümbrikutesse ja kuhu iganes veel, kuni lõpuks polegi võimalik olnud aegadest kronoloogilist ülevaadet saada. Samuti kipuvad digitaliseerimata pildid aja jooksul tuhmuma. Et sedasi ei läheks, panime kokku väikese õpetuse, kuidas pildimaterjali organiseerida.",
        cta: "Loe edasi",
        href: "photo-archiving",
        views: 0,
        comments: 0,
        author: {
            name: "Kaspar Jõeveer",
            title: "tehnik / kolumnist",
            picture: "Kaspar-156x156.png"
        }
    },
    {
        tags: [
            {
                name: "Pildid"
            },
            {
                name: "Fotod"
            },
            {
                name: "Kingitus"
            },
            {
                name: "Positiiv"
            },
            {
                name: "Negatiiv"
            },
            {
                name: "Diapositiiv"
            },
        ],
        title: "Kink vanematele",
        description: "Jõulud on tasapisi lähenemas. See tähendab, et jälle on vaja lagedale tulla terve posu kingiideedega. Kui kampsun, ornament või raamat enam originaalsed pole, siis soovitame kinkida mälestusi. Slaidid, positiivid, negatiivid, fotod ja muud füüsilisel kujul pildid annavad võimaluse vaadata tagasi kogetud elule ning hinnata selle kirevust. Igavesena tundunud hetked asendusid tihtipeale kild-killu kaupa uutega ning vaade tagasi aitab seda selgemini mõista.",
        cta: "Loe edasi",
        href: "parent-gift-idea",
        views: 0,
        comments: 0,
        author: {
            name: "Kaspar Jõeveer",
            title: "tehnik / kolumnist",
            picture: "Kaspar-156x156.png"
        }
    },
    {
        tags: [
            {
                name: "VHS"
            },
            {
                name: "Standardid"
            },
            {
                name: "Digitaliseerimine"
            },
            {
                name: "Konverteerimine"
            },
        ],
        title: "Digitaliseerimise terminoloogia",
        description: "Andmekandjate ajalugu on kirev ning veelgi kirevam on nendega seotud sõnavara. Selgitame, mida levinumad väljendid tähendavad, et saaksite meie tegemistest parema ülevaate.",
        cta: "Loe edasi",
        href: "digitizing-terminology",
        views: 0,
        comments: 0,
        author: {
            name: "Kaspar Jõeveer",
            title: "tehnik / kolumnist",
            picture: "Kaspar-156x156.png"
        }
    },
    {
        tags: [
            {
                name: "VHS"
            },
            {
                name: "VHS-C"
            },
            {
                name: "VCR"
            },
            {
                name: "Ajalugu"
            },
        ],
        title: "VHS-i ajalugu",
        description: "Enamik meist teab, mis tunne oli videot kassettidelt vaadata, kuid vähem teatakse, kuidas saavutasid videokassetid säärase populaarsuse. Kuigi nüüdseks on VHS-i hiilgeaeg läbi, toovad mälestused kassettidest siiski naeratuse suule.",
        cta: "Loe edasi",
        href: "vhs-vcr-history",
        views: 0,
        comments: 0,
        author: {
            name: "Kaspar Jõeveer",
            title: "tehnik / kolumnist",
            picture: "Kaspar-156x156.png"
        }
    },
])

useHead({
title: '"Sõbrapäeva kingitus | Slaid.ee',
meta: [
    { name: 'og:title', content: 'Sõbrapäeva kingitus' },
    { name: 'og:site_name', content: 'Slaid.ee' },
    { name: 'og:locale', content: 'et_EE' },
    // { name: 'og:locale:alternative', content: '' },
    { name: 'og:url', content: 'https://slaid.ee/blog/friend-gift-idea' },
    { name: 'og:type', content: 'article' }, // website
    { name: 'og:description', content: 'Otsid head kingiideed headele sõpradele? Ehk tasuks üle vaadata pildialbumid? Tihti juhtub, et mõni jäädvustatud hetk jääb sõpradega jagamata ning see kujutab endast suurepärast võimalust sõbra üllatamiseks. Oleme kokku piltidega seonduvad kingiideed, et saaksite lihtsa vaevaga inspiratsiooni ammutada.' },
    { name: 'description', content: 'Otsid head kingiideed headele sõpradele? Ehk tasuks üle vaadata pildialbumid? Tihti juhtub, et mõni jäädvustatud hetk jääb sõpradega jagamata ning see kujutab endast suurepärast võimalust sõbra üllatamiseks. Oleme kokku piltidega seonduvad kingiideed, et saaksite lihtsa vaevaga inspiratsiooni ammutada.' },
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
</script>
<template>
    <Navigation />

    <div class="container mx-auto px-5 py-6 md:py-24 md:px-24 items-center text-lg">
        <h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-gray-900"><b>S&otilde;brap&auml;eva kingitus</b></h1>
<p>Ilusasse s&otilde;prusesse mahub palju, kuid kuidas s&otilde;brale tema olulisust kommunikeerida? Vanaemad kingivad lapselastele sokke, kuid s&otilde;pradele sellest ei piisa. Kui pole traditsiooni k&auml;ia koos s&ouml;&ouml;mas v&otilde;i baaris, siis peaks ju kingitus olema midagi isiklikku, eks? Midagi, mis v&otilde;tab tabavalt kokku sideme kahe inimese vahel. Ja mis oleks parem selle s&otilde;prussideme n&auml;itamiseks kui fotokingitus? Fotokingitus, mis j&auml;&auml;dvustaks teie p&otilde;nevaid &uuml;hiseid l&auml;bielamisi.</p>
<p>Siis on asi klaaritud &ndash; isikustatud fotokingitus sinu on &uuml;lim viis &ouml;elda, et oleme selles maailmas koos ja saame olla &uuml;ksteisele kindlad.</p>
<p>Kuid kust alustada, kui m&otilde;elda parima piltkingituse peale? Meil on m&otilde;tteid!</p>
<h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>DIGITAALNE KOLLAAŽ</b></h2>
<p>Kes &uuml;tleb, filmi&otilde;htul peaks filmi vaatama? Selle asemel pane kokku digitaalne kollaaž k&otilde;igist oma s&otilde;braga v&auml;ljas&otilde;itudest &ndash; hommikus&ouml;&ouml;gid, &otilde;htud v&auml;ljas, puhkused, ujukid, spordi&uuml;ritused jne. &Uuml;kski romantiline kom&ouml;&ouml;dia ei too teist v&auml;lja nii palju naeru ja pisaraid kui teie &uuml;hine tee.</p>
<h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>ISIKLIKUD KLEEPSUD</b></h2>
<p>Kes meist ei armastaks vahvaid kleepse? &Uuml;ksk&otilde;ik, mis vanuses me oleme, kleepsud on ideaalne viis v&uuml;rtsitada vanu ja igavaid veepudeleid, s&uuml;learvuteid, p&auml;evikuid v&otilde;i muud. Niisiis, miks mitte l&otilde;butseda kleepsudega ja luua m&otilde;ned parimate s&otilde;prade kleepsud? M&otilde;ni vahva pidu meenutav kleeps veepudelil v&otilde;ib meenutada k&otilde;iki &ouml;id, mil see mida sa j&otilde;id polnud vesi, aga kindlasti oleks pidanud olema.</p>
<h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>VEINIKLAASID JA &Otilde;LLEKANNUD</b></h2>
<p>Olgem ausad. Kui see on kingitus su parimale s&otilde;brale, siis on v&auml;ga hea v&otilde;imalus, et enamus sinu fotom&auml;lestusi keerleb joomise &uuml;mber. Ja selles pole midagi halba. Kleepsud isiklikult &otilde;llekannul v&otilde;i veiniklaasil on suurep&auml;rane meenutamaks eelmisi suurs&uuml;ndmusi j&auml;rgmistel.</p>
<h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>KOHVIKRUUSID</b></h2>
<p>Hommikud ei ole k&otilde;igile ja kohvi ka mitte, aga kui su parimale meeldib hommikul v&auml;ike kofeiinilaks, siis on isikustatud kohvikruus suurep&auml;rane kingiidee s&otilde;pradele. Topeltshotiga latte oma isiklikult kruusist sobib suurep&auml;raselt saatemaks &uuml;ht head hommikust k&otilde;museanssi.</p>
<h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>S&Otilde;NUM PUDELIS</b></h2>
<p>Kas soovite oma isikup&auml;rastatud fotokingitust veidi loomingulisemaks muuta? Kirjutage kiri, pistke see pudelisse ja keerutage selle &uuml;mber posu erinevaid fotosid. Kui ka pudeli &auml;ra kaunistate, &uuml;llatate oma s&otilde;pra kindlasti oma originaalsusega.</p>
<h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>FOTOKOLLAAŽ</b></h2>
<p>T&auml;nap&auml;eval on digitaalfotode loominguliseks kohandamiseks palju v&otilde;imalusi. Kingi s&otilde;brale pikaajalise s&otilde;pruse puhul fototahvel. Kogu kokku m&otilde;ned l&otilde;busad fotod, kirjuta juurde v&auml;ike s&otilde;num v&otilde;i nali ja voil&agrave;, sul on h&auml;mmastav kingitus.</p>
<h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>PUITKUNST JA MAALID</b></h2>
<p>Milleks peatuda fotokollaažiga? T&auml;nap&auml;eval on v&otilde;imalik printida peaaegu k&otilde;igele. Seega, kui su s&otilde;brale meeldib maal&auml;hedane stiil, siis on puitesemetele printimine suurep&auml;rane viis kingituse isikup&auml;rasemaks muutmiseks. Samuti saab Youtube-i abil k&auml;elise osavuse ja lihtsate t&ouml;&ouml;riistadega valmistada isikustatud fotodega kuuma-aluseid ja muud p&otilde;nevat.</p>
<h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>R&Otilde;IVAD</b></h2>
<p>Mis &uuml;tleb parimatele s&otilde;pradele rohkem kui &uuml;ksteise n&auml;gude kandmine sokkidel? Igal juhul on fotodega riietus l&otilde;bus asi, mida kingituseks anda.&nbsp;</p>
<h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>L&Otilde;UENDIPRINT</b></h2>
<p>Mis on parem kunstiteos kui parim s&otilde;prus? Just nii, kuva oma parima s&otilde;bra meistriteost uhkelt oma kodus. Soovi korral saad kinkida sedasi ka tema lemmik kunstiteose, et ta saaks seda ilu iga p&auml;ev kogeda. Pildil&otilde;uendi kinkimisel veendu, et see sobiks kokku tema elamise ja isiksusega. Kui kink l&auml;heb t&auml;ppi, siis v&otilde;ib see kaunistada tema kodu aastaid.</p>
<h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>TEKID JA PADJAD</b></h2>
<p>L&otilde;bus viis s&otilde;pruse t&auml;histamiseks v&otilde;ib olla fotoprindiga teki- ja/v&otilde;i padjap&uuml;&uuml;rid. Eks ta ole pisut koomiline, kuid kingitus peakski ju pisut l&otilde;bus olema? Pealegi muudab see padjas&otilde;jad pisut l&otilde;busamaks.</p>
<h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>MIS J&Auml;RGMISEKS?</b></h2>
<p>Niisiis, n&uuml;&uuml;d, kui sul on m&otilde;istus seatud &uuml;hele (v&otilde;i m&otilde;nele) &uuml;laltoodud parima s&otilde;bra piltkingitustele, mis on j&auml;rgmine samm? Alustage sellest, et teil oleks piisavalt digifotosid, mille seast valida. Kuna t&auml;nap&auml;eva nutitelefonid on k&otilde;igi peamine pildiallikas, ei tohiks see olla liiga suur probleem; kui aga on vanu v&auml;ljaprinte, negatiive v&otilde;i polaroide, mida sa t&otilde;esti oma valitud fotodena kasutada tahad, siis tuleks need digitaliseerida. Seda saad teha ise v&otilde;i kasutades meie teenuseid.</p>
    </div>

    <section class="text-gray-600 body-font overflow-hidden">
    <div class="container px-5 py-24 mx-auto">
        <div class="flex flex-wrap -m-12">
            <article v-for="(article, i) in articles" :key="i" class="p-12 md:w-1/2 flex flex-col items-start">
                <div class="flex flex-wrap">
                    <span v-for="(tag, tagI) in article.tags" :key="tagI" class="cursor-default inline-block m-1 ml-0 py-1 px-2 rounded bg-indigo-50 text-indigo-500 text-xs font-medium tracking-widest">{{ tag.name }}</span>
                </div>
                <div class="mt-4 mb-8">
                    <h2 class="sm:text-3xl text-2xl title-font font-medium text-gray-900 mb-4">{{article.title}}</h2>
                    <p class="leading-relaxed">{{ article.description }}</p>
                </div>
                <div class="flex items-center flex-wrap pb-4 mb-4 border-b-2 border-gray-100 mt-auto w-full">
                <a :href="`/blog/${article.href}`" class="cursor-pointer text-indigo-500 inline-flex items-center"> {{ article.cta }}
                    <svg class="w-4 h-4 ml-2" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round">
                    <path d="M5 12h14"></path>
                    <path d="M12 5l7 7-7 7"></path>
                    </svg>
                </a>
                <span class="text-gray-400 mr-3 inline-flex items-center ml-auto leading-none text-sm pr-3 py-1 border-r-2 border-gray-200">
                    <svg class="w-4 h-4 mr-1" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round" viewBox="0 0 24 24">
                    <path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z"></path>
                    <circle cx="12" cy="12" r="3"></circle>
                    </svg> {{ article.views }}
                </span>
                <span class="text-gray-400 inline-flex items-center leading-none text-sm">
                    <svg class="w-4 h-4 mr-1" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round" viewBox="0 0 24 24">
                    <path d="M21 11.5a8.38 8.38 0 01-.9 3.8 8.5 8.5 0 01-7.6 4.7 8.38 8.38 0 01-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 01-.9-3.8 8.5 8.5 0 014.7-7.6 8.38 8.38 0 013.8-.9h.5a8.48 8.48 0 018 8v.5z"></path>
                    </svg> {{ article.comments}}
                </span>
                </div>
                <div class="inline-flex items-center">
                    <img alt="article-author" :src="`/img/${'Kaspar-156x156'}.png`" class="w-12 h-12 rounded-full flex-shrink-0 object-cover object-center">
                    <span class="flex-grow flex flex-col pl-4">
                        <span class="title-font font-medium text-gray-900"> {{ article.author.name }}</span>
                        <span class="text-gray-400 text-xs tracking-widest mt-0.5"> {{ article.author.title}} </span>
                    </span>
                </div>
            </article>
        </div>
    </div>
    </section>
    <BottomNavigation />
</template>