---
title: Työrakenteiden yleiskatsaus
description: Työrakenne (WBS) on niiden töiden kuvaus, jotka projektissa tehdään. Se on tehtävähierarkia, joka edustaa projektiryhmän tietämystä työn koostumuksesta sekä kunkin osan tai tehtävän koosta, kustannuksista ja kestosta.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 713e38f4218b980c4256e433e90c12adccd70e11
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012222"
---
# <a name="work-breakdown-structures-overview"></a>Työrakenteiden yleiskatsaus

[!include [banner](../includes/banner.md)]

Työrakenne (WBS) on niiden töiden kuvaus, jotka projektissa tehdään. Se on tehtävähierarkia, joka edustaa projektiryhmän tietämystä työn koostumuksesta sekä kunkin osan tai tehtävän koosta, kustannuksista ja kestosta. Työrakenteella on kolme päätarkoitusta:

-   Kuvailla tehtävien töiden rakennetta tai koostumusta.
-   Aikatauluttaa projektin työt.
-   Arvioida kunkin tehtävän kustannukset.

Työrakenteen yksityiskohtaisuus riippuu arvioissa tarvitusta tarkkuustasosta sekä näiden arvioiden seurannalta vaaditusta tasosta. Projektit, joiden aikataulussa tai kustannuksissa on hyvin vähän toleranssivaraa, edellyttävät yleensä yksityiskohtaisempia työrakenteita sekä työn edistymisen ja kustannusten huolellista seurantaa työrakenteeseen verrattuna. Tällaiset projektit ovat yleisiä rakennus- ja koneteollisuudessa. 

Sen sijaan projektit median ja markkinoinnin, ohjelmistojen ja IT-infrastruktuurin kaltaisilla toimialoilla ovet yleensä ainutkertaisia, ja tuottavuus riippuu tehtävän suorittavan henkilön kokemuksesta ja pätevyydestä. Siksi näillä toimialoilla käytetään työrakennetta arvion saamiseksi projektin koosta eikä kyseisen projektin edistymisen yksityiskohtaiseen seurantaan. 

Työrakenteen luominen on intensiivinen prosessi, joka yleensä toteutetaan pitkän ajan kuluessa ja edellyttää yhteistyötä ja tietoja monenlaisilta henkilöiltä. Tässä aiheessa kerrotaan, miten voit käyttää työrakenteen parannuksia täyttämään arvioita ja seurantaa koskevat tarpeesi.

## <a name="prerequisites-for-creating-a-wbs"></a>Työrakenteen luomisen edellytykset
Työrakenteen luomista varten sinun on voitava luoda työaikataulu ja arvioitava työkustannukset.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Työaikataulun luomisen edellytykset

Jos haluat käyttää työrakennetoimintojen täysiä aikatauluominaisuuksia, suorita seuraava määritys:

1.  Määritä oletuskalenteri ja projektikalenteri:
    1.  Valitse **Projektinhallinta ja kirjanpito** &gt; **Määritys** &gt; **Projektinhallinnan ja kirjanpidon parametrit** &gt; **Aikataulutus**. Määritä **Oletusarvoinen työkalenteri** -kentässä oletuskalenteri. Tätä käytetään uusien projektien oletusarvoisena työkalenterina.
    2.  Voit muuttaa tietyn projektin oletuskalenteria. Valitse projektin tietosivu ja päivitä sitten **Projektitiimi ja aikataulutus** -pikavälilehdessä **Aikataulutuskalenteri** -kenttä valitsemalla toinen kalenteri.

2.  Määritä vakiotyöpäivät ja -työajat. Projektin työkalenteriksi määritettyä kalenteria käytetään työrakenteessa seuraavien tietojen määrittämiseen:

-   Työpäivät ja vapaapäivät
-   Päivittäisten työtuntien määrä

Jos haluat määrittää kalenterin työpäivät ja työtunnit tai luoda uuden kalenterin, valitse **Organisaatoin hallinta** &gt; **Yhteiset**&gt; **Kalenterit**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Työkustannusten arvioinnin edellytykset

Jos haluat käyttää työrakenteiden täysiä kustannusarvio-ominaisuuksia, sinun on määritettävä työntekijöiden, työluokkien, kustannusten ja maksujen sekä kohteiden kustannus- ja myyntihinnat.

-   Voit määrittää työn, kustannusten ja maksujen kustannus- ja myyntihinnat valitsemalla **Projektinhallinta ja kirjanpito** &gt; **Määritys** &gt; **Hinnat**.
-   Jos haluat määrittää kohteiden kustannus- ja myyntihinnan, käytä kunkin kohteen **Kauppasopimukset** -sivua tuotetietojen hallinnan **Julkaistut tuotteet** -luettelosivulla.

