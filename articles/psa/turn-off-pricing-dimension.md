---
title: Hinnoitteludimension poistaminen käytöstä
description: Tässä artikkelissa käsitellään hinnoitteludimensioiden määrittämistä Project Service -ratkaisussa.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 81c3cfaad8dc8d057985b509f20c3ba31de45e3b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913156"
---
# <a name="turn-off-a-pricing-dimension"></a>Hinnoitteludimension poistaminen käytöstä

[!include [banner](../includes/psa-now-project-operations.md)]

Hinnoittelustrategiaa on ehkä tarkistettava ja päivitettävä muutaman vuoden välein. Tekemäsi päivitykset voivat edellyttää, että poistat aiemmin luodun hinnoitteludimension käytöstä ja luot uuden. Olet esimerkiksi ehkä aiemmin hinnoitellut **Roolin** mukaan, mutta olet nyt päättänyt, että hinta määräytyy **Työkokemuksen** perusteella. Tämä voi edellyttää, **Roolin** hinnoitteludimensioista ja lisäät **Työkokemuksen** uutena hinnoitteludimensiona. 

Hinnoitteludimension poistaminen käytöstä, riippumatta siitä onko se valmiina oleva vai mukautettu, voidaan tehdä asettamalla **Sovelletaan kustannuksiin** ja **Sovelletaan myyntiin** -kenttien arvoksi hinnoitteludimensiossa **Ei**.

Kun teet näin, näyttöön voi kuitenkin tulla seuraava virhesanoma.

![Liiketoimintaprosessivirhe on todennäköinen, kun hinnoitteludimensio poistetaan käytöstä.](media/Business-Process-Error.png)


Tämä virhesanoma ilmaisee, että käytöstä poistettavalle dimensiolle on aiemmin määritetty hintatietueita. Kaikki **Roolihinta** ja **Rooolihinnan korotus** -tietueet, jotka viittaavat dimensioon tulee poistaa ennen kuin dimension sovellettavuudeksi voidaan asettaa **Ei**. Tämä sääntö koskee sekä valmiita hinnoitteludimensioita että mahdollisesti luotuja mukautettuja hinnoitteludimensioita. Tämän vahvistuksen syy on se, että Project Service -palvelussa on rajoitus, jonka mukaan kullakin **Roolihinta**-tietueella on oltava ainutlaatuinen dimensioyhdistelmä. Esimerkiksi hinnastossa nimeltä **US Cost Rates 2018** on seuraavat **Roolihinta**-rivit. 

| Vakio-otsikko         | Organisaatioyksikkö    |Yksikkö   |Hinta  |Valuutta  |
| -----------------------|-------------|-------|-------|----------|
| Järjestelmäinsinööri|Contoso US|Hour| 100|USD|
| Vanhempi järjestelmäinsinööri|Contoso US|Hour| 150| USD|


Kun poistat käytöstä **Vakio-otsikon** hinnoitteludimensiona, ja Project Servicen hinnoittelumoottori etsii hintaa, se käyttää ainoastaan **Organisaatioyksikkö**-arvoa syötekontekstista. Jos syötekontekstin **Organisaatioyksikkö** on “Contoso US”, lopputulos ei ole deterministinen, koska molemmat rivit täyttävät ehdon. Jotta tämä skenaario voidaan välttää, Project Service tarkistaa **Roolihinta**-tietueita luotaessa, että dimensioiden yhdistelmä on ainutlaatuinen. Jos dimensio on poistettu käytöstä sen jälkeen kun **Roolihinta**-tietueita on luotu, tätä rajoitetta voidaan rikkoa. Siksi on tarpeen, että ennen kuin poistat dimension käytöstä, poistat kaikki ne **Roolihinta**- ja **Roolihinnan korotus** -rivit, joilla on käytetty tätä dimension arvoa.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
