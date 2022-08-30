---
title: Projektin toimittajan laskun peruuttaminen
description: Tässä artikkelissa käsitellään sitä, miten projektin toimittajalaskun voi peruuttaa Microsoft Dynamics 365 Project Operationsissa ja miten projektin toimittajalaskun peruuttamisella on taloudellinen vaikutus.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261086"
---
# <a name="cancel-a-project-vendor-invoice"></a>Projektin toimittajan laskun peruuttaminen

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Kun toimittajan lasku on vahvistettu, sitä ei voi muokata tai poistaa. Jos vahvistetussa toimittajan laskussa tapahtui virhe, voit peruuttaa toimittajan laskun vaikutuksen ja luoda uuden toimittajan laskun Peruuta-toiminnolla.

Kun valitset toimittajan laskulle **Peruuta**, tapahtuu seuraava toiminta:

1. Toimittajan laskun tilaksi päivitetään **Peruutettu**.
2. Peruutetusta toimittajan laskusta ja siihen liittyvistä tietueista tulee vain luku -tietoja, eikä niitä voi muokata tai poistaa.
3. Kaikki toimittajan laskuriveille toimittajan laskun vahvistuksen yhteydessä luodut toteutuneet kustannukset palautetaan.
4. Jos toteutuneet kustannukset on linkitetty toimittajan laskuriveille osana täsmäytystä, alkuperäinen toimittajan laskun vahvistus kumosi ne. Toimittajan laskun peruutuksen aikana nämä toteutuneet kustannukset luodaan uudelleen. Alkuperä osoittaa ajan, kulun tai materiaalinkäytön merkintöihin.
5. Kun toimittajan lasku on peruutettu, voit jälleen luoda korjauskirjauskansioita, käsitellä ajankirjauksia ja peruuttaa alkuperäisen ajan, kulun tai materiaalin toteutuneiden arvojen hyväksynnän.

> [!NOTE]
> Vain vahvistettuja projektin toimittajalaskuja voi peruuttaa. Toimittajan laskuja ei voi peruuttaa muissa tiloissa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