## <a name="creating-a-wbs"></a>Työrakenteen luominen
Työrakenteen luominen koostuu kolmesta aktiviteetista:

1.  **Työn hajottaminen** – Erittele työ hallittaviin osiin tai tehtäviin.
2.  **Työaikataulu** – Arvioi tehtävän suorittamiseen vaadittava aika, määritä tehtävien riippuvuussuhteita ja valitse tehtävien alku- ja loppupäivämääriä.
3.  **Kustannusarvio** – Arvioi kunkin tehtävän kustannukset.

Seuraavissa osissa on käsitellään siitä, miten työrakenneominaisuudet voivat auttaa kussakin näistä aktiviteeteista.

### <a name="work-decomposition"></a>Työn hajottaminen

Työn erittelyn tai hajotelman luominen on yleensä työrakenteen luontiprosessin ensimmäinen vaihe. Työrekennetoiminto tukee seuraavia perusrakenteita työn erittelyä tai hajotelmaa varten. 

**Projektin päätehtävä** Projektin päätehtävä on projektin ylimmän tason yhteenvetotehtävä. Kaikki muut projektitehtävät luodaan sen alle. Päätehtävän nimenä on aina projektin nimi. Pääsolmun työmäärä, päivämäärät ja kesto muodostavat yhteenvedon arvoista päätehtävän alla olevia tehtäviä varten. Et voi muokata pääsolmun ominaisuuksia etkä poistaa pääsolmua.

**Yhteenveto- tai säilötehtävät** Yhteenvetotehtävä on tehtävä, jolla on alapuolellaan alitehtäviä tai jäsentehtäviä. Yhteenvetotehtävällä ei ole omaa työmäärää eikä kustannuksia. Sen sijaan yhteenvetotehtävän työmäärä ja kustannukset ovat sen jäsentehtävien työmäärien ja kustannusten summa. Jäsentehtävien aikaisinta alkamispäivää käytetään yhteenvetotehtävän alkamispäivänä ja jäsentehtävien viimeistä päättymispäivää käytetään päättymispäivänä. Yhteenvetotehtävän nimeä voi muokata, mutta aikataulutusominaisuuksia (työmäärä, päivämäärät, kesto) ei voi muokata. Jos poistat yhteenvetotehtävän, poistat myös kaikki sen jäsentehtävät. 

**Lehtisolmutehtävä** Lehtisolmutehtävä edustaa projektin yksityiskohtaisinta työpakettia. Lehtisolmulla on arvioitu työmäärä, suunniteltu määrä resursseja, suunnitellut alkamis- ja päättymispäivämäärä sekä kesto. 

Voit suorittaa seuraavat hierarkiatoiminnot, kun haluat ottaa käyttöön työhierarkian luonnin tai projektin hajottamisen. 

**Uusi tehtävä** Kaikki luomasi uudet tehtävät lisätään automaattisesti pääsolmun alle ja tehtävälle määritetään automaattisesti työrakennenumero. Työrakennenumero edustaa hierarkian tehtävätasoa. Ensimmäisellä projektin päätehtävän alla olevalla tasolla sijaitsevissa tehtävissä käytetään numerointia 1, 2, 3 jne. Ensimmäisen tason alla olevissa tehtävissä käytetään numerointia 1.1, 1.2, 1.3 jne. Kutakin aiemman tason alapuolelle lisättävää tasoa kohden lisätään uusi numerosarja pisteen jälkeen. 

Tällä hetkellä työrakennenumerointia ei voi mukauttaa. 

**Sisennä tehtävä** Kun sisennät tehtävän, siitä tulee edeltävän tehtävän alitehtävä. Uuden alitehtävän työrakennenumero lasketaan automaattisesti uudelleen uuden päätehtävän työrakennenumeron perusteella. Päätehtävä on nyt yhteenveto- tai säilötehtävä, joten tiitä tulee jäsentehtäviensä koontitehtävä. 

> [!NOTE] 
> Kun tehtäviä sisennetään sellaisen tehtävän alle, joka oli lehtisolmu ennen sisennysmenettelyä, uusi yhteenvetotehtävä menettää omat päivämääränsä, työmääränsä ja resurssimääränsä. Se käyttää nyt yhteenvetoa uusien jäsentehtäviensä arvoista. 

**Ulonna tehtävä** Kun ulonnat tehtävän, se ei ole enää päätehtävänsä jäsentehtävä. Tämän tehtävän työrakennenumero lasketaan automaattisesti uudelleen, jotta se vastaisi tehtävän uutta hierarkiatasoa. Tehtävän aiemman päätehtävän työmäärä, kustannukset ja päivämäärät lasketaan sitten uudelleen siten, että ne eivät enää sisällä kyseistä tehtävää. 

