---
title: Projektin toimittajalaskujen vahvistaminen
description: Tässä artikkelissa käsitellään sitä, miten projektin toimittajalaskun voi vahvistaa Microsoft Dynamics 365 Project Operationsissa ja miten projektin toimittajalaskun vahvistuksella on taloudellinen vaikutus.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475431"
---
# <a name="confirm-project-vendor-invoices"></a>Projektin toimittajalaskujen vahvistaminen

**Käytetään**: Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

Kun **Projektipäällikön manuaalinen tarkistus on pakollinen** -parametri on käytössä, Microsoft Dataversessa luoduilla toimittajan laskuilla on **luonnos**-tila. Tällä tavalla luodut toimittajan laskut on tarkistettava ja vahvistettava manuaalisesti. Kun **Projektipäällikön manuaalinen tarkistus on pakollinen** -parametri ei ole käytössä, Dataversessa luodut toimittajan laskut vahvistetaan automaattisesti. Sinun ei tarvitse tehdä mitään. 

Kun olet tarkistanut kaikki toimittajan laskun rivit Dynamics 365 Project Operationsissa, voit vahvistaa toimittajan laskun **Vahvista**-toiminnon avulla.

Kun valitset toimittajan laskulle **Vahvista**, tapahtuu seuraava toiminta:

1. Toimittajan laskun tilaksi päivitetään **Vahvistettu**.
1. Vahvistetusta toimittajan laskusta ja siihen liittyvistä tietueista tulee vain luku -tietoja, eikä niitä voi muokata tai poistaa.
1. Jos toteutuneet kustannukset viittaavat toimittajan laskuriviin osana täsmäytystä, kaikki kustannusten toteutuneet tiedot, jotka liittyvät viitattuun toimittajan laskuriviin, palautetaan.
1. Uudet toteutuneet kustannukset luodaan käyttämällä toimittajan laskurivin tietoja.
1. Et voi enää luoda korjauskirjauskansioita, käsitellä ajankirjauksien peruutuksia tai peruuttaa alkuperäisen peruutetun ajan, kulun tai materiaalin toteutuneiden arvojen hyväksyntää.
1. Dynamics 365 Financessa **Projektikustannus**-arvo päivittyy käyttämällä projektin integrointikirjauskansiota, ja Hankintojen integrointitili *peruutetaan*, kun Projektin integrointikirjauskansio kirjataan.

> [!NOTE]
> Kun millä tahansa toimittajan laskun rivillä on muu tarkistuksen tila kuin **Valmis**, toimittajan laskua ei voi vahvistaa.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
