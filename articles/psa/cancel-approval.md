---
title: Aiemmin hyväksyttyjen aika- ja kulumerkintöjen peruminen
description: Tässä aiheessa on tietoja aiemmin hyväksytyn projektin aika- ja kulutapahtuman perumisesta.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 84fc057599dd98162320d6104ed4a7612e894ecb
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123329"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Aiemmin hyväksyttyjen aika- tai kulumerkintöjen peruminen

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automationin viimeisimmässä versiossa hyväksyjät voivat perua aika- tai kulumerkintöjä, jotka he ovat aiemmin hyväksyneet.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Aiemmin hyväksytyn aika- tai kulumerkinnän peruminen

Seuraa näitä vaiheita peruaksesi aiemmin hyväksymäsi aika- tai kulumerkinnän.

1. Siirry kohtaan **Projektit** \> **Omat työt** \> **Hyväksynnät**.
2. Vaihda **Hyväksynnät** -luettelosivulla näkymäksi **Omat aikaisemmat hyväksynnät**. Näkyviin tulee luettelo aiemmin hyväksymistäsi aika- ja kulumerkinnöistä.
3. Valitse vähintään yksi merkintä ja valitse sitten **Peru hyväksyntä**. Näyttöön tulee varoitus.
4. Peru hyväksyntä valitsemalla **OK**.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Aika- tai kulumerkinnän perumisen vaikutukset

Kun hyväksyntä perutaan, siihen liittyy sekä toiminnallisia vaikutuksia että taloudellisia vaikutuksia.

### <a name="operational-impact"></a>Toiminnallinen vaikutus

Kun hyväksyntä perutaan, tietueen tilaksi palautuu toiminnallisella puolella **Luonnos** eikä hyväksyntä enää näy **Omat aikaisemmat hyväksynnät** -näkymässä. Sen sijaan peruttu hyväksyntä tulee näkyviin joko näkymässä **Aikamerkinnät hyväksyttäväksi** tai näkymässä **Kulumerkinnät hyväksyttäväksi** riippuen siitä, oliko kyseessä aika- vai kulumerkintä. Lisäksi siihen liittyvän aika- tai kulumerkinnän tilaksi vaihtuu **Lähetetty**, jotta liittyvä merkintä on yhdenmukainen niiden hyväksyntöjen kanssa, joiden tila on **Luonnos**.

Hyväksyjänä voit muokata joitakin hyväksynnän kenttiä, joiden tilana on **Luonnos**. Näitä kenttiä ovat esimerkiksi **Laskutustyyppi** ja **Aikamerkintöjen laskutettavat tunnit**. Kun olet tehnyt muutoksia, voit hyväksyä tietueen uudelleen. Voit myös hylätä merkinnän. Jos hylkäät aikamerkinnän, sen tilaksi vaihtuu **Palautettu**. Jos hylkäät kulumerkinnän, sen tilaksi vaihtuu **Hylätty**. Toiminnalliselta kannalta palautetut ja hylätyt merkinnät toimivat samalla tavalla kuin merkintä, jonka tilana on **Luonnos**. Projektiryhmän jäsen voi joko tehdä tarvittavat muutokset merkintään ja lähettää sen uudelleen hyväksyttäväksi tai poistaa merkinnän kokonaan.

### <a name="financial-impact"></a>Taloudellinen vaikutus

Hyväksynnän perumisella on myös taloudellisia vaikutuksia projektiin. Aluksi vastaavat toteutuneet kustannukset ja myynnit päivitetään seuraavalla tavalla:

- Oikaisun tilaksi määritetään **Oikaistu**.
- Laskutustilaksi määritetään **Peruttu**.

Seuraavaksi todellisten arvojen taulukossa luodaan palautusmerkintöjä. Peruutusmerkintöjen luomista varten järjestelmä kopioi kenttien arvot alkuperäisistä todellisista arvoista. Ainoat arvot, joita ei kopioida, ovat määräarvot. Sen sijaan kyseiset arvot kumotaan. Kumottuja todellisia arvoja luodaan sekä **Kustannus**- että **Laskuttamaton myynti** -muotoisille todellisille arvoille. **Oikaisun tila** -kentän arvoksi kumotuissa todellisissa arvoissa asetetaan **Oikaisukelvoton** ja laskutuksen tilaksi määritetään **Peruttu**.

Kun nämä muutokset on tehty, projektissa kulutetuksi kirjattu summa ja tulot eivät enää vastaa summia, joita nämä todelliset arvot edustavat.
