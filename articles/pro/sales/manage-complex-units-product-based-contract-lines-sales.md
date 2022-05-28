---
title: Tuotepohjaisten sopimusrivien monitasoisten yksiköiden hallinta – lite
description: Tässä aiheessa on tietoja tilauspohjaisten tuotteiden myynnin tukemisesta.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 214593c5b3fbfc5194031af3d3bef59d01750099
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593976"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Tuotepohjaisten sopimusrivien monitasoisten yksiköiden hallinta – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Dynamics 365 Project Operationsissa käytetään määräkertoimia tukemaan tilausperusteisten tuotteiden myyntiä. Tilausperusteisten tuotteiden osalta sopimuksen tai projektin sopimusrivin määrä ilmaistaan käyttäjäkuukausien lukumääränä.

Tilausohjelmiston hinta tallennetaan luetteloon käyttäjäkohtaisena kuukausihintana. Myyntiprosessin aikana sopimusrivillä oleva hinta on yleensä se käyttäjäkohtainen kuukausihinta, jonka myyjä on neuvotellut ja josta hän on antanut alennusta. Kullakin kaupalla on eri määrä käyttäjiä ja eri määrä tilauskuukausia. Sopimusrivin summan laskemiseen käytettävä määrä perustuu käyttäjämäärään ja tilauskuukausien määrään.

Tällaisen myynnin tukemista varten Project Operations tukee *määräkertoimien* käsitettä. Määräkertoimet perustuvat tuotemääritteisiin. Kun määrität tuotteelle tiettyjä ominaisuuksia, voit valita osan näistä määritteistä tai ne kaikki määräkertoimiksi.

Project Operations varmistaa, että määräkertoimiksi valitaan vain numeerisia ominaisuuksia tai tuoteominaisuuksia joilla on numeerinen tietotyyppi. Kun tuote, johon on määritetty määräkertoimia, lisätään sopimusriville, **Määrä**-kenttä muuttuu vain luku -muotoiseksi. Kun olet määrittänyt arvot tuoteominaisuuksille, jotka ovat määräkertoimia, Project Operations laskee sopimusrivin määrän.

Esimerkiksi Dynamics 365 Salesilla voi olla seuraavat ominaisuudet:

- **Käyttäjät**: käyttäjien määrä.
- **Kuukaudet**: tilauskuukausien määrä.
- **Tuotteen SKU**: tuotteen varastointiyksikkö (SKU).

**Käyttäjät**- ja **Kuukaudet**-ominaisuudet voidaan valita määräkertoimiksi muokkaamalla tuoterivin ominaisuuksia.

Määräkertoimia luodaan tuotteen ominaisuuksista seuraavasti:

1. Valitse **Project Operationsissa** **Myynti - tuotteet**.
2. Avaa tuote, jolle määräkertoimet on määritettävä. Varmista, että tuotteen ominaisuudet on jo määritetty.
3. Valitse **Projektin tiedot** -sivulla **Määräkertoimet**-välilehti.
4. Valitse aliruudukossa **+ Uusi kenttälaskenta**.
5. Kirjoita **määräkertoimen** nimi ja valitse ominaisuuden arvo, joka yhdistetään kentän laskentaan.
6. Tallenna ja sulje lomake.
7. Toista vaiheet 2–6 kaikkien niiden ominaisuuksien osalta, jotka yhdessä muodostavat tuotepohjaisen sopimusrivin määrän.

Kun määräkertoimet on määritetty ja käyttäjä luo tuotteelle sopimusrivin, sopimusrivin määrä lukitaan. Määrä lasketaan sitten kyseisen sopimusrivin ominaisuusarvojen tuotteena.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]