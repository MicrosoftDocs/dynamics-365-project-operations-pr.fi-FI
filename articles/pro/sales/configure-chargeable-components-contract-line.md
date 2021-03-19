---
title: Projektipohjaisen sopimusrivin veloitettavien komponenttien määrittäminen – lite
description: Tässä ohjeaiheessa on tietoja laskutettavan osan lisäämisestä projektitoimintojen sopimusriveille.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf3f2a28fc992d6444b35d6ffa0c3f6cadcf16ea
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273914"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Projektipohjaisen sopimusrivin veloitettavien komponenttien määrittäminen – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Projektipohjaiseen sopimusriviin on *sisällytetty* komponentteja ja *laskutettavia* osia.

Sisältyvät komponentit ovat komponentteja, joihin liittyy:

  - Laskutustapa ja asiakasjako
  - Ei-ylitettävät rajoitukset 
  - Projektipohjaisella sopimusrivillä määritetyt laskun toistumisasetukset

Sisällytettyjen komponenttien alijoukko voidaan merkitä laskutettaviksi **laskutustyyppi**-kentän avulla. **Laskutustyyppi**-kenttä on asetusjoukko, joka sallii seuraavat arvot sopimusrivin kontekstissa:

  - Veloitettava
  - Ei veloitettava

Laskutettavat komponentit voidaan määrittää tehtäville, rooleille ja tapahtumaluokille.

Maksukyky määritetään projektisopimusrivin tehtäville, ja se koskee kaikkia riviin sisältyviä tapahtumaluokkia. Jos sopimusrivin **Sisällytä tehtävät** -kenttä on tyhjä tai sen asetus on **Koko projekti**, **Veloitettavat tehtävät** -välilehti ei ole käytettävissä.

Projektisopimusrivin rooleihin määritetty maksuvalmius koskee vain **ajan** tapahtumaluokkaa. Jos sopimusrivin **Sisällytä aika** -kentän sen asetus on **Ei**, **veloitettavat roolit** -välilehti ei ole käytettävissä.

Projektisopimusrivin tapahtumakategorioihin määritetty maksuvalmius koskee vain **Kulu** tapahtumaluokkaa. Jos **Sisällytä kulut** -kentän sen asetus on **Ei**, **Veloitettavat kategoriat** -välilehti ei ole käytettävissä.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Projektitehtävän päivittäminen laskutettavana tai ei-laskutettavana

Projektitehtävä voi olla laskutettava tai ei-laskutettava tietyllä sopimusrivillä, joten seuraavat asetukset ovat mahdollisia:

Jos projektiin perustuva sopimusrivi sisältää **Aikaa** ja tietyn tehtävän, **T1** liitetään siihen laskutettavana. Jos on olemassa toinen sopimusrivi, joka sisältää **Kulun**, voit liittää T1-tehtävän sopimusriviin ei-laskutettavana. Tuloksena on se, että kaikki tehtävään kirjatut ajat ovat veloitettavissa ja kaikki kulut eivät ole laskutettavia.

Tehtävän laskutustyyppi voidaan määrittää sopimusrivin **Veloitettavat tehtävät** -välilehdessä päivittämällä **Laskutustyyppi**-kenttä sopimusrivin tehtävien aliruudukossa. Vaihtoehtoisesti **Laskutustyyppi**-kenttä voidaan päivittää sen projektin tehtävän laskutusasetusten aliruudukossa, joka näyttää tehtävään liitetyt sopimusrivit.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Roolin päivittäminen laskutettavana tai ei-laskutettavana

Tietyn sopimusrivin rooli voi olla laskutettava tai ei-laskutettava.

Roolin laskutustyyppi voidaan määrittää sopimusrivin **laskutettavat roolit** -välilehdessä. Se tehdään päivittämällä **Laskutustyyppi**-kenttä **Veloitettavat roolit** -aliruudukossa.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Tapahtumaluokan päivittäminen laskutettavana tai ei-laskutettavana

Tietyn sopimusrivin tapahtumaluokka voi olla laskutettava tai ei-laskutettava.

Tapahtuman laskutustyyppi voidaan määrittää projektipohjaisen sopimusrivin **laskutettavat luokat** -välilehdessä. Se tehdään päivittämällä **Laskutustyyppi**-kenttä **Veloitettavat luokat** -aliruudukossa.

### <a name="resolve-chargeability"></a>Selvitä verosaatavan syntyminen

Arviota tai todellista luontiaikaa voidaan pitää veloitettavissa vain, jos sopimus riville on lisätty **Aika** ja jos **Tehtävä** ja **Rooli** on määritetty laskutettaviksi sopimusrivillä.

Arviota tai todellista kulua voidaan pitää veloitettavissa vain, jos sopimus riville on lisätty **Kulu** ja jos **Tehtävä** ja **Tapahtuma** on määritetty laskutettaviksi sopimusrivillä.


| Sisältää ajan | Sisältää kulun | Sisältää tehtävät | Rooli           | Luokka       | Tehtävä                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Kyllä           | Kyllä              | Koko projekti | Veloitettava     | Veloitettava     | Laskutus toteutuneesta ajasta: **Laskutettava** </br> Laskutustyyppi tosiasiallisista kustannuksista: **Laskutettava**           |
| Kyllä           | Kyllä              | Valitut tehtävät | Veloitettava     | Veloitettava     | Laskutus toteutuneesta ajasta: **Laskutettava** </br> Laskutustyyppi tosiasiallisista kustannuksista: **Laskutettava**           |
| Kyllä           | Kyllä              | Valitut tehtävät | Ei veloitettava | Veloitettava     | Laskutus toteutuneesta ajasta: **Ei veloitettava** </br> Laskutustyyppi tosiasiallisista kustannuksista: **Laskutettava**       |
| Kyllä           | Kyllä              | Valitut tehtävät | Veloitettava     | Veloitettava     | Laskutus toteutuneesta ajasta: **Ei veloitettava** </br> Laskutustyyppi tosiasiallisista kustannuksista:   **Ei veloitettava** |
| Kyllä           | Kyllä              | Valitut tehtävät | Ei veloitettava | Veloitettava     | Laskutus toteutuneesta ajasta: **Ei veloitettava** </br> Laskutustyyppi tosiasiallisista kustannuksista:   **Ei veloitettava** |
| Kyllä           | Kyllä              | Valitut tehtävät | Ei veloitettava | Ei veloitettava | Laskutus toteutuneesta ajasta: **Ei veloitettava** </br> Laskutustyyppi tosiasiallisista kustannuksista:   **Ei veloitettava** |
| No            | Kyllä              | Koko projekti | Ei voida määrittää   | Veloitettava     | Laskutus toteutuneesta ajasta: **Ei saatavilla**</br>Laskutustyyppi tosiasiallisista kustannuksista: **Laskutettava**          |
| No            | Kyllä              | Koko projekti | Ei voida määrittää   | Ei veloitettava | Laskutus toteutuneesta ajasta: **Ei saatavilla**</br> Laskutustyyppi tosiasiallisista kustannuksista: **Ei veloitettava**     |
| Kyllä           | No               | Koko projekti | Veloitettava     | Ei voida määrittää   | Laskutus toteutuneesta ajasta: **Laskutettava** </br> Laskutustyyppi tosiasiallisista kustannuksista: **Ei saatavilla**        |
| Kyllä           | No               | Koko projekti | Ei veloitettava | Ei voida määrittää   | Laskutus toteutuneesta ajasta: **Ei veloitettava** </br>Laskutustyyppi tosiasiallisista kustannuksista: **Ei   saatavilla**   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]