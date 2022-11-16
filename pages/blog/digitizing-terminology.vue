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
                name: "VHS-C"
            },
            {
                name: "VCR"
            },
            {
                name: "Ajalugu"
            },
        ],
        title: "VHS-i põnev ajalugu",
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
title: 'Digitaliseerimise Terminoloogia | Slaid.ee',
meta: [
    { name: 'og:title', content: 'Slaid - Arhiveerimine & Digitaliseerimine' },
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
        <h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-gray-900"><b>VHS Terminoloogia</b></h1>
        <p class="mb-5">Palju keerulisi termineid? Pole midagi, me oleme siin, et aidata. Nagu iga t&ouml;&ouml;stusharu, kasutab ka filmit&ouml;&ouml;stus palju spetsiifilist s&otilde;navara. Kui te pole selle keelega kursis, v&otilde;ib olla masendav m&otilde;ista, mida te t&auml;pselt loete.</p>
        <p class="mb-5">Vahel on eriline terminoloogia v&otilde;luv, vahel h&auml;iriv, aga kui sellest aru ei saa, on see alati t&uuml;&uuml;tu. Seep&auml;rast piilume koos kardinate taha. Me tahame, et te teaksite t&auml;pselt, mida te loete, et te teaksite t&auml;pselt, mida te ostate.</p>
        <p class="mb-5">Hea uudis on, et enamik neist terminitest k&auml;ib videoformaatide kohta. Vahet pole, kas digitaliseerite VHS-i, VHS-c, MiniDV-d v&otilde;i teete midagi t&auml;iesti erinevat, need terminid peaksid teid selles maailmas toimetulemisega aitama.</p>
        <div class="mb-5 ml-4">
        <p><b>Timecode</b>: Iga lint jookseb teatud aja jooksul. See algab 0:00:00 ja siis l&auml;heb nii kaua kui salvestus on. Kui on viis minutit, loeks ajakood l&otilde;pus 0:05:00. Kui digitaliseerime teie videod, teeme alati kogu video, nii et alustame 0-st ja l&auml;heme, kuni salvestused peatuvad.</p>
        <p><b>Eraldusv&otilde;ime</b>: see termin viitab sellele, kui selge on teie pilt. Tavaliselt m&otilde;&otilde;detakse seda pikslites. Suurem eraldusv&otilde;ime t&auml;hendab suuremat, selgemat pilti ja rohkem piksleid!</p>
        <p><b>Piksel</b>: Piksel on video kontekstis &uuml;ks andmepunkt, ehk t&auml;pp, mille kogumikust video koosneb.</p>
        <p><b>Kuvasuhe (Aspect Ratio)</b>: See termin viitab sellele, kui lai versus kui pikk miski on. N&auml;iteks ruut on 1: 1, sest iga k&uuml;lg on sama pikk. Tavaliselt on videod pikkusest veidi laiemad, nii et tavalised kuvasuhted, millega kokku puutume, on 4: 3, 16: 9 ja 21: 9.</p>
        <p><b>4:3</b> : Enamik ekraane oli enne 2000. aastat 4: 3 suhtes. See t&auml;hendab, et ekraani laius on pikkusest pisut suurem. Kutsume seda ka t&auml;isekraaniks.</p>
        <p><b>16:9 </b>: Koos HD standardi tulekuga l&auml;ks enamus videomeediast &uuml;le 16: 9 kuvasuhtele. 16: 9 on pea kaks korda laiem kui pikk, j&auml;ttes sellest pigem kino mulje.</p>
        <p><b>Standarddefinitsioon (SD)</b> ehk <b>480p</b>: Standarddefinitsioon oli eraldusv&otilde;ime standard enne HD tulekut. SD videod pole nii selged kui HD. Kuna enamik vanemaid meediume salvestati SD-sse, siis nii edastame digitaliseeritud versioonid ka teile. Kahjuks pole video kvaliteedi t&otilde;stmiseks eriti midagi teha. 480p t&auml;hendab, et video on 480 pikslit k&otilde;rge.</p>
        <p><b>High Definition (HD)</b> ehk <b>1080p</b>: High Definition ehk k&otilde;rgresolutsioon, 1080 pikslit k&otilde;rge pildistandard, mis hakkas populaarsust koguma koos andmekandjate digitaliseerimisega.&nbsp;</p>
        <p><b>MP4</b>: Rahvusvaheline failit&uuml;&uuml;p, mida arvutid videofailide lugemiseks kasutavad. Te ei pea teadma muud, kui et me kasutame seda formaati ja teie arvuti oskab sellest videot n&auml;idata.</p>
        <p><b>MOV</b>: Apple'ile kuuluv failit&uuml;&uuml;p, mis t&ouml;&ouml;tab sarnaselt MP4-le. Soovi korral saame jagada faile ka selles formaadis.</p>
        </div>
        <p>Me teame, et on raske m&otilde;ista video-terminoloogiat, millega te kokku ei pea puutuma. Selleks olemegi siin, et teid aidata. Kui teil on k&uuml;simusi m&otilde;ne s&otilde;na kohta, mida Slaidi sirvides kohtate, siis piiluge siia ja peaksite oma vastused saama!</p>
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