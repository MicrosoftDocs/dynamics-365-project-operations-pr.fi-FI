---
title: Resurssien hallintatilojen yleiskatsaus
description: Tässä artikkelissa on tietoja Dynamics 365 Project Operationsin resurssinhallintatoiminnosta.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dd50d12686a6ad17f6a95ccf0c2f1447cc470bf7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928428"
---
# <a name="resource-management-modes-overview"></a>Resurssien hallintatilojen yleiskatsaus

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_


Dynamics 365 Project Operations tukee kahta tilaa, jotta voit suorittaa yleisen varaustyönkulun. Hallintatapa määritetään projektiparametrina, ja sitä voi muokata, jos yrityksen tarpeet muuttuvat.    

## <a name="central-mode"></a>Keskitetty tila
Jos kyseessä on organisaatio, joka keskittää resurssien kohdistuksen projekteihin, keskitetyn tilan avulla voit varmistaa, että projektipäälliköt voivat määrittää resurssitarpeet projektitasolla. Resurssitarpeiden täyttäminen delegoidaan resurssipäällikölle. Projektipäälliköt voivat hyväksyä tai hylätä resurssipäällikön ehdottamat resurssit.

![Keskitetty tila.](./media/resource-management-central.png)

Jos haluat hallita resursseja keskitetyn tilan avulla, katso:

- [Yleisten varattavissa olevien resurssien delegointi tehtävään ja resurssitarpeiden luominen](/dynamics365/project-service/assign-generic-bookable-resource)
- [Nimettyjen resurssien varaaminen resurssitarpeista](/dynamics365/project-service/book-named-resource)
- [Resurssipyynnön lähettäminen](/dynamics365/project-service/submit-resource-request)
- [Resurssipyyntöjen täyttäminen](/dynamics365/project-service/resource-management-fulfill-requests)
- [Ehdotetun projektiresurssin hyväksyminen tai hylkääminen resurssipyynnöstä](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybriditila
Organisaatioille, jotka tarvitsevat resurssien kohdentamisen joustavuutta, hybriditilan avulla sekä projekti päälliköt että resurssipäälliköt voivat varata resursseja.

![Hybriditila.](./media/resource-management-hybrid.png)

Tuetun keskitetyn tilan prosessin lisäksi voit hallita kaikkia muita tuettuja varaustyönkulkuja hybriditilassa seuraavien artikkelien ohjeiden mukaisesti:

Resurssin varaaminen suoraan projektiin:
- [Nimettyjen varattavissa olevien resurssien varaaminen projektiryhmälle ja tehtävien kohdennus](/dynamics365/project-service/assign-named-bookable-resource)

Resurssien varaaminen resurssitarpeesta:
- [Yleisten varattavissa olevien resurssien delegointi tehtävään ja resurssitarpeiden luominen](/dynamics365/project-service/assign-generic-bookable-resource)
- [Nimettyjen resurssien varaaminen resurssitarpeista](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]