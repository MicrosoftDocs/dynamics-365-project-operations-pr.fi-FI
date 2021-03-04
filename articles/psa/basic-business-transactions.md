---
title: Liiketoimintatapahtumat
description: Tässä aiheessa on tietoja liiketoimintatapahtumista.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 3a8506effc453280177d74f94dcf9310e310c098
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149899"
---
# <a name="business-transactions"></a>Liiketoimintatapahtumat

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automationissa *liiketoimintatapahtuma* on abstrakti konsepti, jota ei edusta mikään entiteetti. Jotkut entiteettien yhteiset kentät ja prosessit kuitenkin käyttävät liiketoimintatapahtumien konseptia. Seuraavat entiteetit käyttävät tätä abstraktia konseptia:

- Tarjousrivin tiedot
- Sopimusrivin tiedot
- Arviorivit
- Kirjauskansion rivit
- Todelliset arvot

Näistä entiteeteistä Tarjousrivin tiedot, Sopimusrivin tiedot ja Arviorivit yhdistetään projektin elinkaaren arviointivaiheeseen. Entiteetit Arviorivit ja todelliset arvot yhdistetään projektin elinkaaren suoritusvaiheeseen.

PSA käsittelee näiden viiden entiteetin tietueita liiketoimintatapahtumina. Ainoana erona on, että arviointivaiheeseen yhdistettävien entiteettien tietueet katsotaan talousennusteiksi, kun taas suoritusvaiheeseen yhdistettävien entiteettien tietueet katsotaan taloudellisiksi tosiasioiksi, jotka ovat jo todelliset.

Lisätietoja on aiheissa [Arviot](estimates.md) ja [todelliset arvot.](actuals.md)

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konseptit, joita käytetään vain liiketoimintatapahtumissa
Seuraavia konsepteja käytetään vain liiketoimintatapahtumien konseptissa:

- Tapahtumatyyppi
- Tapahtumaluokka
- Tapahtuman alkuperä
- Tapahtuman yhteys

### <a name="transaction-type"></a>Tapahtumatyyppi

Tapahtumatyyppi edustaa projektiin kohdistuvan taloudellisen vaikutuksen ajoitusta ja kontekstia. Sitä edustaa asetusjoukko, jolla on PSA:ssa seuraavat tuetut arvot:
- Kustannus
- Projektisopimus
- Laskuttamaton myynti
- Laskutettu myynti
- Organisaatioiden välinen myynti
- Resursointiyksikön kustannus

### <a name="transaction-class"></a>Tapahtumaluokka

Tapahtumaluokka edustaa erilaisia kustannustyyppejä, joita projekteissa esiintyy. Sitä edustaa asetusjoukko, jolla on PSA:ssa seuraavat tuetut arvot:

- Time
- Kulut
- Materiaali
- Maksu
- Välitavoite
- Vero

Liiketoimintalogiikka käyttää arvoa **Välitavoite** yleensä kiinteähintaiseen laskutukseen PSA:ssa.

### <a name="transaction-origin"></a>Tapahtuman alkuperä

Tapahtuman alkuperä on entiteetti, joka tallentaa kunkin liiketoimintatapahtuman alkuperän. Kun projektin toteutus alkaa, jokainen liiketoimintatapahtuma tuottaa toisen liiketoimintatapahtuman, joka puolestaan luo toisen ja niin edelleen. Tapahtumien alkuperän entiteetti suunniteltiin tallentamaan tietoja kunkin tapahtuman alkuperästä, mikä helpottaa raportointia ja jäljitettävyyttä. 

### <a name="transaction-connection"></a>Tapahtuman yhteys

Tapahtuman yhteys on entiteetti, joka tallentaa kahden samankaltaisen liiketoimintatapahtuman välisen suhteen. Tällaisia ovat esimerkiksi kustannukset ja niihin liittyvät myynnin todelliset arvot tai tapahtumien palautukset, jotka perustuvat laskutustoimiin, kuten laskujen vahvistamiseen tai laskujen korjaamiseen.

Yhdessä entiteetit Tapahtuman alkuperä ja Tapahtuman yhteys auttavat liiketoimintatapahtumien välisten suhteiden ja tietyn liiketoimintatapahtuman luomiseen johtavien toimien seuraamisessa.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Esimerkki: Tapahtuman alkuperän ja Tapahtuman yhteyden vuorovaikutus

Seuraavassa esimerkissä esitellään aikamerkintöjen tyypillinen käsittely PSA-projektin elinkaaren aikana.

> ![Aikamerkintöjen käsitteleminen Project Service -elinkaaren aikana](media/basic-guide-17.png)
 
1. Aikamerkinnän lähettäminen johtaa kahden kirjauskansion rivin luomiseen: yksi kustannuksia ja toinen laskuttamatonta myyntiä varten.
2. Aikamerkinnän hyväksyminen taas johtaa kahden todellisen arvon luomiseen: yksi kustannuksia ja toinen laskuttamatonta myyntiä varten.
3. Kun käyttäjä luo projektilaskun, laskurivitapahtuma luodaan laskuttamattoman myynnin todellisen arvon tietojen perusteella. 
4. Kun lasku on vahvistettu, luodaan kaksi uutta todellista tapahtumaa: laskuttamattoman myynnin palautus ja laskutetun myynnin todellinen arvo.

Kumpikin näistä tapahtumista johtaa tietueiden luomiseen entiteeteissä Tapahtuman alkuperä ja Tapahtuman yhteys. Tämä auttaa näiden aikamerkinnöissä, kirjauskansion riveissä, todellisissa arvoissa ja laskutusrivin tiedoissa luotavien tietueiden välisten suhteiden seurannassa.

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

Seuraavassa taulukossa esitetään edeltävässä työnkulussa käytettävän Tapahtuman yhteys -entiteetin tietueet.

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