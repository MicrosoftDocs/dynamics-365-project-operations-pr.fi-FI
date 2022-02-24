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
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764546"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Kustannus- ja myyntihintojen määrittäminen luettelotuotteille – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_


Tuoteluettelonimikkeiden hinnoittelu määritetään Dynamics 365 Project Operationsissa samoin kuin Dynamics 365 Salesissa.

Project Operationsissa tuotteita ei voi arvioida tai käyttää projekteissa, joten tuoteluettelohintoja ei tarvitse määrittää tarjousten ja sopimusten projektihinnastoihin.

Määritä tuoteluettelohinnat tarjouksen, sopimuksen tai tilin **Tuotehinta**-kentän avulla. Älä määritä tuoteluettelohintoja projektin hinnastoihin. Projektihinnastot ovat yksinomaisia Project Operationsia varten. Sovelluskohtainen liiketoimintalogiikka kopioi hinnastot tarjouksesta sopimukseen. Tuloksena on palvelussopimuskohtainen hinnasto Kopiointitoiminto voi viivyttää tarjouksen voittoprosessia, jos tarjouksen projektihinnasto muuttuu liian suureksi. Tuotehinnastoja ei kopioida, kun luodaan palvelusopimuksille mukautettuja hinnastoja. Koska kopiointia ei tehdä, tämä ei vaikuta tarjousprosessin suorituskykyyn.
