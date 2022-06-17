---
title: Täysin laskutettujen laskutettujen välitavoitteiden siirtäminen julkaisun yhteydessä
description: Tässä artikkelissa käsitellään sitä, miten asiakkaalta avoimista projektisopimuksista laskutetut kiinteähintaisten laskutuksen välitavoitteet siirretään ennen julkaisupäivää.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d7bb3dbb5acd9be447c405ec17f18d00c500f655
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912236"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Täysin laskutettujen laskutettujen välitavoitteiden siirtäminen julkaisun yhteydessä

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

## <a name="scenario"></a>Skenaario

Contoso julkaisee Microsoft Dynamics 365 Project Operationsin resurssi/ei-varastoitu-skenaarioille. Käyttöönottoaktiviteetteihin kuuluu, että käyttöönottoryhmä siirtää avoimet projektisopimukset vanhasta järjestelmästä. Jotkin projektisopimuksista sisältävät sopimusrivejä, jotka käyttävät kiinteähintaista laskutustapaa ja jotka on jo laskutettu osittain loppuasiakkaalta. Käyttöönottoryhmän on siirrettävä nämä laskutuksen välitavoitteet **Asiakaslasku kirjattu** -muodossa, koska ne on sisällytettävä palvelusopimuksen kokonaisarvoon tuottojen kirjaamista varten. Myyntireskontran ja pääkirjan asiakassaldot eivät kuitenkaan saa muuttua tämän vaikutuksesta.

## <a name="solution"></a>Ratkaisu

### <a name="prerequisites"></a>edellytykset

- Dynamics 365 Finance 10.0.24 tai uudempi versio on asennettava.
- Ympäristön, jossa siirtovaiheet on suoritettava, on oltava ylläpitotilassa. Muita aktiviteetteja ei tulisi suorittaa välitavoitteiden siirtämisen aikana.
- Siirtovaiheita on noudatettava tarkasti tässä kuvatulla tavalla, ja niitä voi käyttää vain käyttöönottoaktiviteettiin. Microsoft ei tue mitään muuta tämän ominaisuuden käyttöä.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Project Operationsin integrointisopimusrivin välitavoitteiden kaksoiskirjoituksen yhdistämismäärityksen käyttöönottoversion luominen 

1. Varmista, että **Project Operations -integraation sopimusrivien välitavoitteet** -entiteetin kohdemääritys on ajan tasalla. 

    1. Siirry Financessa kohtaan **Tietojen hallinta** \> **Tietoentiteetit** ja valitse **Project Operations -integraation sopimusrivien välitavoitteet** -entiteetti. 
    2. Valitse **Muokkaa kohdemäärityksiä**. 
    3. Valitse **Yhdistä välivarastointi kohteeseen** -sivulla , valitse **Luo yhdistämismääritys** ja vahvista sitten, että haluat luoda yhdistämismäärityksen.

2. Pysäytä ja päivitä kaksoiskirjoituksen yhdistämismääritys **Project Operations -integraation sopimusrivien välitavoitteet** (**msdyn\_contractlinescheduleofvalues**). 

    1. Valitse **Tietojen hallinta** \> **Kaksoiskirjoitus**, valitse yhdistämismääritys ja avaa sen tiedot. 
    2. Valitse **Lopeta** ja odota, kunnes järjestelmä pysäyttää määrityksen. 
    3. Valitse **Päivitä taulukot**.

3. Lisää yhdistämismääritys tapahtuman tilaa varten.

    1. Valitse **Lisää määritys**.
    2. Valitse uudella rivillä **Talous- ja toimintosovellukset** -sarakkeessa **TRANSSTATUS \[TRANSSTATUS\]** -kenttä.
    3. Valitse **Microsoft Dataverse** -sarakkeessa **msdyn\_invoicestatus \[Invoice status\]**.
    4. Valitse **Vastaavuuden määrityksen tyyppi** -sarakkeesta oikea nuoli (**\>**).
    5. Valitse avautuvassa valintaikkunassa **Synkronoinnin suunta** - kentässä **Dataversesta talous- ja toimintosovelluksiin**.
    6. Valitse **Lisää muunnos**.
    7. Valitse **Muunnostyyppi**-kentässä **ValueMap**.
    8. Valitse **Lisää arvon yhdistämismääritys**.
    9. Syötä vasempaan kenttään **4**. Syötä oikeaan kenttään **192350001**. 
    10. Valitse **Tallenna** ja sulje valintaikkuna.

