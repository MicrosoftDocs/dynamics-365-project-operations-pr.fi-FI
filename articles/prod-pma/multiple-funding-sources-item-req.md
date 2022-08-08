---
title: Useiden rahoituslähteiden projektisopimusten nimikevaatimukset
description: Tässä artikkelissa on tietoja nimikevaatimusten määrittämisestä ja käytöstä useissa rahoituslähteissä.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028469"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Useiden rahoituslähteiden projektisopimusten nimikevaatimukset

_**Koskee:** Project Operations varastoitavien ja tuotantopohjaisten skenaarioissa_

Jotkin projektipohjaisten toimitusten sopimukset voivat edellyttää useita rahoituslähteitä. Tässä artikkelissa käsitellään sitä, miten valitaan ja määritetään halutut rahoituslähteet, kun projektissa tai projektisopimuksessa tarvitaan useita lähteitä.

## <a name="terminology"></a>Termit

- **Rahoituslähde** – entiteetti, joka käyttää varoja projektisopimukseen. Tämä entiteetti voi olla sisäinen organisaatio tai ulkoinen laskutili (asiakas tai apuraha).
- **Projektiasiakas** – entiteetti, jonne projektityö toimitetaan.
- **Laskutustili** – ulkoinen entiteetti, joka maksaa projektityöstä.

## <a name="example"></a>Esimerkki:

Contoso on voittanut välineiden uusimissopimuksen kahdelle asiakkaalleen: Adatum US ja Adatum Corporate. Palvelusopimus sisältää laitteisto- ja asennuspalvelut, jotka toimitetaan Adatum US -yritykselle (projektiasiakas). Adatum Corporate (laskutustili 1) rahoittaa laitteiston, ja asennustyöt rahoittaa Adatum US (laskutustili 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Määritä laskutustilin oletussäännöt nimiketarpeita varten

### <a name="prerequisites"></a>edellytykset

- Microsoft Dynamics 365 Financen **versio 10.0.27** tai uudempi on pakollinen, jotta voidaan käyttää nimikevaatimuksia, joissa on useita laskutilejä.
- Järjestelmän on otettava käyttöön **Salli nimikevaatimukset ja useita rahoituslähteitä Project Operationsin varasto-/tuotantopohjaisiin skenaarioihin** -ominaisuus **Ominaisuuksien hallinta** -työtilassa.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Laskutustilin oletussääntöjen määritys

Voit määrittää oletussäännöt laskutilille seuraavasti.

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Määritys** \> **Projektinhallinnan ja kirjanpidon parametrit**.
1. Määritä **Yleiset**-välilehden **Myyntitilaukset ja nimiketarpeet**-osassa **Salli projekteille, joilla on useita rahoituslähteitä** -asetuksen arvoksi **Kyllä**.
1. Määritä **Oletusasiakas**-kentässä, mistä nimiketarpeen projektin toimitusasiakas on peräisin oletusarvoisesti:

    - **Rahoituslähteestä** – projektin oletustoimitusasiakas on peräisin rahoituslähteestä. Jos projektisopimukseen liittyy useita rahoituslähteitä, käytetään luettelon ensimmäistä rahoituslähdettä.
    - **Projektista** – Projektin oletustoimitusasiakas tulee asiakkaalta, joka on valittu **Projektitietueen tili** -kentässä.

1. Valinnainen: määritä tai muuta oletuslaskutili projektitietueille:

    1. Valitse **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit** ja avaa projektitietueen tiedot.
    2. Määritä tai päivitä **Yleiset**-välilehdessä **Oletuslaskutili**-kenttä. Määrittämääsi tiliä käytetään projektia varten luotujen uusien nimikevaatimusten oletuslaskutilinä. Jos jätät kentän tyhjäksi, oletusarvon mukaan käytetään ensimmäisen projektisopimuksen rahoituslähteen laskutiliä. Käyttäjät voivat kuitenkin muuttaa tiliä, kun he tallentavat tietueen.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Valitse käytettävä laskutili nimikevaatimusta luotaessa

Voit valita käytettävän laskutilin nimikevaatimusta luotaessa seuraavasti.

1. Valitse **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit** ja valitse projektitietue.
1. Valitse **Suunnitelma**-välilehdessä **Nimiketarpeet**.
1. Luo uusi nimiketarvetietue.

    - Tietueen **Laskutustili**-kentän oletusarvona on projektille määritetty laskutustili. Voit muuttaa **Laskutili**-kentän arvoa ja tallentaa tietueen. Kun tietue on tallennettu, et voi enää päivittää **Laskutustili**-arvoa. Jos nimiketarpeessa on päivitettävä **Laskutili**-arvoa, poista aiemmin luotu nimikevaatimus ja luo sitten uusi, jolla on haluamasi arvo.
    - Nimikkeen tarpeen **Asiakas**-kenttä määritetään oletusarvoisesti **Projektinhallinta ja kirjanpitoparametrit** -sivulla määritetyn **Oletusasiakas**-arvon perusteella.

    Kun nimikkeen tarvetietue tallennetaan, järjestelmä liittää sen **Nimiketarpeen myyntitilaus** -otsikkotietueeseen. Jos avoimella myyntitilauksen otsikolla ei ole valittua laskutiliä, järjestelmä luo sen ja liittää siihen nimiketarverivin.

> [!NOTE]
> Nimiketarpeet laskutetaan aina kokonaan tietueessa määritetyltä laskutililtä. Järjestelmä ei tällä hetkellä tue varojen kohdentamissääntöjä, joissa on nimiketarpeita, eikä se jaa kirjausta varojen kohdistussääntöjen määritysten perusteella.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Nimiketarpeen luominen nimikkeen ennustetietueesta

Nimiketarpeen luominen nimikkeen ennustetietueesta tapahtuu seuraavasti.

1. Valitse **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit** ja valitse projektitietue.
1. Valitse **Suunnitelma**-välilehdessä **Nimike-ennusteet**.
1. Luo uusi nimike-ennustetietue.
1. Valinnainen: Valitse **Projekti**-välilehden **Rahoituslähde**-kentässä haluamasi laskutili.
1. Valitse **Luo nimiketarve** ja vahvista vastaanottamasi sanoma.

    > [!NOTE]
    > Järjestelmä kopioi **rahoituslähteen** arvon nimikkeen ennustetietueesta juuri luotuun nimikkeen tarvetietueeseen.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Oletuslaskutili, kun järjestelmä luo automaattisesti nimikevaatimuksen ostotilausriviltä

Jos **Luo nimiketarve** -asetuksena on **Kyllä** **Projektinhallinnan ja kirjanpidon parametrit** -sivulla, järjestelmä luo automaattisesti nimikevaatimuksen, kun uusi projektin ostotilausrivi tallennetaan. **Laskutili**- ja **Nimiketarve**-kenttien oletusarvona on projektitietueen **Oletuslaskutili**-kentän arvo. Järjestelmä ei tue tällä hetkellä tämäntyyppisten tietueiden laskutilin päivittämistä tai muuttamista.
