---
title: Sisäisen projektin todellisten arvojen vaikutus
description: Tässä aihe tietoja siitä, miten Microsoft Dynamics 365 Project Operationsin sisäisen projektin eri tapahtumat vaikuttavat Toteutunut-taulukkoon.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579762"
---
# <a name="actuals-impact-for-an-internal-project"></a>Sisäisen projektin todellisten arvojen vaikutus

_**Koskee:** Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita, Lite-käyttöönotto - kaupasta proformalaskutukseen_

Seuraavassa taulukossa on esitetty eri tapahtumatyyppien toteutuneet arvot, jotka on luotu eri tapahtumiin sisäisen projektin aktiviteettien yhteydessä.

| Tapahtuma | Kulujen todellinen arvo | Esimerkki: |
|---|---|---|
| Aika luodaan. | Ei käytettävissä | <p>Bob Kozack, Fabrikam US -organisaatioyksiköstä, jonka kustannus on 100 Yhdysvaltain dollaria (100 USD) tunnissa, työstää projektia, jonka nimi on "Arm Installation at Adatum". Tämä projekti on yhdistetty sopimusrivin kiinteähintaiseen laskutustapaan. Tässä on näyteaikamerkintä Bob Kozakilta:</p><p>Bob Kozack - 8 tuntia</p> |
| Aika lähetetään. | Ei käytettävissä | Ajan kirjaamista varten luodaan kustannuksen kirjauskansiorivi. Oletuskustannushinta syötetään kirjauskansioviennissä. |
| Ajan kirjaus on peruutetaan, ennen kuin se hyväksytään. | Ei käytettävissä | |
| Aika hyväksytään. | Todellinen kustannus luodaan. | <p>Uusi luotu toteutunut arvo:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD</li></ul> |
| Ajan hyväksyminen on peruutettu. | <p>Alkuperäisen toteutuneen kustannuksen oikaisun tilaksi päivittyy **Oikaistu**.</p><p>Toteutuneen kustannuksen peruutus luodaan, jonka oikaisun tila on **Oikaisukelvoton**.</p> | <p>Toteutunut arvo, joka päivitetään:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD, *Oikaistu*</li></ul><p>Uusi toteutunut arvo, joka on luotu edellisen taloudellisen vaikutuksen peruuttamiseksi:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, (8 tuntia), (800 USD), *Oikaisukelvoton*</li></ul> |
| Ajan kirjaus on peruutetaan hyväksynnän jälkeen. | <p>Alkuperäisen toteutuneen kustannuksen oikaisun tilaksi päivittyy **Oikaistu**.</p><p>Toteutuneen kustannuksen peruutus luodaan, jonka oikaisun tila on **Oikaisukelvoton**.</p> | <p>Toteutunut arvo, joka päivitetään:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD, *Oikaistu*</li></ul><p>Uusi toteutunut arvo, joka on luotu edellisen taloudellisen vaikutuksen peruuttamiseksi:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, (8 tuntia), (800 USD), *Oikaisukelvoton*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
