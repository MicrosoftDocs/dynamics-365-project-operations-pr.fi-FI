---
title: Myyntihinnaston määrittäminen
description: Tämä aihe tarjoaa tietoja projektin hinnoittelun myyntihinnastoista.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: eb8dfa61a2d17ba644daf1552889cbcde0f1e47a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176247"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="43997-103">Myyntihinnaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="43997-103">Set up a sales price list</span></span>

<span data-ttu-id="43997-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="43997-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="43997-105">Projektihinnastolla on projektitarjousten ja -sopimusten osalta erilainen korvausmalli kuin tuotehinnastolla.</span><span class="sxs-lookup"><span data-stu-id="43997-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="43997-106">Tuoteluetteloperusteisella tarjousrivillä tarjousrivin hinta voidaan korvata suoraan roolien ja luokkien hinnoilla, koska kukin tarjousrivi viittaa tasan yhteen luettelonimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="43997-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="43997-107">Projektiperusteisella tarjousrivillä tarjousrivin hintaa sen sijaan ei voida korvata suoraan roolien ja luokkien hinnoilla.</span><span class="sxs-lookup"><span data-stu-id="43997-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="43997-108">Käytä projektihinnastoa kahden erillisen korvausmallin kanssa.</span><span class="sxs-lookup"><span data-stu-id="43997-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="43997-109">Suosittelemme erillistä hinnastoa projektiresursseille ja luettelonimikkeille, koska ne toimivat eri tavoilla hinnoittelua korvattaessa.</span><span class="sxs-lookup"><span data-stu-id="43997-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="43997-110">Kullakin seuraavista entiteeteistä voi olla yksi tai useampi kohdennettu myyntihinnasto projektihinnoittelua varten:</span><span class="sxs-lookup"><span data-stu-id="43997-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="43997-111">Asiakas (tili)</span><span class="sxs-lookup"><span data-stu-id="43997-111">Customer (account)</span></span> 
- <span data-ttu-id="43997-112">Mahdollisuus</span><span class="sxs-lookup"><span data-stu-id="43997-112">Opportunity</span></span> 
- <span data-ttu-id="43997-113">Tarjous</span><span class="sxs-lookup"><span data-stu-id="43997-113">Quote</span></span> 
- <span data-ttu-id="43997-114">Projektisopimus</span><span class="sxs-lookup"><span data-stu-id="43997-114">Project Contract</span></span>

<span data-ttu-id="43997-115">Näiden entiteettien kohdennukset hinnastoille ilmaistaan projektin hinnastoissa.</span><span class="sxs-lookup"><span data-stu-id="43997-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="43997-116">Myyntientiteeteille Asiakas, Mahdollisuus, Tarjous ja Projektisopimus voidaan kohdentaa yksi tai useampi hinnasto.</span><span class="sxs-lookup"><span data-stu-id="43997-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="43997-117">Asiakkaan tietueeseen ei lisätä oletusarvoista projektihinnastoa.</span><span class="sxs-lookup"><span data-stu-id="43997-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="43997-118">Voit kuitenkin liittää projektihinnaston manuaalisesti asiakkaan tietueeseen.</span><span class="sxs-lookup"><span data-stu-id="43997-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="43997-119">Manuaalista liittämistä pitäisi kuitenkin käyttää vain, kun asiakkaan kanssa on tehty mukautettu hinnoittelusopimus.</span><span class="sxs-lookup"><span data-stu-id="43997-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="43997-120">Kun projektihinnasto liitetään myyntientiteettiin, seuraavat tiedot tarkistetaan:</span><span class="sxs-lookup"><span data-stu-id="43997-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="43997-121">Hinnaston konteksti on **Myynti**.</span><span class="sxs-lookup"><span data-stu-id="43997-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="43997-122">Hinnaston valuutta vastaa asiakkaan hinnastoa.</span><span class="sxs-lookup"><span data-stu-id="43997-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="43997-123">Projektisopimuksen liittyvien projektihinnastojen automaattisessa määrityksessä on seuraava ensisijaisuusjärjestys:</span><span class="sxs-lookup"><span data-stu-id="43997-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="43997-124">Tarjous</span><span class="sxs-lookup"><span data-stu-id="43997-124">Quote</span></span>
2. <span data-ttu-id="43997-125">Mahdollisuus</span><span class="sxs-lookup"><span data-stu-id="43997-125">Opportunity</span></span>
3. <span data-ttu-id="43997-126">Asiakas</span><span class="sxs-lookup"><span data-stu-id="43997-126">Customer</span></span> 
4. <span data-ttu-id="43997-127">Yleiset asetukset</span><span class="sxs-lookup"><span data-stu-id="43997-127">Global settings</span></span> 

<span data-ttu-id="43997-128">Kun projektihinnasto määritetään oletusarvoisesti, järjestelmä tarkistaa, että valuutta vastaa asiakkaan valuuttaa ja että määritetyillä oletushinnastoilla on **Myynti**-konteksti.</span><span class="sxs-lookup"><span data-stu-id="43997-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="43997-129">Entiteeteille Asiakas, Mahdollisuus, Tarjous ja Projektisopimus voidaan kohdentaa useita projektihinnastoja.</span><span class="sxs-lookup"><span data-stu-id="43997-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="43997-130">Tämä ominaisuus tukee päivämääräkohtaisia oletushintoja pitkäaikaisessa projektisopimuksessa, joka voi edellyttää useita hinnastoja inflaatiosta johtuvien hintapäivitysten mahdollistamista varten.</span><span class="sxs-lookup"><span data-stu-id="43997-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="43997-131">Jos entiteetille Asiakas, Mahdollisuus, Tarjous tai Projektisopimus kohdennetuilla hinnastoilla kuitenkin on päällekkäisiä päivämäärävälejä, oletushinnat voivat olla virheellisiä.</span><span class="sxs-lookup"><span data-stu-id="43997-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="43997-132">Tämän vuoksi on varmistettava, että kyseisille entiteeteille ei kohdenneta päällekkäisiä päivämäärävälejä sisältäviä projektihinnastoja.</span><span class="sxs-lookup"><span data-stu-id="43997-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
