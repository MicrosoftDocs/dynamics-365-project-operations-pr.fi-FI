---
title: Miksi toteutuneen ajan myynnin oletushinta on nolla?
description: Tee vianmääritys ja selvitä, miksi toteutuneen ajan myynnin hinnan oletusarvo on 0.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 5f72e0db94392a35fee9fdcf2c4adb8a08feef13
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146209"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Miksi toteutuneen ajan myynnin oletushinta on nolla?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nämä usein kysytyt kysymykset koskevat toteutuneita arvoja, joissa tapahtuman luokaksi on määritetty Aika ja tapahtumatyypiksi Laskuttamaton myynti. Seuraavien kolmen tarkistuksen avulla voit tehdä vianmäärityksen ja selvittää, miksi hinnan (laskun arvon) oletusarvo on 0 toteutuneen ajan myynnille.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Tarkistus 1: Määritä projektin myyntihinnasto

Etsi projekti toteutuneesta projektikentästä ja siirry projektin sivulle. Siirry sitten Myynti-välilehteen. Valitse Projektisopimusrivit-ruudukossa Projektisopimus-kentän linkki. Projektisopimus-sivu avautuu. Siirry Projektisopimus-sivulla Projektihinnastot-välilehteen. Varmista, että siellä on vähintään yksi liitetty hinnasto. Jos projektisopimuksen Projektihinnastot-ruudukkoon ei ole liitetty hinnastoa, olet eristänyt ongelman. Liitä hinnasto Projektihinnastot-ruudukkoon. Tässä liitettävien hinnastojen kontekstikentän arvoksi on määritettävä Myynti ja hinnaston valuuttakentän arvon on oltava sama kuin projektisopimuksen valuuttakentän arvo. Kun olet tehnyt vaaditut korjaukset, voit luoda aikamerkinnän uudelleen ja hyväksyä sen. Tarkista, että toteutuneen laskuttamattoman myynnin hinta on sallittu. 

Jos projektisopimuksen Projektihinnastot-ruudukkoon on liitetty useita hinnastoja, siirry seuraavaan tarkistukseen asiakirjassa.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Tarkistus 2: Onko jokin yllä määritetyistä hinnastoista sallittu toteutuneen ajan myynnin määritettynä päivämääränä?

Project Service -sovelluksessa voidaan käyttää oletushintojen hinnastoa, jos hinnasto on käytössä toteutuneen ajan myynnin päivämääränä. Tarkista seuraavat kohdat ja varmista, ovatko yllä määritetyt hinnastot käytettävissä:
- Tarkista, että liitettyjen hinnastojen Yleinen-välilehden alku- ja loppupäivämäärät on määritetty. Jos yllä määritettyjä hinnastojen alku- ja loppupäivämääriä ei ole määritetty, olet eristänyt ongelman. 
- Ota toteutuneen ajan myynnin päivämääräkentän arvo muistiin ja tarkista, onko mikään hinnastoista käytössä kyseisenä päivänä. Esimerkiksi toteutuneen ajan myynnin päivämäärän tulisi olla hinnaston alku- ja loppupäivämäärän välillä. 
    - Jos toteutuneen ajan myynnin päivämäärä ei kuulu yhdenkään hinnaston päivämääräväliin, olet eristänyt ongelman. Muokkaa hinnaston alku- ja loppupäivämääriä varmistaaksesi, että hinnasto kattaa toteutuneen ajan myynnin päivämäärän. 
    - Jos toteutuneen ajan myynnin päivämäärä kuuluu usean hinnaston päivämääräväliin, olet eristänyt ongelman. Voit korjata ongelman muokkaamalla hinnastojen alku- ja loppupäivämääriä niin, että vain yksi hinnasto kattaa toteutuneen ajan myynnin päivämäärän. 
    - Jos toteutuneen ajan myynnin kattavia hinnastoja on vain yksi, siirry tarkistukseen 3.
Kun olet tehnyt vaaditut korjaukset, voit luoda aikamerkinnän uudelleen ja hyväksyä sen. Tarkista, että toteutuneen ajan myynnillä on sallittu hinta.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Tarkistus 3: Onko hinnastossa hinta toteutuneen ajan myynnin hinnoitteludimensioille?

Jos olet tarkistuksen 1 ja 2 suoritus onnistui, sinulla pitäisi olla nyt vain yksi hinnasto, joka käsittää toteutuneen ajan myynnin päivämäärän. Avaa tämä hinnasto ja siirry Roolin hinnat -välilehteen. Varmista, että toteutuneen ajan myynnin hinnoitteludimensioilla on rivi ruudukossa.

Jos toteutuneen ajan myynnin hinnoitteludimensioiden roolin hinnan ruudukossa ei ole riviä, olet eristänyt ongelman. Luo toteutuneen ajan myynnin hinnoitteludimensioiden Roolin hinnat -ruudukolle rivi. Kun olet tehnyt tämän, voit luoda aikamerkinnän uudelleen ja hyväksyä sen. Tarkista, että toteutuneen ajan myynnin hinta on sallittu.

Jos toteutuneen ajan myynnillä ei ole sallittua hintaa näiden kolmen edellä mainitun tarkistuksen jälkeen ole sallittu, kirjaa tukipyyntö. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]