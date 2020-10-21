---
title: Tuotteet
description: Tässä aiheessa on tietoja tuoteluettelosta, jonka avulla annetaan tietoja asiakkaille organisaation tuotteista ja hinnoittelusta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 28397fd49ad4cdb2c820ef4b6f198f410995ba0f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898707"
---
# <a name="products"></a>Tuotteet

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Tuotteet ovat liiketoiminnan perusta. Dynamics 365 Sales Professionalin tuoteluettelo on tuotteiden ja niiden hintatietojen kokoelma. Voit auttaa myyjiä lisäämään myyntiä luomalla tuoteluettelon nopeasti.

## <a name="add-a-product"></a>Tuotteen lisääminen

1.  Varmista, että sinulla on Sales Professionalin esimiehen tai järjestelmänvalvojan rooli, jotta voit lisätä tuotteita Dynamics 365 Sales Professionaliin.
2.  Valitse sivustokartan **Asetukset**-kohdassa **Tuotteet**.
3.  Valitse **Lisää tuote** ja anna seuraavat tiedot:

    -  **Nimi**
    -  **Tuotetunnus**
    -  **Ylätaso**: Valitse tuotteen ylätason tuoteperhe. Jos olet luomassa tuoteperheessä alitason tuotetta, ylätason tuoteperheen nimi täytetään tässä. Tätä ei voi muuttaa sen jälkeen, kun tietue on tallennettu.
    -  **Voimassa alkaen** / **Voimassa asti**: määritä tuotteen voimassaoloaika valitsemalla **Voimassa alkaen**- ja **Voimassa asti** -päivämäärä.
    -  **Yksikköryhmä**: Valitse yksikköryhmä. Yksikköryhmä on kokoelma yksiköistä, joissa tuotetta myydään, ja se määrittää, mitkä yksittäiset kohteet ryhmitetään suuremmiksi määriksi. Jos esimerkiksi lisäät siemenet tuotteeksi, olet ehkä luonut Siemenet-nimisen yksikköryhmän ja sen ensisijaiseksi yksiköksi on määritetty paketti.
    -  **Oletusyksikkö**: Valitse yleisin yksikkö, jossa tuotetta myydään. Yksiköt ovat määriä tai mittayksiköitä, joissa tuotteita myydään. Jos olet esimerkiksi lisännyt siemenet tuotteena, voit myydä ne paketeissa, laatikoissa tai kuormalavoilla. Kukin niistä on jatkossa tuotteen yksikkö. Jos siemenet myydään useimmiten paketeissa, valitse se yksiköksi.
    -  **Oletushinnasto**: Jos kyseessä on uusi tuote, tätä kenttää ei voi muuttaa. Ennen oletushinnaston valitsemista pitää täyttää kaikki pakolliset kentät ja tallentaa tietue. Vaikka oletushinnasto ei ole pakollinen, tuotteelle kannattaa määrittää oletushinnasto tuotetietueen tallentamisen jälkeen. Tällöin Sales voi käyttää tarjousten, tilausten ja laskujen luonnissa oletushinnastoa, jos asiakastietueessa ei ole hinnastoa.
    -  **Desimaaleja käytettävissä**: Anna kokonaisluku 0–5. Jos tuotetta ei voi jakaa osiin, anna 0. Tarjous-, tilaus- tai laskutustuotetietueen **Määrä**-kentän tarkkuus tarkistetaan tämän kentän arvosta, jos tuotteeseen ei ole liitetty hinnastoa.
    -  **Aihe**: Liittää tuotteeseen aihe. Aiheiden avulla voit luokitella tuotteita ja suodattaa raportteja.

4.  Valitse **Tallenna**.
5.  Siirry **Muut tiedot** -välilehden **Hinnaston nimikkeet** -osaan, valitse **Lisää komentoja** ja valitse sitten **Lisää uusi hinnaston nimike**.
7.  Valitse **Muut tiedot** -välilehden **Tuotesuhde**-osan **Lisää komentoja** -kuvake ja valitse sitten **Lisää uusi tuotesuhde.**
8.  Anna seuraavat tiedot **Uusi tuotesuhde**-lomakkeessa ja valitse komentopalkissa **Tallenna ja sulje**:

    -   **Liittyvä tuote**: Valitse tuote, jonka haluat lisätä liittyvänä tuotteena käsiteltävään aiemmin luotuun tuotetietueeseen.
    -   **Myyntisuhteen tyyppi**: Määritä, haluatko lisätä tuotteen lisämyynti-, ristiinmyynti- vai apuvälinetuotteena vai korvaavana tuotteena.
    -   **Suunta**: Määritä, onko tuotteiden välinen suhde yksi- vai kaksisuuntainen. Jos valitset yksisuuntaisen suhteen, **Liittyvä tuote** -kohdassa valittu tuote näkyy suosituksena aiemmin luodulle tuotteelle mutta ei päinvastoin.

9.  Valitse tuotelomakkeesta **Tallenna**.

## <a name="import-products"></a>Tuotteiden tuonti

Voit käyttää tuontimalleja tietojen joukkotuontiin Dynamics 365 Salesissa.

## <a name="revise-a-product"></a>Tuotteen muuttaminen

Tuotevaraston päivittäminen onnistuu nopeasti korjaamalla tuotteiden ominaisuuksia tarvittaessa ja julkaisemalla nämä tiedot, jotta myyjät näkevät uusimmat varastoon tehdyt muutokset.

