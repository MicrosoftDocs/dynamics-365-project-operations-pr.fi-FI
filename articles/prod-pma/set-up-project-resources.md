---
title: Projektin resurssien määrittäminen
description: Tämä aihe sisältää tietoja projektiresurssien määrittämisestä tai pyytämisestä.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9af71fe0638a5601ded3f0e80301ae5dfa198c1
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682571"
---
# <a name="set-up-project-resources"></a>Projektin resurssien määrittäminen

[!include [banner](../includes/banner.md)]

Sinun on määritettävä kalenteri ja osoitettava se työntekijälle. Kalenteria käytetään projektin ja projektiin varattujen resurssien työaikojen aikatauluttamiseen. Kalenterin määrittämisen aikana projektipäälliköt voivat tasata resursseja osana resurssien optimointia. Resursseille voi määrittää rajoituksia kalenteriaikataulun perusteella. Voit määrittää kalenterin **Kalenterit**-sivulla.

Kun määrität työntekijän projektin resurssiksi, voit valita niistä työntekijöistä, jotka ovat töissä siinä yrityksessä, jolle määrität resursseja. Vaihtoehtoisesti voit valita työntekijöitä muista yrityksistä organisaatiossasi. Näitä työntekijöitä kutsutaan yritystenvälisiksi resursseiksi.

Seuraavissa menettelyissä kerrotaan, miten työntekijä määritetään projektiresurssiksi yrityksessäsi ja miten yritystenvälinen projektiresurssi määritetään.

## <a name="set-up-a-worker-as-a-project-resource"></a>Työntekijän määrittäminen projektiresurssiksi

1. Valitse **Työntekijät**-sivun **Työntekijät**-luettelosta se työntekijä, jonka olet lisäämässä projektiresurssiksi ja avaa työntekijän tietue.
2. Valitse toimintoruudussa **Projekti** &gt; **Määritys** &gt; **Projektin määritys**.
3. Valitse kalenteri ja sulje sitten sivu.

Voit myös määrittää resurssille oletusprojekteja ennakkovarauksina. Ennakkovarauksia voi käyttää, kun resurssi- tai projektipäällikkö tietää etukäteen, missä projekteissa resurssi tulee työskentelemään. Ennakkovaraukset voivat perustua myös projektin rajoittajan tai asiakkaan pyyntöön. Jos haluat tehdä projektille ennakkovarauksen, valitse **Määritä projekteja** -sivulla **Projektit**-välilehden **Jäljellä olevat projektit** -luettelosta asianmukainen projekti.

## <a name="set-up-an-intercompany-resource"></a>Yritystenvälisen resurssin määrittäminen

Kun määrität työntekijän yritystenväliseksi resurssiksi, sinun täytyy suorittaa määritys sekä työntekijän lähtö- että kohdeyrityksessä.

### <a name="in-the-lending-company"></a>Lähtöyrityksessä

1. Varmista Financessa, että lähdeyritys on valittuna ja suorita sitten edellisen kohdan menettely Määritä työntekijä projektiresurssiksi.
2. Valitse **Yritystenvälinen kirjanpito**-sivulla **Uusi**.
3. entiteettiValitse **Oikeushenkilön tunnus** kentässä lähtöyritys. Täytä jäljellä olevat kentät asianmukaisesti ja valitse **Tallenna**.
4. Valitse **Siirtohinta**-sivulla **Uusi**.
5. Valitse **Kohdeoikeushenkilö** -kentässä asianmukainen yritys.
6. Jos haluat lainata kohdeyritykselle vain tämän osan alussa luomasi resurssin, valitse **Resurssi**-kentässä luomasi resurssin nimi. Jos haluat antaa kaikki lähtöyrityksen resurssit kohdeyrityksen käyttöön, jätä **Resurssi**-kenttä tyhjäksi.
7. Märitä **Projektinhallinnan ja kirjanpidon parametrit**-sivun **Yritystenvälinen**-välilehdessä **Ota yritystenvälisten resurssien aikataulutus ja tuntilomakkeet käyttöön** -asetukseksi **Kyllä**.

### <a name="in-the-borrowing-company"></a>Kohdeyrityksessä

- Syötä **Resurssiluettelo**-sivun hakusuodattimeen lähtöyritykselle luomasi resurssin nimi sen varmistamiseksi, että nimi sisällytetään kohdeyrityksen resurssiluetteloon.

## <a name="request-project-resources"></a>Projektiresurssien pyytäminen
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]