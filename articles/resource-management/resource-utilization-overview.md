---
title: Resurssin käytön yleiskatsaus
description: Tässä aiheessa on tietoja resurssin käytöstä Project Operationsissa.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d66b5fc642ef53adf1169ce891a7a5fa26b07d6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279314"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="d5db7-103">Resurssin käytön yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d5db7-103">Resource utilization overview</span></span>

<span data-ttu-id="d5db7-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="d5db7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d5db7-105">Resursseilla voi olla tavoite laskutettavalle käytölle.</span><span class="sxs-lookup"><span data-stu-id="d5db7-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="d5db7-106">Tämä tavoitekäyttö määritetään resurssin oletusroolin määritteeksi tai se määritetään yksittäisen varattavan resurssin tietueessa.</span><span class="sxs-lookup"><span data-stu-id="d5db7-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="d5db7-107">Käytön laskennat perustuvat todellisiin tunteihin, jotka resurssit ovat raportoineet hyväksyttyjen aikakirjausten kautta.</span><span class="sxs-lookup"><span data-stu-id="d5db7-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="d5db7-108">Käytön laskennassa käytetään seuraavia kaavoja:</span><span class="sxs-lookup"><span data-stu-id="d5db7-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="d5db7-109">Lakutettava käyttö = Laskutettavat todelliset tunnit ÷ Resurssin kapasiteetti</span><span class="sxs-lookup"><span data-stu-id="d5db7-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="d5db7-110">Ei-laskutettava käyttö = Todellinen aika, jonka laskutustyyppi ID = Ei-laskutettava, Täydentävä tai Ei käytettävissä ÷ Resurssin kapasiteetti</span><span class="sxs-lookup"><span data-stu-id="d5db7-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="d5db7-111">Sisäinen = Todellinen aika ilman myyntisopimusta ÷ Resurssin kapasiteetti</span><span class="sxs-lookup"><span data-stu-id="d5db7-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="d5db7-112">Resurssin kapasiteetti = Resurssin työtunnit – Poissa toimistosta – Muut kuin työpäivät</span><span class="sxs-lookup"><span data-stu-id="d5db7-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="d5db7-113">**Resurssien käyttöaste** -näkymä on **Resurssit**-ruudussa.</span><span class="sxs-lookup"><span data-stu-id="d5db7-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="d5db7-114">Kukin ruudukon solu kuvaa resurssin laskutettavaa käyttöprosenttia kauden, esimerkiksi päivän, viikon tai kuukauden, aikana.</span><span class="sxs-lookup"><span data-stu-id="d5db7-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="d5db7-115">Solujen värittämiseen käytetään seuraavia kaavoja:</span><span class="sxs-lookup"><span data-stu-id="d5db7-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="d5db7-116">**Vihreä**: laskutettava käyttö > = resurssin tavoitekäyttö</span><span class="sxs-lookup"><span data-stu-id="d5db7-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="d5db7-117">**Keltainen**: tavoitekäyttö - 20 <= laskutettava käyttö < tavoitekäyttö</span><span class="sxs-lookup"><span data-stu-id="d5db7-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="d5db7-118">**Punainen**: laskutettava käyttö < tavoitekäyttö - 20</span><span class="sxs-lookup"><span data-stu-id="d5db7-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="d5db7-119">Koska **Resurssien käyttöaste** -näkymä perustuu aikataulutaulutaulukkoon, voit suodattaa tuloksia käyttämällä aikataulutaulukon suodatustoimintoja.</span><span class="sxs-lookup"><span data-stu-id="d5db7-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="d5db7-120">Ruudukko edellyttää, että määrität kohteen käytön joko roolille tai yksittäiselle resurssille.</span><span class="sxs-lookup"><span data-stu-id="d5db7-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="d5db7-121">Tämä määritys tehdään valitsemalla **Resurssit** > **Resurssiroolit**.</span><span class="sxs-lookup"><span data-stu-id="d5db7-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="d5db7-122">Lisäksi jokaiselle varattavissa olevalle resurssille on määritettävä oletusrooli.</span><span class="sxs-lookup"><span data-stu-id="d5db7-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="d5db7-123">Valitse **Resurssit** > **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="d5db7-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="d5db7-124">Varmista **Project Service** -välilehdessä, että resurssin rooli on määritetty ja että **Onko oletus** -kentän arvo on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d5db7-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="d5db7-125">Voit lisätä muita rooleja, joiden **Onko oletus** = **Ei**.</span><span class="sxs-lookup"><span data-stu-id="d5db7-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="d5db7-126">Roolia, jossa **Onko oletus** = **Kyllä** käytetään määrittämään resurssin käyttöaste tavoitteen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="d5db7-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="d5db7-127">**Project Service** -välilehdellä voit myös määrittää yksittäisen tavoitekäytön resurssille.</span><span class="sxs-lookup"><span data-stu-id="d5db7-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="d5db7-128">Käytön laskenta käyttää sen jälkeen tätä tavoitekäyttöastetta määrittääkseen resurssin tavoitteen resurssin oletusroolin tavoitteen asemesta.</span><span class="sxs-lookup"><span data-stu-id="d5db7-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="d5db7-129">Resurssin käyttöaste näytetään ainoastaan, jos resurssilla on hyväksyttyä laskutettavaa aikaa sen jakson aikana, joka näkyy ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="d5db7-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]