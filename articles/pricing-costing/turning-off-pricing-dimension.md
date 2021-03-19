---
title: Hinnoitteludimension poistaminen käytöstä
description: Tässä aiheessa on tietoja hinnoitteludimensioiden käytöstäpoistosta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274724"
---
# <a name="turning-off-a-pricing-dimension"></a>Hinnoitteludimension poistaminen käytöstä

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Hinnoittelustrategiaa on ehkä tarkistettava ja päivitettävä muutaman vuoden välein. Tekemäsi päivitykset voivat edellyttää, että poistat aiemmin luodun hinnoitteludimension käytöstä ja luot uuden. Olet esimerkiksi ehkä aiemmin hinnoitellut **Roolin** mukaan, mutta olet nyt päättänyt, että hinta määräytyy **Työkokemuksen** perusteella. Tämä voi edellyttää, **Roolin** hinnoitteludimensioista ja lisäät **Työkokemuksen** uutena hinnoitteludimensiona. 

Hinnoitteludimension poistaminen käytöstä, riippumatta siitä onko se valmiina oleva vai mukautettu, voidaan tehdä asettamalla **Sovelletaan kustannuksiin** ja **Sovelletaan myyntiin** -kenttien arvoksi hinnoitteludimensiossa **Ei**.

Jos näin tehdään, näyttöön saattaa tulla seuraava virhesanoma: **Hinnoitteludimensiota ei voi päivittää tai poistaa, jos liittyviä hintatietueita on olemassa.**

![Liiketoimintaprosessivirhe on todennäköinen, kun hinnoitteludimensio poistetaan käytöstä](media/Business-Process-Error.png)

Tämä virhesanoma ilmaisee, että käytöstä poistettavalle dimensiolle on aiemmin määritetty hintatietueita. Kaikki **Roolihinta** ja **Rooolihinnan korotus** -tietueet, jotka viittaavat dimensioon tulee poistaa ennen kuin dimension sovellettavuudeksi voidaan asettaa **Ei**. Tämä sääntö koskee sekä valmiita hinnoitteludimensioita että mahdollisesti luotuja mukautettuja hinnoitteludimensioita. Tämän vahvistuksen syy on se, että kullakin **Roolihinta**-tietueella on oltava ainutlaatuinen dimensioyhdistelmä. Esimerkiksi hinnastossa nimeltä **US Cost Rates 2018** on seuraavat **Roolihinta**-rivit. 

| Vakio-otsikko         | Organisaatioyksikkö    |Yksikkö   |Hinta  |Valuutta  |
| -----------------------|-------------|-------|-------|----------|
| Järjestelmäinsinööri|Contoso US|Hour| 100|USD|
| Vanhempi järjestelmäinsinööri|Contoso US|Hour| 150| USD|


Kun poistat käytöstä **Vakio-otsikon** hinnoitteludimensiona, ja hinnoittelumoottori etsii hintaa, se käyttää ainoastaan **Organisaatioyksikkö**-arvoa syötekontekstista. Jos syötekontekstin **Organisaatioyksikkö** on “Contoso US”, lopputulos ei ole deterministinen, koska molemmat rivit täyttävät ehdon. Jotta tämä skenaario voidaan välttää, järjestelmä tarkistaa **Roolihinta**-tietueita luotaessa, että dimensioiden yhdistelmä on ainutlaatuinen. Jos dimensio on poistettu käytöstä sen jälkeen kun **Roolihinta**-tietueita on luotu, tätä rajoitetta voidaan rikkoa. Siksi on tarpeen, että ennen kuin poistat dimension käytöstä, poistat kaikki ne **Roolihinta**- ja **Roolihinnan korotus** -rivit, joilla on käytetty tätä dimension arvoa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]