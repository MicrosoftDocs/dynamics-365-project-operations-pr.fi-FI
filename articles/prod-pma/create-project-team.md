---
title: Luo projektiryhmä
description: Tässä aiheessa on tietoja projektiryhmien luomisesta ja hallinnasta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270854"
---
# <a name="create-a-project-team"></a>Projektitiimin luominen

[!include [banner](../includes/banner.md)]

Jotta projektipäällikkö voisi käyttää aiemmin projektissa määritettyjä rooleja, hänen on osoitettava roolit projektille. Projektille voidaan osoittaa useita rooleja. Sekaannusten välttämiseksi näille rooleille määritetään automaattisesti otsikko varauksen aikana. Jos projektipäällikkö tarvitsee kolmea ohjelmistosuunnittelijaa, luodaan automaattisesti kolme ohjelmistosuunnittelijan roolia, joiden otsikot ovat **ohjelmistosuunnittelija 1**, **ohjelmistosuunnittelija 2** ja **ohjelmistosuunnittelija 3**. Jos roolille on aiemmin määritetty rooliominaisuudet, niitä käytetään suodattimena resurssin haun aikana. Lisäominaisuuksia voidaan lisätä tarpeen mukaan haun tarkentamiseksi.

Näkymäasetuksia voi myös mukauttaa paremman kuvan antamiseksi resurssien käytettävyydestä. Käytettävyys voidaan esittää tunneittain, viikoittain, kuukausittain, neljännesvuosittain ja vuosittain. Myös resurssien käytettävissä oleva ja jäljellä oleva kapasiteetti voidaan näyttää. Tästä vaihtoehdosta on hyötyä ajanhallinnassa, kun arvioit aktiviteetteihin käytettävissä olevaa aikaa tai resurssien käytettävyyttä.

Projektipäällikkö voi valita sivulla roolin ja sitten, jos vaatimuksen täyttävä resurssi on käytettävissä, päättää varata resurssin täyttämään kyseinen rooli. Huomaa, että resursseja ei tarvitse varata tässä kohtaa suunnitteluvaihetta. Kun luot työrakennemallin, voit korvata roolit projektin henkilöresursseilla. Jos roolit korvataan työrakenteessa henkilöresursseilla, resurssien määritys päivittää automaattisesti projektitiimiluettelon ja aikataulutuksen.

[![Projektitiimin luettelo, joka sisältää sekä roolit että todelliset resurssit](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektipäälliköllä on useita vaihtoehtoja resurssin varaamiseen projektia varten, kuten **Jäljellä oleva kapasiteetti**, **Koko kapasiteetti**, **Prosenttiosuus kapasiteetista** ja **Työtuntien määritys**. Nämä varausvaihtoehdot voidaan peruuttaa milloin tahansa, jos resurssiosoitukset muuttuvat. Kahdenlaisia varauksia tuetaan:

- **Sitova varaus** – Resurssin varaus on hyväksytty ja vahvistettu työskentelemään kiinnityksessä määritetyn keston ajan.
- **Alustava** – Resurssin varaukset on alustettavasti määritetty työskentelemään kiinnityksessä määritetyn keston ajan.

Seuraava menettely selittää, miten projektitiimi luodaan.

## <a name="create-a-project-team"></a>Projektitiimin luominen

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

## <a name="monitor-project-teams"></a>Projektitiimien seuraaminen
1. Valitse **Kaikki projektit** -sivulla **XYZ-päivityksen vaihe 2** -projektin **Projektitunnus**-linkki.
2. Varmista **Projektitiimi ja aikataulutus** -pikavälilehdessä, että luettelossa olevat projektiresurssit ovat oikein.


[!INCLUDE[footer-include](../includes/footer-banner.md)]