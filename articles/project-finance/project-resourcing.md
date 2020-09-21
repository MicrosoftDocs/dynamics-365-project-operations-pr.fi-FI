---
title: Projektin resursointi
description: Tässä aiheessa on tietoja projektin resursoinnista.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751111"
---
# <a name="project-resourcing"></a>Projektin resursointi

[!include [banner](../includes/banner.md)]

Tässä aiheessa on tietoja projektin resursoinnista.

Yksi projektipäälliköiden ja resurssipäälliköiden haasteista projektin suunnitteluvaiheessa on resurssien varaaminen, jossa heidän on määritettävä ja varattava projektin suorittajaksi oikea resurssi. Dynamics 365 Financessa projektien resursointiominaisuudet mahdollistavat sellaisten roolien määrittämisen, joita kohdellaan väliaikaisina resursseina, jotka voi varata tiettyä kiinnitystä tai osakiinnitystä varten. Tällaisen resursoinnin avulla projekti- ja resurssipäälliköt voivat suorittaa seuraavat tehtävät:

- Määrittää roolin, jolla on vaaditut pätevyydet, jotta resursseja on helppo osoittaa oikein.
- Roolien käyttäminen sellaisen alustavan kiinnitysaikataulun määrittämiseen, joka perustuu varattuihin resursseihin.
- Kustannusten arviointi ja alustavan budjetin määrittäminen projektille osoitettujen roolien ja resurssien perusteella.
- Roolien käyttäminen kunkin kiinnityksen vaatimien resurssivarausten arvioimiseen.
- Niiden resurssien määrän arvioiminen, jotka tarvitaan projektin koko elinkaaren ajaksi.
- Työrakenteen (WBS) laatiminen käyttäen alustavia resurssimäärityksiä.

