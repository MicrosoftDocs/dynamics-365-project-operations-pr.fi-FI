---
title: Miksi toteutuneen ajan kustannuksen oletushinta on nolla?
description: Tee vianmääritys ja selvitä, miksi toteutuneen ajan kustannuksen hinnan oletusarvo on 0.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: e1f81268c894e2ff5d607d8008876c84f7eafdf05f8b1f3212263a5dfa89b69d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996972"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Miksi toteutuneen ajan kustannuksen oletushinta on nolla?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nämä usein kysytyt kysymykset koskevat toteutuneita arvoja, joissa tapahtuman luokaksi on määritetty Aika ja tapahtumatyypiksi Kustannus. Seuraavien kolmen tarkistuksen avulla voit tehdä vianmäärityksen ja selvittää, miksi hinnan oletusarvo on 0 toteutuneen ajan kustannukselle.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Tarkistus 1: Määritä projektin kustannushinnasto

Etsi projekti toteutuneesta projektikentästä ja siirry sitten projektin sivulle. Valitse kentässä sopimusyksikön linkki. Tarkista Sopimusyksikkö-sivulla, onko sopimusyksiköllä hinnasto Kustannushinnastot-ruudukossa.

Jos hinnastoja on useita, olet eristänyt ongelman. Project Service tukee vain yhtä hinnastoa organisaatioyksikköä kohti. Poista tästä entiteetistä kaikki muut hinnastot paitsi organisaatioyksikön Kustannushinnastot-ruudukon yksi hinnasto.

Jos organisaatioyksikköön ei ole liitetty hinnastoja, merkitse organisaatioyksikön valuutta muistiin. Siirry Project Service -sovellukseen ja sitten Parametrit-kohtaan. Avaa Hinnastot-välilehti ja tarkista, onko siellä hinnastoja, joiden kontekstiksi on määritetty Kustannus ja valuutaksi organisaatioyksikön valuutta.
 
Jos ehtoja vastaavia hinnastoja ei ole, olet eristänyt ongelman. Varmista, että vähintään yhden hinnaston kontekstiksi on määritetty Kustannus ja valuutta on sama kuin organisaatioyksikön valuutta.

Jos ehtoja vastaavia hinnastoja on useita, jatka tämän asiakirjan lukemista ja tee lisätarkistuksia.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Tarkistus 2: Onko jokin yllä määritetyistä hinnastoista sallittu toteutuneen ajan kustannuksen määritettynä päivämääränä?

Project Service -sovelluksessa voidaan käyttää oletushintojen hinnastoa, jos hinnasto on käytössä toteutuneen ajan kustannuksen päivämääränä. Tarkista seuraavat kohdat ja varmista, ovatko yllä määritetyt hinnastot käytettävissä:

- Tarkista, että liitettyjen hinnastojen Yleinen-välilehden alku- ja loppupäivämäärät on määritetty. Jos yllä määritettyjä hinnastojen alku- ja loppupäivämääriä ei ole määritetty, olet eristänyt ongelman. 
- Ota toteutuneen ajan kustannuksen päivämääräkentän arvo muistiin ja tarkista, onko mikään hinnastoista käytössä kyseisenä päivänä. Esimerkiksi toteutuneen ajan kustannuksen päivämäärän tulisi olla hinnaston alku- ja loppupäivämäärän välillä. 
    - Jos toteutuneen ajan kustannuksen päivämäärä ei kuulu yhdenkään hinnaston päivämääräväliin, olet eristänyt ongelman. Muokkaa hinnaston alku- ja loppupäivämääriä varmistaaksesi, että hinnasto kattaa toteutuneen ajan kustannuksen päivämäärän. 
    - Jos toteutuneen ajan kustannuksen päivämäärä kuuluu usean hinnaston päivämääräväliin, olet eristänyt ongelman. Voit korjata ongelman muokkaamalla hinnastojen alku- ja loppupäivämääriä niin, että vain yksi hinnasto kattaa toteutuneen ajan kustannuksen päivämäärän. 
    - Jos toteutuneen ajan kustannuksen päivämäärän kattavia hinnastoja on vain yksi, siirry asiakirjassa seuraavaan tarkistukseen.
Kun olet tehnyt vaaditut korjaukset, voit luoda aikamerkinnän uudelleen ja hyväksyä sen. Tarkista, että toteutuneen ajan kustannuksella on sallittu hinta.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Tarkistus 3: Onko hinnastossa hinta toteutuneen ajan kustannuksen hinnoitteludimensioille?

Jos olet tarkistuksen 1 ja 2 suoritus onnistui, sinulla pitäisi olla nyt vain yksi hinnasto, joka käsittää toteutuneen ajan kustannuksen päivämäärän. Avaa tämä hinnasto ja siirry Roolin hinnat -välilehteen. Varmista, että toteutuneen ajan kustannuksen hinnoitteludimensioilla on rivi ruudukossa.

Jos toteutuneen ajan kustannuksen hinnoitteludimensioiden roolin hinnan ruudukossa ei ole riviä, olet eristänyt ongelman. Luo toteutuneen ajan kustannuksen hinnoitteludimensioiden Roolin hinnat -ruudukolle rivi. Kun olet tehnyt tämän, voit luoda aikamerkinnän uudelleen ja hyväksyä sen. Tarkista, että toteutuneen ajan kustannuksen hinta on sallittu.
 
Jos toteutuneen ajan kustannuksella ei ole sallittua hintaa näiden kolmen edellä mainitun tarkistuksen jälkeen ole sallittu, kirjaa tukipyyntö.





[!INCLUDE[footer-include](../includes/footer-banner.md)]