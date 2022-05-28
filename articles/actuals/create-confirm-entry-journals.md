---
title: Luo ja vahvista merkintöjen kirjauskansioita
description: Tässä aiheessa on tietoja merkintöjen kirjauskansioiden luomisesta ja vahvistamisesta Microsoft Dynamics 365 Project Operationsissa.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584224"
---
# <a name="create-and-confirm-entry-journals"></a>Luo ja vahvista merkintöjen kirjauskansioita

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Merkintöjen kirjauskansioita käytetään toteutuneiden tietojen kirjaamisessa suoraan Microsoft Dynamics 365 Project Operationsiin. Kun käytät merkintöjen kirjauskansioita, sinun ei tarvitse syöttää aika-, kulu- ja materiaalikäyttölokeja Project Operationsissa.

Yhden merkintöjen kirjauskansion avulla voit luoda useita kirjauskansiorivejä. Kun kirjauskansio vahvistetaan, merkintöjen kirjauskansion rivi kirjaa toteutuneet seuraaville tiedoille:

- Kustannus tai tuotto valitun tapahtumatyypin mukaan.
- Valittu tapahtumaluokka. Käytettävissä olevat luokat ovat **aika**, **kulu**, **materiaali**, **ennakkomaksu**, **välitavoite** ja **vero**.
- Projekti ja/tai tehtävä, joka on valittu kirjauskansiorivillä.

Luo merkintöjen kirjauskansio Project Operationsissa seuraavien vaiheiden mukaisesti.

