---
title: Uutuudet ja muutokset Project Service Automation -versiossa 3
description: Tässä aiheessa on tietoja Project Service Automation -version 3 uusista ja muuttuneista ominaisuuksista.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6ce4c549b04716d466efa262dbc6a4abf28ea9eb
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150664"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Uutuudet ja muutokset Project Service Automation -versiossa 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä aiheessa on tietoja Project Service Automation -sovelluksen käyttöliittymän, toiminnallisuuden ja terminologian muutoksista version 2 tai version 1 ja 3 välillä.

## <a name="project-scheduling"></a>Projektien aikatauluttaminen
Projektinaikataulu, joka tunnettiin aiempien versioiden WBS (Work Breakdown Structure) -rakenteena, on nimetty uudelleen Aikatauluksi, ja sitä käytetään valitsemalla **Aikataulu** -välilehti. 

![Projektiaikataulu](media/psa-schedule-01.png)

Aikataulussa on nyt uusi käyttöliittymä, joka on sekä moderni että helppokäyttöinen. Pohjana oleva Project Service Automationin ajoitusmoduuli ei kuitenkaan ole muuttunut. Aikataulutaulukon toimintopalkki mahdollistaa aikataulun käytön samalla tavalla kuin Project Service Automationin edellisessä versiossa. Muita aikatauluun tehtyjä muutoksia ovat:

- **Gantt-kaavio** - Gantt-kaavio ei ole enää käytettävissä. Uusi Gantt-visualisointi palaa tulevaan päivitykseen.
- **Sarakeotsikot** – voit piilottaa sarakkeiden otsikot ruudukossa napsauttamalla sarakkeen otsikon vieressä olevaa alanuolta. 
- **Sarakkeet** – voit näyttää piilotetut sarakkeet valitsemalla **Lisää sarake.** 
- **Tapahtumaluokka** – **Tapahtumaluokka**-haku on lisätty aikataulutaulukkoon, ja se näytetään oletuksena. 
 
## <a name="project-templates"></a>Projektimallit
Seuraavat muutokset on tehty projektimallin toimintoihin.

### <a name="create-a-project-template"></a>Luo projektimalli 
Voit luoda versiossa 3 projektimallin, joka on samanlainen kuin edellisissä Project Service Automationin versioissa. Mallissa voi olla vain aikataulu, ja aika taulussa voi olla kohdennuksia, mutta ne eivät ole pakollisia. Jos aikataulussa on kohdennuksia, ne voivat olla vain yleisiä resursseja varten. Voit luoda resurssivaatimuksia yleisille resursseille, mutta niitä ei voi varata todellisiin resursseihin mallissa. Et voi varata todellista resurssia mallin ryhmälle. 

### <a name="create-a-template-from-an-existing-template"></a>Uuden mallin luominen aiemmin luodun mallin pohjalta
Kun luot uuden projektimallin aiemmin luodusta mallista Project Service Automation -versiossa 3, tapahtuu seuraavaa: 

- Lähdeprojektin aikataulu kopioidaan malliin. 
- Yleiset resurssit kopioidaan ryhmään, ja kaikki yleiset resurssikohdennukset kopioidaan. Yleisten resurssien vaatimuksia ei kopioida. 

### <a name="create-a-template-from-an-existing-project"></a>Uuden mallin luominen aiemmin luodun projektin pohjalta
Kun luot uuden projektimallin aiemmin luodusta projektista PSA-versiossa 3, tapahtuu seuraavaa: 

- Lähdeprojektin aikataulu kopioidaan malliin. 
- Yleiset resurssit kopioidaan ryhmään, ja kaikki yleiset resurssikohdennukset säilytetään. Yleisten resurssien vaatimuksia ei kopioida.    
- Sekä kohdennetut että kohdentamattomat nimetyt resurssit poistetaan ryhmästä ja korvataan yleisillä resursseilla.
- Jos asiakastiedot ovat käytettävissä, ne poistetaan. 
- Jos järjestelmässä on viittauksia tarjouksiin ja sopimuksiin, ne poistetaan. 

### <a name="create-a-project-from-a-template"></a>Luo projekti mallista
Kun luot uuden projektimallin aiemmin luodusta mallista Project Service Automation -versiossa 3, tapahtuu seuraavaa:

