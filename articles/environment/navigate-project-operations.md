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
ms.openlocfilehash: 50b44b014fcbb730b273322390227ae82cbdcefc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289995"
---
# <a name="navigate-project-operations"></a><span data-ttu-id="cf85c-103">Project Operationsissa siirtyminen</span><span class="sxs-lookup"><span data-stu-id="cf85c-103">Navigate Project Operations</span></span>

<span data-ttu-id="cf85c-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="cf85c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="cf85c-105">Dynamics 365 Project Operations resurssi-/ei-varastoitaville skenaarioille sisältää kaksi komponenttia:</span><span class="sxs-lookup"><span data-stu-id="cf85c-105">Dynamics 365 Project Operations for resource/non-stocked scenarios consists of two components:</span></span> 

 - <span data-ttu-id="cf85c-106">**Common Data Service (CDS) -ympäristön Project Operations**: tämä komponentti sisältää ominaisuuksia ja prosesseja mahdollisuudesta proformalaskutukseen.</span><span class="sxs-lookup"><span data-stu-id="cf85c-106">**Project Operations on Common Data Service (CDS) environment**: This component covers capabilities and processes from opportunity to proforma invoicing.</span></span> 
 - <span data-ttu-id="cf85c-107">**Dynamics 365 Finance -ympäristön projektinhallinta ja kirjanpito**: tämä komponentti sisältää kulujenhallintaominaisuuksia, projektin kirjanpidon ja tuloutuksen.</span><span class="sxs-lookup"><span data-stu-id="cf85c-107">**Project management and accounting on Dynamics 365 Finance environment**: This component covers expense management capabilities, project accounting, and revenue recognition.</span></span> 

<span data-ttu-id="cf85c-108">Kun Project Operations on valmisteltu tässä aiheessa kuvatulla tavalla, Project Operationsin molempia komponentteja on helppo käyttää Lifecycle Servicesin (LCS) **Ympäristön tiedot** -sivulta.</span><span class="sxs-lookup"><span data-stu-id="cf85c-108">After you provision Project Operations as described in this topic, the Lifecycle Services (LCS) **Environment details** page provides easy access to both components of Project Operations.</span></span>  

<span data-ttu-id="cf85c-109">Siirry Project Operationsiin CDS-ympäristössä käyttämällä ympäristön nimeä kohdassa **Common Data Servicen ympäristön nimi**.</span><span class="sxs-lookup"><span data-stu-id="cf85c-109">Use the environment name in the section, **Common Data Service Environment Name** to navigate to Project Operations on a CDS environment.</span></span> 

  ![Common Data Service -ympäristön nimi](./media/environment-name.PNG)

<span data-ttu-id="cf85c-111">Siirry Financessa **Projektinhallinta ja kirjanpito** -moduuliin valitsemalla **Kirjautuminen** > **Kirjautuminen ympäristöön**.</span><span class="sxs-lookup"><span data-stu-id="cf85c-111">Select **Login** > **Log on to environment** to navigate to the **Project management and accounting** module in Finance.</span></span>  

   ![Kirjautuminen Financeen](./media/environment-login.PNG)

> [!NOTE]
> <span data-ttu-id="cf85c-113">Project Operationsia voi käyttää Common Data Servicessa ja **Projektinhallinta ja kirjanpito** -moduulissa suoraan kummankin URL-osoitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="cf85c-113">You can access Project Operations in the Common Data Service and the **Project management and accounting** module directly by using their respective URLs.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]