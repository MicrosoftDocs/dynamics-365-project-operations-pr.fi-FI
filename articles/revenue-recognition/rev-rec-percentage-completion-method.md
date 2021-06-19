---
title: Kiinteähintaisen tuoton arviointiprojektit
description: Tässä aiheessa on tietoja kiinteähintaisesta tuotosta projekteissa.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013797"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="2b09c-103">Kiinteähintaisen tuoton arviointiprojektit</span><span class="sxs-lookup"><span data-stu-id="2b09c-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="2b09c-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="2b09c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2b09c-105">Kun luot projektisopimusrivin, jolla on seuraavat määritteet Dynamics 365 Project Operationsin Microsoft Dataversessä, järjestelmä luo automaattisesti kiinteähintaisen tuoton arviointiprojektin.</span><span class="sxs-lookup"><span data-stu-id="2b09c-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="2b09c-106">Tämän projektin tiedot perustuvat seuraaviin:</span><span class="sxs-lookup"><span data-stu-id="2b09c-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="2b09c-107">Kiinteän hinnan laskutusmenetelmä.</span><span class="sxs-lookup"><span data-stu-id="2b09c-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="2b09c-108">Liittyvä projekti.</span><span class="sxs-lookup"><span data-stu-id="2b09c-108">An associated project.</span></span>
  - <span data-ttu-id="2b09c-109">Vähintään yksi välitavoite, joka on määritetty **Laskutusaikataulu**-välilehdellä **Projektisopimuksen rivi** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2b09c-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="2b09c-110">Kiinteähintaisen tuoton arviointiprojektien tarkastelu</span><span class="sxs-lookup"><span data-stu-id="2b09c-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="2b09c-111">Voit tarkastella kiinteähintaisen tuoton arviointiprojekteja suorittamalla seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="2b09c-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="2b09c-112">Siirry Dynamics 365 Finance -ympäristössä kohtaan **Projektinhallinta ja kirjanpito** > **Projektit** > **Kiinteähintaisen tuoton arviointiprojektit**.</span><span class="sxs-lookup"><span data-stu-id="2b09c-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="2b09c-113">Valitse tarkasteltava projekti ja kaksoisnapsauta **Arviointiprojektin tunnusta** avataksesi tietueen ja tarkastellaksesi projektin tietoja.</span><span class="sxs-lookup"><span data-stu-id="2b09c-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="2b09c-114">Laajenna **Projekti**-välilehti. **Valitut projektit** -ruudukossa näkyy yksi projekti.</span><span class="sxs-lookup"><span data-stu-id="2b09c-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="2b09c-115">Järjestelmä käyttää tätä oletusprojektina, koska se on projektisopimuksen riviin liittyvä projekti.</span><span class="sxs-lookup"><span data-stu-id="2b09c-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="2b09c-116">Jos haluat muuttaa kytkentää, valitse lisää projekteja ja lisää ne **Valitut projektit**-ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="2b09c-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="2b09c-117">Jos ruudukossa valitaan useita projekteja, projektin valmistumisprosentti- ja tuottoarviot lasketaan yhteen kaikista valituista projekteista.</span><span class="sxs-lookup"><span data-stu-id="2b09c-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="2b09c-118">Projektikustannukset, tuottoprofiili, kustannusmalli ja kausikoodi voidaan määrittää manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="2b09c-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="2b09c-119">Jos niitä ei ole määritetty manuaalisesti, arvot ovat oletusarvoja, jotka on saatu ensimmäisen arvion laskemisen aikana projektista käyttäen sääntöjä, jotka on määritetty projektin kustannus- ja tuottoprofiileille.</span><span class="sxs-lookup"><span data-stu-id="2b09c-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]