- Aikataulu, ryhmä ja kohdennukset kopioidaan uuteen projektiin.   
- Aloituspäivä on joko kopiointipäivä tai käyttäjän valitsema.   
- Jos mallissa yleisiä ryhmän jäseniä, joilla on resurssitarpeita, tarpeita ei kopioida eikä luoda automaattisesti. Ne on luotava. 

## <a name="copy-a-project"></a>Kopioi projekti
Kun kopioit projektin Project Service Automation -versiossa 3, tapahtuu seuraavaa: 

- Arvioitu alkamispäivä kopioidaan, mutta sitä voi muuttaa.  
- Projektin aikataulu ja tehtävät kopioidaan. 
- Yleiset resurssit ja niiden kohdennukset kopioidaan. Yleisten resurssien resurssivaatimuksia ei kopioida. Ne on luotava. 
- Todellisia resursseja ja niiden kohdennuksia ei kopioida. Ne korvataan sen sijaan yleisillä resursseilla. 
- Toteutuneita arvoja ei kopioida uuteen projektiin. 

## <a name="move-a-scheduled-project"></a>Ajoitetun projektin siirtäminen
Kun siirrät aiemmin luodun projektin aikataulua eteenpäin, tapahtuu seuraavaa: 

- Tehtävien päivämäärät siirretään automaattisesti, jotta ne vastaisivat siirtojaksoa. 
- Kohdennetut yleiset resurssit säilyvät kohdennettuina.   
- Jos ne luodaan ennen projektin siirtämistä, yleisen resurssin vaatimukset säilyvät samoina, eikä niitä luoda automaattisesti uudelleen. Ne on luotava uudelleen, jotta ne vastaisivat tehtävien siirtämisen vuoksi uusia tehtäviä. 
- Todellisiin resursseihin tehtävät muutokset vastaavat tehtävän päivämäärän liikettä. Todellisten resurssien varaukset eivät muutu. Varauksia on muokattava täsmäytys-näkymän avulla. 
- Ryhmän resurssit, joilla on varauksia mutta ei kohdennuksia eivät muutu. 
- Nykyarvot eivät siirry. 

## <a name="estimates"></a>Arviot
Arviot on jaettu kahdelle välilehdelle, **Resurssikohdennukset** ja **Arviot**. **Resurssin kohdennus** -välilehti sisältää työmääräarviot ja näyttää resurssien kohdennukset tehtäviin aikavaiheisessa näkymässä. Voit muokata arvioita sen perusteella, mitä aikataulutusmoottori on tuottanut.

![Resurssien kohdennukset -välilehti näyttää työmääräarviot ja resurssien kohdennukset tehtäviin](media/resource-assignments-tab-02.png)

**Arviot** -välilehdellä näkyvät resurssien kohdennusten kustannus- ja myyntisummat. Summat ovat vain luku-tilassa. Kustannuslaskenta ja myyntihinnoittelu perustuvat nyt aikataulun ryhmän jäsenten varauksiin. Tämä tarkoittaa sitä, että kohdentamaton tehtävä näkyy kohdentamattoman segmentin alla. Tämä tarkoittaa myös sitä, että ilman **Roolia**, joka on oletushinnoitteludimensio, ei ole arvioitua kustannusta tai myyntiä, jos olemassa on projektiin liittyvä asiakas tai sopimus/tarjous. 

![Arviot-välilehti, jolla näkyvät kustannus- ja myyntisummat](media/estimates-tab-03.png)
  
Luokkaa tuetaan myös aikataulunäkymän tehtävissä. Arvioiden ryhmittely luokan mukaan aikavaiheistetussa arvionäkymässä antaa paremman kokemuksen, varsinkin silloin, kun projektissa on myös kuluarvioita. Kuluarviot syötetään ruudukon avulla erilliselle välilehdelle. 

Kuluarviot voidaan syöttää **Kuluarviot** -väli ehden ruudukkoon. 