[![Projektin elinkaari](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Kun projektin suunnittelu etenee, suunnitellut resurssit voidaan korvata henkilöresursseilla. Projektipäällikkö voi myös palata päivittämään resursointivaraukset missä tahansa projektin vaiheessa.

## <a name="set-up-project-resources"></a>Projektin resurssien määrittäminen
Sinun on määritettävä kalenteri ja osoitettava se työntekijälle. Kalenteria käytetään projektin ja projektiin varattujen resurssien työaikojen aikatauluttamiseen. Kalenterin määrittämisen aikana projektipäälliköt voivat tasata resursseja osana resurssien optimointia. Resursseille voi määrittää rajoituksia kalenteriaikataulun perusteella. Voit määrittää kalenterin **Kalenterit**-sivulla.

Kun määrität työntekijän projektin resurssiksi, voit valita niistä työntekijöistä, jotka ovat töissä siinä yrityksessä, jolle määrität resursseja. Vaihtoehtoisesti voit valita työntekijöitä muista yrityksistä organisaatiossasi. Näitä työntekijöitä kutsutaan yritystenvälisiksi resursseiksi.

Seuraavissa menettelyissä kerrotaan, miten työntekijä määritetään projektiresurssiksi yrityksessäsi ja miten yritystenvälinen projektiresurssi määritetään.

### <a name="set-up-a-worker-as-a-project-resource"></a>Työntekijän määrittäminen projektiresurssiksi

1. Valitse **Työntekijät**-sivun **Työntekijät**-luettelosta se työntekijä, jonka olet lisäämässä projektiresurssiksi ja avaa työntekijän tietue.
2. Valitse toimintoruudussa **Projekti** &gt; **Määritys** &gt; **Projektin määritys**.
3. Valitse kalenteri ja sulje sitten sivu.

Voit myös määrittää resurssille oletusprojekteja ennakkovarauksina. Ennakkovarauksia voi käyttää, kun resurssi- tai projektipäällikkö tietää etukäteen, missä projekteissa resurssi tulee työskentelemään. Ennakkovaraukset voivat perustua myös projektin rajoittajan tai asiakkaan pyyntöön. Jos haluat tehdä projektille ennakkovarauksen, valitse **Määritä projekteja** -sivulla **Projektit**-välilehden **Jäljellä olevat projektit** -luettelosta asianmukainen projekti.

### <a name="set-up-an-intercompany-resource"></a>Yritystenvälisen resurssin määrittäminen

Kun määrität työntekijän yritystenväliseksi resurssiksi, sinun täytyy suorittaa määritys sekä työntekijän lähtö- että kohdeyrityksessä.

**Lähtöyrityksessä**

1. Varmista Financessa, että lähdeyritys on valittuna ja suorita sitten edellisen kohdan menettely Määritä työntekijä projektiresurssiksi.
2. Valitse **Yritystenvälinen kirjanpito**-sivulla **Uusi**.
3. entiteettiValitse **Oikeushenkilön tunnus** kentässä lähtöyritys. Täytä jäljellä olevat kentät asianmukaisesti ja valitse **Tallenna**.
4. Valitse **Siirtohinta**-sivulla **Uusi**.
5. Valitse **Kohdeoikeushenkilö** -kentässä asianmukainen yritys.
6. Jos haluat lainata kohdeyritykselle vain tämän osan alussa luomasi resurssin, valitse **Resurssi**-kentässä luomasi resurssin nimi. Jos haluat antaa kaikki lähtöyrityksen resurssit kohdeyrityksen käyttöön, jätä **Resurssi**-kenttä tyhjäksi.
7. Märitä **Projektinhallinnan ja kirjanpidon parametrit**-sivun **Yritystenvälinen**-välilehdessä **Ota yritystenvälisten resurssien aikataulutus ja tuntilomakkeet käyttöön** -asetukseksi **Kyllä**.

**Kohdeyrityksessä**

- Syötä **Resurssiluettelo**-sivun hakusuodattimeen lähtöyritykselle luomasi resurssin nimi sen varmistamiseksi, että nimi sisällytetään kohdeyrityksen resurssiluetteloon.

## <a name="manage-resource-competencies"></a>Resurssien pätevyyksien hallinta
Resurssien pätevyydet ovat keskeinen osa resurssienhallintaa. Pätevyyksiä voidaan käyttää perustana niiden resurssien määrittämisessä, joilla on oikea taitojen, koulutuksen, sertifiointien ja projektikokemuksen yhdistelmä. Nämä tiedot kannattaa määrittää jokaisen resurssin osalta ja päivittää säännöllisesti. Näin voit maksimoida ominaisuudet, kun tietyt resurssin pätevyydet vastaavat vaatimuksia projektin resurssinosoituksen aikana.

[![Esimerkkejä taidoista, sertifioinneista, koulutuksesta ja projektikokemuksesta](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Seuraavissa ohjeissa kerrotaan, miten voit määrittää joitakin resurssin pätevyyksiä.

Jos haluat määrittää työntekijälle pätevyyksiä, voit käyttää **Työtekijät**-luettelosivustoa henkilöresursseissa tai **Resurssit**-luettelosivua projektinhallinnassa ja kirjanpidossa. Seuraavissa menettelyissä käytetään henkilöresurssien **Työntekijät**-luettelosivua.

### <a name="set-up-competencies-certificates"></a>Määritä pätevyyksiä: sertifikaatit

1. Valitse **Työntekijät**-luettelosivulla sen työntekijän rivi, jolle lisätään sertifikaattitietoja.
2. Valitse toimintoruudun **Työntekijät**-välilehden **Pätevyydet**-ryhmässä **Sertifikaatit**.
3. Valitse **Uusi** ja valitse sitten **Sertifikaattityyppi**-kentässä **PMP**.
4. Valitse **Alkamispäivä**-kentässä **1.10.2015** ja valitse sitten **Tallenna**.

### <a name="set-up-competencies-skills"></a>Määritä pätevyyksiä: taidot

1. Varmista **Työntekijät**-luettelosivulla, että edellisessä menettelyssä käyttämäsi työntekijä on yhä valittuna. Valitse sitten toimintoruudun **Työntekijät**-välilehden **Pätevyydet**-ryhmässä **Taidot**.
2. Valitse **Uusi**.
3. Valitse **Taito**-kentässä **Projektinhallinta**.
4. Valitse **Taso**-kentässä **5 Asiantuntija**.
5. Valitse **Tasopäivämäärä**-kentässä **14.1.2014**.
6. Syötä **Kokemus vuosissa** -kenttään **10**.
7. Valitse **Tallenna** ja sulje sivu.

## <a name="create-a-new-project"></a>Luo uusi projekti
1. Valitse **Projektinhallinta**-sivulla **Uusi projekti** ja syötä seuraavat arvot:

    - **Projektityyppi:** Aika ja materiaali
    - **Projektin nimi:** XYZ-päivityksen vaihe 2
    - **Projektiryhmä:** TM\_WIP
    - **Projektisopimuksen tunnus:** 00000002

2. Valitse **Luo projekti**.

### <a name="assign-a-resource-to-a-project"></a>Resurssin osoittaminen projektille

1. Valitse **Työntekijät**-sivun **Työntekijät**-luettelosta sen työntekijän tietue, jolle olet aiemmin määrittänyt pätevyyksiä, ja avaa työntekijän tietue.
2. Valitse toimintoruudun **Projekti**-välilehden **Määritys**-ryhmässä **Osoita projekteja**.
3. Käytä suodattimena **XYZ-päivityksen vaihe 2** -projektia suodattimena **Resurssivahvistuksen projektiosoitukset**-sivun **Projektit**-välilehden **Lisää projekti valittuihin projekteihin** -kentässä.
4. Valitse **Jäljellä olevat projektit** -ruudussa projekti ja lisää se sitten **Valitut projektit**-ruutuun valitsemalla nuolipainike.

Voit myös määrittää resurssille luokkia tarpeen mukaan. Luokan tyyppi on joko **Kustannus** tai **Tuotto**. Organisaatiosi määrittää luokkatyypin. Jos resurssille ei ole määritetty luokkia, Finance hakee tuntihintojen oletusluokan kustannuksille ja tuotoille.

### <a name="set-up-project-resource-and-role-characteristics"></a>Projektiresurssin ja rooliominaisuuksien määrittäminen

Projektipäällikkö voi luoda projektin edellyttämiä rooleja projektin resusointitoiminnon avulla. Rooleja voidaan käyttää, jos vahvistetut resurssit ovat vielä tuntemattomia, kun resursseja varataan. Roolit voidaan varata väliaikaisesti suunnitelluiksi resursseiksi, jotta voit jatkaa projektin suunnitteluvaiheita.

[![Esimerkki roolista](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Skenaario:** Contoso palkattiin suorittamaan Aika ja materiaali -projekti, jolla on hyväksytty projektin peruskirja. Aliprojektipäällikkö määrittää edelleen projektin vaikutusaluetta. Resurssipäällikkö on tällä hetkellä määrittämässä erityisiä resursseja, jotka varataan työskentelemään uudessa projektissa. Projektin kriittisen luonteen vuoksi projektin rahoittaja pyysi projektipäällikköä yhdeksi rooleista. Resurssipäällikön täytyy hankkia uusi resurssi ja määrittää se järjestelmässä, jos aliprojektipäällikkö tarvitsee resurssin tiedot projektisuunnittelun aikana.

Seuraavissa vaiheissa näytetään, miten resurssipäällikkö voi määrittää projektipäällikön roolin ja osoittaa sille resurssiominaisuuksia. Roolia voi myöhemmin käyttää sellaisten käytettävissä olevien resurssien hakemiseen, jotka täyttävät resurssin pätevyysvaatimukset.

1. Valitse **Määritä roolit**-sivulla **Uusi** ja syötä seuraavat arvot:

    - **Roolin tunnus:** Projektipäällikkö
    - **Kuvaus:** Projektipäällikkö

2. Valitse **Luo**.
3. Valitse **Projektipäällikkö**-rooli ja valitse sitten **Määritä ominaisuudet**.
4. Valitse **Ominaisuustyyppi**-kentässä **Taito**.
5. Syötä haettava taito **Käytettävissä olevat ominaisuudet** -kenttään.
6. Valitse **Ominaisuustyyppi**-kentässä **Sertifikaatti**.
7. Syötä haettava sertifikaattityyppi **Käytettävissä olevat ominaisuudet** -kenttään.

### <a name="assign-a-project-resource-to-a-project"></a>Projektiresurssin osoittaminen projektille

1. Valitse **Kaikki projektit** -sivulla **XYZ-päivityksen vaihe 2** -projekti.
2. Valitse **Projektitiimi ja aikataulutus** -välilehdellä **Lisää**.
3. Valitse **Rooli**-kentässä **Tiimin jäsen**.
4. Valitse **Varaa kalenterissa**.
5. Valitse **Resurssin käytettävyys** -sivulla **Näytä asetukset**.
6. Syötä **Säädä näkymäasetuksia**-sivulle seuraavat arvot:

    - **Päivämäärävälinäkymän muoto:** Päivä
    - **Näytä käytettävyyskuvaukset:** Kyllä
    - **Näytä jäljellä oleva kapasiteetti:** Kyllä

7. Valitse resurssi resurssiluettelosta.
8. Valitse **Tee sitova varaus** ja **Täysi kapasiteetti**.


### <a name="assign-a-resource-to-a-default-role"></a>Osoita resurssi oletusroolille

Jotta projekti- tai resurssipäälliköt voisivat porautua helpommin syvemmälle projektille varattavissa oleviin resursseihin. Voit liittää oletusroolin aiemmin luotuun resurssiin tai juuri hankittuun resurssiin. Kun esimerkiksi Taneli palkattiin, hänellä oli kokemus ja taidot liiketoiminta-analyytikon roolin täyttämiseen. Resurssipäällikkö osoitti kyseisen roolin Tanelin oletusrooliksi. Siksi resurssipäällikkö lisäsi Tanelin niiden liiketoiminta-analyytikkojen varantoon, jotka ovat käytettävissä projekteissa työskentelemiseen.

Resurssivarauksen aikana projektipäälliköt voivat suodattaa niitä rooliresursseja, jotka ovat käytettävissä projekteissa työskentelemiseen. He voivat käyttää näitä tietoja yhtenä perusteena, kun he suorittavat useiden perusteiden päätösanalyysiä resurssin täyttämisen aikana. He voivat myös lisätä suodattimeen muita resurssiominaisuuksia hakeakseen resursseja, joilla on tietyt taidot, koulutus ja kokemus tiettyä projektia varten.

**Skenaario:** Hyväksytty projekti on alkanut ja projektipäällikön rooli varattiin suunnitelluksi resurssiksi projektin suunnitteluvaiheessa. Resurssipäällikkö on nyt hankkinut resurssin täyttämään projektipäällikön roolin.

1. Valitse **Resurssiluettelo**-sivulla **Taneli Kultaranta**.
2. Valitse **Resurssin rooli**-sivulla **Uusi** ja syötä seuraavat arvot:

    - **Voimaantulo:** Anna nykyinen päivämäärä.
    - **Vanheneminen:** Syötä **Ei koskaan**.
    - **Rooli:** Syötä **Projektipäällikkö**.

3. Valitse **Tallenna** ja sulje sivu.
4. Lisää **Pätevyydet**-välilehdessä taito **ProjectMgmt** ja sertifikaatti **PMP**.

## <a name="set-up-role-based-pricing"></a>Roolipohjaisen hinnoittelun määrittäminen
Kaikki kustannus-, myynti- ja siirtohinnat voidaan määrittää rooleille.

1. Valitse **Myyntihinta (tunti)**-sivulla **Uusi** ja syötä voimaantulopäivä.
2. Valitse rooli **Rooli**-sarakkeesta.
3. Syötä **Hinnoittelu**-sarakkeeseen hinta valitulle resurssiroolille.

## <a name="form-a-project-team"></a>Projektitiimin muodostaminen
Jotta projektipäällikkö voisi käyttää aiemmin projektissa määritettyjä rooleja, hänen on osoitettava roolit projektille. Projektille voidaan osoittaa useita rooleja. Sekaannusten välttämiseksi näille rooleille määritetään automaattisesti otsikko varauksen aikana. Jos projektipäällikkö tarvitsee kolmea ohjelmistosuunnittelijaa, luodaan automaattisesti kolme ohjelmistosuunnittelijan roolia, joiden otsikot ovat **ohjelmistosuunnittelija 1**, **ohjelmistosuunnittelija 2** ja **ohjelmistosuunnittelija 3**. Jos roolille on aiemmin määritetty rooliominaisuudet, niitä käytetään suodattimena resurssin haun aikana. Lisäominaisuuksia voidaan lisätä tarpeen mukaan haun tarkentamiseksi.

Näkymäasetuksia voi myös mukauttaa paremman kuvan antamiseksi resurssien käytettävyydestä. Käytettävyys voidaan esittää tunneittain, viikoittain, kuukausittain, neljännesvuosittain ja vuosittain. Myös resurssien käytettävissä oleva ja jäljellä oleva kapasiteetti voidaan näyttää. Tästä vaihtoehdosta on hyötyä ajanhallinnassa, kun arvioit aktiviteetteihin käytettävissä olevaa aikaa tai resurssien käytettävyyttä.

Projektipäällikkö voi valita sivulla roolin ja sitten, jos vaatimuksen täyttävä resurssi on käytettävissä, päättää varata resurssin täyttämään kyseinen rooli. Huomaa, että resursseja ei tarvitse varata tässä kohtaa suunnitteluvaihetta. Kun luot työrakennemallin, voit korvata roolit projektin henkilöresursseilla. Jos roolit korvataan työrakenteessa henkilöresursseilla, resurssien määritys päivittää automaattisesti projektitiimiluettelon ja aikataulutuksen.

[![Projektitiimin luettelo, joka sisältää sekä roolit että todelliset resurssit](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektipäälliköllä on useita vaihtoehtoja resurssin varaamiseen projektia varten, kuten **Jäljellä oleva kapasiteetti**, **Koko kapasiteetti**, **Prosenttiosuus kapasiteetista** ja **Työtuntien määritys**. Nämä varausvaihtoehdot voidaan peruuttaa milloin tahansa, jos resurssiosoitukset muuttuvat. Kahdenlaisia varauksia tuetaan:

- **Sitova varaus** – Resurssin varaus on hyväksytty ja vahvistettu työskentelemään kiinnityksessä määritetyn keston ajan.
- **Alustava** – Resurssin varaukset on alustettavasti määritetty työskentelemään kiinnityksessä määritetyn keston ajan.

Seuraava menettely selittää, miten projektitiimi luodaan.

### <a name="create-a-project-team"></a>Projektitiimin luominen

1. Valitse **Kaikki projektit** -luettelosivulta projekti ja valitse sitten **Muokkaa**.
2. Syötä **Projektitiimi ja aikataulutus** -välilehden **Aikataulun päättymispäivä**-kenttään aikataulun alkamispäivä plus yksi kuukausi. Jos aikataulu esimerkiksi alkaa 24. kesäkuuta 2017 (24.6.2017), syötä **24.7.2017**.
3. Valitse **Lisää**.
4. Valitse **Lisää rooleja projektiin** -ruudun **Rooli**-kentässä **Projektipäällikkö**.
5. Valitse **Vaadittavat pätevyydet**.
6. **Valitse ominaisuudet** -sivulla ovat oletusarvoisesti valittuna ne ominaisuudet, jotka olet aiemmin määrittänyt projektipäällikön roolille. Valitse **OK**.
7. Kirjoita **Lisää rooleja projektiin**-sivun **Resurssien määrä**-kenttään **1**.
8. Haku näyttää **Resurssi**-kentässä kaikki resurssit, joilla on vaadittavat pätevyydet. Valitse **Taneli Kultaranta** ja sitten **Luo**.
9. Valitse **Projekti**-sivulla **Lisää**.
10. Valitse **Lisää rooleja projektiin** -ruudun **Rooli**-kentässä **Tiiminjäsen**. Syötä **Resurssien määrä** -kenttään **5**.
11. Valitse **Luo**.
12. Valitse **Projektit**-sivulla **Täytä resurssi**.

## <a name="resource-capacity-synchronization"></a>Resurssikapasiteetin synkronointi
Resurssisynkronoinnin prosessit auttavat sen varmistamisessa, että kalenterin ja peruskalenterin tiedot kopioidaan projektin resurssiaikataulutukseen. Jos kalenteria muutetaan, prosessit tekevät tarvittavat päivitykset projektiresurssien aikataulutukseen. Prosessit auttavat myös parantamaan tehokkuutta, koska kalenterin resurssitiedot synkronoidaan etukäteen. Siksi päivitykset resurssiaikataulutustietoihin tapahtuvat nopeammin. Suosittelemme prosessien aikatauluttamista erissä sen sijaan, että ne aikataulutettaisiin yksi kerrallaan. Muussa tapauksessa on vaarana, että joku on unohtanut mukana olevat päivämäärät, kun tiedot on viimeksi synkronoitu. Jos mukana olevia päivämääriä ei käytetä, päivämäärän synkronoinnissa voi esiintyä aukkoja.

![Kalenterin synkronointi](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Resurssikapasiteettien koontien synkronointi

Synkronointiprosessi on suunniteltu synkronoimaan kaikki resurssikalenterin tiedot. Näihin tietoihin kuuluvat peruskalenterin tiedot kaikista muutoksista projektin resurssikalenterin kapasiteettitaulukkoon. Jos projektiin lisätään uusia resursseja, synkronointi auttaa varmistamaan, että päivitetyt kalenteritiedot ovat käytettävissä. Synkronoinnin vois suorittaa milloin tahansa.

On suositeltavaa synkronoida erissä. Asetukset ovat käytettävissä kapasiteettivarausten synkronoinnin yhteydessä.

1. Valitse **Projektinhallinta ja kirjanpito** &gt; **Jaksoittainen** &gt; **Kapasiteetin synkronointi** &gt; **Synkronoi resurssikapasiteettien koonnit**.
2. Määritä seuraavan taulukon asetukset.

    | Asetus      | Kuvaus |
    |-------------|-------------|
    | Jaksokoodi | Voit myös valita pääkirjan päivämäärävälin koodin määrittääksesi resurssikapasiteettien koontien synkronointiprosessin alkamis- ja päättymispäivät. |
    | Alkamispäivä  | Syötä resurssikapasiteettien koontien synkronointiprosessin alkamispäivä. |
    | Päättymispäivä    | Syötä resurssikapasiteettien koontien synkronointiprosessin päättymispäivä. |

[![Synkronointiprosessi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Roolien määrittäminen työrakennemalleissa
Projektipäälliköt voivat määrittää työrakeennemalleja, joita he voivat käyttää luodessaan työrakenteita uusille projekteille. Projektipäälliköt voivat lisätä rooleja luodessaan mallin. Käytä seuraavaa menettelyä osoittaaksesi roolin työrakennemallille.

1. Valitse **Projektinhallinta ja kirjanpito** &gt; **Määritys** &gt; **Projektit** &gt; **Työrakennemallit**.
2. Valitse **Tiedot** valittua työrakennemallia varten.
3. Valitse tehtävä luettelosta ja valitse sitten **Rooli**-kentässä rooli, jolle tehtävä osoitetaan.

### <a name="work-with-a-wbs"></a>Työrakenteen kanssa työskentely

Voit luoda uuden työrakenteen tai voit kopioida työrakenteen olemassa olevasta työrakennemallista. Projektipäällikkö voi helposti hallita resursseja määrittämällä rooleja työrakenteen uusille tehtäville. Roolit voidaan korvata joko sen jälkeen, kun resurssi on hankittu tai kun tehtävän suorittamiseen on tunnistettu vahvistettu resurssi. Tämän joustavuuden ansiosta projektipäälliköt voivat suorittaa seuraavat tehtävät:

- Työrakennetyöpakettien edellyttämien resurssien määrän tunnistaminen.
- Projektin kustannusten arviointi.
- Alustavan budjetin määrittäminen.
- Aktiviteetin kestoin arvioiminen roolien ja resurssien perusteella.
- Projektinhallintasuunnitelmien kehittäminen käytettävissä olevien projektitietojen perusteella.

Työrakenteeseen on lisätty lisäasetuksia, jotta resursointitoimintoa voidaan hyödyntää paremmin.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Asetus</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Resurssimääritykset</td>
<td>Tarkastella työrakenteen tehtävien osoitettuja resursseja, päivämääriä, tuntimääriä ja varaustyyppejä.</td>
</tr>
<tr class="even">
<td>Tiimin automaattinen luonti</td>
<td>Lisää suunniteltuja resursseja automaattisesti käyttämällä rooleja, jotka on osoitettu tehtävälle. Finance ehdottaa automaattisesti suunniteltuja resursseja käyttämällä rooleihin perustuvaa moniperusteista päätösanalyysia. Kun roolit ja työmäärä (tuntia) on määritetty työrakenteen tehtäville ja kun rakenne on julkaistu, valitse <strong>Luo tiimi automaattisesti</strong>. Tarvittava suunniteltujen resurssien määrä lisätään työrakenteeseen ja <strong>Projektin ja tiimin aikataulutus</strong> -välilehteen.</td>
</tr>
<tr class="odd">
<td>Resurssi (avautuva luettelo)</td>
<td><strong>Käynnistä resurssimääritys</strong> -sivulla voit valita sitovasti tai alustavasti varattavia resursseja määritetyn keston perusteella. Voit muokata näkymäasetuksia nähdäksesi ja voidaksesi määrittää resurssiaktiviteettien kestoja. Voit valita ja osoittaa resursseja työpakettien tasolla käyttämällä seuraavia asetuksia:
<ul>
<li><strong>Hyväksy</strong> – Vahvista muutokset tehtävälle osoitettuun resurssiin.</li>
<li><strong>Peruuta</strong> – Peruuta muutokset tehtävälle osoitettuun resurssiin.</li>
<li><strong>Osoita automaattisesti</strong> – Käytettävissä oleva henkilöresurssi, jolla on vastaava rooli, valitaan ja osoitettaan valitulle tehtävälle automaattisesti.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Valitse **Kaikki projektit** -sivulla **XYZ-päivityksen vaihe 2** -projekti.
2. Valitse **Suunnittele** &gt; **Aktiviteetit** &gt; **Työrakenne**.
3. Lisää seuraavat tason yksi aktiviteetit työrakenteeseen valitsemalla **Uusi**:

    - Aloitus
    - Suunnittelu
    - Suoritetaan
    - Seuranta ja valvonta
    - Sulje

4. Määritä päivämäärät ja työmäärä (tuntia) seuraavassa kuvassa näkyvällä tavalla.

    [![Päivämäärien ja työmäärän määrittäminen](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Valitse **Aloitus**-tehtävärivi ja sitten **Rooli**-kentässä **Projektipäällikkö**.
6. Valitse **Julkaise**.
7. Valitse saman rivin **Resurssi**-kentässä **Taneli Kultaranta** ja valitse sitten **Hyväksy**.
8. Valitse **Suunnittelu**-tehtävärivi ja valitse sitten **Rooli**-kentässä **Liiketoiminta-analyytikko**.
9. Valitse **Julkaise** ja sitten **Luo tiimi automaattisesti**.
10. Valitse avautuvassa viestiruudussa **Kyllä**.
11. Tarkista, että **Resurssi**-kentän arvo on **Liiketoiminta-analyytikko 1**.
12. Avaa **Liiketoiminta-analyytikko 1** -resurssin haku ja valitse **Käynnistä resurssimääritykset**. Valitse sitten tehtävälle työntekijä.
13. Valitse **Osoita alustavasti** &gt; **Koko kapasiteetti**.

    > [!NOTE] 
    > Et saa varoitusta siitä, että määritetty resurssi on nyt 2, koska resurssien määränä säilyy 1.

14. Vahvista työrakenteen resurssimääritys **Työrakenne**-sivulla ja valitse sitten **Tallenna**.

## <a name="resource-fulfillment-for-planned-resources"></a>Resurssien täyttäminen suunniteltujen resurssien osalta
Projektipäällikkö voi suunnitella projektiin tarvittavat resurssiroolit. Resurssipäällikkö näkee nämä suunnitellut resurssit **Resurssin täyttäminen** -sivulla pyyntöinä ja voi osoittaa todellisia resursseja.

1. Valitse **Kaikki projektit** -sivulla **XYZ-päivityksen vaihe 2** -projekti.
2. Valitse **Projekti** ja sitten **Muokkaa**.
3. Valitse **Projektitiimi ja aikataulutus** -välilehdellä **Lisää**.
4. Valitse **Lisää rooleja** -valintaikkunassa rooli **Ohjelmistokehittäjä**.
5. Valitse **Luo** ja sulje sitten projektisivu.
6. Valitse **Resurssin täyttäminen** -sivulla **Ohjelmistokehittäjä 1** projektille **XYZ-päivitysprojektin vaihe 2** -projektille.
7. Valitse työntekijä ja sitten **Osoita**.
8. Tarkista, että roolin **Ohjelmistokehittäjä 1** rivi on poistettu **XYZ-päivitysprojektin vaihe 2** -projektin osalta.
9. Tarkista **XYZ-päivitysprojektin vaihe 2** -projektin **Projektitiimi ja aikataulutus** -välilehdellä, että edellisessä vaiheessa valitsemasi työntekijä on lisätty roolilla **Ohjelmistokehittäjä**.

## <a name="requests-for-project-resources"></a>Projektiresurssipyynnöt
Projektiresurssien aikataulutustoiminto salli resurssipäälliköiden jakaa henkilöresursseja vain kiinnityksiin tai projekteihin. Voit ottaa tämän toiminnon käyttöön täyttämällä suorittamalla seuraavat tehtävät tai varmistamalla, että ne on suoritettu:

- Numerosarjojen määrittäminen.
- Projektinhallinnan ja kirjanpidon työnkulkujen määritys.
- Resurssipyyntöjen työnkulkujen käyttööotto.

Kun edeltävät tehtävät on suoritettu, voit suorittaa seuraavat tehtävät tarpeen mukaan:

- Resurssipyynnön luominen alustavasti varatusta henkilöresurssista.
- Resurssipyyntöjen seuranta.
- Resurssipyyntöjen täyttäminen.
- Pyydä henkilöresurssia työrakenteesta.
- Varaa resursseja projektiin ilman henkilöresurssia koskevaa pyyntöä.

## <a name="monitor-project-teams"></a>Projektitiimien seuraaminen
1. Valitse **Kaikki projektit** -sivulla **XYZ-päivityksen vaihe 2** -projektin **Projektitunnus**-linkki.
2. Varmista **Projektitiimi ja aikataulutus** -pikavälilehdessä, että luettelossa olevat projektiresurssit ovat oikein.
