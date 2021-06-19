---
title: Hinnoitteludimension poistaminen käytöstä
description: Tämä aihe näyttää, miten hinnoitteludimensiot määritetään Project Service -ratkaisussa.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014292"
---
# <a name="turn-off-a-pricing-dimension"></a>Hinnoitteludimension poistaminen käytöstä

[!include [banner](../includes/psa-now-project-operations.md)]

Hinnoittelustrategiaa on ehkä tarkistettava ja päivitettävä muutaman vuoden välein. Tekemäsi päivitykset voivat edellyttää, että poistat aiemmin luodun hinnoitteludimension käytöstä ja luot uuden. Olet esimerkiksi ehkä aiemmin hinnoitellut **Roolin** mukaan, mutta olet nyt päättänyt, että hinta määräytyy **Työkokemuksen** perusteella. Tämä voi edellyttää, **Roolin** hinnoitteludimensioista ja lisäät **Työkokemuksen** uutena hinnoitteludimensiona. 

Hinnoitteludimension poistaminen käytöstä, riippumatta siitä onko se valmiina oleva vai mukautettu, voidaan tehdä asettamalla **Sovelletaan kustannuksiin** ja **Sovelletaan myyntiin** -kenttien arvoksi hinnoitteludimensiossa **Ei**.

Kun teet näin, näyttöön voi kuitenkin tulla seuraava virhesanoma.

![Liiketoimintaprosessivirhe on todennäköinen, kun hinnoitteludimensio poistetaan käytöstä](media/Business-Process-Error.png)


Tämä virhesanoma ilmaisee, että käytöstä poistettavalle dimensiolle on aiemmin määritetty hintatietueita. Kaikki **Roolihinta** ja **Rooolihinnan korotus** -tietueet, jotka viittaavat dimensioon tulee poistaa ennen kuin dimension sovellettavuudeksi voidaan asettaa **Ei**. Tämä sääntö koskee sekä valmiita hinnoitteludimensioita että mahdollisesti luotuja mukautettuja hinnoitteludimensioita. Tämän vahvistuksen syy on se, että Project Service -palvelussa on rajoitus, jonka mukaan kullakin **Roolihinta**-tietueella on oltava ainutlaatuinen dimensioyhdistelmä. Esimerkiksi hinnastossa nimeltä **US Cost Rates 2018** on seuraavat **Roolihinta**-rivit. 

| Vakio-otsikko         | Organisaatioyksikkö    |Yksikkö   |Hinta  |Valuutta  |
| -----------------------|-------------|-------|-------|----------|
| Järjestelmäinsinööri|Contoso US|tunti| 100|USD|
| Vanhempi järjestelmäinsinööri|Contoso US|tunti| 150| USD|


Kun poistat käytöstä **Vakio-otsikon** hinnoitteludimensiona, ja Project Servicen hinnoittelumoottori etsii hintaa, se käyttää ainoastaan **Organisaatioyksikkö**-arvoa syötekontekstista. Jos syötekontekstin **Organisaatioyksikkö** on ”Contoso US”, lopputulos ei ole deterministinen, koska molemmat rivit täyttävät ehdon. Jotta tämä skenaario voidaan välttää, Project Service tarkistaa **Roolihinta**-tietueita luotaessa, että dimensioiden yhdistelmä on ainutlaatuinen. Jos dimensio on poistettu käytöstä sen jälkeen kun **Roolihinta**-tietueita on luotu, tätä rajoitetta voidaan rikkoa. Siksi on tarpeen, että ennen kuin poistat dimension käytöstä, poistat kaikki ne **Roolihinta**- ja **Roolihinnan korotus** -rivit, joilla on käytetty tätä dimension arvoa.



[!INCLUDE[footer-include](../includes/footer-banner.md)]