---
title: Äkillisen ennakon luominen palvelusopimuksessa
description: Tässä aiheessa on tietoja ennakon luomisesta sopimuksessa tarpeen mukaan.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 790a0281f72eff5f241d11da025b5b4af643a567
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/21/2020
ms.locfileid: "4595959"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Äkillisen ennakon luominen palvelusopimuksessa

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Microsoft Dynamics 365 Project Operations tukee laskutusskenaarioita, joissa on ennakkomaksuja ja maksuennakoita. **Ennakoiden** käyttö **Project Operationsissa** muistuttaa sopimusten **ennakkomaksuja**. 

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
