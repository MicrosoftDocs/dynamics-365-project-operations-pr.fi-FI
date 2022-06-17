---
title: Tapahtumien alkuperä – todellisten arvojen linkittäminen lähteeseen
description: Tässä artikkelissa käsitellään sitä, miten tapahtumien alkuperän käsitettä käytetään todellisten tietojen linkittämiseen alkuperäisiin lähdetietueisiin, kuten aikamerkintöihin, kulukirjauksiin tai materiaalin käyttölokeihin.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921298"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Tapahtumien alkuperä – todellisten arvojen linkittäminen lähteeseen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Tapahtumien alkuperätietueet luodaan siten, että ne linkittävät toteutuneet arvot lähteeseen, kuten aikakirjauksiin, kulumerkintöihin, materiaalin käyttölokeihin ja projektilaskuihin.

Seuraavassa esimerkissä esitellään aikamerkintöjen tyypillinen käsittely Project Operationsissa projektin elinkaaren aikana.

> ![Aikamerkintöjen käsittely Project Operationsissa.](media/basic-guide-17.png)
 
1. Aikamerkinnän lähettäminen johtaa kahden kirjauskansion rivin luomiseen: yksi kustannuksia ja toinen laskuttamatonta myyntiä varten.
2. Aikamerkinnän hyväksyminen taas johtaa kahden todellisen arvon luomiseen: yksi kustannuksia ja toinen laskuttamatonta myyntiä varten.
3. Kun käyttäjä luo projektilaskun, laskurivitapahtuma luodaan laskuttamattoman myynnin todellisen arvon tietojen perusteella.
4. Kun lasku on vahvistettu, luodaan kaksi uutta todellista tapahtumaa: laskuttamattoman myynnin palautus ja laskutetun myynnin todellinen arvo.

Kukin tämän käsittelytyönkulun tapahtumista käynnistää tietueiden luomisen entiteeteissä Tapahtuman alkuperä. Tämä auttaa näiden aikamerkinnöissä, kirjauskansion riveissä, todellisissa arvoissa ja laskutusrivin tiedoissa luotavien tietueiden välisten suhteiden seurannassa.

Seuraavassa taulukossa esitetään edeltävässä työnkulussa käytettävän Tapahtuman alkuperä -entiteetin tietueet.

