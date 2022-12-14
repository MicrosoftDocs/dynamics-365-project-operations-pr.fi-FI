---
title: Project Operations Liten käyttöönotto
description: Tässä artikkelissa on tietoja siitä, miten asennetaan Project Operationsin lite -käyttöönotto – kauppa proformalaskutukseen.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810974"
---
# <a name="deploy-project-operations-lite"></a>Project Operations Liten käyttöönotto

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_



Project Operations tukee useita käyttöönottomalleja. Lisätietoja parhaan käyttöönottomallin valinnasta on kohdassa [Käyttöönottotyypit](determine-deployment-type.md).


> [!IMPORTANT]
> Tämä Lite-käytöönotto – kauppa proformalaskutukseen, -käytöönotto johtaa **Project Operationsin Vain Dataverse -käyttöönottoon**.

- [Project Operationsin asentaminen uuteen Dataverse-ympäristöön](#new)
- [Asentaminen olemassa olevaan Dataverse-ympäristöön](#existing)
- [Asenna olemassa olevaan Dataverse-ympäristöön, jossa on kaksoiskirjoituskomponentteja](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Project Operations Liten asentaminen uuteen Dataverse-ympäristöön

1. [Yleisenä tai Power Platform -järjestelmänvalvojana](/power-platform/admin/global-service-administrators-can-administer-without-license), jolla on Project Operations -käyttöoikeus, voit luoda uuden Dataverse-ympäristön [Power Platform -hallintakeskuksessa](https://admin.powerplatform.com). Varmista, että **luot tietokannan tätä ympäristöä varten** ja että **Dynamics 365 -sovellukset** ovat käytössä. Lisätietoja on kohdassa [Ympäristöjen luominen ja hallinta Power Platform -hallintakeskuksessa](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Valitse **Microsoft Dynamics 365 Project Operations** Dynamics 365 -sovellusten käyttöönottoluettelosta.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Project Operations Liten asentaminen aiemmin luotuun Dataverse-ympäristöön 
1. [Yleisenä tai Power Platform -järjestelmänvalvojana](/power-platform/admin/global-service-administrators-can-administer-without-license), jolla on Project Operations -käyttöoikeus, etsi [Power Platform -hallintakeskuksesta](https://admin.powerplatform.com) ympäristö, johon haluat asentaa Project Operationsin.
1. Asenna **Microsoft Dynamics 365 Project Operations** Dynamics 365 -sovellusten käyttöönottoluettelosta. Lisätietoja on aiheessa [Dynamics 365 -sovellusten hallinta](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Project Operations Liten asentaminen olemassa olevaan Dataverse-ympäristöön, jossa kaksoiskirjoitusratkaisut ovat jo olemassa

Jos haluat jatkaa Project Operationsin käyttöä Lite-käyttöönottotilassa, toimi seuraavasti:

1. [Yleisenä tai Power Platform -järjestelmänvalvojana](/power-platform/admin/global-service-administrators-can-administer-without-license), jolla on Project Operations -käyttöoikeus, etsi [Power Platform -hallintakeskuksesta](https://admin.powerplatform.com) ympäristö, johon haluat asentaa Project Operationsin.
1. Asenna **Microsoft Dynamics 365 Project Operations** Dynamics 365 -sovellusten käyttöönottoluettelosta. Lisätietoja on aiheessa [Dynamics 365 -sovellusten hallinta](/power-platform/admin/manage-apps).
1. Koska ympäristössäsi on kaksoiskirjoituskomponentteja, jotka auttavat asennettujen rahoitus- ja toimintasovellusten integroinnissa, Project Operationsin asennus asentaa myös toiminnot ja laajennukset, joita tarvitaan projektiin liittyvien tietojen integroimiseen rahoitus- ja toimintosovelluksiin. Koska haluat suorittaa Project Operations -toimintoja Lite-käyttöönotossa, nämä integrointikomponentit on poistettava, koska ne luovat rajoituksia ja ylimääräisiä kustannuksia Lite-käyttöönottoskenaarioille. Poista manuaalisesti ratkaisut **Dynamics 365 Project Operations -kaksoiskirjoitus** ja **Dynamics 365 Project Operations -kaksoiskirjoituksen entiteettikartat** näiden komponenttien poistamista varten.
1. Siirrykohtaan **Project Operations -> Asetukset -> Parametrit**. Avaa **Projektiparametri**-tietosivu ja määritä **Ratkaisun päivityksen toiminta** -kentän arvoksi  **vain Lite**. Näin varmistetaan, että projektitoimintojen myöhemmät päivitykset eivät tuo integrointiosia takaisin Project Operationsiin.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
