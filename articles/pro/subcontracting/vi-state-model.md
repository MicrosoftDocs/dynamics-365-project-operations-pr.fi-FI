---
title: Toimittajan laskun tilasiirtymät
description: Tässä aiheessa selitetään toimittajan laskun tilan siirtymät Microsoft Dynamics 365 Project Operationsissa.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584684"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Toimittajan laskun tilasiirtymät

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Tässä aiheessa selitetään toimittajan laskun tilan siirtymät Microsoft Dynamics 365 Project Operationsissa. Käytössä ovat seuraavat tilat: **Luonnos**, **Tarkistettavana**, **Vahvistettu**, **Pidossa** ja **Peruutettu**.

Seuraavissa kuvissa on kuvattu tilasiirtymiä.

![Alihankintasopimuksen tilasiirtymämalli.](../media/VI_State_Model.jpg)

Seuraavassa taulukossa on kuvaus siitä, mitä kukin tila edustaa toimittajan laskun elinkaaressa Project Operationsissa.

| Vaihe | Description | Sallitut siirtymät |
| --- | --- | --- |
| Luonnos | Tämä tila on toimittajan laskun ensimmäinen tila. Riveihin ja hinnoitteluun voidaan tehdään muutoksia. Tässä tilassa olevaa toimittajan laskua voi muokata tai poistaa. | Käsiteltävänä |
| Tarkistettavana | Tämä tila edustaa toimittajan laskun käsittelytilaa. Vähintään yhdellä toimittajan laskurivillä on tarkistuksen tila **Kesken**. | Vahvistettu, Pidossa |
| Vahvistettu | Tämä tila tarkoittaa toimittajan laskun vaihetta, jossa sovellus on luonut toteutuneet kustannukset kullekin toimittajan laskun riville. Kaikki linkitettyjen kustannusten toteutuneet summat, jotka on yhdistetty toimittajan laskun riveille, on palautettu ja korvattu toimittajan laskun rivien toteutuneiden kustannusten arvoilla. Tässä tilassa olevaa toimittajan laskua ei voi muokata tai poistaa. **Peruuta**-painikkeella voit peruuttaa vahvistetun toimittajan laskun. Peruuta-toiminto kumoaa Vahvista-toiminnon vaikutuksen. | Peruutettu |
| Pidossa | <p>Tämä tila tarkoittaa toimittajan laskun vaihetta, jossa toimittajan laskua ei voi siirtää laskun ongelman tai toimittajan tilan takia. Tässä tilassa olevaa toimittajan laskua ei voi vahvistaa, peruuttaa, muokata tai poistaa.</p><p>Avaa uudelleen -toiminnon avulla voit siirtää toimittajan laskun **Luonnos**- tai **Tarkistettavana** -tilaan. Jos vähintään yhden toimittajan laskun rivin tarkistuksen tila on **Kesken** tai **Valmis**, toimittajan lasku avataan uudelleen **Tarkistettavana**-tilassa. Jos kaikkien toimittajan laskun rivien tarkistuksen tilana on **Ei aloitettu**, toimittajan lasku avataan uudelleen **Luonnos**-tilassa.</p> | Luonnos, Tarkistettavana |
| Peruutettu | Tämä tila edustaa alihankinnan vaihetta, jossa alihankittujen resurssien materiaalitoimitusta tai alihankittujen resurssien työtä ei enää tarvita. Tässä tilassa olevaa alihankintaa ei voi käyttää projektin henkilöstö-, resurssi- ja materiaalivaatimusten arvioimiseen, eikä sitä voi myöskään käyttää projektin ajan, kulujen ja materiaalikäytön viitteenä. Tässä tilassa olevaa alihankintaa ei voi muokata tai poistaa. | Ei mikään |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]