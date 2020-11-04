---
title: Tarjousrivin laskutettavan osan määrittäminen
description: Tässä ohjeaiheessa on tietoja laskutettavan ja ei-laskutettavan komponentin määrittämisestä projektipohjaisella tarjousrivillä.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075469"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Tarjousrivin laskutettavan osan määrittäminen

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Projektipohjaiseen tarjousrivillä on *sisällytettyjen* osien ja *laskutettavien* osien käsitteet.

Sisällytettyjä osia voivat olla seuraavat:

  - Laskutustapa ja asiakasjako
  - Ei-ylitettävät rajoitukset 
  - Projektipohjaisella tarjousrivillä määritetyt laskun toistumisasetukset

Sisällytettyjen komponenttien alijoukko voidaan merkitä laskutettaviksi **laskutustyyppi** -kentän avulla. **Laskutustyyppi** -kenttä on asetusjoukko, joka sallii seuraavat arvot tarjousrivin kontekstissa:

  - Veloitettava
  - Ei veloitettava

Laskutettavat komponentit voidaan määrittää tehtäville, rooleille ja tapahtumaluokille.

Maksukyky määritetään tarjousrivin tehtäville, ja se koskee kaikkia siihen riviin sisältyviä tapahtumaluokkia. Jos sopimusrivin **Sisällytä tehtävät** -kentän asetus on **Koko projekti** tai se on jätetty tyhjäksi, **Veloitettavat tehtävät** -välilehti ei ole käytettävissä.

Laskutettavuus määritetään tarjousrivin rooleissa, ja se koskee vain **Ajan** tapahtumaluokkaa. Jos **Sisällytä aika** -kentän asetus on **Ei** projektitarjousrivillä, **Veloitettavat roolit** -välilehti ei ole käytettävissä.

Veloitettavuus määritetään tarjousrivin tapahtumaluokissa ja koskee vain **Kulu** -tapahtumaluokkaa. Jos **Sisällytä kulut** -kentän asetus on **Ei** projektitarjousrivillä, **Veloitettavat luokat** -välilehti ei ole käytettävissä.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Projektitehtävän päivittäminen laskutettavaksi tai ei-laskutettavaksi

Projektitehtävä voi olla laskutettava tai ei-laskutettava tietyn projektipohjaisen tarjousrivin yhteydessä, mikä mahdollistaa seuraavan asennuksen:

Jos projektiin perustuva tarjousrivi sisältää **Ajan** ja tehtävän **T1** , tehtävä liitetään tarjousriviin laskutettavana. Jos on olemassa toinen tarjousrivi, joka sisältää **Kulut** , voit liittää **T1** -tehtävän tarjousriviin ei-laskutettavana. Tuloksena on, että kaikki tehtävään kirjattu aika on laskutettavaa ja kaikki tehtävään kirjatut kulut ovat ei-laskutettavia.

Tehtävän laskutustyyppi voidaan määrittää projektipohjaisen tarjousrivin **Laskutettavat tehtävät** -välilehdessä päivittämällä **Laskutustyyppi** -kenttä **Tarjousrivin tehtävät** -aliruudukossa. Vaihtoehtoisesti voit päivittää projektitehtävän laskutustyypin projektin tehtävälaskutusasetuksen aliruudukon **Laskutustyyppi** -kentässä, joka näyttää tehtävään liittyvät tarjousrivit.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Roolin päivittäminen laskutettavaksi tai ei-laskutettavaksi

Rooli voi olla laskutettava tai ei-laskutettava tietyn projektipohjaisen tarjousrivin kontekstissa.

Roolin laskutustyyppi voidaan määrittää projektipohjaisen tarjousrivin **Laskutettavat roolit** -välilehdessä päivittämällä **Laskutustyyppi** -kenttä **Laskutettavat roolit** -aliruudukossa.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Päivitä tapahtumaluokka laskutettavaksi tai ei-laskutettavaksi

Tietyn tarjousrivin tapahtumaluokka voi olla laskutettava tai ei-laskutettava.

Tapahtuman laskutustyyppi voidaan määrittää projektipohjaisen tarjousrivin **Laskutettavat luokat** -välilehdessä päivittämällä **Laskutustyyppi** -kenttä **Laskutettavat luokat** -aliruudukossa.

### <a name="resolve-chargeability"></a>Selvitä verosaatavan syntyminen
Arviota tai todellista luontiaikaa voidaan pitää veloitettavissa vain, jos tarjousriville on lisätty **Aika** ja jos **Tehtävä** ja **Rooli** on määritetty laskutettaviksi tarjousrivillä.

Arviota tai todellista kulua voidaan pitää veloitettavissa vain, jos tarjousriville on lisätty **Kulu** ja jos **Tehtävä** ja **Tapahtumaluokka** on määritetty laskutettaviksi tarjousrivillä.

| Sisältää ajan | Sisältää kulun | Sisällytettävät tehtävät | Rooli | Luokka | Tehtävä | Laskutus |
| --- | --- | --- | --- | --- | --- | --- |
| Kyllä | Kyllä | Koko projekti | Veloitettava | Veloitettava | Ei voida määrittää | Laskutus toteutuneesta ajasta: Laskutettava </br>Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava |
| Kyllä | Kyllä | Vain valitut tehtävät | Veloitettava | Veloitettava | Veloitettava | Laskutus toteutuneesta ajasta: Laskutettava</br>Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava |
| Kyllä | Kyllä | Vain valitut tehtävät | Ei veloitettava | Veloitettava | Veloitettava | Laskutus toteutuneesta ajasta: Ei veloitettava</br>Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava |
| Kyllä | Kyllä | Vain valitut tehtävät | Veloitettava | Veloitettava | Ei veloitettava | Laskutus toteutuneesta ajasta: Ei veloitettava</br> Laskutustyyppi tosiasiallisista kustannuksista: Ei veloitettava |
| Kyllä | Kyllä | Vain valitut tehtävät | Ei veloitettava | Veloitettava | Ei veloitettava | Laskutus toteutuneesta ajasta: Ei veloitettava</br> Laskutustyyppi tosiasiallisista kustannuksista: Ei veloitettava |
| Kyllä | Kyllä | Vain valitut tehtävät | Ei veloitettava | Ei veloitettava | Veloitettava | Laskutus toteutuneesta ajasta: Ei veloitettava</br> Laskutustyyppi tosiasiallisista kustannuksista: Ei veloitettava |
| No | Kyllä | Koko projekti | Ei voida määrittää | Veloitettava | Ei voida määrittää | Laskutus toteutuneesta ajasta: Ei saatavilla </br>Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava |
| No | Kyllä | Koko projekti | Ei voida määrittää | Ei veloitettava | Ei voida määrittää | Laskutus toteutuneesta ajasta: Ei saatavilla </br>Laskutustyyppi tosiasiallisista kustannuksista: Ei veloitettava |
| Kyllä | No | Koko projekti | Veloitettava | Ei voida määrittää | Ei voida määrittää | Laskutus toteutuneesta ajasta: Laskutettava</br>Laskutustyyppi tosiasiallisista kustannuksista: Ei saatavilla |
| Kyllä | No | Koko projekti | Ei veloitettava | Ei voida määrittää | Ei voida määrittää | Laskutus toteutuneesta ajasta: Ei veloitettava </br>Laskutustyyppi tosiasiallisista kustannuksista: Ei saatavilla |