![Kuluarviot-välilehti, jolla näkyy kuluarvioiden ruudukko](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Resurssienhallinta
Project Service Automation -versiossa 3, jossa on uusi Unified Client -käyttöliittymä ja muutoksia varausten ja kohdennusten välisessä suhteessa, projektin miehittäminen yleisillä tai todellisilla resursseilla on muuttunut dramaattisesti versiosta 2 ja versiosta 1. Varattavissa olevien resurssien käsitteet **todellinen** ja **yleinen** pysyvät kuitenkin samoina, samoin kuin ryhmän jäsenet, vaatimukset, kohdennukset ja varaukset.   

![Resurssivalitsimen käyttäminen](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Todellisen varattavissa olevan resurssin kohdentaminen 
Project Service Automation -versiossa 3 varaukset ja tehtävämääritykset eivät ole yhtä tiiviisti sidoksissa toisiinsa kuin Project Service Automationin aiemmissa versioissa. Ryhmänruudukon avulla voit varata **todellisen** ryhmän jäsenen, joka on samanlainen kuin in-market.

Kun käytät resurssin valitsinta aikataulussa, voit valita ryhmä-näkymästä luodun ryhmän jäsenen ja kohdentaa hänet sitten tehtäviin. Voit jatkaa tehtävien kohdentamista heille, myös heidän varaustensa ohi. **Täsmäytys**-välilehden avulla voit täsmäyttää ryhmän jäseniä, joilla on eroja varausten ja kohdennusten välillä.

Resurssivalitsin näyttää projektin ryhmän jäsenet. Resurssi valitsimen avulla voit myös etsiä ja tarkastella muita varattavia resursseja, jotka eivät kuulu projektiryhmään. Voit kohdentaa ne tehtävään, ja niistä tulee osa projektiryhmää. Sinun täytyy varata ne käyttämällä **Aikataulutaulukkoa** tai **Täsmäytys**-välilehteä.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Voit kohdentaa yleisen varattavissa olevan resurssin tehtävään ja projektiryhmään ja täydentää sitten varauksen todellisella resurssilla aikataulutaulukon kautta. 
Project Service Automation -versiossa 3 Luo ryhmä -toimintoa ei käytetä yleisiin resursseihin. Sen sijaan voit luoda ja kohdentaa yleisen resurssin suoraan aikataulusta kirjoittamalla yleisen resurssin nimen aikataulun resurssisoluun. Voit myös valita resurssikuvakkeen solusta ja kirjoittaa sitten resurssin valitsimella sen yleisen resurssin nimen, jonka haluat luoda. Tämä avaa pikaluontipaneelin, jonka avulla voit määrittää yleisen resurssiryhmän jäsenen roolin ja organisaatioyksikön. Kun olet luonut resurssin, se on kohdennettu tehtävälle ja voit edelleen määrittää kyseisen yleisen resurssin muihin aikataulun tehtäviin.    
 
Kun olet kohdentanut resurssin kaikille asianmukaisille tehtäville, voit luoda resurssivaatimuksen ja täyttää sen sitten suoraan varaamalla **Aikataulutaulukosta** tai lähettämällä resurssipyynnön. Voit myös lisätä yleisiä resursseja suoraan ryhmän jäsenen ruudukkoon. 

Yleiset resurssit lisätään projektiryhmään ilman resurssivaatimuksia ja projektin alkamis- ja päättymispäivämääriä, kunnes resurssivaatimus luodaan. Jos haluat luoda vaatimuksen, valitse yleinen resurssi ja valitse sitten **Luo**. Vaatimuslinkki tulee nyt näkyviin, ja tarvittavat tunnit täytetään kohdennettujen tuntien mukaan. Voit avata ja päivittää vaatimuksen napsauttamalla linkkiä.
  
Kun varaus on valmis ja nimetty resurssi täyttää sen kokonaan, yleinen resurssi korvataan nimetyllä resurssilla ja aikataulussa oleva kohdennus päivitetään nimetyllä resurssilla. 

Tarpeita varten ehdotetut resurssit on nyt tallennettu välilehdelle erillisen osan sijaan.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Useita nimettyjä resursseja, jotka täyttävät yleisen resurssin
Kun tarve täyttyy useilla resursseilla, yleinen resurssi säilyy ryhmässä ja kohdennetaan tehtävään. Nimettyjä ryhmän jäseniä, jotka on varattu, ei määritetä osana työtä. Projektipäällikkö voi kohdentaa työn todellisille resursseille tarpeen mukaan.  **Täsmäytys**-näkymä sisältää erittelyn varauksista useille resursseille ja kohdennuksille. Tämä ei tapahdu automaattisesti, koska monimutkaisissa skenaarioissa, kuten siinä tapauksessa, jossa on joukko tehtäviä, jotka muodostavat tarpeen, on otettava huomioon, miten projektipäällikkö haluaa delegoida. Koska järjestelmä ei ymmärrä tarkoitusta, oletukset ovat todennäköisesti erilaisia kuin tarkoitus, ja tuloksena syntyy virheellinen tai arvaamaton tulos. Ennustettava tulos on se, että yleinen resurssi säilyy määritettynä, kunnes projektipäällikkö määrittää resurssit tietoisesti **Täsmäytys**-näkymän avulla.

### <a name="reconciliation"></a>Täsmäytys
**Täsmäytys**-välilehti näyttää varaukset ja kaikki kohdennukset jokaiselle projektiryhmän jäsenelle. Näkymä näyttää tunnit soluissa, jotka voivat edustaa aikajapisteitä kuukausista päiviin asti. Tämän näkymän avulla projektipäälliköt voivat täsmäyttää ryhmänsä jäsenten varaukset ja kohdennukset. Tästä on hyötyä, koska varaukset ja tehtävien kohdennukset eivät ole tiukasti kytkettyjä, joten projektia suunniteltaessa on mahdollista saada enemmän joustavuutta. 

![Täsmäytys-välilehti näyttää varaukset ja kaikki kohdennukset projektiryhmän jäsenille.](media/resource-reconciliation-tab-06.png)

Näkymä ottaa erot ryhmän jäsenen varausten ja heidän kohdennustensa yhteenvedon välillä kullekin resurssille, ja näyttää seuraavat kaksi eroa, jotka voivat esiintyä varausten ja kohdennusten välillä projektissa: 

- **Varauspula** - varauspulaa tapahtuu, kun resurssilla on enemmän kohdennuksia kuin varauksia. Koska tätä kapasiteettia ei ole varattu, projektipäällikkö voi korjata tilanteen laajentamalla resurssin varauksia kattamaan puutteen. 
- **Ylimääräiset varaukset** - ylimääräisiä varauksia tapahtuu, kun resurssi on kirjattu projektiin, mutta sitä ei ole kohdennettu tehtäviin.  Tämä tilanne voi olla hyväksyttävä, jos resurssi on esimerkiksi varattu ennen tehtävän kohdennusta. Muissa tapauksissa resurssia ei ehkä kuitenkaan ole suunniteltu kohdennettavaksi, ja projektipäällikön tulisi harkita resurssin varausten peruuttamista, jotta kapasiteettia voidaan käyttää toisessa projektissa. 

Tilanteissa, joissa resurssille on kohdennuksia mutta ei varauksia (varauspula), voit valita kootun varauksen puutteen ja valita sitten **Laajenna varausta**. Tässä voit tarkastella varausta, jota tarvitaan resurssin vähyyden ja käytettävyyden korjaamiseksi. 
 
## <a name="time-and-expense"></a>Aika ja kulut
Tässä osassa on tietoja Project Service Automationin version 3 ajan, kulun ja hyväksynnän muutoksista. Osana Dynamics 365 Project Service Automation -ratkaisua **Ajan syöttö** - toiminto on päivitetty Unified Interface -kehyksen käyttöönottoa varten. Tämä mahdollistaa yhdenmukaisen ja yhtenäisen käyttöliittymän tarjoamisen, joka noudattaa joustavia suunnitteluperiaatteita, jotka takaavat optimaalisen katselun missä tahansa näytön koossa tai laitteessa. 

### <a name="landing-page"></a>Saapumissivu
Ei-laajennettava mukautettu ajansyöttökokemus on vanhentunut versiossa 3. Sen tilalla on nyt laajennettava ja käytettävissä oleva luonnollinen ruudukkokokemus. Voit käyttää ajan syötön toimintoja vasemmalla olevan sivustokartan avulla. Tämän muutoksen ansiosta et voi enää syöttää aikaa yhdelle viikolle kerrallaan. Sen sijaan jokaiselle ruudukon päivälle on luotava aikamerkintä. Muutaman merkinnän luomisen jälkeen käyttäjät voivat luoda useita aikamerkintöjä kerralla **Kopiointi**-toiminnon avulla, josta kerrotaan myöhemmin lisää tässä aiheessa. 

![Ajan syötön saapumissivu](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Uusien aikamerkintöjen luominen 
Napauta **Uusi** tehtäväpalkissa avataksesi aikamerkinnälle pikaluontisivun, jolla syötetään kesto minuuteissa, tunneissa tai päivissä. Voit tehdä tämän kirjoittamalla vain h, m tai d sekä määrän.  

![Aikamerkinnän pikaluonti](media/quick-create-time-entry-08.png)

Järjestelmänäkymät tukevat valintakenttiä. Kun olet esimerkiksi kirjoittanut projektin tiedot, **Projekti tehtävä** -kenttä määritetään oletusarvoisesti **Omat avoimet projektitehtävät** -näkymään. Jos haluat luoda aikamerkintöjä tehtäville, joita ei ole kohdennettu käyttäjälle, valitse **Vaihda näkymää** valintaruudussa, ja valitse sen jälkeen **Kaikki aktiiviset projektitehtävät** -näkymä. Kun aikamerkintä on luotu ja näkyvissä ruudukossa, voit muokata rivin arvoja suoraan ruudukossa.  

### <a name="bulk-createcopy"></a>Joukkoluonti/kopiointi 
Sen jälkeen, kun muutama aikamerkintä on luotu, voit käyttää kopiointitoimintoa luodaksesi kerralla useita aikamerkintöjä. Napauta **Kopioi** avataksesi **Kopioi**-dialogin. Aseta päivämääräväli, jolta ajan jaksoja on kopioitava kohdassa **Lähdejakso: Alkamispäivä**. Määritä päivämäärä, jolle aikamerkinnät on luotava kohdassa **Kohdejakso: alkamispäivä**. Valitse **Kopioi**, jos haluat kopioida aikamerkinnät vastaavalle viikonpäivälle **Kohdejaksossa**. Esimerkiksi edellisen viikon maanantain aikakirjaus kopioidaan sen viikon maanantaille, joka on määritetty **Kohdejaksossa**. 

![Kopioi useita aikamerkintöjä](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Tuo tiedot 
Kohdennukset ja vaihto noudattavat samaa käyttöliittymämääritelmää, joka antaa käyttäjän määritellä päivämäärävälin, jolta varaukset on tuotava. Sen jälkeen on valittava varaukset, jotka tulisi kopioida **Luonnos** -aikamerkinnöiksi. Versiossa 3 ei enää näy **Ehdotettuja** aikamerkintöjä ruudukossa ja kalenterissa.  

### <a name="change-in-calendar-control"></a>Kalenterin ohjausobjektin muutos
Versiossa 3 olemme siirtyneet pois mukautetun kalenterin ohjausobjektista ja käytämme nyt UC-kalenteria viikon merkintöjen näyttämiseen. Tämän kalenterin avulla voit tarkastella päivää, viikkoa ja kuukautta. 

> [!NOTE]
> Kalenterin rajoitus on se, että tämä ohjausobjekti ei tue yksittäisten kalenterikohteiden toimintoja. Et voi esimerkiksi valita yhtä tai useampaa kalenterikohdetta ja lähettää tai poistaa niitä. Kun napsautat kalenterikohdetta, näkyviin tulee **Aikamerkintä**-entiteetin sivu, jolla voi tehdä lisätoimenpiteitä. 

### <a name="extensibility"></a>Laajennettavuus
**Talleta tietoja mukautetuissa kentissä ainoastaan aika- ja kulumerkintäentiteeteissä** - Aikamerkintä käyttää muokattavaa ruudukkoa, vain luku -ruudukkoa ja kalenteriohjausobjekteja alustalta. Kaikki nämä ohjausobjektit ovat alkuperäisiä, joten ne tukevat mukautuksia. Project Service Automation -versiossa 3 voit lisätä mukautettuja kenttiä, määrittää valintakenttiä ja varmuuskopioida niitä mukautettuihin näkymiin. Voit myös määrittää mukautetun liiketoimintalogiikan mukautettujen kenttien valittujen arvojen perusteella.  

**Kerää tietoja mukautetuista aijan ja kulujen syöttökentistä ja lisää ne lähetys- ja hyväksyntävuota tukeviin entiteetteihin** - aikamerkintöjen tyypillinen käsittely näkyy seuraavassa kaaviossa.

![Ajan syötön työnkulku](media/process-time-entries-10.png)

Jos liiketoimintavaatimukset määrittävät, että aika- ja kuluentiteettejä varten on tallennettava mukautettuja hinnoitteludimensioita ja kopioitava aika- ja kuluresurssin asettamat arvot mukautettuun hinnoitteludimensioon kaikkien edellisessä kuvassa olevien entiteettien kautta, katso aihetta [Määritä mukautettuja kenttiä hinnoitteludimensioiksi](set-up-pricing-dimensions.md)

Jos haluat tukealiiketoiminta vaatimuksia silloin, kun aika- ja kuluentiteettien on tallennettava mukautettuja ei-hinnoitteludimensioita ja kopioitava arvot, voit käyttää hinnoitteludimensioiden asetuksia ja ilmaista mukautetut dimensiot hinnoitteludimensioina ilman kustannuksia tai laskutushintaa. Toinen skenaario on mukautetun kentän lisääminen jokaisen entiteettiin käyttämällä samaa kentän nimeä kaikissa kohteissa. Mukautettuja laajennuksia voidaan luoda liittämään tietueita entiteetteihin, jotka osallistuvat lähetys/hyväksyntävuohon käyttämällä tapahtuman alku- ja tapahtuman yhteys -entiteettejä.  

### <a name="delegate-time-and-expense-entry"></a>Delegoi aika- ja kulukirjaus
Common Data Service -ympäristö ei tue yhden käyttäjän esiintymistä toisena, mikä tarkoittaa, että Project Service Automation -versiossa 3 ei tueta delegoituja aika- ja kulumerkintöjä. Kumppanit ja Asiakkaat ovat kuitenkin voineet ottaa käyttöön vaihtoehtoisen tavan, joka mahdollistaa delegoitujen ajansyöttökokemusten tukemisen versiossa 3. Tämä on vain korvaava tapa eikä täydellinen ratkaisu, joten on tärkeää ymmärtää sen rajoitukset ja käyttää tätä lähestymistapaa vain, jos rajoitukset ovat hyväksyttäviä. 

> [!IMPORTANT]
> Nämä tiedot ovat vain ehdotettuja ohjeita, joiden avulla kumppani tai asiakas voi ottaa mukautetun toteutuksen käyttöön. Tuoteryhmä ei tarjoa virallista tukea tälle toiminnallemme minkään tukikanavasi kautta.

### <a name="customization-details"></a>Mukautustiedot 
Mukauttamisen avulla voit lisätä **Varattavissa olevan** resurssin luomis- ja muokkauskokemuksiin, joiden avulla käyttäjä voi toimia edustajana muuttamalla **Varausresurssi** -kentän toiseksi käyttäjäksi, jolle aika-ja kulu kirjaukset on tallennettava. Seuraavat vaiheet kattavat ajan syöttämisen delegoinnin. Samoja tietoja käytetään kulujen syöttämisen delegoinnin yhteydessä. 
 
1.  Varmista, että delegoitu käyttäjä on saanut yleisen käyttöoikeuden projekteihin ja projektitehtäviin. 
1.  Koska **Varattavissa oleva** resurssi, joka on **Aikamerkintä**-entiteetin kenttä, ei näy **Pikaluonti**-sivulla, se on lisättävä.

    -tai-

    Luomalla mukautetun näkymän, joka sisältää **Varattavissa oleva resurssi** -sarakkeen, voit tarkastella vain resurssille luotuja aikamerkintöjä. Julkaise mukautukset sovellusmoduulin suunnittelijassa, jotta näkymä näkyy **Näkymän valitsin** -kohdassa **Aikamerkinnät** -sivulla. Kaksi laajennosta käsittelee esimiehen asettamista ei-projekteihin liittyville aikamerkinnöille:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Luo uusi laajennus, jos haluat korvata **Esimies**-kentän **Varattavissa oleva resurssi** -kentässä määritetyn käyttäjän esimiehellä. Käytä samaa **Toteutusvaihetta** kuin ulkoinen (OOB) laajennos (asivarmistus), ja käytä **Suoritusjärjestystä**, joka on korkeampi kuin OOB-laajennokset (suurempi kuin 1). Näin varmistetaan, että mukautettu laajennus suoritetaan OOB-laajennusten jälkeen.  
 
### <a name="end-user-experience"></a>Käyttäjäkokemus
1.  Kun luot aikamerkinnän pikaluontisivulla, syötä projektin ja projektitehtävän tiedot ja valitse sitten käyttäjä **Varattavissa oleva resurssi** -kentälle, jolle aikamerkintöjä on tarpeen kirjata. 
2.  Tämän kentän oletusarvo on sisäänkirjautunut käyttäjä, mutta ottaen huomioon, että käyttäjä kirjoitti yli tämän kentän, aikamerkintä luodaan nyt valittuna **Varattavissa olevana resurssina**.
3.  Kun lähetät näille tietueille luomasi aikakirjaukset, tapahtumat asetetaan jonoon projektin hyväksyjälle kuten odotettua. 
4.  Kun peruutat aikamerkintöjä, jotka on tehty toiselle käyttäjälle, aikamerkinnät palautetaan tilaan **Luonnos** ja **Varattavissa oleva resurssi** -kenttä on asetettu toiseen käyttäjään. 
5.  Vaihtoehtoisesti voit siirtyä mukautettuun näkymään ja suodattaa toisen käyttäjän luomat aikakirjaukset. 
 
### <a name="limitations"></a>Rajoitukset
**Kopiointi**- ja **Tuonti**-toiminnot toimivat ainoastaan sen käyttäjän kontekstissa, joka on kirjautunut sisään. Tämä tarkoittaa, että ei ole mahdollista kopioida tai tuoda aikamerkintöjä, jotka luotiin käyttäjälle, joka kirjautui sisään varattavissa olevana resurssina.

Aikakirjaukset, jotka eivät ole projektille, reititetään hyväksymistä varten varattavissa olevan resurssin esimiehelle ainoastaan, jos vaihe 4 on suoritettu yllä olevassa osiossa **Mukautustiedot**. Muussa tapauksessa toisen käyttäjän muut kuin projektiajan määritykset reititetään virheellisesti kirjautuneen käyttäjän esimiehelle. 

### <a name="other-changes"></a>Muita muutoksia 
**Varaukset ja tehtävät** -toiminto on poistettu. 

## <a name="multidimensional-pricing"></a>Moniulotteiset hinnat
Project Service Automationin version 3 avulla voidaan maksimoida joustavuus ja vastata liiketoimintatarpeisiin, sillä se tukee hinnoitteludimensiojoukkojen erillistä soveltamista kustannus- ja laskutushintoihin. Dimension arvot voidaan määrittää oletusarvoiksi, ja sitten ne välitetään kustannuslaskennan ja hinnoittelun kautta resurssien profiloinnista ajan syöttämisen kautta projektin todellisiin arvoihin. Asiakaskohtainen määritys ja muokkaaminen tai laajentaminen hyödyntää vakiotyyppistä mukautettavuuden infrastruktuuria.

Project Service Automation toimittaa oletusjoukon hinnoitteludimensioita ja -rooleja sekä resurssiyksiköitä, ja se sallii kunkin roolin ja organisaatioyksikön yhdistelmän hintojen ja kustannusten määrittämiselle.

Jos Project Service Automation -asiakkaat haluavat edelleen käyttää näitä valmiita kenttiä hinnoitteludimensioina versiossa 3, muutoksia ei tehdä. Voit jatkaa Project Service Automationin käyttöä tavalliseen tapaan. Jos resursseille on kuitenkin määritettävä hinta tai kustannus käyttämällä muita lisämääritteitä, versio 3 mahdollistaa omien mukautettujen hinnoitteludimensioiden lisäämisen Project Service Automationiin. Mukautettujen hinnoitteludimensioiden laajentaminen on monimutkainen määrityskokemus. 

## <a name="quotes-and-contracts"></a>Tarjoukset ja sopimukset
Project Service Automation -versiossa 3 on muutettu tarjousten ja sopimusten määrittämisen ja hallinnan alueita. Seuraavissa osissa on tarkempia tietoja.

### <a name="set-up-chargeability-options"></a>Veloitusasetusten määrittäminen
Versioissa 1 ja 2 roolien ja luokkien veloitusasetukset erityisille tarjouksille ja sopimuksille tehtiin käyttäen **Valoitettavuus**-näkymää, joka oli ylänavigoinnissa tarjousrivillä ja sopimusrivillä. Näin voitiin määrittää myös näiden roolien ja kululuokkien hinnat.

Versiosta 3 alkaen veloitusasetusten asettaminen roolien ja kululuokkien mukaan tehdään tarjouksen tai sopimusrivin tasolla. Hinnoitteluasetukset ovat erillään veloitusasetuksista. Voit tarkastella **Laskutettavia rooleja** ja **Laskutettavia luokkia** **Tarjousrivin** ja **Sopimusrivin** välilehtinä ilman, että sinun tarvitsee käyttää yläsiirtymistoimintoa.

![Veloitettavat roolit](media/chargeable-12.png)
 
Veloitettavien roolien ja Veloitettavien luokkien asetuksissa hyödynnetään myös valmiina olevaa, muokattavaa ruudukko-ohjausobjektia. Jokaista roolia ja luokkaa varten tuettavat asetukset laskutustyypille Tarjous- ja Sopimus-vaiheen aikana säilyvät muuttumattomina edellisistä versioista, ja ovat **Veloitettava** ja **Ei-veloitettava**. **Veloitukseton** ei ole tuettu tyyppi Tarjous- tai Sopimus-vaiheen aikana **Veloituksetonta** tuetaan vain Ajan tai Kulujen hyväksynnässä.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Luo ja muokkaa mukautettua hinnoittelua Project Service Automation -tarjousta ja -projektisopimusta varten
Versioissa 1 ja 2 mukautettujen hinnastojen käyttäminen tietyille tarjouksille ja sopimuksille tehtiin käyttäen toimintoa **Muokkaa hintoja** **Veloitettavuus**-näkymässä. **Veloitettavuus**-näkymä sijaitsi tarjousrivin tai sopimusrivin yläsiirtymisessä. Näin voitiin määrittää myös näiden roolien ja kululuokkien veloitusasetukset.

Versiosta 3 alkaen mukautetun projektihinnaston luominen ja käyttäminen Project Service Automation -tarjouksessa ja Project Service Automation -projektisopimuksessa on erotettu veloitusasetuksista. Project Service Automation -tarjouksilla ja Project Service Automation -projektisopimuksilla on uusi välilehti nimeltä **Projektihinnastot**. Tämä välilehti näyttää liitetyn näkymän kaikista projektihinnastoista, jotka on liitetty Project Service Automation -tarjoukseen tai -projektisopimukseen. Jos haluat luoda mukautetun hinnaston aiemmin luodusta hinnastosta, joka on jo liitetty projektitarjoukseen tai sopimukseen, valitse **Luo mukautettu hinnoittelu**. Tämä kopioi kaikki liittyvät hinnastot ja liittää ne tarjoukseen tai sopimukseen. Nyt voit avata hinnaston sekä muokata roolin tai kululuokan hintaa, jotta kyseiset hinnoittelumuutokset koskevat vain tätä tarjousta tai sopimusta. 
  
Seuraavassa kuvassa on tilanne ennen kuin mukautetut hinnastot on luotu.

![Ennen muokattuja hinnastoja](media/before-custom-price-lists-13.png)

Seuraavassa kuvassa on tilanne sen jälkeen kun mukautetut hinnastot on luotu.

![Muokattujen hinnastojen jälkeen](media/after-custom-price-lists-14.png)

> [!NOTE]
> Lyhyt viive on mahdollinen **Luo mukautettu hinnoittelu** -painikkeen napauttamisen ja hinnaston luomisen välillä. Suosittelemme, että päivität ruudukon sen sijaan, että napauttaisit useita kertoja. Mukautettu hinnasto on luotu, jos siihen liitetyssä hinnaston nimessä on tarjouksen nimi tai siihen on liitetty projektisopimuksen nimi.
