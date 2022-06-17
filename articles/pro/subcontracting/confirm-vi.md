---
title: Projektin toimittajalaskun vahvistaminen
description: Tässä artikkelissa käsitellään sitä, miten projektin toimittajalaskun voi vahvistaa Microsoft Dynamics 365 Project Operationsissa ja miten projektin toimittajalaskun vahvistuksella on taloudellinen vaikutus.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932430"
---
# <a name="confirm-a-project-vendor-invoice"></a>Projektin toimittajalaskun vahvistaminen

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Kun olet tarkistanut kaikki toimittajan laskun rivit Microsoft Dynamics 365 Project Operationsissa, voit vahvistaa toimittajan laskun Vahvista-toiminnon avulla.

Kun valitset toimittajan laskulle **Vahvista**, tapahtuu seuraava toiminta:

1. Toimittajan laskun tilaksi päivitetään **Vahvistettu**.
2. Vahvistetusta toimittajan laskusta ja siihen liittyvistä tietueista tulee vain luku -tietoja, eikä niitä voi muokata tai poistaa.
3. Jos toteutuneet kustannukset viittaavat toimittajan laskuriviin osana täsmäytystä, kaikki kustannusten toteutuneet tiedot, jotka liittyvät viitattuun toimittajan laskuriviin, palautetaan.
4. Uudet toteutuneet kustannukset luodaan käyttämällä toimittajan laskurivin tietoja.
5. Kun toimittajan lasku on vahvistettu, et voi enää luoda korjauskirjauskansioita, käsitellä ajankirjauksia tai peruuttaa alkuperäisen ajan, kulun tai materiaalin toteutuneiden arvojen hyväksyntää.

> [!NOTE]
> Kun millä tahansa toimittajan laskun rivillä on muu tarkistuksen tila kuin **Valmis**, toimittajan laskua ei voi vahvistaa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
