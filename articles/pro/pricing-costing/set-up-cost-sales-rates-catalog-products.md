---
title: Kustannus- ja myyntihintojen määrittäminen luettelotuotteille – lite
description: Tässä artikkelissa on tietoja siitä, miten tuoteluettelon nimikkeiden kustannus- ja myyntihinnat määritetään.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917388"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Kustannus- ja myyntihintojen määrittäminen luettelotuotteille – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_


Tuoteluettelonimikkeiden hinnoittelu määritetään Dynamics 365 Project Operationsissa samoin kuin Dynamics 365 Salesissa.

Project Operationsissa tuotteita ei voi arvioida tai käyttää projekteissa, joten tuoteluettelohintoja ei tarvitse määrittää tarjousten ja sopimusten projektihinnastoihin.

Määritä tuoteluettelohinnat tarjouksen, sopimuksen tai tilin **Tuotehinta**-kentän avulla. Älä määritä tuoteluettelohintoja projektin hinnastoihin. Projektihinnastot ovat yksinomaisia Project Operationsia varten. Sovelluskohtainen liiketoimintalogiikka kopioi hinnastot tarjouksesta sopimukseen. Tuloksena on palvelussopimuskohtainen hinnasto Kopiointitoiminto voi viivyttää tarjouksen voittoprosessia, jos tarjouksen projektihinnasto muuttuu liian suureksi. Tuotehinnastoja ei kopioida, kun luodaan palvelusopimuksille mukautettuja hinnastoja. Koska kopiointia ei tehdä, tämä ei vaikuta tarjousprosessin suorituskykyyn.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]