1. Valitse **Myynti** \> **tapahtumat** \> **kirjauskansiot**.
2. Luo kirjauskansio valitsemalla **Merkintöjen kirjauskansio**-luettelosivun toimintoruudusta **Uusi**.
3. Kirjoita **Uusi kirjauskansio** -sivun **Kuvaus**-kenttään kirjauskansion kuvaus.
4. Varmista, että **Kirjauskansiotyyppi**-kentän asetuksena on **Kirjaus** ja valitse sitten **Tallenna**. Kun uusi merkintöjen kirjauskansio on tallennettu, kirjauskansiosivulla on oltava **Kirjauskansion rivit** -välilehti.
5. Luo merkintöjen kirjauskansion rivi valitsemalla **Kirjauskansiorivit**-välilehden ruudukon yläpuolella olevalta työkaluriviltä **Uusi**.
6. Määritä merkintöjen kirjauskansion **Pikaluonti**-ikkunassa kentät seuraavassa taulukossa kuvatulla tavalla.

    | Field | Description | Toiminnallinen vaikutus |
    | --- | --- | --- |
    | Tapahtumaluokka | Kirjauskansiorivi voidaan luokitella yhteen kuudesta tapahtumaluokasta: **Aika**, **Kulu**, **Materiaali**, **Ennakkomaksu**, **Välitavoite** tai **Vero**. | **Vero**-tapahtumaluokka on vanhentunut Project Operationsissa. <br> Jos luot **Vero**-tapahtumaluokan, sitä ei käsitellä laskutuksessa eikä kustannuksen tai tuoton laskennassa. **Välitavoite** on tapahtumaluokka vain tuottoa varten. <br>**Ennakkomaksu**-tapahtumaluokka tarkoittaa asiakkaalta saatua ennakkoa. Se tulisi aina luoda laskutetun myynnin ja laskuttamattoman myynnin kirjauskansiorivien pareina. |
    | Tapahtumatyyppi | **Kustannus**-, **Organisaatioiden välinen myynti**- ja **Resursointiyksikön kustannus** -tapahtumatyyppejä tulisi käyttää kustannusten kirjaamiseen.<br> **Laskuttamattoman myynnin** ja **laskutetun myynnin** tapahtumatyyppejä tulisi käyttää myyntituottojen kirjaamiseen. | **Ennakkomaksu**-tapahtumaluokka toimii vain **Laskuttamaton myynti**- ja **Laskutettu myynti** -tapahtumatyyppien kanssa.<br> **Välitavoitteen** tapahtumaluokka toimii vain **laskutetun myynnin** tapahtumatyypin kanssa. <br>**Organisaatioiden välinen myynti**- ja **Resursointiyksikön kustannus** -tapahtumatyyppejä käytetään vain **Aika**-tapahtumaluokkaan, ja ne ovat käytettävissä vain merkintöjen kirjauskansioissa Lite-käyttöönotossa, eivät silloin, kun Project Operations otetaan käyttöön resurssi- tai ei-varastoitava -skenaarioissa. |
    | Valitse tuote | Kun **Materiaali**-tapahtumaluokka on valittu, tässä kentässä voit määrittää, onko kirjauskansion riville luomasi materiaalitapahtuma olemassa oleva tuote vai käsin lisätty tuote. | Jos valitset **Käsin lisätty tuote**, voit antaa tuotteelle nimen. |
    | Tuote | Viittaus luettelon tuotteeseen. | |
    | Description | Kirjauskansiorivin kuvaus, joka on helppo tunnistaa. | Laskuttamattomille myyntikirjausriveille arvoa käytetään kuvauksena, kun laskurivin tiedot luodaan. |
    | Ulkoinen kuvaus | Kirjauskansiorivin kuvaus, jota voidaan käyttää jakamiseen ulkoisten sidosryhmien kanssa. | Laskuttamattomille myyntikirjausriveille arvoa käytetään ulkoisena kuvauksena, kun laskurivin tiedot luodaan. Se voi näkyä myös asiakkaalle lähetettävässä laskussa. |
    | Laskutustyyppi | Arvo, joka osoittaa, lasketaanko kirjausrivi projektin laskutettavaksi, maksuttomaksi vai ei-laskutettavaksi komponentiksi. | Tyypillisessä työnkulussa laskutustyyppi johdetaan palvelusopimuksessa määritettyjen sovittujen ehtojen perusteella. Kun kirjaat kirjauskansiorivin, voit kuitenkin kirjoittaa arvon tähän kenttään. |
    | Asiakirjan päivämäärä | Käytä tapahtuman tapahtumapäivää. | |
    | Aloituspäivämäärä | Käytä tapahtuman tapahtumapäivää. | Tätä kenttää käytetään vertailussa **laskuttamattoman myynnin** tyypin tapahtumien laskun luontipäivämäärän kanssa. Vertailun avulla voit päättää, onko tapahtuma tulevaisuuteen päivätty vai menneisyyteen päivätty. Vain menneisyyteen päivätyt tapahtumat lisätään laskuun. |
    | Päättymispäivämäärä | Käytä tapahtuman tapahtumapäivää. | |
    | Kirjanpitopäivämäärä | Käytä päivämäärää, jolloin kirjanpidon vaikutus rekisteröidään. | |
    | Palvelusopimusrivin asiakas | Jos sopimusrivillä on vain yksi asiakas, oletusarvoisesti tämä kenttä määritetään sopimusrivin asiakkaaksi, kun kirjauskansiorivi tallennetaan. Jos sopimusrivillä on useita asiakkaita, valitse oikea asiakas sopimusriviltä. | Jos järjestelmä ei pysty määrittämään sopimusrivin asiakasta kirjauskansiorivillä ja jos se on tyhjä kirjauskansioriviltä luodun **Laskuttamaton myynti** -tyypin toteutuneessa arvossa, toteutunutta ei laskuteta. |
    | Project | Valitse projekti, jossa toteutuneet kirjataan. | Järjestelmä yrittää määrittää palvelusopimuksen, sopimusrivin ja sopimusrivin asiakkaan valitun projektin, tapahtumaluokan ja tehtävän perusteella. |
    | Tehtävä | Valitse tehtävä, jossa toteutuneet kirjataan. | Jos olet liittänyt sopimusriveille tehtäviä palvelusopimuksen määrittämisen aikana, järjestelmä määrittää valitun tehtävän sekä projekti- ja tapahtumaluokan avulla palvelusopimuksen, sopimusrivin ja sopimusrivin asiakkaan. |
    | Tapahtumakategoria | Valitse tapahtumaluokka, jossa toteutuneet kirjataan. | Valittu tapahtumaluokka määrittää kuluille oletushinnan, joka kirjoitetaan kirjauskansioriville, kun se tallennetaan. |
    | Rooli | Tällä kentällä on merkitystä aikakirjauskansion riveillä. Valitse projektiin ja/tai tehtävään aikaa käyttäneen resurssin rooli. | Jos käytät aikakirjauskansioriveillä resurssikustannusten ja laskujen oletuskustannusten kirjaamiseen käyttövalmista määritystä, valittua roolia käytetään yhdessä resursointiyksikön kanssa määrittämään oletushinta, joka kirjoitetaan kirjauskansioriville tallennettaessa. Jos käytät oletushintojen syöttämiseen mukautettua määritystä, tarkista määrityksestä, käytetäänkö **Rooli**-kenttää oletusarvojen syöttämiseen. |
    | Alihankinta | Jos kirjauskansiorivi vastaa alihankkijan kapasiteettia tai alihankinnan kuluja tai materiaaleja, valitse asianomainen alihankintasopimus. | Kun kustannuskirjauskansiorivit kirjataan, valittu alihankintasopimus määrittää hinnaston, jota käytetään oletusyksikkökustannuksen syöttämiseen. |
    | Alihankintarivi | Jos kirjauskansiorivi vastaa alihankkijan kapasiteettia tai alihankinnan kuluja tai materiaaleja, valitse asianomainen alihankintarivi. | Kun kustannuskirjauskansiorivit kirjataan, valittu alihankintarivi varmistaa, että alihankintarivillä käytettävissä olevat kapasiteetin laskelmat lasketaan oikein. |
    | Summamenetelmä | Tämä kentän oletusasetuksena on **Määrä kerrottuna hinnalla**. Kun tätä menetelmää käytetään, summa lasketaan seuraavasti *Määrä* × *Hinta*. Toinen tuettu menetelmä on **Kiinteä hinta**. Kun tätä menetelmää käytetään, hinta määritetään summaksi eikä määrää käytetä laskutoimituksessa. | |
    | Yksikköaikataulu ja yksikkö | Yksikköaikataulu ja yksikkö yhdessä yksilöivät määrän yksikön. | Yksikön ja tapahtumaluokan yhdistelmää käytetään kulujen oletushintojen lisäämiseen. Project Operationsin oletusmäärityksessä yksikön, roolin ja resursointiyksikön yhdistelmää käytetään ajan oletushintojen syöttämiseen. Jos olet tehnyt mukautetun määrityksen oletushintojen syöttöä varten, sitä käytetään yhdessä yksikön kanssa. Yksikön ja tuotteen yhdistelmää käytetään materiaalien oletushintojen lisäämiseen. |
    | Määrä | Anna määrä. | |
    | Hinta | Jos hinta jätetään tyhjäksi, kun kirjauskansiorivi luodaan, asiaankuuluvia arvoja käytettään oletushintojen syöttämiseen tapahtumaluokan mukaan. Jos hinta syötetään, kun kirjauskansiorivi luodaan, käytetään hintaa. | |
    | Vero | Kirjoita mikä tahansa verosumma. | Syötettävän verosumman mukaan koko summa lasketaan seuraavasti: *Summa* + *Vero*. |