**Siirrä ylöspäin ja Siirrä alaspäin** Kun valitset **Siirrä ylöspäin** ja **Siirrä alaspäin**, muutat tehtävän sijaintia päätehtävänsä hierarkiassa. Tehtävän sijainti ei vaikuta tehtävän työmäärään, kustannuksiin päivämääriin tai kestoon. Tehtävän työrakennenumero kuitenkin lasketaan automaattisesti uudelleen, jotta se vastaisi tehtävän uutta sijaintia.

### <a name="schedule-estimation"></a>Aikatauluarvio

Aikatauluarvio on yleensä työrakenteen luomisen toinen vaihe. Paras käytäntö on toteuttaa aikatauluarvio, kun olet luonut tehtävät. Financen **Työrakenne**-sivulla on kaksi osaa. Yläruutu on tarkoitettu aikatauluarviolle, ja alaruudussa on **Arvioidut kustannukset ja tuotot** -välilehti, jota voit käyttää kustannusten arviointiin. 
**Tehtäväriippuvaisuudet** Työrakenteessa voidaan luoda tehtävien välille edeltäjäsuhde. Kun määrität tehtävälle edeltäjätehtäviä, tehtävä voi alkaa vasta, kun kaikki edeltäjätehtävät on suoritettu. Tehtävän suunnitelluksi alkamispäiväksi määritetään aina sen kaikkien edeltäjien viimeisin päivämäärä. 

**Tehtävien ajoitus** Seuraavat tekijät määrittävät lehtisolmutehtävien aikataulutuksen:

-   Edeltäjät
-   Työmäärä
-   Resurssien määrä
-   aloitus- ja päättymispäivät

Lehtisolmutehtävän, jolla ei ole edeltäjiä, aloituspäivämääräksi määritetään automaattisesti projektin ajoituksen aloituspäivämäärä. Lehtisolmutehtävän kesto vastaa aina alkamis- ja päättymispäivämäärien välisten työpäivien lukumäärää. 

*<strong><em>Aikataulutussäännöt</em></strong>* Kun automaattinen aikataulutusapu on käytössä, lehtisolmutehtävien tehtäväaikataulutukseen pätevät seuraavat säännöt:

-   Tehtävän alkamis- ja päättymispäivien on aina oltava projektin ajoituskalenterin mukaisia työpäiviä.
-   Tehtävän, jolla on edeltäjiä, aloituspäivämääräksi määritetään automaattisesti sen edeltäjien myöhäisin lopetuspäivämäärä.
-   Tehtävän työmäärä lasketaan automaattisesti seuraavasti:

Henkilömäärä × kesto × projektikalenterin normaalin työpäivän tuntimäärä. 

Joissakin tapauksissa haluat ehkä poiketa näistä säännöistä. Voit poistaa automaattisen aikataulutuksen käytöstä, jos haluat estää, että Finance määrittää tai korjaa automaattisesti lehtisolmun tehtävien ominaisuuksia. Kun määrität tehtävälle tietoja, jotka aiheuttavat aikataulutussääntöjen rikkomisen, tehtävän osalta näytetään aikataulutusvirheen kuvake. Jos et halua aikataulutusvirheiden näkyvän, poista ominaisuus käytöstä napsauttamalla kohtaa **Aikataulutusvirheet näytetään**. 

> [!NOTE] 
> Yhteenveto- tai säilötehtävän arvot lasketaan edelleen jäsentehtävien arvojen summana riippumatta siitä, onko automaattinen aikataulutusapu käytössä. 

**Aikataulutusvirheiden korjaaminen** Kun automaattinen aikataulutusapu on käytössä, aikataulutusvirheitä ei todennäköisesti tapahdu. Jos taas poistat automaattisen aikataulutusavun käytöstä ja otat sen sitten uudelleen käyttöön myöhemmin, työrakenneluettelossa saattaa näkyä aikataulutusvirhekuvakkeita. 

**Aikataulutusvirheiden tehtäväkohtainen korjaaminen** Kun kaksoisnapsautat tietyn tehtävän aikatauluvirhekuvaketta, tulee näkyviin valintaikkuna, joka sisältää kaikki kyseisen tehtävän aikataulutusvirheet. Voit päättää, mitkä tehtävän aikataulutusvirheet korjataan. 

**Kaikkien aikataulutusvirheiden korjaaminen** Jos haluat Financen korjaavan kaikki työrakenteen aikataulutusvirheet, valitse toimintoruudussa **Korjaa kaikki aikataulutuksen ristiriidat**. 

