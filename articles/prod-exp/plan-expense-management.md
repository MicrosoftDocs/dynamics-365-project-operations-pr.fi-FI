---
title: Määritä käyttöoikeuksien hallinta
description: Tässä artikkelissa kerrotaan, millaiset asiat pitää ottaa huomioon ja millaisia päätöksiä pitää tehdä suunnitteluprosessin aikana, ennen kuin Microsoft Dynamics 365 Financen matkalaskut määritetään.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c9424b8aaf867254bde085cffaa649c846920cc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933994"
---
# <a name="configure-expense-management"></a>Määritä käyttöoikeuksien hallinta

Tässä artikkelissa käsitellään suunnitteluun liittyviä seikkoja ja päätöksiä, jotka on tehtävä suunnitteluprosessin aikana ennen kulunhallinnan määrittämistä. Kulunhallinnassa voit tallentaa tietoja esimerkiksi maksutavoista, matkustusehdotuksista, kuluraporteista ja käytännöistä.

Koska monet niistä päätöksistä, joita teet, kun suunnittelet kulunhallinnan määrityksiä, perustuvat organisaation hierarkiaan ja talousrakenteeseen, sinun on viitattava kyseisten alueiden suunnitteluasiakirjoihin.

## <a name="intercompany-expenses"></a>Konsernin sisäiset kulut

Kun otat konserniyritysten väliset kulut käyttöön, voit sallia, että yritykset ja työntekijät aiheuttavat kuluja toisen yrityksen puolesta, ja kerätä maksuja organisaation juridisesta työyksiköstä. Esimerkiksi yrityksen työntekijä A täydentää projektia yritykselle B, ja projektiin liittyy matkustamiseen liittyviä kuluja. Jos konsernin sisäiset kulut on otettu käyttöön, työntekijä voi sitten arkistoida kuluraportin, joka kirjaa kulun yritykselle B, ja tämän jälkeen yrityksen A on maksettava kulu. Jos organisaatiolla ei ole useita yrityksiä, konsernin sisäisiä kuluja ei tarvitse ottaa käyttöön.

**Päätös:** Haluatko ottaa käyttöön konsernin sisäiset kulut?

## <a name="financial-management"></a>Taloushallinto

Kulujen hallinta on integroitu tiiviisti organisaation taloushallintoon. Monet kulun hallinnan määritykset perustuvat päätöksiin, jotka olet tehnyt organisaation taloudesta. Seuraavissa osissa kuvataan eri alueita, jotka edellyttävät suunnittelua ja päätöksiä, organisaation talouspäätösten ja johtoryhmän ohjeiden mukaan.

### <a name="per-diems"></a>Päivärahat

Sinun täytyy määrittää työntekijän päivärahat, joita organisaatiosi tarjoaa. Koska päivärahoja käytetään yleensä kattamaan esimerkiksi ateriat, majoitus ja muut satunnaiset kulut, voit luoda säännöt organisaation tarjouksista. päivärahahinnat voivat perustua vuodenaikaan, matkustuspaikkaan tai molempiin. Kun määrität päivärahasäännön, voit määrittää, että prosenttiosuus päivärahahinnasta pidätetään, jos työntekijä saa ilmaisia aterioita tai palveluita. Voit myös määrittää päivärahamäärät asettamaan vähimmäis- ja enimmäistuntimäärät, joita päivärahaa voidaan soveltaa työntekijän matkoihin.

**Päätökset:**

- Päivärahasääntöjen oletusarvot ensimmäisinä ja viimeisinä päivinä:

    - Mikä on pienin tuntimäärä, jonka työntekijä voi vaatia päiväksi ja silti saada päivärahan?
    - Onko olemassa alennusmäärä, joka on tarjottu ateriaa varten ensimmäisenä ja viimeisenä päivänä? Jos vähennys on olemassa, mikä on vähennysprosentti?
    - Onko olemassa alennusmäärä, joka on tarjottu hotellia varten ensimmäisenä ja viimeisenä päivänä? Jos vähennys on olemassa, mikä on vähennysprosentti?
    - Onko olemassa alennusmäärä, joka on tarjottu muita kuluja varten, jotka tapahtuvat ensimmäisenä ja viimeisenä päivänä? Jos vähennys on olemassa, mikä on vähennysprosentti?

- Oletuspäivärahasäännöt:

    - Onko kunkin aterian päiväraha-alennuksessa alennusprosentti, jos ateria on esimerkiksi maksuton? Jos vähennys on olemassa, mikä on vähennysprosentti ateriaa kohti?
    - Onko aterioiden vähennys laskettu päivää kohti, matkaa kohti vai per aterioiden määrä päivässä?
    - Onko päivärahasummat pyöristettävä säännöllisellä tavalla vai pyöristettävä?
    - Lasketaanko päivärahat 24 tunnin jakson vai kalenteripäivän perusteella?

- Sijaintiin perustuvat päiväraha säännöt:

    - Vaihtelevatko päivärahahinnat sijainnin mukaan? Mitkä sijainnit sisältyvät?
    - Jos päivärahat vaihtelevat sijainnin mukaan, kullekin sijainnille määritetään seuraavien kulujen prosenttiosuus:

        - Ateriat
        - Hotelli
        - Muut kulut

### <a name="expense-management-journals-and-accounts"></a>Kulujen hallinnan kirjauskansiot ja asiakkuudet

Kulujen hallinta edellyttää, että käytössä on useita päiväkirjoja ja asiakkaita. Sinun on esimerkiksi päätettävä, käytetäänkö samaa tiliä käteisennakko- ja luottokorttikiistoissa.

**Päätökset:**

- Mille kirjanpitokirjauskansiolle on kirjattu kuluraportit?
- Mitä tiliä käytetään käteisennakolle?
- Tuleeko käteisennakot kirjata heti?

