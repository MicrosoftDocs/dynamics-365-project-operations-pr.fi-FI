---
title: Alihankinnan tilan siirtymät
description: Tässä artikkelissa käsitellään alihankinnan tilan siirtymiä Microsoft Dynamics 365 Project Operationsissa, kun alihankinta luodaan, suoritetaan ja suljetaan.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 02553099a6728c19c219659dff431ff9a5cf10fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261189"
---
# <a name="state-transitions-on-a-subcontract"></a>Alihankinnan tilan siirtymät 

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Tässä artikkelissa käsitellään alihankinnan tilan siirtymiä Microsoft Dynamics 365 Project Operationsissa. Tila on joko luonnos, vahvistettu, suljettu tai peruutettu. Seuraava kuva edustaa tilan siirtymiä.

![Alihankinnan tilamalli](../media/SubconStates.png)  

Seuraavassa taulukossa on kuvaus siitä, mitä kukin tila edustaa alihankinnan elinkaaressa Project Operationsissa.

| Vaihe | Description | Sallitut siirtymät |
| --- | --- | --- |
| Luonnos | Tämä edustaa alihankinnan alkutilaa. Toimittajan kanssa käydään neuvotteluja. Riveihin ja hinnoitteluun tehdään muutoksia. Tässä tilassa olevaa alihankintaa voidaan käyttää projektin henkilöstö-, resurssi- ja materiaalivaatimusten arvioimiseen. Sitä voidaan käyttää myös projektin ajan, kulujen ja materiaalikäytön viitteenä. Tässä tilassa olevaa alihankintaa voi muokata ja sen voi poistaa. | Vahvistettu |
| Vahvistettu | Tämä edustaa alihankinnan vaihetta, jossa neuvottelut toimittajan kanssa hinnoittelusta ja ostettavista rivinimikkeistä ovat valmiit. Alihankittujen materiaalien toimitus tai alihankittujen resurssien työ on kuitenkin vielä kesken. Tässä tilassa olevaa alihankintaa voidaan käyttää projektin henkilöstö-, resurssi- ja materiaalivaatimusten arvioimiseen. Sitä voidaan käyttää myös projektin ajan, kulujen ja materiaalikäytön viitteenä. Tässä tilassa olevaa alihankintaa ei voi muokata tai poistaa. **Peruuta**-painikkeen avulla voi peruuttaa vahvistetun alihankinnan. **Avaa uudelleen** -painikkeen avulla voit avata alihankinnan uudelleen ja palauttaa sen **Luonnos**-tilaan. Käytä **Sulje**-painiketta sulkeaksesi vahvistetun alihankinnan. | Suljettu <br> Peruutettu <br> Luonnos |
| Suljettu | Tämä edustaa alihankinnan vaihetta, jossa alihankittujen resurssien materiaalitoimitus tai alihankittujen resurssien työ on valmis. Tässä tilassa olevaa alihankintaa ei voi enää käyttää projektin henkilöstö-, resurssi- ja materiaalivaatimusten arvioimiseen. Sitä ei voi myöskään enää käyttää projektin ajan, kulujen ja materiaalikäytön viitteenä. Tässä tilassa olevaa alihankintaa ei voi muokata tai poistaa. | Ei mikään |
| Peruutettu | Tämä edustaa alihankinnan vaihetta, jossa alihankittujen resurssien materiaalitoimitusta tai alihankittujen resurssien työtä ei enää tarvita. Tässä tilassa olevaa alihankintaa ei voi käyttää projektin henkilöstö-, resurssi- ja materiaalivaatimusten arvioimiseen, eikä sitä voi myöskään käyttää projektin ajan, kulujen ja materiaalikäytön viitteenä. Tässä tilassa olevaa alihankintaa ei voi muokata tai poistaa. | Ei mikään |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
