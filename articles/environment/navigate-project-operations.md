---
title: Project Operationsissa siirtyminen
description: Tässä aiheessa on tietoja Project Operationsin käyttämisestä Lifecycle Servicesessa.
author: sigitac
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d948c1cfe2d95e61f2405a9a23e7045af678ae40
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642044"
---
# <a name="navigate-project-operations"></a><span data-ttu-id="bf5e8-103">Project Operationsissa siirtyminen</span><span class="sxs-lookup"><span data-stu-id="bf5e8-103">Navigate Project Operations</span></span>

<span data-ttu-id="bf5e8-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="bf5e8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="bf5e8-105">Dynamics 365 Project Operations resurssi-/ei-varastoitaville skenaarioille sisältää kaksi komponenttia:</span><span class="sxs-lookup"><span data-stu-id="bf5e8-105">Dynamics 365 Project Operations for resource/non-stocked scenarios consists of two components:</span></span> 

 - <span data-ttu-id="bf5e8-106">**Common Data Service (CDS) -ympäristön Project Operations**: tämä komponentti sisältää ominaisuuksia ja prosesseja mahdollisuudesta proformalaskutukseen.</span><span class="sxs-lookup"><span data-stu-id="bf5e8-106">**Project Operations on Common Data Service (CDS) environment**: This component covers capabilities and processes from opportunity to proforma invoicing.</span></span> 
 - <span data-ttu-id="bf5e8-107">**Dynamics 365 Finance -ympäristön projektinhallinta ja kirjanpito**: tämä komponentti sisältää kulujenhallintaominaisuuksia, projektin kirjanpidon ja tuloutuksen.</span><span class="sxs-lookup"><span data-stu-id="bf5e8-107">**Project management and accounting on Dynamics 365 Finance environment**: This component covers expense management capabilities, project accounting, and revenue recognition.</span></span> 

<span data-ttu-id="bf5e8-108">Kun Project Operations on valmisteltu tässä aiheessa kuvatulla tavalla, Project Operationsin molempia komponentteja on helppo käyttää Lifecycle Servicesin (LCS) **Ympäristön tiedot** -sivulta.</span><span class="sxs-lookup"><span data-stu-id="bf5e8-108">After you provision Project Operations as described in this topic, the Lifecycle Services (LCS) **Environment details** page provides easy access to both components of Project Operations.</span></span>  

<span data-ttu-id="bf5e8-109">Siirry Project Operationsiin CDS-ympäristössä käyttämällä ympäristön nimeä kohdassa **Common Data Servicen ympäristön nimi**.</span><span class="sxs-lookup"><span data-stu-id="bf5e8-109">Use the environment name in the section, **Common Data Service Environment Name** to navigate to Project Operations on a CDS environment.</span></span> 

  ![Common Data Service -ympäristön nimi](./media/environment-name.PNG)

<span data-ttu-id="bf5e8-111">Siirry Financessa **Projektinhallinta ja kirjanpito** -moduuliin valitsemalla **Kirjautuminen** > **Kirjautuminen ympäristöön**.</span><span class="sxs-lookup"><span data-stu-id="bf5e8-111">Select **Login** > **Log on to environment** to navigate to the **Project management and accounting** module in Finance.</span></span>  

   ![Kirjautuminen Financeen](./media/environment-login.PNG)

> [!NOTE]
> <span data-ttu-id="bf5e8-113">Project Operationsia voi käyttää Common Data Servicessa ja **Projektinhallinta ja kirjanpito** -moduulissa suoraan kummankin URL-osoitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="bf5e8-113">You can access Project Operations in the Common Data Service and the **Project management and accounting** module directly by using their respective URLs.</span></span> 
