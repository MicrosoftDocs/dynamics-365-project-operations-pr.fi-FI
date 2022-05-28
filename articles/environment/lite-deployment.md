---
title: Project Operationsin käyttöönotto – lite
description: Tässä aiheessa on tietoja siitä, miten voit asentaa Project Operationsin lite – kauppa proformalaskutukseen -käyttöönoton.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580728"
---
# <a name="deploy-project-operations---lite"></a>Project Operationsin käyttöönotto – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_



Project Operations tukee useita käyttöönottomalleja. Lisätietoja parhaan käyttöönottomallin valinnasta on kohdassa [Käyttöönottotyypit](determine-deployment-type.md).


> [!IMPORTANT]
> Tämä Lite-käytöönotto – kauppa proformalaskutukseen, -käytöönotto johtaa **Project Operationsin Vain Dataverse -käyttöönottoon**.

- [Project Operationsin asentaminen uuteen Dataverse-ympäristöön](#new)
- [Asentaminen olemassa olevaan Dataverse-ympäristöön](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Project Operationsin asentaminen uuteen Dataverse-ympäristöön

1. [Yleisenä tai Power Platform -järjestelmänvalvojana](/power-platform/admin/global-service-administrators-can-administer-without-license), jolla on Project Operations -käyttöoikeus, voit luoda uuden Dataverse-ympäristön [Power Platform -hallintakeskuksessa](https://admin.powerplatform.com). Varmista, että **luot tietokannan tätä ympäristöä varten** ja että **Dynamics 365 -sovellukset** ovat käytössä. Lisätietoja on kohdassa [Ympäristöjen luominen ja hallinta Power Platform -hallintakeskuksessa](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Valitse **Microsoft Dynamics 365 Project Operations** Dynamics 365 -sovellusten käyttöönottoluettelosta.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Project Operationsin asentaminen aiemmin luotuun Dataverse-ympäristöön
1. Varmista, että ympäristölle ei ole määritetty [kaksoiskirjoitusta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), sillä silloin asennus asentaa [Project Operationsin resurssi/ei-varastoitu skenaarioiden](project-operations-integrated-deployment-overview.md) ominaisuudet.
2. [Yleisenä tai Power Platform -järjestelmänvalvojana](/power-platform/admin/global-service-administrators-can-administer-without-license), jolla on Project Operations -käyttöoikeus, etsi [Power Platform -hallintakeskuksesta](https://admin.powerplatform.com) ympäristö, johon haluat asentaa Project Operationsin.
3. Asenna **Microsoft Dynamics 365 Project Operations** Dynamics 365 -sovellusten käyttöönottoluettelosta. Lisätietoja on aiheessa [Dynamics 365 -sovellusten hallinta](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
