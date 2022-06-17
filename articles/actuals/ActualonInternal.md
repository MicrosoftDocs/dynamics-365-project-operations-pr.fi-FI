---
title: Sisäisen projektin todellisten arvojen vaikutus
description: Tässä artikkelissa on tietoja siitä, miten Microsoft Dynamics 365 Project Operationsin sisäisen projektin eri tapahtumat vaikuttavat Toteutunut-taulukkoon.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921344"
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
