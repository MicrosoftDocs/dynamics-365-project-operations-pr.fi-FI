---
title: Tilapäisen ennakon luominen palvelusopimuksessa – lite
description: Tässä aiheessa on tietoja ennakon luomisesta sopimuksessa tarpeen mukaan.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181358"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Tilapäisen ennakon luominen palvelusopimuksessa – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Microsoft Dynamics 365 Project Operations tukee laskutusskenaarioita, jotka koskevat ennakkomaksuja ja ennakoita. **Ennakoiden** käyttö **Project Operationsissa** muistuttaa sopimusten **ennakkomaksuja**. 

Laskuta ennakko asiakkaalta seuraavasti:

1. Siirry **Projektisopimus**-riville ja valitse sitten **Ennakot ja ennakkomaksut**-välilehti.
2. Valitse alaruudukossa, jossa on luettelo kaikista aiemmin kirjatuista ennakoista ja ennakkomaksuista, **+ Uusi projektisopimuksen ennakkomaksu**. 

    **Pikaluonti**-lomake avautuu ennakkomaksun tai ennakon kirjaamista varten.
    
3. Seuraavassa taulukossa on luettelo kentistä, joilla ennakko kirjataan, ja seikoista, jotka on otettava huomioon uusia ennakoita luotaessa:

    | Field | Kuvaus | Loppupään vaikutus |
    | --- | --- | --- |
    | **Projektisopimuksen asiakas** | Tämä kenttä ilmaisee, miltä sopimuksen asiakkaalta tämä ennakko laskutetaan. | Jos sopimuksessa on useita asiakkaita ja niistä jokaiselta halutaan laskuttaa tietty ennakkomaksu- tai ennakkosumma, luo ennakko erikseen kullekin asiakkaalle. |
    | **Kuvaus** | Ennakon tarkoituksen tai ajoituksen kuvaus auttaa tunnistamaan ennakon. | Kuvaus näytetään ennakon laskurivillä. |
    | **Summa** | Ennakkomaksun tai ennakon summa. | Summa näytetään ennakon laskurivillä. |
    | **Laskun pvm** | Päivämäärä, jolloin ennakko laskutetaan asiakkaalle. | Tämä on päivämäärä, jolloin automatisoitu laskun luontiprosessi luo ennakon laskurivin. |
    | **Laskun tila** | Tämä asetusjoukko ilmaisee, lisätäänkö ennakko tämän asiakkaan luonnoslaskuun. Mahdolliset arvot:</br>- **Ei valmis laskuttamista varten**</br>- **Valmis laskuttamista varten** | Jos ennakon tai ennakkomaksun merkintänä on **Valmis laskutettavaksi**, se lisätään rivien aikana luonnoslaskuun. Vain täysin laskutettua ennakkoa voidaan käyttää täsmäyttämään seuraavan laskukauden projektikustannuksia. |

4. Kirjaa ennakko tai ennakkomaksu valitsemalla **Tallenna ja sulje** pikaluonti-ikkunassa.
