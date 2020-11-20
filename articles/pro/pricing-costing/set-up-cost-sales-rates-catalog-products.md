---
title: Kustannus- ja myyntihintojen määrittäminen luettelotuotteille – lite
description: Tässä aiheessa on tietoja siitä, miten tuoteluettelon nimikkeiden kustannus- ja myyntihinnat määritetään.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176697"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Kustannus- ja myyntihintojen määrittäminen luettelotuotteille – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_


Tuoteluettelonimikkeiden hinnoittelun määrittäminen Dynamics 365 Project Operationsissa on sama kuin Dynamics 365 Salesissa.

Koska tuotteita ei voi arvioida tai käyttää Project Operationsin projekteissa, tuoteluettelon hintoja ei tarvitse määrittää projektihinnastoissa tarjouksia ja sopimuksia varten.

Tuoteluettelon hinnat on määritettävä tarjouksen, palvelusopimuksen tai asiakkuuden **tuotehinta**-kentässä. Älä määritä tuoteluettelon hintoja näiden kohteille projektin hinnastoissa. Projektihinnastot ovat yksinomaisia Project Operationsia varten. Sovelluskohtainen liiketoimintalogiikka kopioi hinnastot tarjouksesta palvelusopimukseen. Tuloksena on palvelussopimuskohtainen hinnasto Kopiointitoiminto voi viivyttää tarjouksen voittoprosessia, jos tarjouksen projektihinnasto muuttuu liian suureksi. Tuotehinnastoja ei kopioida, kun luodaan palvelusopimuksille mukautettuja hinnastoja. Tämä tarkoittaa sitä, että tuotehinnastot eivät vaikuta tarjouksen voittoprosessin tehokkuuteen.
