---
title: Kustannus- ja myyntihintojen määrittäminen luettelotuotteille
description: Tässä aiheessa on tietoja siitä, miten tuoteluettelon nimikkeiden kustannus- ja myyntihinnat määritetään.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075415"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Kustannus- ja myyntihintojen määrittäminen luettelotuotteille

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_


Tuoteluettelonimikkeiden hinnoittelun määrittäminen Dynamics 365 Project Operationsissa on sama kuin Dynamics 365 Salesissa.

Koska tuotteita ei voi arvioida tai käyttää Project Operationsin projekteissa, tuoteluettelon hintoja ei tarvitse määrittää projektihinnastoissa tarjouksia ja sopimuksia varten.

Tuoteluettelon hinnat on määritettävä tarjouksen, palvelusopimuksen tai asiakkuuden **tuotehinta** -kentässä. Älä määritä tuoteluettelon hintoja näiden kohteille projektin hinnastoissa. Projektihinnastot ovat yksinomaisia Project Operationsia varten. Sovelluskohtainen liiketoimintalogiikka kopioi hinnastot tarjouksesta palvelusopimukseen. Tuloksena on palvelussopimuskohtainen hinnasto Kopiointitoiminto voi viivyttää tarjouksen voittoprosessia, jos tarjouksen projektihinnasto muuttuu liian suureksi. Tuotehinnastoja ei kopioida, kun luodaan palvelusopimuksille mukautettuja hinnastoja. Tämä tarkoittaa sitä, että tuotehinnastot eivät vaikuta tarjouksen voittoprosessin tehokkuuteen.
