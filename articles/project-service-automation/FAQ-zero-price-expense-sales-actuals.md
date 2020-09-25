---
title: Miksi toteutuneen kulumyynnin oletushinta on nolla?
description: Seuraavien kolmen tarkistuksen avulla voit tehdä vianmäärityksen ja selvittää, miksi hinnan oletusarvo on 0 toteutuneelle kulumyynnille.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 85a177ec-ad61-450d-bfe6-cdea7a415566
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ccbad4ac969ffe4f09744557e2a9be68aa93e8c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751238"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Miksi toteutuneen kulumyynnin oletushinta on nolla?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nämä usein kysytyt kysymykset koskevat toteutuneita kuluja, joissa tapahtuman luokaksi on määritetty Kulu ja tapahtumatyypiksi Laskuttamaton myynti. Seuraavien kolmen tarkistuksen avulla voit tehdä vianmäärityksen ja selvittää, miksi hinnan (laskun arvon) oletusarvo on 0 toteutuneelle kulumyynnille.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Tarkistus 1: Määritä projektin myyntihinnasto

Etsi projekti toteutuneesta projektikentästä ja siirry projektin sivulle. Siirry sitten Myynti-välilehteen. Valitse Projektisopimusrivit-ruudukossa Projektisopimus-kentän linkki. Projektisopimus-sivu avautuu. Siirry Projektisopimus-sivulla Projektihinnastot-välilehteen. Varmista, että siellä on vähintään yksi liitetty hinnasto.

Jos projektisopimuksen Projektihinnastot-ruudukkoon ei ole liitetty hinnastoa, toimi seuraavasti:

- Liitä hinnasto Projektihinnastot-ruudukkoon. Tässä liitettävien hinnastojen kontekstikentän arvoksi on määritettävä Myynti ja hinnaston valuuttakentän arvon on oltava sama kuin projektisopimuksen valuuttakentän arvo. Kun olet tehnyt vaaditut korjaukset, voit luoda kulumerkinnän uudelleen ja hyväksyä sen. Tarkista, että toteutuneen laskuttamattoman myynnin hinta on sallittu.
- Jos projektisopimuksen Projektihinnastot-ruudukkoon on liitetty useita hinnastoja, siirry tarkistukseen 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Tarkistus 2: Onko jokin yllä määritetyistä hinnastoista sallittu toteutuneen kulun määritettynä päivämääränä?

Project Service -sovelluksessa voidaan käyttää oletushintojen hinnastoa, jos hinnasto on käytössä toteutuneen kulumyynnin päivämääränä. Tarkista seuraavat kohdat ja varmista, ovatko yllä määritetyt hinnastot käytettävissä:

- Aloita varmistamalla, että liitettyjen hinnastojen Yleinen-välilehden alku- ja loppupäivämäärät on määritetty. Jos yllä määritettyjä hinnastojen alku- ja loppupäivämääriä ei ole määritetty, olet eristänyt ongelman. 
- Ota toteutuneen kulumyynnin päivämääräkentän arvo muistiin ja tarkista, onko mikään hinnastoista käytössä kyseisenä päivänä. Esimerkiksi toteutuneen kulun päivämäärän tulisi olla hinnaston alku- ja loppupäivämäärän välillä. 
    - Jos toteutuneen kulumyynnin päivämäärä ei kuulu yhdenkään hinnaston päivämääräväliin, olet eristänyt ongelman. Muokkaa hinnaston alku- ja loppupäivämääriä varmistaaksesi, että hinnasto kattaa toteutuneen kulun päivämäärän. 
    - Jos toteutuneen kulumyynnin päivämäärä kuuluu usean hinnaston päivämääräväliin, olet eristänyt ongelman. Voit korjata ongelman muokkaamalla hinnastojen alku- ja loppupäivämääriä niin, että vain yksi hinnasto kattaa toteutuneen kulun päivämäärän. 
    - Jos toteutuneen kulun kattavia hinnastoja on vain yksi, siirry tarkistukseen 3.
Kun olet tehnyt vaaditut korjaukset, voit luoda kulumerkinnän uudelleen ja hyväksyä sen. Tarkista, että toteutuneen laskuttamattoman myynnin hinta on sallittu.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Tarkistus 3: Onko soveltuvan projektihinnaston kululuokalla sallittu hinta? 

Jos olet tarkistuksen 1 ja 2 suoritus onnistui, sinulla pitäisi olla nyt vain yksi projektihinnasto, joka käsittää toteutuneen kulumyynnin päivämäärän. Avaa projektihinnasto ja siirry Luokan hinnat -välilehteen. Varmista, että toteutuneen kulun määritetyllä kululuokalla on rivi ruudukossa.
 
- Jos riviä ei ole, olet eristänyt ongelman. Luo toteutuneen kulun luokalle rivi Luokan hinta -ruudukkoon. Kun olet tehnyt tämän, voit luoda kulumerkinnän uudelleen ja hyväksyä sen. Tarkista, että toteutuneen laskuttamattoman myynnin hinta on sallittu. 
- Jos Luokan hinnat -ruudukossa on rivi kululuokalle, tarkista, onko rivin hinta sallittu.

Näiden tapojen avulla voit tarkistaa, onko hinta sallittu:

- Jos luokan hintarivin Hinnoittelutapa-kentän arvoksi on määritetty Kustannusten mukaan, toteutuneen kulumyynnin yksikköhinnan oletusarvo on kulumerkinnän arvo.
- Jos luokan hintarivin Hinnoittelutapa-kentän arvoksi on määritetty Prosenttia hankintahinnasta, tarkista, onko Prosentti-kentän arvo sallittu. Toteutuneen kulumyynnin yksikköhinnan oletusarvo saadaan kohdistamalla tämä hankintahinnan prosenttiosuus kulumerkinnän hintaan.
- Jos luokan hintarivin Hinnoittelutapa-kentän arvoksi on määritetty Yksikköhinta, tarkista, onko Hinta-kentän arvo sallittu. Toteutuneen kulumyynnin yksikköhinnan oletusarvo on Hinta-kentän valuuttasumma.

JOs kululuokan hinnan asetus ei ole sallittu, olet eristänyt ongelman. Ratkaisu on muuttaa kululuokan luokan hintarivin arvoksi sallittu hinta edellä mainittujen sääntöjen mukaisesti. Kun olet tehnyt tämän, voit luoda kulumerkinnän uudelleen ja hyväksyä sen. Tarkista sitten, että toteutuneen laskuttamattoman myynnin hinta on sallittu.

Jos toteutuneella kulumyynnillä ei ole sallittua hintaa näiden kolmen edellä mainitun tarkistuksen jälkeen ole sallittu, kirjaa tukipyyntö.

