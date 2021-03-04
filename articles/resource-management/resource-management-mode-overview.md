---
title: Resurssien hallintatilojen yleiskatsaus
description: Tämä aihe tarjoaa tietoja Dynamics 365 Project Operationsin uusista resurssinhallintatoiminnosta.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118514"
---
# <a name="resource-management-modes-overview"></a>Resurssien hallintatilojen yleiskatsaus

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_


Dynamics 365 Project Operations tukee kahta tilaa, jotta voit suorittaa varaustyönkulun kokonaisuudessaan. Hallintatapa määritetään projektiparametrina, ja sitä voi muokata, jos yrityksen tarpeet muuttuvat.    

## <a name="central-mode"></a>Keskitetty tila
Jos kyseessä on organisaatio, joka keskittää resurssien kohdistuksen projekteihin, keskitetyn tilan avulla voit varmistaa, että projektipäälliköt voivat määrittää resurssitarpeet projektitasolla. Resurssitarpeiden täyttäminen delegoidaan resurssipäällikölle. Projektipäälliköt voivat hyväksyä tai hylätä resurssipäällikön ehdottamat resurssit.

![Keskitetty tila](./media/resource-management-central.png)

Jos haluat hallita resursseja keskitetyn tilan avulla, katso:

- [Yleisten varattavissa olevien resurssien delegointi tehtävään ja resurssitarpeiden luominen](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Nimettyjen resurssien varaaminen resurssitarpeista](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Resurssipyynnön lähettäminen](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Resurssipyyntöjen täyttäminen](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Ehdotetun projektiresurssin hyväksyminen tai hylkääminen resurssipyynnöstä](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybriditila
Organisaatioille, jotka tarvitsevat resurssien kohdentamisen joustavuutta, hybriditilan avulla sekä projekti päälliköt että resurssipäälliköt voivat varata resursseja.

![Hybriditila](./media/resource-management-hybrid.png)

Tuetun keskitetyn tilan prosessin lisäksi voit hallita kaikkia muita tuettuja varaustyönkulkuja hybriditilassa seuraavien aiheiden ohjeiden mukaisesti:

Resurssin varaaminen suoraan projektiin:
- [Nimettyjen varattavissa olevien resurssien varaaminen projektiryhmälle ja tehtävien kohdennus](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Resurssien varaaminen resurssitarpeesta:
- [Yleisten varattavissa olevien resurssien delegointi tehtävään ja resurssitarpeiden luominen](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Nimettyjen resurssien varaaminen resurssitarpeista](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]