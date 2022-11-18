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
                name: "Sõbrapäev"
            },
            {
                name: "Kingitus"
            },
            {
                name: "Idee"
            },
        ],
        title: "Sõbrapäeva kingitus",
        description: "Otsid head kingiideed headele sõpradele? Ehk tasuks üle vaadata pildialbumid? Tihti juhtub, et mõni jäädvustatud hetk jääb sõpradega jagamata ning see kujutab endast suurepärast võimalust sõbra üllatamiseks. Oleme kokku piltidega seonduvad kingiideed, et saaksite lihtsa vaevaga inspiratsiooni ammutada.",
        cta: "Loe edasi",
        href: "friend-gift-idea",
        views: 0,
        comments: 0,
        author: {
            name: "Kaspar Jõeveer",
            title: "tehnik / kolumnist",
            picture: "Kaspar-156x156.png"
        },
        seo: {

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
])

useHead({
title: 'Digitaliseerimise Terminoloogia | Slaid.ee',
meta: [
    { name: 'og:title', content: 'Digitaliseerimise Terminoloogia' },
    { name: 'og:site_name', content: 'Slaid.ee' },
    { name: 'og:locale', content: 'et_EE' },
    // { name: 'og:locale:alternative', content: '' },
    { name: 'og:url', content: 'https://slaid.ee' },
    { name: 'og:type', content: 'article' }, // website
    { name: 'og:description', content: 'Andmekandjate ajalugu on kirev ning veelgi kirevam on nendega seotud sõnavara. Selgitame, mida levinumad väljendid tähendavad, et saaksite meie tegemistest parema ülevaate.' },
    { name: 'description', content: 'Andmekandjate ajalugu on kirev ning veelgi kirevam on nendega seotud sõnavara. Selgitame, mida levinumad väljendid tähendavad, et saaksite meie tegemistest parema ülevaate.' },
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
    { name: 'description', content: '' }
],
bodyAttrs: {
    class: 'test'
},
//script: [ { children: 'console.log(\'Hello world\')' } ]
})
</script>
<template>
    <Navigation />

    <div class="content container mx-auto px-5 py-6 md:py-24 md:px-24 items-center text-lg">
        <h1 class="title-font sm:text-4xl text-3xl mb-8 font-medium text-gray-900"><b>VHS-i ajalugu</b></h1>
        <h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>JULGELT PEALE</b></h2>
        <p>Eelmise sajandi l&otilde;pus ei konkureerinud VHS standardformaadiga keegi. Kasutusmugavus, taskukohasus, suhteliselt hea kvaliteet ja ligip&auml;&auml;setavus tegid sellest standardi igas videom&auml;ngijas. Kuigi VHS on n&uuml;&uuml;dseks kadunud k&otilde;ikjalt peale kodukappide, kus nad ikka vapralt oma aega ootavad, on nad siiski &uuml;ks suurima m&otilde;juga meediaformaate ajaloos. Ajaloo poolest, on VHS palju huvitavam kui lihtne videokassett, mis ilmus eikusagilt siis kadus peaaegu sama kiiresti. Enne VHS-i olemasolu leiutati 1950. aastatel formaat nimega VTR. VTR oli kordades suurem VHS-i eelk&auml;ia, mis suutis filmirullile videoid salvestada ja uuesti salvestada. Lisaks suurusele oli probleemiks ka seadme tohutu maksumus, mis ulatus sadadesse tuhandetesse dollaritesse. Seda said luvada endale vaid telejaamad ja professionaalsed stuudiod, kuid VTR-i taas-salvestatav tehnoloogia sillutas teed k&auml;ttesaadavama ja kasutatavama VHS-i olemasolule tulevikus.</p>
        <h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>VHS</b></h2>
        <p>Tuginedes samale tehnoloogiale, mida VTR kasutas, hakkas Victor Company of Japan (JVC) tegelema tarbeversiooni loomisega. 1971. aastal t&ouml;&ouml;tasid kaks Jaapani insener, et teha v&otilde;imalikuks videokassetid, mida me nii kallilt hindasime. Esimene versioon kodus kasutatavast VHS formaadist oli siiski oma hinna poolest liiga kallis. VCR (VHS-i salvestusseade) maksis Ameerika &Uuml;hendriikides 1986. aastal samuti umbes 1000 dollarit, inflatsioonikalkulaatorit kasutades saaksite arvutada seadme umbkaudse maksumuse t&auml;nases p&auml;evas. Kuid &uuml;sna pea tuli turule ka Betamax, et saada t&ouml;&ouml;stusstandardiks. Kuigi m&otilde;lemal standardil oli oma v&otilde;lu, v&otilde;itus l&otilde;ppkokkuv&otilde;ttes VHS. Pea igas kodus oli oma teleriga &uuml;hendatud VCR. VHS kui esimene omalaadne standard ning standards&otilde;ja v&otilde;itja vallutas kiiresti enamike majapidamiste riiulid.</p>
        <h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>P&Auml;RAND MAAILMALE</b></h2>
        <p>VHS oli kodukino ja personaalmeedia arengu lahutamatu osa. VCR (salvestusv&otilde;imekusega VHS m&auml;ngija) tegi telesaadete ja koduvideote salvestamise keskmise kodaniku jaoks piisavalt lihtsaks ja taskukohaseks, et seda vajadusel kasutada. VHS valitses videosalvestusturgu vankumatult ja seet&otilde;ttu on olulisem kui kunagi varem tagada, et teil on digitaalsed koopiad k&otilde;igist teie arhiivides olevatest VHS kassettidest.. Koduraamatukogu ajakohasena hoidmine sellises formaadis, mida saate veel kasutada, on oluline, et teie m&auml;lestused ajaga ei kaoks ega tuhmuks... isegi kui teile tundub, et teie VHSid on teile igavesti lojaalsed.</p>
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