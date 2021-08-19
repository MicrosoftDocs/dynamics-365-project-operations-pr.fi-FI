---
title: Luo uusi projekti
description: Tässä aiheessa on tietoja uuden projektin luomisesta.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5aa5e00252697f91a585eaaa83a0c8a39b315cc1b25fcbf6343fdf2ce31a824e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985947"
---
# <a name="create-a-new-project"></a>Luo uusi projekti

[!include [banner](../includes/banner.md)]

Luodaksesi uuden projektin, toimi seuraavasti.

1. Valitse **Projektinhallinta**-sivulla **Uusi projekti** ja syötä seuraavat arvot:

    - **Projektityyppi:** Aika ja materiaali
    - **Projektin nimi:** XYZ-päivityksen vaihe 2
    - **Projektiryhmä:** TM\_WIP
    - **Projektisopimuksen tunnus:** 00000002

2. Valitse **Luo projekti**.

## <a name="assign-a-resource-to-a-project"></a>Resurssin osoittaminen projektille

1. Valitse **Työntekijät**-sivun **Työntekijät**-luettelosta sen työntekijän tietue, jolle olet aiemmin määrittänyt pätevyyksiä, ja avaa työntekijän tietue.
2. Valitse toimintoruudun **Projekti**-välilehden **Määritys**-ryhmässä **Osoita projekteja**.
3. Käytä suodattimena **XYZ-päivityksen vaihe 2** -projektia suodattimena **Resurssivahvistuksen projektiosoitukset**-sivun **Projektit**-välilehden **Lisää projekti valittuihin projekteihin** -kentässä.
4. Valitse **Jäljellä olevat projektit** -ruudussa projekti ja lisää se sitten **Valitut projektit**-ruutuun valitsemalla nuolipainike.

Voit myös määrittää resurssille luokkia tarpeen mukaan. Luokan tyyppi on joko **Kustannus** tai **Tuotto**. Organisaatiosi määrittää luokkatyypin. Jos resurssille ei ole määritetty luokkia, Finance hakee tuntihintojen oletusluokan kustannuksille ja tuotoille.

## <a name="set-up-project-resource-and-role-characteristics"></a>Projektiresurssin ja rooliominaisuuksien määrittäminen

Projektipäällikkö voi luoda projektin edellyttämiä rooleja projektin resusointitoiminnon avulla. Rooleja voidaan käyttää, jos vahvistetut resurssit ovat vielä tuntemattomia, kun resursseja varataan. Roolit voidaan varata väliaikaisesti suunnitelluiksi resursseiksi, jotta voit jatkaa projektin suunnitteluvaiheita.

[![Esimerkki roolista.](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Skenaario:** Contoso palkattiin suorittamaan Aika ja materiaalit -projekti, jolla on hyväksytty projektin perustamisasiakirja. Aliprojektipäällikkö määrittää edelleen projektin vaikutusaluetta. Resurssipäällikkö on tällä hetkellä määrittämässä erityisiä resursseja, jotka varataan työskentelemään uudessa projektissa. Projektin kriittisen luonteen vuoksi projektin rahoittaja pyysi projektipäällikköä yhdeksi rooleista. Resurssipäällikön täytyy hankkia uusi resurssi ja määrittää se järjestelmässä, jos aliprojektipäällikkö tarvitsee resurssin tiedot projektisuunnittelun aikana.

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

## <a name="assign-a-project-resource-to-a-project"></a>Projektiresurssin osoittaminen projektille

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

## <a name="assign-a-resource-to-a-default-role"></a>Osoita resurssi oletusroolille

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]