---
title: Projektisopimusten hallinta
description: Tässä aiheessa on tietoja projektipohjaisten sopimusten tarkastelemisesta.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a4357d5cf184a3c6ada3ae33631694c31bb5b00
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273194"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="13fc5-103">Projektisopimusten hallinta</span><span class="sxs-lookup"><span data-stu-id="13fc5-103">Manage project contracts</span></span>

<span data-ttu-id="13fc5-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="13fc5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="13fc5-105">Dynamics 365 Project Operationsin projektisopimuksilla siepataan ja hallitaan sopimuksen sitoumuksia ja projektin laskutustietoja.</span><span class="sxs-lookup"><span data-stu-id="13fc5-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="13fc5-106">Project Operationsin projektisopimuksen rakenne on räätälöity projektipohjaiseen työhön seuraavien komponenttien avulla:</span><span class="sxs-lookup"><span data-stu-id="13fc5-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="13fc5-107">Sopimusrivit, joilla määritetään projektilaskussa ylätason komponentteina ilmoitetut erilliset työkomponentit.</span><span class="sxs-lookup"><span data-stu-id="13fc5-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="13fc5-108">Sopimusrivin tiedot, jotka määrittävät ja arvioivat kunkin ylätason komponentin tai sopimusrivin työn.</span><span class="sxs-lookup"><span data-stu-id="13fc5-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="13fc5-109">Arvio sisältää sopimusriviin sidotun työn aikataulun ja taloudelliset seikat.</span><span class="sxs-lookup"><span data-stu-id="13fc5-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="13fc5-110">Sopimusmallit ja veloitettavat komponentit määritetään kullekin sopimusriville, joka sisältää kunkin sopimusrivin ja koko sopimuksen laskutusjärjestelyn.</span><span class="sxs-lookup"><span data-stu-id="13fc5-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="13fc5-111">Kaikkien projektipohjaisten sopimusten näyttäminen</span><span class="sxs-lookup"><span data-stu-id="13fc5-111">View all project-based contracts</span></span>

<span data-ttu-id="13fc5-112">Luettelo kaikista projektisopimuksista, jotka näkyvät **Sopimukset**-luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="13fc5-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="13fc5-113">Valitse **Myynti** > **Sopimukset**.</span><span class="sxs-lookup"><span data-stu-id="13fc5-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="13fc5-114">Näkyviin tulee luettelo kaikista järjestelmässä olevista projektisopimuksista.</span><span class="sxs-lookup"><span data-stu-id="13fc5-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="13fc5-115">Valitse muita suodatettuja näkyviä valitsemalla **Näkymävalitsin** (näkymän nimen vieressä oleva avattavan luettelon nuoli).</span><span class="sxs-lookup"><span data-stu-id="13fc5-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="13fc5-116">Voit luoda omia näkymiä mukautetuilla suodatusehdoilla.</span><span class="sxs-lookup"><span data-stu-id="13fc5-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="13fc5-117">Sopimuksia voidaan luoda tai poistaa tällä luettelosivulla tai tietosivuilla.</span><span class="sxs-lookup"><span data-stu-id="13fc5-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]