> [!NOTE] 
> Tämä toiminto voi aiheuttaa merkittäviä muutoksia työrakenteeseen. Virheet korjataan seuraavassa järjestyksessä:

1.  Kaikkien tehtävien arvioitua työmäärää muokataan siten, että se vastaa projektikalenterissa määritettyä kapasiteettia.
2.  Kunkin tehtävän alkamispäivää muokataan siten, että tehtävä käynnistyy sen jälkeen, kun kaikki sen edeltäjätehtävät on suoritettu.
3.  Kunkin tehtävän alkamispäivää muokataan, jotta edeltäjätehtävien alkamispäivät ei jää aukkoja.

### <a name="cost-estimation"></a>Kustannusarvio

Kuten tässä asiakirjassa aiemmin mainittiin, voit määrittää kustannusarvion kullekin lehtisolmun tehtävälle käyttämällä **Työrakenne**-sivun alaruudun **Arvioidut kustannukset ja tuotot**-välilehteä. 

> [!NOTE] 
> Et voi muokata yhteenveto- tai säilötehtävän kustannusarviota. Yhteenvetotehtävän kustannusarvio vastaa sen lehtisolmutehtävien kustannusarvioiden summaa. Kunkin tehtävän arvioitu kokonaiskustannus lasketaan seuraavien tapahtumatyyppien arvioitujen kustannusmäärien summana:

-   Työ
-   Nimike tai materiaali
-   Kulut

**Maksu**-tapahtumatyyppiä käytetään maksuihin perustuvien tuottojen arviointiin. Tällä tapahtumatyypillä ei ole kustannuskomponenttia, joten sitä ei oteta huomioon kustannuksia arvioitaessa. 

**Tilillä**-tapahtumatyyppiä käytetään sovitun myyntiarvon tallentamiseen kiinteäarvoisissa projekteissa. Tätä tapahtuma tyyppiä ei myöskään oteta huomioon arvioitaessa kustannuksia. 

Kun arvioit työn, materiaalin ja kulujen kustannuksia kussakin tehtävässä, sinun on määritettävä arvioidulle kustannukselle projektiluokka. 

**Työkustannusten arviointi** Määrität jokaiselle lehtisolmutehtävälle työmäärän tunneissa sekä oletusluokan. Siten, kun määrität tehtävälle aikataulun, kyseisen tehtävän työvoimakustannusten arvio lisätään automaattisesti työn oletusluokkaan. Tämä kustannusarvio näkyy kyseisen tehtävän **Rivitiedot**-ruudukon **Arvioidut kustannukset ja tuotot**-välilehdessä. Jos tarvitset enemmän työvoima kustannusarvioita, voit lisätä ne tähän välilehteen. Jos lisäät tai vähennät työvoimakustannusarvion työtunteja, tehtävän aikataulu lasketaan automaattisesti uudelleen. 

**Kulu- ja materiaalikustannusten arviointi** **Arvioidut kustannukset ja tuotot** -välilehden avulla voit myös arvioida tehtävän kulu- ja materiaalikustannukset, jos tarvitset arvioita. 

Kunkin työ- tai kuluarviorivin kustannus- ja myyntihinta perustuvat kunkin luokan määritykselle kohdan **Projektinhallinta ja kirjanpito** &gt; **Asetukset** &gt; **Hinnoittelu** hinnoittelutaulukoissa. Nimikkeiden osalta kustannus- ja myyntihinta lisätään oletusarvoisesti tuotetietojen hallinnan **Julkaistut tuotteet** -luettelosivun nimikkeistä tai kauppasopimuksista.

## <a name="tracking-progress-on-the-wbs"></a>Edistymisen seuranta työrakenteessa
Jotkut toimialat seuraavat projektin edistymistä työrakenteeseen verrattuna hyvin yksityiskohtaisella tasolla, kun taas toiset seuraavat edistymistä korkeammalla työrakenteen tasolla. Tässä osassa kuvataan, miten voit käyttää työrakenneseurantaa projektivaatimustesi osalta. 

Financessa on kolme näkymää projektin työrakenteelle: Suunnittelunäkymä, Työmäärän seurantanäkymä ja Kustannusten seurantanäkymä.

### <a name="planning-view"></a>Suunnittelunäkymä

Suunnittelunäkymässä näkyy aikataulu- ja kustannustietojen suunniteltu tai perustason arvio. Vaikka projektin työrakenteen version ja perustason seuraamiseen ei ole toimintoja, tämän näkymän arvot on tarkoitettu edustamaan perusversiota. Tämän aiheen osissa Aikatauluarvio ja Kustannusarvio kuvataan tätä näkymää ja sitä, miten sitä käytetään työrakenteen luomiseen.

