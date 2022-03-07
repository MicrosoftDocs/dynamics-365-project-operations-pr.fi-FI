---
title: Monimutkaisten yksiköiden, kuten käyttäjäkohtaisten ja kuukausikohtaisten yksiköiden, hallinta tuotepohjaisilla tarjousriveillä – lite
description: Tässä aiheessa on tietoja monimutkaisten yksiköiden hallinnasta tuotepohjaisilla tarjousriveillä
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 78bdb64d901cf68ce02c168987c2386e1416f6ee
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994762"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Monimutkaisten yksiköiden, kuten käyttäjäkohtaisten ja kuukausikohtaisten yksiköiden, hallinta tuotepohjaisilla tarjousriveillä – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Dynamics 365 Project Operationsissa käytetään määräkertoimia tukemaan tilausperusteisten tuotteiden myyntiä. Tilausperusteisten tuotteiden osalta tarjouksen tai projektisopimuksen rivin määrä ilmaistaan käyttäjäkuukausien lukumääränä.

Yleensä tilausohjelmiston hinta tallennetaan luetteloon käyttäjäkohtaisena kuukausihintana. Myyntiprosessin aikana tarjousrivillä oleva hinta on yleensä se käyttäjäkohtainen kuukausihinta, jonka IT-myyjä on neuvotellut ja josta hän on antanut alennusta. Kullakin kaupalla on eri määrä käyttäjiä ja eri määrä tilauskuukausia. Tarjousrivin summan laskemiseen käytettävä määrä perustuu käyttäjämäärän ja tilauskuukausien määrään kertolaskuun.

Tällaisen myynnin tukemista varten Project Operationsissa on otettu käyttöön määräkertoimien konsepti. Määräkertoimet perustuvat Dynamics 365:n tuotemääritteisiin. Kun määrität tuotteelle tiettyjä ominaisuuksia, voit Project Operationsissa valita osan näistä määritteistä tai ne kaikki määräkertoimiksi.

Project Operations varmistaa, että määräkertoimiksi valitaan vain numeerisia ominaisuuksia tai tuoteominaisuuksia joilla on numeerinen tietotyyppi. Kun lisäät tarjousriviin tuotteen, jolla on määräkertoimia, **Määrä**-kenttä muuttuu vain luku -tilaan. Kun olet määrittänyt arvot tuoteominaisuuksille, jotka ovat määräkertoimia, Project Operations laskee tarjousrivin määrän.

Esimerkiksi Dynamics 365 Salesilla voi olla seuraavat ominaisuudet:

- **Käyttäjät**: Käyttäjien määrä
- **Kuukaudet**: Tilauskuukausien määrä
- **Tuote-SKU**

**Käyttäjät**- ja **Kuukaudet**-ominaisuudet voidaan valita määräkertoimiksi muokkaamalla tuoterivin ominaisuuksia.

Voit luoda määräkertoimet tuotteen ominaisuuksista seuraavasti:

1. Siirry Project Operationsin vasemmassa siirtymisruudussa kohtaan **Myynti** > **Tuotteet**.
2. Avaa tuote, jolle on määritettävä määräkertoimet. Varmista, että tuotteen ominaisuudet on jo määritetty.
3. Valitse tuotteen **Projektitiedot**- sivulla **Määräkertoimet**-välilehti.
4. Valitse aliruudukossa **+ Uusi kenttälaskenta**.
5. Kirjoita määräkertoimen nimi ja valitse ominaisuuden arvo, joka yhdistetään kentän laskentaan.
6. Tallenna ja sulje lomake. Toista nämä vaiheet kaikille ominaisuuksille, joita käytetään tuotepohjaisen tarjousrivin määrän laskennassa.

Kun luot tuotteelle tuotepohjaisen tarjousrivin, tarjousrivin määrä lukitaan. Määrä lasketaan tuotteena niiden ominaisuusarvojen kertolaskuna, jotka syötetään kyseiselle tarjousriville.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]