## <a name="confirm-an-entry-journal"></a>Merkintöjen kirjauskansion vahvistaminen

Kun olet syöttänyt kaikki merkintöjen kirjauskansion rivit, voit vahvistaa kirjauskansion. Tämä prosessi kirjaa jokaisen kirjauskansiorivin toteutuneina arvoina asianmukaisiin projekteihin.

Kun kirjauskansio on vahvistettu, sitä tai sen rivejä ei voi enää muokata.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Merkintöjen kirjauskansion vahvistuksen luomat toteutuneet arvot

On olemassa muutamia eroja merkintöjen kirjauskansion vahvistuksen luomien toteutuneiden arvojen ja niiden toteutuneiden arvojen, jotka luodaan ajan, kulun ja materiaalin käyttölokien ja laskun vahvistuksen yhteydessä Project Operationsissa:

- Merkintöjen kirjauskansiot eivät linkitä toteutuneita kustannuksia laskuttamattoman myynnin toteutuneisiin arvoihin tapahtumayhteyksien avulla. Toteutuneet arvot, jotka luodaan, kun Aika-, Kulu- ja Materiaali-käyttölokit hyväksytään, yhdistävät aina kustannuksen ja laskuttamattoman myynnin toteutuneet summat tapahtumayhteyksien avulla.
- Merkintöjen kirjauskansiot eivät linkitä toteutuneita kustannuksia laskuttamattoman myynnin toteutuneita arvoja alkuperäiseen tietueeseen tapahtuman alkuperän avulla. Toteutuneet arvot, jotka luodaan, kun Aika-, Kulu- ja Materiaali-käyttölokit hyväksytään, yhdistävät aina kustannuksen ja laskuttamattoman myynnin toteutuneet summat alkuperäiseen aikamerkintään tapahtuman alkuperän avulla.
- Kun merkintöjen kirjauskansion vahvistuksen luomat laskuttamattoman myynnin toteutuneet summat laskutetaan, laskun vahvistuksen aikana luodut laskutetut myynnin toteutuneet summat linkitetään laskuttamattoman myynnin toteutuneisiin summiin samalla tavalla kuin laskuttamattoman myynnin toteutuneet summat, jotka luodaan, kun ajan, kulun ja materiaalin käyttölokit hyväksytään.
- Organisaationvälisten resurssien syöttämälle ajalle luodut kirjauskansiorivit eivät aiheuta sitä, että **Resursointiyksikön kustannus**- ja **Organisaatioiden välinen myynti** -tyyppien toteutuneet arvot luodaan automaattisesti. Toteutuneet arvot on luotava manuaalisesti. Tämä toiminta eroaa organisaationvälisten resurssien kirjaamista aikamerkinnöistä. Tällöin kun aika hyväksytään, sovellus luo automaattisesti projektille **Kustannus**-tyypin toteutuneet arvot ja **Resursointiyksikön kustannus**- ja **Organisaatioiden välinen myynti** -tyyppien toteutuneet tiedot työntekijän omistavalle divisioonalle. Tämän jälkeen se linkittää nämä toteutuneet arvot yhteen tapahtumayhteyksien ja tapahtumien alkuperän perusteella ja linkittää ne alkuperäiseen aikamerkintään.
- Kun merkintöjen kirjauskansiot vahvistetaan, ne luovat toteutuneet arvot. Korjauskirjauskansioita ei kuitenkaan voi käyttää korjaamaan näitä toteutuneita arvoja. Tämä toiminta eroaa toteutuneista arvoista, jotka luodaan, kun aika-, kulu- ja materiaalikäyttölokit hyväksytään. Tällöin sovelluksen avulla voit korjata toteutuneet arvot korjauskirjauskansioita, mikäli niitä ei ole vielä laskutettu. Jos ne on jo laskutettu, voit edelleen korjata todellisen arvon, jos käsittelet todellisen arvon hyvityksen asiakkaalle.

> [!NOTE]
> Merkintöjen kirjauskansiot eivät pakota tarkkoja oletussääntöjä. Käytä siksi näitä merkintöjen kirjauskansioita mahdollisimman vähän, ja ole varovainen ja varmista, ettet luo järjestelmään vioittuneita taloustietoja. Luo toteutuneet summat aina kun mahdollista ajan, kulun ja materiaalin käyttölokien, projektisopimusten välitavoitteen ja ennakkomaksun sekä projektilaskun vahvistusprosessin avulla merkintöjen kirjauskansioiden sijaan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