### <a name="effort-tracking-view"></a>Työmäärän seurantanäkymä

Työmääräseurannan näkymässä näkyy työrakenteen tehtävien edistymisen seuranta. Siinä verrataan tehtävän kertyneitä toteutuneita työmääriä tunteina suunniteltuihin työmäärätunteihin. Työmääräseurannan näkymän arvot perustuvat seuraaviin kaavoihin:

-   Edistymisprosentti = Todellinen työmäärä tähän päivämäärään saakka ÷ Tehtävälle suunniteltu työmäärä
-   Jäljellä oleva työmäärä (eli valmistumisarvio \[ETC\]) = Suunniteltu työmäärä – Todellinen työmäärä tähän päivämäärään mennessä
-   Valmistumisen kustannusarvio (EAC) = Jäljellä oleva työmäärä + Todellinen työmäärä tähän päivämäärään mennessä
-   Ennustettu työmäärän varianssi = Suunniteltu työmäärä – EAC

Työmäärän seurantanäkymä näyttää tehtävän työmäärän varianssinennusteen, joka perustuu siihen, onko valmistumisen kustannusarvio suurempi vai pienempi kuin suunniteltu työmäärä:

-   Jos valmistumisen kustannusarvio on suunniteltua työmäärää suurempi, tehtävän ennustetaan vaativan enemmän aikaa kuin alun perin oli suunniteltu, ja se on perässä aikataulusta.
-   Jos valmistumisen kustannusarvio on suunniteltua työmäärää pienempi, tehtävän ennustetaan vaativan vähemmän aikaa kuin alun perin oli suunniteltu, ja se on edellä aikataulua.

**Projektipäällikön uusi työmääräennuste** Joskus projektipäällikön tai muun projektin edistymistä seuraavan henkilön on tarkistettava tehtävän alkuperäisiä arvioita. Tehtävä saattaa erilaisista syistä edetä alkuperäistä odotusta nopeammin tai hitaammin. Esimerkiksi laajuutta on saatettu vähentää tai työntekijöillä saattaa olla alkuperäistä suunnitelmaa vähemmän kokemusta. Ennusteet ovat projektipäällikön näkemyksiä arvioista projektin kulloisenkin tilanteen perusteella. Yleisesti ottaen perusaikataulun lukuja ei kannata muuttaa, koska projektin perusaikataulu edustaa projektin aikataulun ja kustannusarvion laajasti julkaistua asiakirjaa, josta projektin kaikki sidosryhmät ovat sopineet. 

Projektipäälliköt voivat muuttaa tehtäväien työmääriä kahdella tavalla:

-   Sen jäljellä olevan työmäärän muuttaminen, joka päivittää tehtävän kulloisenkin jäljellä olevan työmäärän automaattisesti.
-   Sen edistymisprosentin muuttaminen, joka päivittää tehtävän kulloisenkin todellisen edistymisen automaattisesti.

Molemmat lähestymistavat aiheuttavat tehtävän valmistumisarvion, valmistumisen kustannusarvion ja edistymisprosentin sekä ennustetun työmäärän varianssin uudelleenlaskennan. Myös yhteenvetotehtävien valmistumisarvion, valmistumisen kustannusarvion ja edistymisprosentti lasketaan uudelleen. Lisäksi niiden ennustettu työmäärän varianssi päivitetään. 

**Muutettu yhteenvetotehtäväien työmäärä** Voit muuttaa yhteenveto- tai säilötehtävien työmäärää. Riippumatta siitä, muutatko näitä arvoja käyttäen yhteenvetotehtävien jäljellä olevaa työmäärää vai edistymisprosenttia, laskennat suoritetaan automaattisesti seuraavassa järjestyksessä:

1.  EAC, ETC ja tehtävän edistymisprosentti lasketaan.
2.  Uusi valmistumisen kustannusarvio jaetaan alitehtäviin samassa suhteessa kuin alkuperäinen valmistumisen kustannusarvion summa.
3.  Kullekin lehtisolmutehtävälle lasketaan uusi valmistumisen kustannusarvio.
4.  Jäljellä oleva työmäärä ja edistymisprosentti lasketaan uudelleen kaikkien vaikutusalueen alitehtävien osalta uuden valmistumisen kustannusarvion arvon perusteella. Myös tehtävien työmäärän varianssi lasketaan uudelleen.
5.  Myös yhteenvetotehtävien valmistumisen kustannusarvio lasketaan uudelleen lehtisolmujen perusteella.

