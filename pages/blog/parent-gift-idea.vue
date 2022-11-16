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
title: 'Kink vanematele | Slaid.ee',
meta: [
    { name: 'og:title', content: 'Kink vanematele' },
    { name: 'og:site_name', content: 'Slaid.ee' },
    { name: 'og:locale', content: 'et_EE' },
    // { name: 'og:locale:alternative', content: '' },
    { name: 'og:url', content: 'https://slaid.ee' },
    { name: 'og:type', content: 'article' }, // website
    { name: 'og:description', content: 'Jõulud on tasapisi lähenemas. See tähendab, et jälle on vaja lagedale tulla terve posu kingiideedega. Kui kampsun, ornament või raamat enam originaalsed pole, siis soovitame kinkida mälestusi. Slaidid, positiivid, negatiivid, fotod ja muud füüsilisel kujul pildid annavad võimaluse vaadata tagasi kogetud elule ning hinnata selle kirevust. Igavesena tundunud hetked asendusid tihtipeale kild-killu kaupa uutega ning vaade tagasi aitab seda selgemini mõista.' },
    { name: 'description', content: 'Jõulud on tasapisi lähenemas. See tähendab, et jälle on vaja lagedale tulla terve posu kingiideedega. Kui kampsun, ornament või raamat enam originaalsed pole, siis soovitame kinkida mälestusi. Slaidid, positiivid, negatiivid, fotod ja muud füüsilisel kujul pildid annavad võimaluse vaadata tagasi kogetud elule ning hinnata selle kirevust. Igavesena tundunud hetked asendusid tihtipeale kild-killu kaupa uutega ning vaade tagasi aitab seda selgemini mõista.' },
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
        <h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-gray-900"><b>Kingitus vanematele</b></h1>
        <p><span style="font-weight: 400;">J&otilde;ulud on tasapisi l&auml;henemas. See t&auml;hendab, et j&auml;lle on vaja lagedale tulla terve posu kingiideedega. Kui soovid teha kingitusi oma vanematele, siis soovitame kinkida m&auml;lestusi. Slaidid, positiivid, negatiivid, fotod ja muud f&uuml;&uuml;silisel kujul pildid annavad v&otilde;imaluse vaadata tagasi kogetud elule ning hinnata selle kirevust. Igavesena tundunud hetked asendusid tihtipeale kild-killu kaupa uutega ning vaade tagasi aitab seda selgemini m&otilde;ista.</span></p>
        <p><span style="font-weight: 400;">M&otilde;ni m&otilde;te ilusa kingituse vormistamiseks:</span></p>
        <h2><b>DIGITAALNE PILDIRAAM</b></h2>
        <p><span style="font-weight: 400;">Kui on soov n&auml;idata rohkem kui &uuml;ht pilti samas pildiraamis, v&otilde;ite proovida digitaalset pildiraami. &Otilde;ige &uuml;lesseadistuse korral v&otilde;ib digitaalne pildiraam v&otilde;ib olla ka tore viis uute piltide jagamiseks.</span></p>
        <h2><b>PERE FOTOSESSIOON</b></h2>
        <p><span style="font-weight: 400;">Ainus, mis on p&otilde;nevam kui vanad fotod, on uued fotod. Pere fotosessioon v&otilde;ib olla suurep&auml;rane viis selgel ja meeldival viisil uut ajalugu j&auml;&auml;dvustada.</span></p>
        <h2><b>FOTOKINGITUSED</b></h2>
        <p><span style="font-weight: 400;">Fotod ei pea olema ainult paberil v&otilde;i virtuaalsed. Soovi korral v&otilde;ime tr&uuml;kkida pilte erinevatele asjadele.</span></p>
        <div class="idea-list">

            <p><b>Padi</b><span style="font-weight: 400;"> &ndash; mis on lohutavam, kui puhata pea padjal, millel on laste pilt?&nbsp;</span></p>
        <p><b>Kalender </b><span style="font-weight: 400;">&ndash; Kalender on suurep&auml;rane viis elu v&otilde;lu hindamiseks. Pole m&otilde;tet kulutada aega tasuta saadud reklaamkalendritele, kui iga kuu kohta v&auml;&auml;rt m&auml;lestused olemas on.</span></p>
        <p><b>Pusle</b><span style="font-weight: 400;"> &ndash; kas soovite perekondlikku m&auml;ngu&otilde;htut veidi v&uuml;rtsitada? Muretsege perele pildimuster. Pusle on suurep&auml;rane vahend kannatlikkuse, koost&ouml;&ouml; ning omavaheliste suhete arendamiseks.</span></p>
        <p><b>K&ouml;&ouml;gip&otilde;ll </b><span style="font-weight: 400;">&ndash; Kuigi vanemate toidud on oivalised ka omaette, muudab nende valmistamise veelgi l&otilde;busamaks kaunis k&ouml;&ouml;gip&otilde;ll.</span></p>
        <p><b>Medaljon</b><span style="font-weight: 400;">&ndash; elegantne viis hoida l&auml;hedasi s&uuml;dame v&otilde;i pilgu l&auml;heduses.</span></p>
        <p><b>Kohvikruus </b><span style="font-weight: 400;">&ndash; V&auml;&auml;rt kohvikruus saadab omanikku aastaid ja leiab tema s&uuml;dames sooja koha. Kui tal sellist kiindumust oma kruusi vastu pole, on lootust seda hea kingiga muuta.</span></p>
        <p><b>V&otilde;tmehoidja v&otilde;i kandekott</b><span style="font-weight: 400;"> &ndash; kui saaks, prooviks ema ilmselt oma lapsi igale poole viia. Kohandatud foto v&otilde;tmehoidja v&otilde;i kandekott kingituseks, n&uuml;&uuml;d saab.</span></p>
        </div>
        <h2><b>FOTODE DIGITALISEERIMINE JA ARHIVEERIMINE</b></h2>
        <p><span style="font-weight: 400;">Kui see kink on veel tegemata, siis on t&auml;helepanuta j&auml;&auml;nud suurep&auml;rane viis tuua vanemate silmist v&auml;lja r&otilde;&otilde;mupisarad. Kinkige vanematele maitsekas Slaid.ee kinkekaart v&otilde;i saatke meile oma digitaliseerimata pildimaterjal. M&otilde;lemal juhul saavad andmed elektrooniliselt j&auml;&auml;dvustatud m&auml;lupulgale ja/v&otilde;i DVD-le. Protsess annab suurep&auml;rase v&otilde;imaluse uuesti l&auml;bi elada oma pulmap&auml;eva, laste s&uuml;ndi, unustamatut puhkust, r&otilde;&otilde;msalt m&ouml;&ouml;dunud p&uuml;hasid ja palju muud. Kingitus digitaalses formaadis on lihtne jagada, vaadata ja s&auml;ilitada. Paneme olulist r&otilde;hku, et meie teenuste kasutamine oleks lihtne, sujuv ja meeldiv.</span></p>
    </div>
    

    <aside class="text-gray-600 body-font overflow-hidden">
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
</aside>
    <BottomNavigation />
</template>

<style>
.content p {
    margin-bottom: 1rem;
}
.content .idea-list {
    margin-bottom: 1rem;
    margin-left: 1rem;
}
.content .idea-list p {
    margin-bottom: 0;
}
</style>