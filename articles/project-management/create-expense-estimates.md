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
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075270"
---
# <a name="expense-estimates"></a><span data-ttu-id="e43e5-103">Kulujen arviot</span><span class="sxs-lookup"><span data-stu-id="e43e5-103">Expense estimates</span></span>
<span data-ttu-id="e43e5-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="e43e5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e43e5-105">Resurssipohjaisten arvioiden määrittämisen ohella Dynamics 365 Project Operationsin avulla projektipäälliköt voivat määrittää projektipohjaiset kulut kullekin projektille.</span><span class="sxs-lookup"><span data-stu-id="e43e5-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="e43e5-106">Kukin kulunimike voidaan liittää tiettyyn projektitehtävään tai kululuokkaan.</span><span class="sxs-lookup"><span data-stu-id="e43e5-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="e43e5-107">Kululuokat määritetään yleensä organisaatiotasolla.</span><span class="sxs-lookup"><span data-stu-id="e43e5-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="e43e5-108">Kunkin kululuokan hinnoittelu määritetään yleensä seuraavassa hierarkiassa:</span><span class="sxs-lookup"><span data-stu-id="e43e5-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="e43e5-109">Organisaatio</span><span class="sxs-lookup"><span data-stu-id="e43e5-109">Organization</span></span>
- <span data-ttu-id="e43e5-110">Asiakas</span><span class="sxs-lookup"><span data-stu-id="e43e5-110">Customer</span></span>
- <span data-ttu-id="e43e5-111">Tarjous/sopimus</span><span class="sxs-lookup"><span data-stu-id="e43e5-111">Quote/contract</span></span>

<span data-ttu-id="e43e5-112">Voit tarkastella, lisätä tai poistaa projektikuluja tekemällä seuraavat toimet.</span><span class="sxs-lookup"><span data-stu-id="e43e5-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="e43e5-113">Siirry kohtaan **Projektit** ja valitse projekti, jota haluat käsitellä.</span><span class="sxs-lookup"><span data-stu-id="e43e5-113">Go to **Projects** , and select the project you want to work on.</span></span>
2. <span data-ttu-id="e43e5-114">Valitse **Projektiarviot** -välilehti ja tarkastele projektikulujen luetteloa.</span><span class="sxs-lookup"><span data-stu-id="e43e5-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="e43e5-115">Lisää kulu valitsemalla **Uusi kulu**.</span><span class="sxs-lookup"><span data-stu-id="e43e5-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="e43e5-116">Voit myös valita poistettavan kulun ja valita sitten **Poista kulu**.</span><span class="sxs-lookup"><span data-stu-id="e43e5-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="e43e5-117">Kullekin kulurivinimikkeelle määritetään seuraavat määritteet:</span><span class="sxs-lookup"><span data-stu-id="e43e5-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="e43e5-118">**Luokka** : Yleiset ryhmittelyt, joita käytetään kuvaamaan kaikkia projektissa aiheutuneita kuluja.</span><span class="sxs-lookup"><span data-stu-id="e43e5-118">**Category** : The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="e43e5-119">**Alkamispäivä** : Päivämäärä, jona kulun ennustetaan syntyvän.</span><span class="sxs-lookup"><span data-stu-id="e43e5-119">**Start Date** : The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="e43e5-120">**Määrä** : Tietyn luokan kulunimikkeiden arvioitu määrä.</span><span class="sxs-lookup"><span data-stu-id="e43e5-120">**Quantity** : The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="e43e5-121">**Yksikkökustannushinta** : Yksikköhinta, jota käytettiin laskettaessa kulun kustannusta.</span><span class="sxs-lookup"><span data-stu-id="e43e5-121">**Unit Cost Price** : The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="e43e5-122">**Yksikkömyyntihinta** : Yksikköhinta, jota käytettiin laskettaessa kulun myyntihintoja.</span><span class="sxs-lookup"><span data-stu-id="e43e5-122">**Unit Sales Price** : The unit price used to calculate the sale prices of the expense.</span></span>