### <a name="payment-methods"></a>Maksutavat

Kun sallit työntekijöiden kulujen syntymisen yrityksen puolesta, sinun täytyy määrittää maksutavat, joita työntekijöillä on oikeus käyttää. Voit esimerkiksi sallia työntekijöiden käyttää käteistä tai yrityksen luottokorttia. Työntekijät voivat myös sallia henkilökohtaisten luottokorttien käytön ja hyvittää työntekijöitä. Sinun on tehtävä seuraavat päätökset kullekin sallitulle maksutavalle.

**Päätökset:**

- Mitkä maksutavat ovat sallittuja?
- Kuka omistaa maksutavan kulut?
- Onko vastatilin tyyppiä? Jos vastatilintyyppi on olemassa, mikä se on?
- Jos vastatilintyyppi on olemassa, mikä tili on?
- Jos maksutapa on luottokortti, käytetäänkö maksutapaa vain tuotujen tapahtumien yhteydessä?

### <a name="expense-categories-and-shared-categories"></a>Kululuokat ja jaetut luokat

Kun työntekijät luovat kuluraportin, kukin heidän tallentamansa kulu on liitettävä kululuokkaan. Kululuokat johdetaan jaetuista luokista, jotka voidaan jakaa organisaation yritysten kesken. Nämä luokat voidaan jakaa myös projektinhallintaan ja kirjanpitoon sen mukaan, miten organisaatio on määritetty. Määritä organisaatiosi määrittelyn ja toteutusryhmän antamien ohjeiden perusteella, käytetäänkö kuluhallinnassa käytettyjä luokkia vain kulujen hallinnassa vai pitäisikö ne jakaa projektinhallinnan ja kirjanpidon sekä kuluhallinnan kesken. Huomaa, että nämä luokat voidaan jakaa projektin ja kulun tai projektin ja tuotannon kesken, mutta ei kulujen ja tuotannon kesken. Sinun täytyy tehdä seuraavat päätökset kullekin kululuokalle.

**Päätökset:**

- Mikä on kululuokka? Esimerkkeinä voidaan mainita luokat lennoille, hotellille tai kilometrikorvauksille.
- Voiko kululuokkaa käyttää myös projektinhallinnassa ja kirjanpidossa?
- Mikä on kulutyyppi?
- Mikä on kululuokan oletusmaksutapa?
- Onko kululuokan kulut eriteltävä?
- Mikä on kululuokan oletuspäätili?
- Mikä on kululuokan nimikkeen oletusarvonlisäveroryhmä?
- Sallitaanko kululuokalle muita maksutapoja? Jos lisämaksutavat ovat sallittuja, mitä ne ovat?
- Onko kululuokassa aliluokkia? Jos aliluokkia on, on tehtävä myös seuraavat päätökset:

    - Jätetäänkö jotkin aliluokat pois veronpalautuksesta?
    - Mikä on aliluokkien nimikkeen arvonlisäveroryhmä?

Jos kululuokkaa käytetään myös projektinhallinnassa ja kirjanpidossa, vastaa muihin kysymyksiin. Muussa tapauksessa voit siirtyä seuraavaan osaan.

- Mitä kustannustilejä käytetään seuraaviin kuluihin?

    - Kustannus
    - Palkanlaskennan kohdistus
    - KET-kustannusarvo
    - Kustannusnimike
    - KET-kustannuksen arvonimike
    - Jaksotettu tappio
    - KET – jaksotettu tappio

- Mitä tuottotilejä käytetään seuraaviin?

    - Laskutettu tuotto
    - Jaksotetun tuoton myyntiarvo
    - KET – myynnin arvo
    - Jaksotettu tuotto – tuotanto
    - KET – tuotanto
    - Jaksotettu tuotto – voitto
    - KET – voitto
    - Jaksotettu tuotto – tilaus
    - KET – tilaus

### <a name="taxes"></a>Verot

Jos kyseessä on kulujen liittyvä verotus, sinun täytyy määrittää, mitä kuluraporteissa on sisällytetty tai otettu käyttöön.

**Päätökset:**

- Sisältyykö liikevaihtovero kulusummiin?
- Onko veronpalautus otettava käyttöön kuluina?

    > [!NOTE]
    > Kun suunnittelit pääkirjan, jos olet päättänyt käyttää USA:n myyntiveroa ja käyttää verosääntöjä, et voi ottaa kulujen veron palautumista käyttöön. (Jos haluat käyttää USA:n myyntiveroa ja käyttää verosääntöjä, määritä **Käytä arvon lisäveron verosääntöjä** -asetuksen arvoksi **Kyllä** .)

## <a name="policies"></a>Käytännöt

Luomalla kuluraporttikäytäntöjä voit auttaa organisaatiota säästämään aikaa ja rahaa, kun työntekijöille aiheutuu kuluja sen puolesta. Käytännöt varmistavat, että työntekijät pysyvät budjetissa, toimittavat kaikki tarvittavat tiedot ja käyttävät rahaa vain tarpeen mukaan. Sinun täytyy tehdä seuraavat päätökset kullekin kuluraporttikäytännölle ja kullekin luotavalle kuluraportin hyväksyntäkäytännölle.

**Päätökset:**

- Mikä on käytännön nimi?
- Mihin kulukäytäntöä käytetään?
- Jos olet aiemmin päättänyt ottaa käyttöön konserniyritysten väliset kulut, mitkä organisaatiosi yritykset voivat käyttää tätä käytäntöä?
- Milloin käytäntö tulee voimaan?
- Milloin käytäntö vanhenee?
- Mikä on käytäntösääntö?
- Mikä on käytäntösäännön tulos?


[!INCLUDE[footer-include](../includes/footer-banner.md)]