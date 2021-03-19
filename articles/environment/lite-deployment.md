---
title: Project Operationsin käyttöönotto – lite
description: Tässä aiheessa on tietoja siitä, miten voit asentaa Project Operationsin lite – kauppa proformalaskutukseen -käyttöönoton.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0af8067fc0673890a317ac6f4e62d74b7f4eebca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290085"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="c0dba-103">Project Operationsin käyttöönotto – lite</span><span class="sxs-lookup"><span data-stu-id="c0dba-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="c0dba-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="c0dba-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c0dba-105">Project Operations tukee useita käyttöönottomalleja.</span><span class="sxs-lookup"><span data-stu-id="c0dba-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="c0dba-106">Lisätietoja parhaan käyttöönottomallin valinnasta on kohdassa [Käyttöönottotyypit](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="c0dba-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="c0dba-107">Tämä Lite-käytöönotto – kauppa proformalaskutukseen, -käytöönotto johtaa **Project Operationsin Vain Common Data Service -käyttöönottoon**.</span><span class="sxs-lookup"><span data-stu-id="c0dba-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="c0dba-108">Project Operationsin asentaminen uuteen CDS-ympäristöön</span><span class="sxs-lookup"><span data-stu-id="c0dba-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="c0dba-109">Asentaminen olemassa olevaan CDS-ympäristöön</span><span class="sxs-lookup"><span data-stu-id="c0dba-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="c0dba-110">Project Operationsin asentaminen uuteen CDS-ympäristöön</span><span class="sxs-lookup"><span data-stu-id="c0dba-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="c0dba-111">[Yleisenä tai Power Platform -järjestelmänvalvojana](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license), jolla on Project Operations -käyttöoikeus, voit luoda uuden CDS-ympäristön [Power Platform -hallintakeskuksessa](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="c0dba-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="c0dba-112">Varmista, että **CDS-tietokanta** ja **Dynamics 365 -sovellukset** ovat käytössä.</span><span class="sxs-lookup"><span data-stu-id="c0dba-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="c0dba-113">Lisätietoja on kohdassa [Ympäristöjen luominen ja hallinta Power Platform -hallintakeskuksessa](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="c0dba-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="c0dba-114">Valitse **Microsoft Dynamics 365 Project Operations** Dynamics 365 -sovellusten käyttöönottoluettelosta.</span><span class="sxs-lookup"><span data-stu-id="c0dba-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="c0dba-115">Project Operationsin asentaminen aiemmin luotuun CDS-ympäristöön</span><span class="sxs-lookup"><span data-stu-id="c0dba-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="c0dba-116">[Yleisenä tai Power Platform -järjestelmänvalvojana](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license), jolla on Project Operations -käyttöoikeus, etsi [Power Platform -hallintakeskuksesta](https://admin.powerplatform.com) ympäristö, johon haluat asentaa Project Operationsin.</span><span class="sxs-lookup"><span data-stu-id="c0dba-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="c0dba-117">Asenna **Microsoft Dynamics 365 Project Operations** Dynamics 365 -sovellusten käyttöönottoluettelosta.</span><span class="sxs-lookup"><span data-stu-id="c0dba-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="c0dba-118">Lisätietoja on aiheessa [Dynamics 365 -sovellusten hallinta](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="c0dba-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]