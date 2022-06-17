---
title: Vaikutukset toteutuneisiin vuorovaikutuksen myynnin ennakkovaiheessa
description: Tässä artikkelissa on tietoja siitä, miten eri tapahtumat vaikuttavat Toteutuneet-taulukkoon Microsoft Dynamics 365 Project Operationsissa, kun vuorovaikutus on ennakkomyyntivaiheessa.
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
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922356"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Vaikutukset toteutuneisiin vuorovaikutuksen myynnin ennakkovaiheessa

_**Koskee:** Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita, Lite-käyttöönotto - kaupasta proformalaskutukseen_

Seuraavassa taulukossa on esitetty eri tapahtumatyyppien toteutuneet arvot, jotka on luotu eri tapahtumiin projektin aktiviteettien ennakkomyyntivaiheen yhteydessä.

| Tapahtuma | Kulujen todellinen arvo | Esimerkki: |
|---|---|---|
| Aika luodaan. | Ei käytettävissä | <p>Bob Kozack, Fabrikam US -organisaatioyksiköstä, jonka kustannus on 100 Yhdysvaltain dollaria (100 USD) tunnissa, työstää projektia, jonka nimi on "Arm Installation at Adatum". Tämä projekti on yhdistetty sopimusrivin kiinteähintaiseen laskutustapaan. Tässä on näyteaikamerkintä Bob Kozakilta:</p><p>Bob Kozack - 8 tuntia</p> |
| Aika lähetetään. | Ei käytettävissä | Ajan kirjaamista varten luodaan kustannuksen kirjauskansiorivi. Oletuskustannushinta syötetään kirjauskansioviennissä. |
| Ajan kirjaus on peruutetaan, ennen kuin se hyväksytään. | Ei käytettävissä | |
| Aika hyväksytään. | Todellinen kustannus luodaan. | <p>Uusi luotu toteutunut arvo:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD</li></ul> |
| Ajan hyväksyminen on peruutettu. | <p>Alkuperäisen toteutuneen kustannuksen oikaisun tilaksi päivittyy **Oikaistu**.</p><p>Toteutuneen kustannuksen peruutus luodaan, jonka oikaisun tila on **Oikaisukelvoton**.</p> | <p>Toteutunut arvo, joka päivitetään:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD, *Oikaistu*</li></ul><p>Uusi toteutunut arvo, joka on luotu edellisen taloudellisen vaikutuksen peruuttamiseksi:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, (8 tuntia), (800 USD), *Oikaisukelvoton*</li></ul> |
| Ajan kirjaus on peruutetaan hyväksynnän jälkeen. | <p>Alkuperäisen toteutuneen kustannuksen oikaisun tilaksi päivittyy **Oikaistu**.</p><p>Toteutuneen kustannuksen peruutus luodaan, jonka oikaisun tila on **Oikaisukelvoton**.</p> | <p>Toteutunut arvo, joka päivitetään:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD, *Oikaistu*</li></ul><p>Uusi toteutunut arvo, joka on luotu edellisen taloudellisen vaikutuksen peruuttamiseksi:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, (8 tuntia), (800 USD), *Oikaisukelvoton*</li></ul> |
| Tarjous on voitettu ja palvelusopimus luodaan. | <p>Vanhan toteutuneen kustannuksen oikaisun tilaksi päivittyy **Oikaistu**.</p><p>Luodaan toteutuneiden kustannusten peruutus, joiden oikaisun tila on **Oikaisukelvoton**.</p><p>Uudet toteutuneet kustannukset luodaan sen jälkeen, kun sopimussäännöt on uudelleenarvioitu.</p> | <p>Toteutunut arvo, joka päivitetään:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD, *Oikaistu*</li></ul><p>Uusi toteutunut arvo, joka on luotu edellisen taloudellisen vaikutuksen peruuttamiseksi:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, (8 tuntia), (800 USD), *Oikaisukelvoton*</li></ul><p>Uudet toteutuneet arvot, jotka luodaan uudelleenarvostettuun talousvaikutukseen, kun tarjous on voitettu ja sopimus luodaan:</p><ul><li>**Toteutunut kustannus:** Bob Kozack, 8 tuntia, 800 USD</li><li>**Laskuttamaton myynti – toteutuneet:** Bob Kozack, 8 tuntia, 1 600 USD</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
