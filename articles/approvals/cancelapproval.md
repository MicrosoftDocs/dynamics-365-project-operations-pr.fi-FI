---
title: Aiemmin hyväksyttyjen merkintöjen hyväksynnän peruuttaminen
description: Tässä artikkelissa käsitellään sitä, miten projektipäällikkö voi peruuttaa aiemmin hyväksyttyjen ajan-, kulu- tai materiaalikäytön merkintöjen hyväksynnän.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930452"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Aiemmin hyväksyttyjen merkintöjen hyväksynnän peruuttaminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Projektipäällikkö tai hyväksyjä voi peruuttaa aiemmin hyväksyttyjen ajan-, kulu- tai materiaalikäytön merkintöjen hyväksynnän. 

Seuraa näitä vaiheita peruaksesi aiemmin hyväksymäsi aika-, kulu- tai materiaalinkäyttömerkinnän.

1. Siirry kohtaan **Projektit** \> **Omat työt** \> **Hyväksynnät**.
2. **Hyväksynnät**-luettelosivulla näkyvät kaikki hyväksyntää odottavat aikamerkinnät. Vaihda näkymäksi **Omat aiemmat hyväksynnät**.
3. Valitse peruutettava aika-, kulu- tai materiaalihyväksyntä. Valitse sitten toimintoruudussa **Peruuta hyväksyntä**.
4. Vahvista toiminto valitsemalla näkyviin tulevassa vahvistussanomaruudussa **OK**.

> [!IMPORTANT]
> Asiakkaalta jo aiemmin laskutettua hyväksyttyä aikaa, kulua tai materiaalin käyttömerkintää ei voi peruuttaa. Jos yrität, saat sanoman, jonka mukaan hyväksyntää ei voi peruuttaa, koska se on jo laskutettu. Tällöin voit pyytää hyväksynnän peruutusta vain, jos korjauslaskua käytetään kokonaishyvitykseen tai palautukseen asiakkaalle alkuperäisen laskun mukaan.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Aiemmin hyväksyttyjen merkintöjen hyväksynnän peruuttamisen vaikutus

Kun hyväksyntä perutaan, siihen liittyy sekä toiminnallisia vaikutuksia että taloudellisia vaikutuksia.

### <a name="operational-impact"></a>Toiminnallinen vaikutus

Jos merkinnän hyväksyntä peruutetaan, hyväksyntätietue merkitään tilaan **Lähetetty**. Merkinnän tilaksi vaihtuu **Lähetetty**. Tässä vaiheessa projektiryhmän jäsen voi peruuttaa merkinnän lähettämättä palautuspyyntöä.

Hyväksyjä voi muuttaa **laskutettavan määrän** ja **laskutustyypin** arvoja ja hyväksyä merkinnän vielä kerran.

### <a name="financial-impact"></a>Taloudellinen vaikutus

Jos merkinnän hyväksyminen peruutetaan, vastaavat toteutuneet kustannukset ja myynnit päivitetään seuraavalla tavalla:

- **Oikaisun tila** -kenttä päivittyy **Oikaistuksi**.
- **Laskutuksen tila** -kenttä päivittyy **Peruutetuksi**.

Seuraavaksi todellisten arvojen taulukossa luodaan palautusmerkintöjä. Peruutusmerkintöjen luomista varten järjestelmä kopioi kenttien arvot alkuperäisistä todellisista arvoista. Ainoat arvot, joita ei kopioida, ovat määräarvot. Sen sijaan kyseiset arvot kumotaan. Kumottuja todellisia arvoja luodaan sekä **Kustannus**- että **Laskuttamaton myynti** -muotoisille todellisille arvoille. **Oikaisun tila** -kentän arvoksi käänteisissä nykyarvoissa asetetaan **Oikaisukelvoton** ja **Laskutuksen tila** -kentän arvoksi **Peruutettu**. Näiden muutosten vuoksi projektin kirjatut menot ja tulot eivät enää vastaa summia, joita nämä nykyarvot edustavat.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
