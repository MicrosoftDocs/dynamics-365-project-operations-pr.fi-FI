---
title: Kulujen arviot
description: Tässä aiheessa on tietoja projektipohjaisten kulujen määrittämisestä tai arvioinnista.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908076"
---
# <a name="expense-estimates"></a><span data-ttu-id="02fbd-103">Kulujen arviot</span><span class="sxs-lookup"><span data-stu-id="02fbd-103">Expense estimates</span></span>
<span data-ttu-id="02fbd-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="02fbd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="02fbd-105">Resurssipohjaisten arvioiden määrittämisen ohella Dynamics 365 Project Operationsin avulla projektipäälliköt voivat määrittää projektipohjaiset kulut kullekin projektille.</span><span class="sxs-lookup"><span data-stu-id="02fbd-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="02fbd-106">Kukin kulunimike voidaan liittää tiettyyn projektitehtävään tai kululuokkaan.</span><span class="sxs-lookup"><span data-stu-id="02fbd-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="02fbd-107">Kululuokat määritetään yleensä organisaatiotasolla.</span><span class="sxs-lookup"><span data-stu-id="02fbd-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="02fbd-108">Kunkin kululuokan hinnoittelu määritetään yleensä seuraavassa hierarkiassa:</span><span class="sxs-lookup"><span data-stu-id="02fbd-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="02fbd-109">Organisaatio</span><span class="sxs-lookup"><span data-stu-id="02fbd-109">Organization</span></span>
- <span data-ttu-id="02fbd-110">Asiakas</span><span class="sxs-lookup"><span data-stu-id="02fbd-110">Customer</span></span>
- <span data-ttu-id="02fbd-111">Tarjous/sopimus</span><span class="sxs-lookup"><span data-stu-id="02fbd-111">Quote/contract</span></span>

<span data-ttu-id="02fbd-112">Voit tarkastella, lisätä tai poistaa projektikuluja tekemällä seuraavat toimet.</span><span class="sxs-lookup"><span data-stu-id="02fbd-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="02fbd-113">Siirry kohtaan **Projektit** ja valitse projekti, jota haluat käsitellä.</span><span class="sxs-lookup"><span data-stu-id="02fbd-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="02fbd-114">Valitse **Projektiarviot**-välilehti ja tarkastele projektikulujen luetteloa.</span><span class="sxs-lookup"><span data-stu-id="02fbd-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="02fbd-115">Lisää kulu valitsemalla **Uusi kulu**.</span><span class="sxs-lookup"><span data-stu-id="02fbd-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="02fbd-116">Voit myös valita poistettavan kulun ja valita sitten **Poista kulu**.</span><span class="sxs-lookup"><span data-stu-id="02fbd-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="02fbd-117">Kullekin kulurivinimikkeelle määritetään seuraavat määritteet:</span><span class="sxs-lookup"><span data-stu-id="02fbd-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="02fbd-118">**Luokka**: Yleiset ryhmittelyt, joita käytetään kuvaamaan kaikkia projektissa aiheutuneita kuluja.</span><span class="sxs-lookup"><span data-stu-id="02fbd-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="02fbd-119">**Alkamispäivä**: Päivämäärä, jona kulun ennustetaan syntyvän.</span><span class="sxs-lookup"><span data-stu-id="02fbd-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="02fbd-120">**Määrä**: Tietyn luokan kulunimikkeiden arvioitu määrä.</span><span class="sxs-lookup"><span data-stu-id="02fbd-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="02fbd-121">**Yksikkökustannushinta**: Yksikköhinta, jota käytettiin laskettaessa kulun kustannusta.</span><span class="sxs-lookup"><span data-stu-id="02fbd-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="02fbd-122">**Yksikkömyyntihinta**: Yksikköhinta, jota käytettiin laskettaessa kulun myyntihintoja.</span><span class="sxs-lookup"><span data-stu-id="02fbd-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