4. Tallenna kaksoiskirjoitusmäärityksen versio valitsemalla **Tallenna nimellä**. 
5. Valitse **Lisää taulukko** -ruudun **Julkaisija**-kentässä **Oletusjulkaisija**.
6. Anna **Versio**-kentässä versio.
7. Kirjoita **Kuvaus**-kenttään huomautus tästä määrityksen käyttöönottoversiosta. 
8. Valitse **Tallenna**.
9. Käynnistä yhdistämismääritys.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Laskutettujen välitavoitteiden siirtäminen Dataverse-ympäristöön

1. Luo Project Operationsin Dataverse-ympäristössä välitavoitteita, joiden laskun tila on **Valmis laskutettavaksi**. Älä siirrä tässä vaiheessa välitavoitteita, joita ei ole laskutettu.

    > [!NOTE]
    > Varmista ennen laskutuksen välitavoitteiden siirtoa, että projektisopimusriviin liittyvät taloushallinnon dimensiot on määritetty odotetusti. Taloushallinnon dimensioita ei voi muokata siirron päätyttyä.

2. Kun kaikki välitavoitteet on siirretty, lopeta seuraavat kaksoiskirjoitusmääritykset:

    - Project Operations -integraation sopimusrivien välitavoitteet (msdyn\_contractlinescheduleofvalues)
    - Project Operations -integroinnin todelliset arvot (msdyn\_actuals)
    - Projektin laskuehdotus V2 (laskut)

    Voit pysäyttää määritykset seuraavassa kuvatulla tavalla:

    1. Valitse Financessa **Tietojen hallinta** \> **Kaksoiskirjoitus**, valitse yhdistämismääritys ja avaa sen tiedot.
    2. Valitse **Lopeta** ja odota, kunnes järjestelmä pysäyttää määrityksen.

3. Luo Project Operationsin Dataverse-ympäristössä laskutuksen välitavoitteiden proformalaskut ja vahvista ne. 

    1. Siirry sivustokartassa projektisopimuksiin, valitse sopimukset ja valitse sitten **Luo laskut**.
    2. Kun laskut on luotu, avaa ne sivustokartan **Laskut**-valikosta ja valitse sitten **Vahvista**.

    Tässä vaiheessa tarvittavat tietueet luodaan Dataverse-ympäristöön. Se ei kuitenkaan vaikuta taloushallinnon ja myyntireskontran määritykseen, koska aiemmin mainitut kaksoiskirjoitusmääritykset on pysäytetty.

4. Kun kaikki proformalaskut on vahvistettu, palauta kaikki kaksoiskirjoitusmääritykset alkuperäiseen tilaansa.

    1. Päivitä kaksoiskirjoituksen yhdistämismäärityksen **Project Operations -integraation sopimusrivien välitavoitteet** (**msdyn\_contractlinescheduleofvalues**) versio takaisin alkuperäiseksi. 
    2. Valitse kaksoiskirjoitusmääritys määritysluettelosta, valitse **Taulukkomäärityksen versio** ja valitse sitten taulukon määrityksen alkuperäinen versio.
    3. Valitse **Tallenna**.
    4. Käynnistä seuraavat kaksoiskirjoitusmääritykset uudelleen:

        - Project Operations -integraation sopimusrivien välitavoitteet (msdyn\_contractlinescheduleofvalues)
        - Project Operations -integroinnin todelliset arvot (msdyn\_actuals)
        - Projektin laskuehdotus V2 (laskut)

Välitavoitteet on nyt siirretty, ja järjestelmä on valmis ottamaan käyttöön seuraavat käyttöönottoaktiviteetin vaiheet.
