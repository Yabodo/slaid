<script setup lang="ts">

let articles = ref([
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
title: 'Kuidas organiseerida pildiarhiivi? | Slaid.ee',
meta: [
    { name: 'og:title', content: 'Kuidas organiseerida pildiarhiivi?' },
    { name: 'og:site_name', content: 'Slaid.ee' },
    { name: 'og:locale', content: 'et_EE' },
    // { name: 'og:locale:alternative', content: '' },
    { name: 'og:url', content: 'https://slaid.ee' },
    { name: 'og:type', content: 'article' }, // website
    { name: 'og:description', content: 'Meile kõigile meeldib pildistada ja pildistamine oli võimalik juba enne nutitelefonide teket. Paraku jäävad tehtud pildid tihtipeale vanasse seadmesse, pildistamisäppi, kastidesse, albumitesse, ümbrikutesse ja kuhu iganes veel, kuni lõpuks polegi võimalik olnud aegadest kronoloogilist ülevaadet saada. Samuti kipuvad digitaliseerimata pildid aja jooksul tuhmuma. Et sedasi ei läheks, panime kokku väikese õpetuse, kuidas pildimaterjali organiseerida.' },
    { name: 'description', content: 'Meile kõigile meeldib pildistada ja pildistamine oli võimalik juba enne nutitelefonide teket. Paraku jäävad tehtud pildid tihtipeale vanasse seadmesse, pildistamisäppi, kastidesse, albumitesse, ümbrikutesse ja kuhu iganes veel, kuni lõpuks polegi võimalik olnud aegadest kronoloogilist ülevaadet saada. Samuti kipuvad digitaliseerimata pildid aja jooksul tuhmuma. Et sedasi ei läheks, panime kokku väikese õpetuse, kuidas pildimaterjali organiseerida.' },
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
})
</script>
<template>
    <Navigation />

    <div class="container mx-auto px-5 py-6 md:py-24 md:px-24 items-center text-lg">
        <h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-gray-900"><b>Kuidas organiseerida pildiarhiivi?</b></h1>
        <p>Fotod kipuvad aastatega kuhjuma, isegi siis, kui pildistad vaid pereliikmeid ja erilisi s&uuml;ndmusi. Kui sul on peres fotograafe, saab neid fotosid veelgi rohkem ja kui sa pole ettevaatlik, on neid t&auml;is terve elamine.</p>
        <p>Oled seda ilmselt sada korda l&auml;bi elanud, et tahaks oma fotosid s&auml;ilitada, sest see on su perekonna ajalugu, kuid seal samas on ka &uuml;lekaalukas tung segadusest vabaneda. L&otilde;puks s&auml;ilitate siiski oma fotod.</p>
        <p>Teine probleem on selles, et pildid tuhmuvad. Kui fotod vananevad, muudavad nad v&auml;rvi. Mida kauem on pildid kaitseta, seda t&otilde;en&auml;olisemalt saavad nad kahjustada niiskuse, putukate, n&auml;riliste, tule ja muu tulemusena. Oma vanade fotode korrastamine ja digitaliseerimine on suurep&auml;rane v&otilde;imalus neid veel aastaid omada. Aga kuidas sa 30 aasta eest fotosid korraldad? Kust alustada?</p>
        <p>Meil on m&otilde;ned n&otilde;uanded, mis teid aitavad!</p>
        <h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>VANADE FOTODE ORGANISEERIMINE</b></h2>
        <h3><b>Koguge fotod kokku</b></h3>
        <p>Tr&uuml;kitud fotode korraldamine pole enamasti nii raske. Fotode organiseerimise alustamiseks koguge kokku k&otilde;ik oma pildid ja fotoalbumid. Kui kavatsete oma fotosid digitaliseerida v&otilde;i luua tulevastele p&otilde;lvedele ajaliini, siis v&otilde;iksite fotod h&otilde;lpsamaks k&auml;sitlemiseks ja sortimiseks albumitest eemaldada. V&otilde;ti on saada kogu oma fotokogu &uuml;hte kohta, nii et nende paigutamine fotokastidesse, kingakarpi v&otilde;i isegi plastkasti v&otilde;ib aidata k&otilde;ike koos hoida.&nbsp;</p>
        <h3><b>Vaadake varandus &uuml;le</b></h3>
        <p>Kui olete k&otilde;ik oma fotod kokku kogunud, siis vaadake need &uuml;le, et saada hea ettekujutus sellest, mis teil on. See aitab teil ka otsustada, kuidas neid sorteerida. Seda saate teha materjali kogudes, kuid paremini toimib see, kui istute maha ja p&uuml;hendate kogu oma t&auml;helepanu materjaliga tutvumiseks. Nii n&auml;ete, millised on k&otilde;ik fotod, kui kaugele need tagasi ulatuvad, kui on inimesi, keda soovite tuvastada ja kui on duplikaate.</p>
        <p>Samal ajal, kui fotosid vaatad, kontrolli ka, et kas negatiivid/positiivid on nendega kaasas. Proovi v&otilde;imalusel negatiive sobivate fotodega &uuml;henduses hoida. See tuleb hiljem kasuks ja aitab organiseerimisel.</p>
        <h3><b>Organiseerige materjal</b></h3>
        <p>J&auml;rgmine samm on fotode sorteerimine. Selleks on mitu v&otilde;imalust. Saate neid sortida kronoloogiliselt, alustades k&otilde;ige varasemast ja l&otilde;petades k&otilde;ige uuemaga, v&otilde;i teha seda teema, s&uuml;ndmuse, perekonna v&otilde;i isiku j&auml;rgi. Populaarne on ka lugude j&auml;rgi organiseerimine, kuid soovitame seda teha hiljem elektroonilises vormis.. Selle ilu on see, et sedasi saate kommunikeerida oma pere ajalugu l&auml;bi erinevate lugude. Fotode l&auml;bivaatamisel saate ilmselt parema &uuml;levaate soovitud organiseerimismustritest ja pildi r&auml;&auml;gitud lugudest.</p>
        <p>Kronoloogiline sorteerimine v&otilde;ib k&otilde;lada l&otilde;busalt, aga metsiku koguse fotode puhul v&otilde;ib see olla suur t&ouml;&ouml;, eriti kui sul on suur pere. Pildimaterjali v&auml;iksemate perede kaupa eraldamine ja/v&otilde;i osapoolte kaasamine v&otilde;ib olla sel juhul samuti lahendus. Soovitame mingit pidi pildid siiski j&auml;rjekorda seada, sest ajaga muutub nende organiseerimine &uuml;ha keerukamaks.</p>
        <h3><b>Arhiveerige &otilde;igesti</b></h3>
        <p>Prinditud fotode organiseerimine ja sorteerimine on aegan&otilde;udev, kuid isegi korralikult talletatud fotod v&otilde;ivad v&otilde;tta palju ruumi. Kui vaatate sortimisprotsessi k&auml;igus oma pere fotosid, siis hakake m&otilde;tlema nende jaoks parimatele salvestusv&otilde;imalustele. Selles m&auml;ngib rolli fotode maht, kuid nende sortimine m&otilde;jutab t&otilde;en&auml;oliselt ka nende s&auml;ilitamist. Kui sordite isiku v&otilde;i pere j&auml;rgi, v&otilde;ivad pere fotoalbumid h&auml;sti t&ouml;&ouml;tada. Kui sordite kronoloogiliselt, v&otilde;ivad fotode s&auml;ilituskarbid v&otilde;i fotoraamat olla need, mida vajate.</p>
        <p>Ilus v&auml;ljal&otilde;igete raamat v&otilde;imaldab lisada arhiivile veidi isiksust ja jutustada suurep&auml;raseid lugusid, mida hinnatakse veel aastaid. Arhiveerimisel soovitame kasutada piltide kvaliteedi s&auml;ilitamiseks glassiin&uuml;mbrikuid, et originaalmaterjal maksimaalselt kaua v&auml;rskena s&auml;iliks.</p>
        <p>Kuigi fotode sorteerimisel v&otilde;ivad kasuks tulla kingakarbid, pappkarbid ja plastmahutid, ei ole need head pikaajaliseks s&auml;ilitamiseks.</p>
        <p>&nbsp;</p>
        <h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>N&Auml;PUN&Auml;ITEID FOTODE K&Auml;SITLEMISEKS JA SORTEERIMISEKS</b></h2>
        <ul>
        <li class="flex items-center">
        <svg class="w-4 h-4 mr-1.5 text-green-500 dark:text-green-400 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path></svg>
        Vaadake ja sorteerige fotosid suurel tasasel pinnal nagu laud v&otilde;i p&otilde;rand, mis on kuiv, puhas ning pole l&auml;bik&auml;idav.</li>
        <li class="flex items-center">
        <svg class="w-4 h-4 mr-1.5 text-green-500 dark:text-green-400 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path></svg>
        Veenduge, et teil on mitu karpi v&otilde;i mahutit fotode hoiustamiseks.</li>
        <li class="flex items-center">
        <svg class="w-4 h-4 mr-1.5 text-green-500 dark:text-green-400 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path></svg>
        Proovige negatiive ja fotosid &uuml;ksteisest mitte eraldada.</li>
        <li class="flex items-center">
        <svg class="w-4 h-4 mr-1.5 text-green-500 dark:text-green-400 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path></svg>
        Kaaluge udukaadrite (pildid, mida kasutada ei saa) &auml;raviskamist (va. videokaadrid).</li>
        <li class="flex items-center">
        <svg class="w-4 h-4 mr-1.5 text-green-500 dark:text-green-400 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path></svg>
        Otsustage, mida soovite duplikaatidega teha, kas soovite need alles j&auml;tta, pakkuda neid teistele pereliikmetele v&otilde;i need &auml;ra visata.</li>
        <li class="flex items-center">
        <svg class="w-4 h-4 mr-1.5 text-green-500 dark:text-green-400 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path></svg>
        K&auml;sitlege fotosid fotokinnaste v&otilde;i puuvillast kinnastega.</li>
        <li class="flex items-center">
        <svg class="w-4 h-4 mr-1.5 text-green-500 dark:text-green-400 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path></svg>
        Fotode tagak&uuml;ljele kirjutamiseks kasutage happevaba fotopliiatsit.</li>
        <li class="flex items-center">
        <svg class="w-4 h-4 mr-1.5 text-green-500 dark:text-green-400 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path></svg>
        M&auml;rgistage fotod, mida sooviksite p&auml;rast digitaliseerimist arvutis t&ouml;&ouml;delda.</li>
        <li class="flex items-center">
        <svg class="w-4 h-4 mr-1.5 text-green-500 dark:text-green-400 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path></svg>
        Kasutage m&auml;rkmete tegemiseks v&otilde;i iga fotokogu sildistamiseks registrikaarte.</li>
        </ul>
        <p>&nbsp;</p>
        <h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>FOTODE DIGITALISEERIMINE</b></h2>
        <p>Perepiltide digitaliseerimine on suurep&auml;rane v&otilde;imalus nende hoidmiseks. Digitaalne foto v&otilde;tab palju v&auml;hem ruumi kui tr&uuml;kitud foto. Veelgi enam, saate neid kaitsta aja- v&otilde;i keskkonnateguritest tingitud lagunemise eest. Slaid pakub ka fotode digitaliseerimist, kuid saate seda ka ise teha. Kui teil on palju fotosid, v&otilde;ib ettev&otilde;tte kasutamine olla ajaliselt t&otilde;husam valik ja pikas perspektiivis ka odavam.</p>
        <p>Digitaliseeritud fotode suur pluss on see, et saate neid jagada sotsiaalmeedias, jagada neid teiste pereliikmetega, kasutada Photoshopi v&otilde;i m&otilde;nda muud pildit&ouml;&ouml;tlusprogrammi uute teoste loomiseks, ilma et originaalpildiga midagi juhtuks.</p>
        <h3><b>Ise digitaliseerimine</b></h3>
        <p>Kui soovite oma fotosid ise digitaliseerida, saate t&ouml;&ouml; tegemiseks kasutada fotosk&auml;nnerit. Fotosk&auml;nnereid on erinevaid ning olemasoleva sk&auml;nneri kasutamine v&otilde;ib olla hea v&otilde;imalus s&auml;&auml;sta raha. Sk&auml;nneri puudumisel v&otilde;ib selle ostmine minna kulukamaks kui teenuse sisseostmine. Kui&nbsp; otsustate siiski endale sk&auml;nneri soetada, siis ostke hea kvaliteediga sk&auml;nner, et te ei peaks hinna kokkuhoidu kinni maksma madalama pildikvaliteedi v&otilde;i ooteajaga.</p>
        <h3><b>Kasutage digitaliseerimisteenust</b></h3>
        <p>Kui l&auml;hete fotode digitaliseerimise teenusega, v&otilde;ib see olla kergelt kulukam ette, kuid kui te v&otilde;tate arvesse sk&auml;nneri hinda, jooksevkulusid ja fotode sk&auml;nneerimisele kuluvat aega, on fotode skaneerimise teenus m&otilde;istlik. See on lihtne, kiire ja probleemideta, nii et kui soovite kokku hoida oma aega ja energiat, siis v&otilde;ite kaaluda ka sk&auml;nnimisteenuse sisseostmist meilt v&otilde;i mujalt.</p>
        <h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>Arhiveerimine</b></h2>
        <p>Kui olete oma fotod digitaliseerinud, peate need organiseerima. Hea fotohaldus h&otilde;lmab failide nimetamist k&otilde;ige otsitava jaoks, kaustade loomist sorteerimise parandamiseks ja indeksi loomist, et saaksite kiiresti ja lihtsalt leida, mida otsite. Samuti saate lisada failile teavet, et see oleks lihtne, nii et see sisaldas kuup&auml;eva, s&uuml;ndmust, asjakohaseid nimesid v&otilde;i muid m&auml;rks&otilde;nu, mis v&otilde;imaldavad teil fotosid otsida ja leida, mida vajate.&nbsp;</p>
        <p>Kindlasti v&otilde;tke aega end parimate arhiveerimise tavadega kurssi viimiseks. Mida p&otilde;hjalikum on ettevalmistus, seda tasuvam on tulemus. Mida t&auml;iuslikum on arhiiv, seda h&otilde;lpsam on Teie ligip&auml;&auml;s m&ouml;&ouml;dunud elule ja seda selgem on &uuml;levaade.&nbsp;</p>
        <p>Slaid.ee pakub arhiveerimisteenuseid ainult kokkuleppekorras. Soovi korral lisage oma tellimusse tasuta konsultatsioon.</p>
        <h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>Tee k&otilde;igest varukoopiad!</b></h2>
        <p>Esimene asi, mida peate tegema, kui olete oma fotod digitaliseerinud, on teha varukoopia. Pilvesalvestus on taskukohane, turvaline ja lihtne viis fototeegi ja elektrooniliste failide, sealhulgas digitaalsete fotode salvestamiseks, kuid see ei ole ainus viis. Kui soovite tugevamat privaatsusgarantiid, siis kaaluge f&uuml;&uuml;silist andmekandjat, k&otilde;vaketast, m&auml;lupulka, CD-plaate. Pilvesalvestuseks sobivad DropBox, Google Photos, Google Drive, Flickr. Pilvehoiu ilu seisneb selles, et saate kui iganes palju digitaalseid pilte, muretsemata et ruum saab otsa. Pilv on sinuga alati kaasas ja juurdep&auml;&auml;s andmetele on lihtne s&otilde;ltumata kas kasutate arvutit v&otilde;i nutiseadet. Suure kasutamise korral kaasneb aga pilveteenustega igakuine tasu, samas kui f&uuml;&uuml;silisel kujul hoiustamine t&auml;hendab ainult &uuml;he v&otilde;i ehk kahe kordset kulu (topeltkoopiad).</p>
        <h2 class="title-font sm:text-2xl text-xl my-4 font-medium text-gray-900"><b>L&otilde;petuseks</b></h2>
        <p>Slaid.ee pakub video ning pildimaterjali digitaliseerimise teenuseid. Kui materjali on rohkem v&otilde;i on soov, siis saame Teid aidata ka arhiveerimisega. Kui tunnete, et teil on t&auml;iendavaid k&uuml;simusi, millele te blogist vastust ei leia, siis v&otilde;tke meiega julgelt &uuml;hendust. Seniks, j&otilde;udu digitaliseerimise ning arhiveerimisega, see tasub end &auml;ra!</p>
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