---
title: Kustannus- ja myyntihintojen määrittäminen luettelotuotteille – lite
description: Tässä aiheessa on tietoja siitä, miten tuoteluettelon nimikkeiden kustannus- ja myyntihinnat määritetään.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bfb28e710c7b6da17d94679a72659f81df7a58e376e4bad94b58c36de781b197
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996027"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Kustannus- ja myyntihintojen määrittäminen luettelotuotteille – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_


Tuoteluettelonimikkeiden hinnoittelu määritetään Dynamics 365 Project Operationsissa samoin kuin Dynamics 365 Salesissa.

Project Operationsissa tuotteita ei voi arvioida tai käyttää projekteissa, joten tuoteluettelohintoja ei tarvitse määrittää tarjousten ja sopimusten projektihinnastoihin.

Määritä tuoteluettelohinnat tarjouksen, sopimuksen tai tilin **Tuotehinta**-kentän avulla. Älä määritä tuoteluettelohintoja projektin hinnastoihin. Projektihinnastot ovat yksinomaisia Project Operationsia varten. Sovelluskohtainen liiketoimintalogiikka kopioi hinnastot tarjouksesta sopimukseen. Tuloksena on palvelussopimuskohtainen hinnasto Kopiointitoiminto voi viivyttää tarjouksen voittoprosessia, jos tarjouksen projektihinnasto muuttuu liian suureksi. Tuotehinnastoja ei kopioida, kun luodaan palvelusopimuksille mukautettuja hinnastoja. Koska kopiointia ei tehdä, tämä ei vaikuta tarjousprosessin suorituskykyyn.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]