---
title: Matkalaskujen kirjaaminen
description: Tässä artikkelissa käsitellään kuluraporttien kirjaamista.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524865"
---
# <a name="post-expense-reports"></a>Matkalaskujen kirjaaminen

Kun kuluraportti on hyväksytty ja siirretty yleiseen päiväkirjaan, se voidaan kirjata. Kun kirjaat kuluraportin, kulut, joista voidaan palauttaa arvonlisävero (ALV), tunnistetaan. ALV-maksujen tarkistamisen ja palauttamisen tehtävä määritetään työntekijälle, joka on vastuussa kuluraportin tarkistamisesta.

Jos kuluraportin kulut veloitetaan muulle yritykselle kuin yritykselle, joka työllistää työntekijän, sinun täytyy tarkistaa sekä yritys jolle kyseiset kulut ollaan velkaa että yritys, joka on velkaa. Esimerkiksi kuluraportin lähettänyt työntekijä toimii DAT-yrityksessä, mutta veloitti kulun DIR-yritykseltä. Tällöin DAT on yritys, jolle kulu ollaan velkaa, ja DIR on yritys joka on velkaa kulun. Kun olet tarkistanut nämä kirjauskansionrivit, voit kirjata kulurivit pääkirjanpitoon.

Voit kirjata kuluraportin valitsemalla **Hyväksytyt kuluraportit** -sivulla kuluraportin ja valitsemalla sitten toimintoruudussa **Kirjaa**.

Voit myös kirjata kaikki luettelon kuluraportit samalla kertaa. Valitse kaikki kuluraportit ja valitse sitten **Kirjaa**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Ota käyttöön toiminto kulujen velan kirjaamiseksi toimittajan valuuttana käteismaksutavan ominaisuutta varten

**Mahdollisuus kirjata kuluvelka toimittajan valuuttana käteismaksutavan** -ominaisuuden avulla kuluraportit voidaan kirjata toimittajan valuuttana käteismaksutapaa varten.

Tällä hetkellä kun lähetät kassakuluja, kuluraportit kirjataan kirjanpitovaluuttana. Summan muuntamisen vuoksi tapahtumavaluutan, kirjanpitovaluutan ja toimittajan valuutan välillä toimittajalle maksetaan virheellinen summa, jos kulun tapahtumapäivämäärällä ja todellisella maksupäivällä on eri vaihtokurssit.

Tämä ominaisuus varmistaa, että toimittajan saldo kirjataan toimittajan valuuttana, kun kuluraportti kirjataan.

1. Siirry kohtaan **Työtilat** \> **Ominaisuuksien hallinta**.
2. Etsi ja valitse luettelosta **Mahdollisuus kirjata kuluvelka toimittajan valuuttana** käteismaksumenetelmää varten ja valitse sitten **Ota käyttöön nyt**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
