---
title: Kustannus- ja myyntihintojen määrittäminen luettelotuotteille – lite
description: Tässä aiheessa on tietoja siitä, miten tuoteluettelon nimikkeiden kustannus- ja myyntihinnat määritetään.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274454"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Kustannus- ja myyntihintojen määrittäminen luettelotuotteille – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_


Tuoteluettelonimikkeiden hinnoittelu määritetään Dynamics 365 Project Operationsissa samoin kuin Dynamics 365 Salesissa.

Project Operationsissa tuotteita ei voi arvioida tai käyttää projekteissa, joten tuoteluettelohintoja ei tarvitse määrittää tarjousten ja sopimusten projektihinnastoihin.

Määritä tuoteluettelohinnat tarjouksen, sopimuksen tai tilin **Tuotehinta**-kentän avulla. Älä määritä tuoteluettelohintoja projektin hinnastoihin. Projektihinnastot ovat yksinomaisia Project Operationsia varten. Sovelluskohtainen liiketoimintalogiikka kopioi hinnastot tarjouksesta sopimukseen. Tuloksena on palvelussopimuskohtainen hinnasto Kopiointitoiminto voi viivyttää tarjouksen voittoprosessia, jos tarjouksen projektihinnasto muuttuu liian suureksi. Tuotehinnastoja ei kopioida, kun luodaan palvelusopimuksille mukautettuja hinnastoja. Koska kopiointia ei tehdä, tämä ei vaikuta tarjousprosessin suorituskykyyn.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]