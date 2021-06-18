---
title: Project Operationsin käyttöönotto – lite
description: Tässä aiheessa on tietoja siitä, miten voit asentaa Project Operationsin lite – kauppa proformalaskutukseen -käyttöönoton.
author: stsporen
ms.date: 10/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb1f1ad86e19d84d68a40b32b2fdb08dc4777a78
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995527"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="8c26f-103">Project Operationsin käyttöönotto – lite</span><span class="sxs-lookup"><span data-stu-id="8c26f-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="8c26f-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="8c26f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8c26f-105">Project Operations tukee useita käyttöönottomalleja.</span><span class="sxs-lookup"><span data-stu-id="8c26f-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="8c26f-106">Lisätietoja parhaan käyttöönottomallin valinnasta on kohdassa [Käyttöönottotyypit](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="8c26f-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="8c26f-107">Tämä Lite-käytöönotto – kauppa proformalaskutukseen, -käytöönotto johtaa **Project Operationsin Vain Common Data Service -käyttöönottoon**.</span><span class="sxs-lookup"><span data-stu-id="8c26f-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="8c26f-108">Project Operationsin asentaminen uuteen CDS-ympäristöön</span><span class="sxs-lookup"><span data-stu-id="8c26f-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="8c26f-109">Asentaminen olemassa olevaan CDS-ympäristöön</span><span class="sxs-lookup"><span data-stu-id="8c26f-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="8c26f-110">Project Operationsin asentaminen uuteen CDS-ympäristöön</span><span class="sxs-lookup"><span data-stu-id="8c26f-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="8c26f-111">[Yleisenä tai Power Platform -järjestelmänvalvojana](/power-platform/admin/global-service-administrators-can-administer-without-license), jolla on Project Operations -käyttöoikeus, voit luoda uuden CDS-ympäristön [Power Platform -hallintakeskuksessa](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="8c26f-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="8c26f-112">Varmista, että **CDS-tietokanta** ja **Dynamics 365 -sovellukset** ovat käytössä.</span><span class="sxs-lookup"><span data-stu-id="8c26f-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="8c26f-113">Lisätietoja on kohdassa [Ympäristöjen luominen ja hallinta Power Platform -hallintakeskuksessa](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="8c26f-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="8c26f-114">Valitse **Microsoft Dynamics 365 Project Operations** Dynamics 365 -sovellusten käyttöönottoluettelosta.</span><span class="sxs-lookup"><span data-stu-id="8c26f-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="8c26f-115">Project Operationsin asentaminen aiemmin luotuun CDS-ympäristöön</span><span class="sxs-lookup"><span data-stu-id="8c26f-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="8c26f-116">[Yleisenä tai Power Platform -järjestelmänvalvojana](/power-platform/admin/global-service-administrators-can-administer-without-license), jolla on Project Operations -käyttöoikeus, etsi [Power Platform -hallintakeskuksesta](https://admin.powerplatform.com) ympäristö, johon haluat asentaa Project Operationsin.</span><span class="sxs-lookup"><span data-stu-id="8c26f-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="8c26f-117">Asenna **Microsoft Dynamics 365 Project Operations** Dynamics 365 -sovellusten käyttöönottoluettelosta.</span><span class="sxs-lookup"><span data-stu-id="8c26f-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="8c26f-118">Lisätietoja on aiheessa [Dynamics 365 -sovellusten hallinta](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="8c26f-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]