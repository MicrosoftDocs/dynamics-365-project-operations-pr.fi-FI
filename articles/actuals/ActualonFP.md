---
title: Toteutuneiden arvojen vaikutus kiinteähintaisessa aktiviteetissa
description: Tässä artikkelissa on tietoja siitä, miten eri tapahtumat vaikuttavat Toteutuneet-taulukkoon kiinteän hinnan aktiviteetin elinkaaren aikana Microsoft Dynamics 365 Project Operationsissa.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918124"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Toteutuneiden arvojen vaikutus kiinteähintaisessa aktiviteetissa

_**Koskee:** Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita, Lite-käyttöönotto - kaupasta proformalaskutukseen_

Seuraavassa taulukossa on esitetty eri tapahtumatyyppien toteutuneet arvot, jotka on luotu eri tapahtumiin kiinteän hinnan aktiviteetin yhteydessä.

| Tapahtuma | Kulujen todellinen arvo | Laskuttamattoman myynnin nykyarvo | Laskutettu toteutunut myynti | Esimerkki: |
|---|---|---|---|---|
| Aika luodaan. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | <p>Bob Kozack, Fabrikam US -organisaatioyksiköstä, jonka kustannus on 100 Yhdysvaltain dollaria (100 USD) tunnissa, työstää projektia, jonka nimi on "Arm Installation at Adatum". Tämä projekti on yhdistetty sopimusrivin kiinteähintaiseen laskutustapaan. Tässä on näyteaikamerkintä Bob Kozakilta:</p><p>Bob Kozack - 8 tuntia</p> |
| Aika lähetetään. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ajan kirjaamista varten luodaan kustannuksen kirjauskansiorivi. Oletuskustannushinta syötetään kirjauskansioviennissä. |
| Ajan kirjaus on peruutetaan, ennen kuin se hyväksytään. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | |
| Aika hyväksytään. | Todellinen kustannus luodaan. | Ei käytettävissä | Ei käytettävissä | <p>Uusi luotu toteutunut arvo:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD</li></ul> |
| Ajan hyväksyminen on peruutettu. | <p>Alkuperäisen toteutuneen kustannuksen oikaisun tilaksi päivittyy **Oikaistu**.</p><p>Toteutuneen kustannuksen peruutus luodaan, jonka oikaisun tila on **Oikaisukelvoton**.</p> | Ei käytettävissä | Ei käytettävissä | <p>Toteutunut arvo, joka päivitetään:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD, *Oikaistu*</li></ul><p>Uusi toteutunut arvo, joka on luotu edellisen taloudellisen vaikutuksen peruuttamiseksi:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, (8 tuntia), (800 USD), *Oikaisukelvoton*</li></ul> |
| Ajan kirjaus on peruutetaan hyväksynnän jälkeen. | <p>Alkuperäisen toteutuneen kustannuksen oikaisun tilaksi päivittyy **Oikaistu**.</p><p>Toteutuneen kustannuksen peruutus luodaan, jonka oikaisun tila on **Oikaisukelvoton**.</p> | Ei käytettävissä | Ei käytettävissä | <p>Toteutunut arvo, joka päivitetään:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD, *Oikaistu*</li></ul><p>Uusi toteutunut arvo, joka on luotu edellisen taloudellisen vaikutuksen peruuttamiseksi:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, (8 tuntia), (800 USD), *Oikaisukelvoton*</li></ul> |
| Palvelusopimus on vahvistettu. | <p>Vanhan toteutuneen kustannuksen oikaisun tilaksi päivittyy **Oikaistu**.</p><p>Luodaan toteutuneiden kustannusten peruutus, joiden oikaisun tila on **Oikaisukelvoton**.</p><p>Uudet toteutuneet kustannukset luodaan sen jälkeen, kun sopimussäännöt on uudelleenarvioitu.</p> | Ei käytettävissä | Ei käytettävissä | <p>Toteutunut arvo, joka päivitetään:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD, *Oikaistu*</li></ul><p>Uusi toteutunut arvo, joka on luotu edellisen taloudellisen vaikutuksen peruuttamiseksi:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, (8 tuntia), (800 USD), *Oikaisukelvoton*</li></ul><p>Uusi toteutunut arvo, joka on luotu uudelleen arvioidulle taloudelliselle vaikutukselle:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD</li></ul> |
| Lasku luodaan. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | |
| Laskulle vahvistetaan välitavoite. | Ei käytettävissä | Ei käytettävissä | Uusi välitavoitepohjainen laskutettu toteutunut myynti luodaan. | <p>Olemassa oleva toteutunut arvo, joka ei muutu:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD</li></ul><p>Uusi toteutunut arvo, joka on luotu laskutetun myynnin arvojen kirjausta varten:</p><ul><li>**Laskutettu myynti – toteutuneet:** Välitavoite, 5 000 USD</li></ul> |
| Lasku korjataan välitavoitteen hyvittämiseksi. | Ei käytettävissä | Ei käytettävissä | Luodaan laskutetun myynnin toteutuneen arvon peruutus. | <p>Olemassa oleva toteutunut arvo, joka ei muutu:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD</li></ul><p>Toteutunut arvo, joka päivitetään:</p><ul><li>**Laskutettu myynti – toteutuneet:** Välitavoite, 5 000 USD, *Oikaistu*</li></ul><p>Uusi toteutunut arvo, joka on luotu edellisen laskutetun myynnin arvojen peruuttamista varten:</p><ul><li>**Laskutettu myynti – toteutuneet:** Välitavoite, (5 000 USD), *Oikaisukelvoton*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