| Tapahtuma                        | Alkuperä                   | Alkuperän tyyppi                       | Tapahtuma                       | Tapahtumatyyppi         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Aikamerkinnän lähetys        | Aikamerkintätietueen GUID   | Aikamerkintä                        | Kirjauskansion rivin tietueen GUID (kustannus)   | Kirjauskansion rivi             |
| Aikamerkintätietueen GUID       | Aikamerkintä               | Kirjauskansion rivin tietueen GUID (myynti)  | Kirjauskansion rivi                      |                          |
| Ajan hyväksyminen                | Kirjauskansion rivin tietueen GUID | Kirjauskansion rivi                      | Laskuttamattoman myynnin tietueen GUID        | Todellinen                   |
| Aikamerkintätietueen GUID       | Aikamerkintä               | Laskuttamattoman myynnin tietueen GUID        | Todellinen                            |                          |
| Kirjauskansion rivin tietueen GUID     | Kirjauskansion rivi             | Kustannuksen todellisen arvon tietueen GUID           | Todellinen                            |                          |
| Aikamerkintätietueen GUID       | Aikamerkintä               | Kustannuksen todellisen arvon tietueen GUID           | Todellinen                            |                          |
| Laskun luonti             | Aikamerkintätietueen GUID   | Aikamerkintä                        | Laskurivin tapahtuman GUID     | Laskurivin tapahtuma |
| Kirjauskansion rivin tietueen GUID     | Kirjauskansion rivi             | Laskurivin tapahtuman GUID     | Laskurivin tapahtuma          |                          |
| Laskun vahvistaminen         | Laskurivin GUID        | Laskurivi                      | Laskutetun myynnin tietueen GUID          | Todellinen                   |
| Laskun GUID                 | Lasku                  | Laskutetun myynnin tietueen GUID          | Todellinen                            |                          |
| Laskurivin tietojen GUID     | Laskurivin tiedot      | Laskutetun myynnin tietueen GUID          | Todellinen                            |                          |
| Aikamerkintätietueen GUID       | Aikamerkintä               | Laskutetun myynnin tietueen GUID          | Todellinen                            |                          |
| Kirjauskansion rivin tietueen GUID     | Kirjauskansion rivi             | Laskutetun myynnin tietueen GUID          | Todellinen                            |                          |
| Aikamerkintätietueen GUID       | Aikamerkintä               | Laskuttamattoman myynnin palautuksen GUID      | Todellinen                            |                          |
| Kirjauskansion rivin tietueen GUID     | Kirjauskansion rivi             | Laskuttamattoman myynnin palautuksen GUID      | Todellinen                            |                          |
| Laskuluonnoksen korjaus     | Vanhan ILD:n GUID             | Laskurivin tapahtuma          | Korjaavan ILD:n GUID               | Laskurivin tapahtuma |
| Vanhan IL:n GUID                  | Laskurivi             | Korjaavan ILD:n GUID               | Laskurivin tapahtuma          |                          |
| Vanhan laskun GUID             | Lasku                  | Korjaavan ILD:n GUID               | Laskurivin tapahtuma          |                          |
| Aikamerkintätietueen GUID       | Aikamerkintä               | Korjaavan ILD:n GUID               | Laskurivin tapahtuma          |                          |
| Kirjauskansion rivin tietueen GUID     | Kirjauskansion rivi             | Korjaavan ILD:n GUID               | Laskurivin tapahtuma          |                          |
| Vahvistettu laskun korjaus | Vanhan ILD:n GUID             | Laskurivin tapahtuma          | Palautetun laskutetun myynnin todellisen arvon GUID | Todellinen                   |
| Vanhan IL:n GUID                  | Laskurivi             | Palautetun laskutetun myynnin todellisen arvon GUID | Todellinen                            |                          |
| Vanhan laskun GUID             | Lasku                  | Palautetun laskutetun myynnin todellisen arvon GUID | Todellinen                            |                          |
| Aikamerkintätietueen GUID       | Aikamerkintä               | Palautetun laskutetun myynnin todellisen arvon GUID | Todellinen                            |                          |
| Kirjauskansion rivin tietueen GUID     | Kirjauskansion rivi             | Palautetun laskutetun myynnin todellisen arvon GUID | Todellinen                            |                          |
| Vanhan ILD:n GUID                 | Laskurivin tapahtuma | Uuden laskuttamattoman myynnin todellisen arvon GUID    | Todellinen                            |                          |
| Vanhan IL:n GUID                  | Laskurivi             | Uuden laskuttamattoman myynnin todellisen arvon GUID    | Todellinen                            |                          |
| Vanhan laskun GUID             | Lasku                  | Uuden laskuttamattoman myynnin todellisen arvon GUID    | Todellinen                            |                          |
| Aikamerkintätietueen GUID       | Aikamerkintä               | Uuden laskuttamattoman myynnin todellisen arvon GUID    | Todellinen                            |                          |
| Kirjauskansion rivin tietueen GUID     | Kirjauskansion rivi             | Uuden laskuttamattoman myynnin todellisen arvon GUID    | Todellinen                            |                          |
| Korjaavan ILD:n GUID          | Laskurivin tapahtuma | Uuden laskuttamattoman myynnin todellisen arvon GUID    | Todellinen                            |                          |
| Korjaavan IL:n GUID           | Laskurivi             | Uuden laskuttamattoman myynnin todellisen arvon GUID    | Todellinen                            |                          |
| Korjauslaskun GUID      | Lasku                  | Uuden laskuttamattoman myynnin todellisen arvon GUID    | Todellinen                            |                          |


Seuraavassa kuvassa on esitetty toteutuneiden arvojen ja niiden lähteiden välille luodut linkit eri tapahtumille käyttämällä Project Operationsin aikamerkintöjen esimerkkiä.

> ![Toteutuneiden tietojen linkittäminen lähdetietueisiin Project Operationsissa.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