Määritä taso, jolla työrakennetta seurataan ja ylläpidetään, valitsemalla **Laajenna tasolle** työmäärän seurantanäkymässä. Työrakenne laajennetaan automaattisesti tälle tasolle työmäärän seurantanäkymässä aina, kun se avataan.

### <a name="cost-tracking-view"></a>Kustannusten seurannan näkymä

Kustannusten seurantanäkymässä näkyy tehtävän toteutuneiden kustannusten seuranta. Tässä näkymässä verrataan tehtävän todellisia kustannuksia kulloiseenkin päivämäärään mennessä verrataan tehtävän suunniteltuihin kustannuksiin. Kustannusten seurantanäkymän arvot perustuvat seuraaviin kaavoihin:

-   Toteutuneiden kustannusten prosenttiosuus = Toteutuneet kustannukset tähän päivämäärään asti ÷ Tehtävän suunnitellut kustannukset
-   Kustannukset valmistuessa (CTC) = Suunnitellut kustannukset – Tähän päivämäärään mennessä toteutuneet kustannukset
-   Valmistumisen kustannusarvio (EAC) = Kustannukset valmistuessa + Tähän päivämäärään mennessä toteutuneet kustannukset
-   Arvioitujen kustannusten varianssi = Suunnitellut kustannukset – EAC

Kustannusteen seurantanäkymä näyttää tehtävän kustannusten varianssinennusteen, joka perustuu siihen, onko valmistumisen kustannusarvio suurempi vai pienempi kuin suunnitellut kustannukset:

-   Jos valmistumisen kustannusarvio on suunniteltuja kustannuksia suurempi, tehtävän ennustetaan vaativan enemmän rahaa kuin alun perin oli suunniteltu, ja se on ylittämässä budjetin.
-   Jos valmistumisen kustannusarvio on suunniteltuja kustannuksia pienempi, tehtävän ennustetaan vaativan vähemmän rahaa kuin alun perin oli suunniteltu, ja se on alittamassa budjetin.

**Projektipäällikön uusi kustannusennuste** Projektipäälliköiden on käytettävä tehtävän alkuperäistä kustannusarviota tarkistettaessa kustannuksia valmistuessa. Projektipäällikkö voi kustannukset valmistuessa -arvon siksi kustannukseksi, joka tarvitaan tehtävän suorittamiseen. Jos muokkaat kustannukset valmistuessa -arvoa, valmistumisen kustannusarvio, toteutuneiden kustannusten prosenttiosuus ja tehtävän ennustettu kustannusten varianssi lasketaan uudelleen. Myös yhteenvetotehtävien valmistumisarvion, valmistumisen kustannusarvion ja toteutuneet kustannukset lasketaan uudelleen. Lisäksi niiden ennustettu kustannusten varianssi päivitetään. 

> [!NOTE] 
> Kun muutat työrakennetehtävän työmäärää Työmäärän seurantanäkymässä, tehtävän kustannukset valmistuessa, valmistumisen kustannusarvio, toteutuneiden kustannusten prosenttiosuus ja ennustettu kustannusten varianssi lasketaan uudelleen Kustannusten seurantanäkymässä. Kustannusten muutokset eivät kuitenkaan vaikuta Työmäärän seurantanäkymän arvoihin, koska tapahtumatyyppikohtaisia kustannuksia (työ, materiaali tai kulu) tai projektiluokkaa ei muuteta. 

**Yhteenvetotehtävien kustannusten ennusteiden tarkistaminen** Voit tarkistaa yhteenvetotehtävien kustannuksia, jolloin laskennat suoritetaan automaattisesti seuraavassa järjestyksessä:

1.  Tehtävän kustannukset valmistuessa, valmistumisen kustannusarvio ja toteutuneiden kustannusten prosenttiosuus lasketaan uudelleen.
2.  Uusi valmistumisen kustannusarvio jaetaan alitehtäville samassa suhteessa kuin tehtäväien alkuperäinen valmistumisen kustannusarvio.
3.  Kunkin tehtävän uusi valmistumisen kustannusarvio lasketaan.
4.  Kustannukset valmistuessa ja toteutuneiden kustannusten prosenttiosuus lasketaan valmistumisen kustannusarvion arvon perusteella uudelleen vaikutusalueen alitehtävien osalta. Myös tehtävien kustannusten varianssi lasketaan uudelleen.
5.  Kaikkien yhteenvetotehtävien valmistumisen kustannusarvio lasketaan uudelleen tämän muutoksen perusteella.

Määritä taso, jolla työrakennetta seurataan ja ylläpidetään, valitsemalla **Laajenna tasolle** Kustannusten seurantanäkymässä. Työrakenne laajennetaan tälle tasolle Kustannusten seurantanäkymässä aina, kun se avataan.