1.  Varmista, että sinulla on jokin seuraavista käyttöoikeusrooleista tai vastaavat käyttöoikeuksista: Järjestelmänvalvoja, Järjestelmän mukauttaja, Myyntipäällikkö, Myyntijohtaja, Markkinointijohtaja tai Toimitusjohtaja.
2.  Valitse sivustokartassa **Tuotteet**.
3.  Avaa muutettava aktiivinen tuote ja valitse komentopalkissa **Muuta**.
4.  Valitse **Vahvista muuttaminen** -valintaikkunassa **Vahvista**. Tuotteen tilaksi tulee **Tarkistettavana**.
5.  Kun olet tehnyt muutokset, valitse komentopalkissa **Julkaise**.

    > [!TIP]
    > Jos haluat palauttaa muutokset ja jatkaa tuotteen viimeisellä aktiivisella versiolla, valitse **Palauta.** Tuotteen tila muuttuu takaisin **Aktiivinen**-tilaan.

## <a name="clone-a-product"></a>Tuotteen kloonaminen 

Voit säästää aikaa uuden tuotteen luomisessa kloonaamalla aiemmin luodun tuotteen. Alkuperäisestä tietueesta luotava kopion tiedot ovat nimeä ja tunnusta lukuun ottamatta samat.

1.  Varmista, että sinulla on jokin seuraavista käyttöoikeusrooleista tai vastaavat käyttöoikeuksista: Järjestelmänvalvoja, Järjestelmän mukauttaja, Myyntipäällikkö, Myyntijohtaja, Markkinointijohtaja tai Toimitusjohtaja.
2.  Valitse sivustokartassa **Tuotteet**.
3.  Valitse kloonattavan tuotteen tietue ja valitse komentopalkissa **Klooni**. Vahvistusvalintaikkuna avautuu.
4.  Valitse **Vahvista**.

Avautuva uusi tuotetietue sisältää muuten samat tiedot kuin alkuperäinen tietue, mutta sillä on eri nimi ja tunnus.

## <a name="retire-a-product"></a>Tuotteen poistaminen käytöstä 

Jos organisaatio ei enää myy tuotetta, poista tuote käytöstä, jotta se ei ole enää myynnin asiakaspalvelijoiden käytettävissä.

1.  Varmista, että sinulla on Järjestelmänvalvojan tai Sales Professionalin esimiehen rooli tai vastaavat käyttöoikeudet.
2.  Valitse sivustokartassa **Tuotteet**.
3.  Avaa käytöstä poistettava aktiivinen tuote ja valitse komentopalkissa **Poista käytöstä**.
4.  Valitse **Vahvista käytöstä poistaminen** -valintaikkunassa **Vahvista**.


## <a name="delete-a-product"></a>Tuotteen poistaminen

Voit lopettaa tuotteen myynnin poistamalla sen.

> [!IMPORTANT]
> Et voi palauttaa poistettua tietuetta.

1.  Varmista, että sinulla on Järjestelmänvalvojan tai Sales Professionalin esimiehen rooli tai vastaavat käyttöoikeudet.
2.  Valitse sivustokartassa **Tuotteet**.
3.  Valitse poistettava tuotetietue ja valitse komentopalkissa **Poista**.
4.  Valitse **Vahvista poistaminen** -valintaikkunassa **Jatka**.
 
 ## <a name="quantity-factors-for-products"></a>Tuotteiden määräkertoimet

Määräkertoimia käytetään tukemaan tilausperusteisten tuotteiden myyntiä. Tilausperusteisten tuotteiden osalta tarjouksen tai projektisopimuksen rivin määrä ilmaistaan käyttäjäkuukausien lukumääränä.

Yleensä tilausohjelmiston hinta tallennetaan luetteloon käyttäjäkohtaisena kuukausihintana. Voit kuitenkin käyttää muitakin aikakuvauksia. Myyntiprosessin aikana tarjousrivillä oleva hinta on yleensä se käyttäjäkohtainen kuukausihinta, jonka IT-myyjä on neuvotellut ja josta hän on antanut alennusta. Kullakin kaupalla on eri määrä käyttäjiä ja eri määrä tilauskuukausia. Tarjousrivin summan laskemiseen käytettävä määrä perustuu käyttäjämäärään ja tilauskuukausien määrään.

Määräkertoimet perustuvat tuotemääritteisiin. Kun määrität tuotteelle tiettyjä ominaisuuksia, voit valita osan näistä määritteistä tai ne kaikki määräkertoimiksi.

Järjestelmä varmistaa, että määräkertoimiksi valitaan vain numeerisia ominaisuuksia tai tuoteominaisuuksia joilla on numeerinen tietotyyppi. Kun tarjousriville lisätään tuote, jolle on määritetty määräkertoimia, tarjousrivin **Määrä** -kentästä tulee vain luku -kenttä. Kun olet määrittänyt arvot tuoteominaisuuksille, jotka ovat määräkertoimia, tarjousrivin määrä lasketaan.

Käytettävissä voivat olla esimerkiksi seuraavat ominaisuudet: 

- **Käyttäjät**: Käyttäjien määrä 
- **Kuukaudet**: Tilauskuukausien määrä
- **Tuote-SKU** 

**Käyttäjät**- ja **Kuukaudet**-ominaisuudet voidaan valita määräkertoimiksi muokkaamalla tuoterivin ominaisuuksia. 
