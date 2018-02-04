<template>
  <div id="app">
    <h1>Mosty na dálnicích a silnicích I.-III. tříd v nejhorším, tedy havarijním stavu</h1>
    <h2>Kliknutím zobrazíte podrobný seznam</h2>  
    <p>V České republice je podle údajů z roku 2017 na dálnicích  a silnicích I. až III. tříd celkem 17957 mostů. V evidenci mostních objektů většinou chybí mosty na místních a účelových komunikacích v majetku obcí. Podle odhadu Unie mostařů ČR je to dalších zhruba 14 tisíc mostů a 180 tisíc propustků v délce do dvou metrů.</p>
    <AccordionMenu :contents="contents"></AccordionMenu>
    <p>Zdroj: ŘSD, jednotlivé krajské úřady a Správy údržby silnic</p>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
  return {
    contents: [
    {
      title: 'Jihomoravský kraj: 29 mostů',
      msg: '<ul><li>II/379 - Podomí - oprava v přípravě</li> <li>37424 - Pilské údolí - oprava projekčně připravena</li> <li>II/152 - Most přes místní potok v Moravských Bránicích - oprava v přípravě</li> <li>II/386 - Most přes Melkranský potok za Novým Dvorem - oprava projekčně připravena</li> <li>II/394 - Most přes Bobravu před Tetčicemi - oprava v přípravě</li> <li>II/430 - Most přes Roketnici u Maxlůvky - oprava v přípravě</li> <li>15267 - Most přes Troubský potok u Nebovid I - oprava probíhá</li> <li>15267 - Most přes Troubský potok u Nebovid II - oprava probíhá</li> <li>3795 - Most přes Blahoňůvku za Kuřimským Jestřabím - oprava probíhá</li> <li>37913 - Most přes Lubě v Drásově</li> <li>3834 - Most přes Kovalovický potok před Vin. Šumicemi</li> <li>3901 - Most přes místní potok před Borovníkem</li> <li>39513 - Most přes náhon v Syrovicích</li> <li>39517 - Most přes Lejtnu v Bratčicích</li> <li>42510 - Most přes polní příkop za Rajhradem - oprava v přípravě</li> <li>II/430 - Olomoucká přes železnici - oprava v přípravě</li> <li>37915 - Studená, Merhautova přes ČD</li> <li>II/416 - Hrušky - oprava v přípravě</li> <li>II/416 - Hostěrádky-Rešov - oprava probíhá</li> <li>II/418 - Otnice - oprava v přípravě</li> <li>II/431 - Kojátky - oprava probíhá</li> <li>II/462 - Vyškov - oprava v přípravě</li> <li>4712 - V. Vážany - oprava projekčně připravena</li> <li>502 - Němčany - oprava v přípravě</li> <li>37736  - Radslavice - oprava projekčně připravena</li> <li>37926 - Drnovice</li> <li>4179 - Zbýšov   - oprava probíhá</li> <li>4191 - Slavkov - oprava projekčně připravena</li> <li>4199 - Milešovice - oprava probíhá</li></ul>',
    },
    {
      title: 'Olomoucký kraj: 17 mostů',
      msg: '<ul><li>II/441 - Most přes Kyjanický potok za osadou Kyjanice</li> <li>II/441 - Most přes místní potok v obci Potštát</li> <li>II/446 -(Most přes místní potok na ulici Hanušovická v obci Staré Město</li> <li>II/448 - Most přes potok Pilavka za osadou Kandia</li> <li>4498 - Most přes příkop ve městě Litovel</li> <li>4498 - Most přes mlýnský náhon v obci Nové Mlýny</li> <li>4571 - Most přes Obecní potok IV před osadou Zálesí</li> <li>03546 - Most přes místní potok před obcí Březové</li> <li>31239 - Most přes Kamenný potok před osadou Podlesí</li> <li>31238A - Most přes řeku Morava k vlakové stanici Podlesí</li> <li>44318 - Most přes  Bystřici v obci Mariánské Údolí</li> <li>44417 - Most přes Pasecký p. za obcí Paseka</li> <li>44423 - Most přes Lesklou rokli ve městě Šternberk</li> <li>44429 - Most přes p. Sitka u os. Horní Žleb</li> <li>44434 - Most přes zátopní území za obcí Domašov u Šternberka</li> <li>44443 - Most přes místní za obcí Domašov nad Bystřicí</li> <li>44646 - Most přes řeku Krupá na ulici Lipová ve Starém Městě</li></ul>',
    },
    {
      title: 'Liberecký kraj: 12 mostů',
      msg: '<li>II/283 - Most přes inundaci u Tatobit Pod skálou</li> <li>II/284 - Most u č.p. 96 v dolní Nové Vsi nad Popelkou</li> <li>II/289 - Most přes řeku Jizeru v Semilech</li> <li>II/292 - Most přes Mlýnský potok za Pelechovem</li> <li>III/2893 - Most v Semilech pod hřbitovem, ul. Koštofranská</li> <li>III/2901 - Most přes potok ve Frýdlantě - Větrově</li> <li>III/2914 - Most přes zátopní území potoka za Bulovkou</li> <li>III/2951 - Most přes potok Jílovku v obci Martinice v Krkonoších</li> <li>26839 - Most přes Svitávku v Kunraticích u Cvikova</li> <li>27814 - Most přes strouhu na Záskalí</li> <li>28624 - Most přes potok Cedron, křižovatka Benecko, Mrklov</li> <li>29063 - Most přes Sklenařický potok v Jablonci nad Jizerou, Třtí</li>',
    },
    {
      title: 'Středočeský kraj: 11 mostů',
      msg: '<ul><li>33818-7 Most přes potok za obcí Ovčáry – probíhá rekonstrukce</li> <li>34635-2 Most přes laterální kanál, Lužec nad Vltavou – proběhla provizorní oprava, připravuje se snesení mostu a nahrazení novým objektem – stavbu připravuje Ředitelství vodních cest</li> <li>34635-2a Most přes laterální kanál, Lužec nad Vltavou – proběhla provizorní oprava, připravuje se snesení mostu a nahrazení novým objektem – stavbu připravuje Ředitelství vodních cest</li> <li>23610-1 most přes potok v Novém Jáchymově – provedla se provizorní oprava, most v ochranném pásmu kulturní památky</li> <li>00323-1a přes dálnici D1 Praha-Brno u Jažlovic – probíhá výstavba nového mostu</li> <li>1256-1 Most přes potok Orlina v obci Vlašim - most o malé délce přemostění – 2,01 metru, nově přeřazen do mostních objektů (dříve propust), zadána oprava</li> <li>10125-1 Most přes potok v obci Nučice – provedena provizorní oprava mostních opěr (přezdění), bylo vydáno stavební povolení, předpoklad realizace 2018</li> <li>27612-1 přes meliorační sběrač před obcí Husí Lhota - předpoklad opravy v průběhu roku 2018</li> <li>240-022 - Most přes Červený a Bakovský potok ve Velvarech - v průběhu roku 2018 bude postaven nový most. Po celou dobu výstavby bude silnice II/240 uzavřená.</li> <li>33716-1 - Most přes potok Křenovku v obci Pernštejnec - most bude v průběhu roku 2018 nahrazený novým</li> <li>2427-1 - Most přes odvodňovací strouhu před obcí Klíčany - most je kůli nosnosti zúžený. Stavba nového by měla začít v druhé polovině 2018</li></ul>',
    },
    {
      title: 'Ředitelství silnic a dálnic: 6 mostů',
      msg: '<ul><li>I/6 - Most přes potok za Krušovicemi - aktuálně provizorní oprava, v druhé polovině roku 2018 začne komplexní oprava</li> <li>I/11 - Most přes řeku Desná v obci Petrov nad Desnou - koordinace s Povodím a obcí, oprava 2018 nebo 2019</li> <li>I/23 - Most přes potok Lubí v Třebíči - opravena jedna polovina, oprava bude pokračovat do poloviny roku 2018</li> <li>I/27 - Most přes přívalovou strouhu před obcí Chotěšov - příprava projektu na opravu</li> <li>I/44 - Most přes místní potok v obci Vlachov - bude vyřazen z evidence 2018, demolice</li> <li>I/57 - Most přes polní příkop před obcí Branka - provedeno provizorní zabezpečení, zpracovává se projektová dokumentace</li> <li>I/11 - Most přes řeku Tyru v obci Oldřichovice - oprava 2018</li></ul>',
    },
    {
      title: 'Kraj Vysočina: 5 mostů',
      msg: '<ul><li>38810 - Most přes místní potok před obcí SMRČEK</li>   <li>38711 - Most přes potok Věžná v obci VĚŽNÁ</li> <li>36055 - Most přes řeku Balinku v obci BALINY</li> <li>35429 - Most přes odtok z rybníka v obci BOHDALOV</li> <li>03814 - Most přes Šlapánku v Mírovce, uzavření k 15.1.2018, probíhá projektová příprava, na jaře bude snesen a postaven nový</li></ul>',
    },
    {
      title: 'Pardubický kraj: 4 mosty',
      msg: '<ul><li>35514 - Most přes Žejbro v Rosicích u Chrasti</li> <li>II/355 - Most přes Novohradku v obci Dvakačovice</li> <li>II/368 - Most Dlouhá Loučka - Útěchov</li> <li>3716 - Most u Bezděčí u Trnávky - omezený průjezd pro nákladní auta</li></ul>',
    },
    {
      title: 'Královéhradecký kraj: 3 mosty',
      msg: '<ul><li>32722 - Most přes Mlýnskou Cidlinu - most je pro motorová vozidla uzavřený</li> <li>32722 - Most přes Cidlinu - most je pro motorová vozidla uzavřený</li> <li>3082 - Most plukovníka Šrámka v Hradecké části Svinary přes Orlici - kraj plánuje nový most začít stavět v roce 2018, dokončený bude 2019</li></ul>',
    },
    {
      title: 'Kralovarský kraj: 1 most',
      msg: '<ul><li>Lávka na cyklostezce v Mostově u Odravy.  Lávka je zavřená, kraj ji opravuje a chce ji pro cyklisty zprovoznit na jaře 2018. </li></ul>',
    }
    ],
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: square;
  padding: 0;
  margin-top: 0;
}

li {
  margin: 0 10px;
  text-align: left;
}

a {
  color: #42b983;
}

</style>
