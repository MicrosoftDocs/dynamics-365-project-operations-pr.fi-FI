---
title: Todellisten arvojen linkittäminen alkuperäisiin tietueisiin
description: Tässä aiheessa kerrotaaman, miten toteutuneet arvot linkitetään alkuperäisiin tietueisiin, kuten aikamerkintä-, kulumerkintä- ja materiaalinkäyttölokeihin.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5a70d2c2b3f98028b4e4998ed25ab73a275c66e4b8137eb573b943658a1a41e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991752"
---
# <a name="link-actuals-to-original-records"></a>Todellisten arvojen linkittäminen alkuperäisiin tietueisiin

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_


Dynamics 365 Project Operationsissa *liiketoimintatapahtuma* on abstrakti käsite, jota ei edusta mikään entiteetti. Jotkut entiteettien yhteiset kentät ja prosessit kuitenkin käyttävät liiketoimintatapahtumien konseptia. Seuraavat entiteetit käyttävät tätä käsitettä:

- Tarjousrivin tiedot
- Sopimusrivin tiedot
- Arviorivit
- Kirjauskansion rivit
- Todelliset arvot

Näistä entiteeteistä **Tarjousrivin tiedot**, **Sopimusrivin tiedot** ja **Arviorivit** yhdistetään projektin elinkaaren arviovaiheeseen. **Kirjauskansiorivit** ja **Todellisten arvojen entiteetit** yhdistetään projektin elinkaaren suoritusvaiheeseen.

Project Operations tunnistaa tietueet näissä viidessä entiteetissä liiketoimintatapahtumiksi. Ainoana erona on, että arviovaiheeseen yhdistettävien entiteettien tietueet katsotaan talousennusteiksi, kun taas suoritusvaiheeseen yhdistettävien entiteettien tietueet katsotaan taloudellisiksi tosiasioiksi, jotka ovat jo tapahtuneet.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konseptit, joita käytetään vain liiketoimintatapahtumissa
Seuraavia konsepteja käytetään vain liiketoimintatapahtumien konseptissa:

- Tapahtumatyyppi
- Tapahtumaluokka
- Tapahtuman alkuperä
- Tapahtuman yhteys

### <a name="transaction-type"></a>Tapahtumatyyppi

Tapahtumatyyppi edustaa projektiin kohdistuvan taloudellisen vaikutuksen ajoitusta ja kontekstia. Tätä edustaa asetusjoukko, jolla on Project Operationsissa seuraavat tuetut arvot:

  - Kustannus
  - Projektisopimus
  - Laskuttamaton myynti
  - Laskutettu myynti
  - Organisaatioiden välinen myynti
  - Resursointiyksikön kustannus

### <a name="transaction-class"></a>Tapahtumaluokka

Tapahtumaluokka edustaa erilaisia kustannustyyppejä, joita projekteissa esiintyy. Tätä edustaa asetusjoukko, jolla on Project Operationsissa seuraavat tuetut arvot:

  - Aika
  - Kulut
  - Materiaali
  - Maksu
  - Välitavoite
  - Vero

Liiketoimintalogiikka käyttää tyypillisesti arvoa **Välitavoite** kiinteähintaiseen laskutukseen Project Operationsissa.

### <a name="transaction-origin"></a>Tapahtuman alkuperä

**Tapahtuman alkuperä** on entiteetti, joka tallentaa kunkin liiketoimintatapahtuman alkuperän. Projektin aikana jokainen liiketoimintatapahtuma aiheuttaa toisen liiketoimintatapahtuman, joka puolestaan luo toisen liiketoimintatapahtuman. Tapahtumien alkuperän entiteetti on suunniteltu siten, että se tallentaa tietoja kunkin tapahtuman alkuperästä, mikä helpottaa raportointia ja jäljittämistä. 

### <a name="transaction-connection"></a>Tapahtuman yhteys

**Tapahtuman yhteys** on entiteetti, joka tallentaa kahden samankaltaisen liiketoimintatapahtuman välisen suhteen. Tällaisia ovat esimerkiksi kustannukset ja niihin liittyvät myynnin todelliset arvot tai tapahtumien palautukset, jotka perustuvat laskutustoimiin, kuten laskujen vahvistamiseen tai laskujen korjaamiseen.