### <a name="earned-value-management"></a>Ansaitun arvon hallinta

Voit käyttää ansaitun arvon menetelmää projektin edistymisen seurantaan. Voit tarkastella ansaitun arvon mittareita projektipäällikön roolikeskuksessa. Ansaitun arvon kaavio-osa näyttää suunnitellun arvon ja todellisten kustannusten aikajaksotetut arvot. Ansaittu arvo kulloisenakin päivämääränä näytetään pisteenä. Ansaitun arvon aikajaksotettuja tietoja ei tällä hetkellä ole saatavilla. 

Ansaitun arvon kaavion aikajakso esitetään viikoittain tai kuukausittain. Tässä osassa kuvataan ansaitun arvon menetelmän kolme pilaria: suunniteltu arvo, ansaittu arvo ja toteutuneet kustannukset. 

**Suunniteltu arvo** Ansaitun arvon teorian mukaan suunnitellun arvon piirros edustaa sitä, miten projektitiimi suunnitteli ansaitsevansa arvoa projektissa. 

Finacessa käytetään 0:100-ansaintasääntöä, kun sillä piirretään suunniteltua arvoa. Tämän säännön perusteella tehtävän arvo kirjataan tehtävälle sen päättymispäivänä. Arvoa ei kirjata, ennen kuin tehtävä on 100-prosenttisesti valmis. 

Projektinhallinnassa ja kirjanpidossa syötetään lehtisolmujen päättymispäivämäärä ja niiden suunnitellut kustannukset. Kun suunnitellun arvon kaavio näytetään viikoittain, suunnitellusta arvosta tehdään viikoittainen yhteenveto kaikkien lehtisolmutehtävien osalta koko projektin keston ajan. 

**Ansaittu arvo** Ansaitun arvon teorian mukaan ansaitun arvon piirros edustaa sitä, miten projektitiimi todellisuudessa ansaitsee arvoa projektissa. 

Finacessa käytetään 0:100-ansaintasääntöä, kun sillä piirretään ansaittua arvoa. Tämän säännön perusteella tehtävän arvo kirjataan tehtävälle sen päättymispäivänä. Arvoa ei kirjata, ennen kuin tehtävä on 100-prosenttisesti valmis. 

Ansaittua arvoa laskettaessa otetaan huomioon kunkin tehtävän edistymisprosentti. 0:100-ansaintasäännön mukaan vain tiettynä ajanjaksona valmistuvat tehtävät otetaan huomioon ansaitun arvon laskennassa kyseisen jakson päättyessä. Projektin ansaitun arvon laskennassa käytetään kaikkia tehtäviä, jotka on suoritettu kaavion luontihetkellä. 

> [!NOTE] 
> Tällä hetkellä työrakenteen seurannan järjestelmässä ei ole tarvittavia tietorakenteita kunkin tehtävän historiallisten edistymisprosenttien tallentamiseen. Tämän vuoksi ansaittu arvo voidaan raportoida vain siltä ajalta, jolta kuutio on käsitelty. Käsittele kuutio säännöllisesti päivittääksesi roolikeskuksessa näkyvät ansaitun arvon tiedot. 

**Todelliset kustannukset** Ansaitun arvon teorian mukaan toteutuneiden kustannusten piirros edustaa sitä, miten projektissa käytetään rahaa. 

Projektille kirjattuja tapahtumia käytetään toteutuneen kustannusjanan piirtämiseen. Kustannukset summataan päivämäärän mukaan. Näitä tietoja käytetään sitten toteutuneiden kustannusten piirtämiseen ansaitun arvon kaaviossa viikko- tai kuukausiperusteisesti.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Suunnitellun arvon, ansaitun arvon ja todellisten kustannusten käsitteiden käyttäminen

**Aikataulun varianssi** Suunnittelussa luodaan työennuste aikajanalla. Siksi suunniteltu arvo edustaa sitä, miten projektin suunnittelijat ajattelivat töiden valmistuvan projektissa. Kun projekti on käynnissä, töitä saadaan valmiiksi ja projekti ansaitsee arvoa. Vertailemalla suunniteltua arvoa ansaittuun arvoon voit selvittää, miten projektin työt etenevät. Tämän vertailun tulosta kutsutaan aikataulun varianssiksi. 

Jos ajanjakson suunniteltu arvo on ansaittua arvoa suurempi, projektissa suoritettu työmäärä on suunniteltua pienempi. Siten projekti on jäljessä aikataulusta. Koska suunniteltu arvo ja ansaittu arvo ilmaistaan rahallisesti, projektin viiveelle määritetään myös rahallinen arvo. 

