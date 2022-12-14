---
title: Tilapäisen ennakon luominen projektisopimuksessa
description: Tässä artikkelissa on tietoja ennakon luomisesta sopimuksessa tarpeen mukaan.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 62e41e5faeb5e40143e26e2cdf48c1279941a6b4
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824840"
---
# <a name="create-an-ad-hoc-advance-on-a-project-contract"></a>Tilapäisen ennakon luominen projektisopimuksessa

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