Yhdessä **Tapahtuman alkuperä** ja **Tapahtuman yhteys** auttavat liiketoimintatapahtumien välisten suhteiden ja tiettyyn liiketoimintatapahtumaan johtavien toimien seuraamisessa.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Esimerkki: Tapahtuman alkuperän ja Tapahtuman yhteyden vuorovaikutus

Seuraavassa esimerkissä esitellään aikamerkintöjen tyypillinen käsittely Project Operationsissa projektin elinkaaren aikana.

> ![Aikamerkintöjen käsitteleminen Project Service -elinkaaren aikana.](media/basic-guide-17.png)
 
1. Aikamerkinnän lähettäminen luo kaksi kirjauskansion riviä: yhden kustannuksia ja toisen laskuttamatonta myyntiä varten.
2. Aikamerkinnän hyväksyminen luo kaksi todellista arvoa: yhden todellisen arvon kustannuksia ja toisen todellisen arvon laskuttamatonta myyntiä varten.
3. Kun uusi projektilasku luodaan, laskurivitapahtuma luodaan laskuttamattoman myynnin todellisen arvon tietojen perusteella. 
4. Kun lasku vahvistetaan, luodaan kaksi uutta todellista arvoa: laskuttamattoman myynnin palautuksen todellinen arvo ja laskutetun myynnin todellinen arvo.

Kukin näistä tapahtumista luo tietueen **Tapahtumien alkuperä** - ja **Tapahtuman yhteys** -entiteetteihin. Näiden uusien tietueiden avulla voidaan rakentaa suhdehistoria tietueiden välille, joita luodaan aikamerkinnöissä, kirjauskansion riveillä, todellisissa arvoissa ja laskurivin tiedoissa.

Seuraavassa taulukossa esitetään työnkulussa käytettävän **Tapahtuman alkuperä** -entiteetin tietueet.

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

Seuraavassa taulukossa esitetään työnkulussa käytettävän **Tapahtuman yhteys** -entiteetin tietueet.

| Tapahtuma                          | Tapahtuma 1                 | Tapahtuman 1 rooli | Tapahtuman 1 tyyppi           | Tapahtuma 2                | Tapahtuman 2 rooli | Tapahtuman 2 tyyppi |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Aikamerkinnän lähetys          | Kirjauskansion rivin (myynti) GUID     | Laskuttamaton myynti     | msdyn_journalline            | Kirjauskansion rivin (kustannus) GUID     | Kustannus               | msdyn_journalline  |
| Ajan hyväksyminen                  | Uusien laskuttamattoman myynnin todellisen arvon GUID  | Laskuttamaton myynti     | msdyn_actual                 | Kustannuksen todellisen arvon (kustannus) GUID       | Kustannus               | msdyn_actual       |
| Laskun luonti               | Laskurivin tietojen GUID      | Laskutettu myynti       | msdyn_invoicelinetransaction | Uuden laskuttamattoman myynnin todellisen arvon GUID   | Laskuttamaton myynti     | msdyn_actual       |
| Laskun vahvistaminen           | Palauttavan todellisen arvon GUID         | Palauttava          | msdyn_actual                 | Alkuperäisen laskuttamattoman myynnin GUID | Alkuperäinen           | msdyn_actual       |
| Laskutetun myynnin GUID              | Laskutettu myynti                  | msdyn_actual       | Uuden laskuttamattoman myynnin todellisen arvon GUID   | Laskuttamaton myynti               | msdyn_actual       |                    |
| Laskuluonnoksen korjaus       | Laskurivin tapahtuman GUID | Korvaava          | msdyn_invoicelinetransaction | Laskutetun myynnin GUID            | Alkuperäinen           | msdyn_actual       |
| Laskun korjauksen vahvistaminen     | Laskutetun myynnin palautuksen GUID    | Palauttava          | msdyn_actual                 | Laskutetun myynnin GUID            | Alkuperäinen           | msdyn_actual       |
| Uuden laskuttamattoman myynnin todellisen arvon GUID | Korvaava                     | msdyn_actual       | Laskutetun myynnin GUID            | Alkuperäinen                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