Jos ajanjakson suunniteltu arvo on ansaittua arvoa pienempi, projektissa suoritettu työmäärä on suunniteltua suurempi. Siten projekti on edellä aikataulua. Myös tälle ajalle määritetään rahallinen arvo.

**Kustannusten varianssi** Koska ansaitussa arvossa käytetään kustannushintaa kertoimena, ansaittu arvo ilmaisee projektissa suoritetun työn kustannukset. Projektin edetessä tapahtumalokissa näkyy rahamäärä, joka projektissa todella on käytetty. Vertaamalla ansaittua arvoa toteutuneisiin kustannuksiin voit vertailla keskenään käytettyä rahamäärää ja ansaittua arvoa. Tämän vertailun tulosta kutsutaan kustannusten varianssiksi. 

Jos ajanjakson toteutuneet kustannukset ylittävät ansaitun arvon, on käytetty enemmän rahaa kuin on ansaittu. Siksi projekti on ylittämässä budjetin. 

Jos ajanjakson toteutuneet kustannukset alittavat ansaitun arvon, on ansaittu enemmän rahaa kuin on käytetty. Siksi projekti on alittamassa budjetin.

## <a name="wbs-templates"></a>Työrakennemallit
Voit käyttää työrakennemallien toimintoa luodaksesi vakiomalleja projekteille. Jos yrityksesi tarjoamiin projekteihin liittyy paljon toistuvaa töitä, sinun kannattaa harkita työrakennemallin luomista. 

Voit luoda työrakennemallin aiemmin luodun projektin työrakenteen, jotta projektin suunnittelun aikana kerätyt tiedot ja parhaat käytännöt voidaan käyttää uudelleen samankaltaisissa projekteissa myöhemmin. Joskus koko työrakennetta ei kuitenkaan kannata tallentaa mallina. Siksi voit luoda malleja myös projektin työrakenteen osista.

### <a name="saving-a-projects-wbs-as-a-template"></a>Projektin työrakenteen tallentaminen mallina

Kun olet luonut mallin, voit tuoda sen uuden projektin työrakenteeseen pääsolmun alle tai minkä tahansa projektin työrakenteen tehtävän alle.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Työrakennemallin tuominen projektin työrakenteeseen

Kun tuot tehtäviä, mallin tehtävät järjestelmään sen tehtävän alkamispäivän perusteella, jonka alle ne tuodaan. Tuonnin aikana mallitehtävien edeltäjäsuhteita käytetään tuotujen tehtävien alkamispäivien laskemiseen. Kohdeprojektin vakiotyökalenteria käytetään tuotujen tehtävien päättymispäivien laskemiseen siten, että nykyisen projektin työkalenterissa määritetyt työpäivät ja vakiotyöajat säilyvät. 

Arviorivien kustannussummia ja myyntihintoja käytetään takaamaan, että projekti- tai projektisopimuskohtaisilla hinnoilla on kelvolliset päivämäärät.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Erot projektin työrakenteen ja työrakennemallin välillä

-   Työrakennemallien tehtävillä ei ole alkamis- tai päättymispäiviä.

Työrakennemallien työ- ja vapaapäiviä ei ole määritetty.

-   Työrakennemalleissa käytetään aina aikataulutuskalenteria, joka määritetään kaikkien projektien oletuskalenteriksi.

Vakioaikataulutuskalenteria käytetään vain vakiotyöpäivän tuntimäärän selvittämiseen.

-   Edeltäjäsuhteita ei kopioida työrakennemalliin.

Koska työrakennemalleissa ei ole päivämääriä, edeltäjän päättymispäivämäärään perustuvaa alkamispäivälogiikkaa ei tarvita.

-   Työkustannusten arviorivi luodaan automaattisesti, kun työrakennemallissa luodaan tehtävä. Myyntihinta ja kustannusmäärä kopioidaan valitulta työntekijältä.

Kulut ja nimikekustannukset voidaan luoda manuaalisesti samalla tavalla kuin projektin työrakenteessa.

-   Aikataulutusvirheitä näytetään, kun seuraavasta kaavasta poiketaan:

Työmäärä = Resurssien määrä × Kesto × Vakiotyöpäivän tuntien määrä 

Voit korjata kaikki aikataulutusvirheet samalla kertaa valitsemalla **Korjaa kaikki aikataulutusvirheet**. 

Voit myös korjata aikataulutusvirheet yksitellen napsauttamalla kunkin tehtävän varoituskuvaketta.





[!INCLUDE[footer-include](../includes/footer-banner.md)]