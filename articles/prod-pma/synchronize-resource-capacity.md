---
title: Resurssin kapasiteetin synkronointi
description: Tässä aiheessa on tietoja resurssin kapasiteetin synkronoimisesta eri kalentereissa ja projekteissa.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288555"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="d1200-103">Resurssin kapasiteetin synkronointi</span><span class="sxs-lookup"><span data-stu-id="d1200-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1200-104">Resurssisynkronoinnin prosessit auttavat sen varmistamisessa, että kalenterin ja peruskalenterin tiedot kopioidaan projektin resurssiaikataulutukseen.</span><span class="sxs-lookup"><span data-stu-id="d1200-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="d1200-105">Jos kalenteria muutetaan, prosessit tekevät tarvittavat päivitykset projektiresurssien aikataulutukseen.</span><span class="sxs-lookup"><span data-stu-id="d1200-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="d1200-106">Prosessit auttavat myös parantamaan tehokkuutta, koska kalenterin resurssitiedot synkronoidaan etukäteen.</span><span class="sxs-lookup"><span data-stu-id="d1200-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="d1200-107">Siksi päivitykset resurssiaikataulutustietoihin tapahtuvat nopeammin.</span><span class="sxs-lookup"><span data-stu-id="d1200-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="d1200-108">Suosittelemme prosessien aikatauluttamista erissä sen sijaan, että ne aikataulutettaisiin yksi kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="d1200-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="d1200-109">Muussa tapauksessa on vaarana, että joku on unohtanut mukana olevat päivämäärät, kun tiedot on viimeksi synkronoitu.</span><span class="sxs-lookup"><span data-stu-id="d1200-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="d1200-110">Jos mukana olevia päivämääriä ei käytetä, päivämäärän synkronoinnissa voi esiintyä aukkoja.</span><span class="sxs-lookup"><span data-stu-id="d1200-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalenterin synkronointi](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="d1200-112">Resurssikapasiteettien koontien synkronointi</span><span class="sxs-lookup"><span data-stu-id="d1200-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="d1200-113">Synkronointiprosessi on suunniteltu synkronoimaan kaikki resurssikalenterin tiedot.</span><span class="sxs-lookup"><span data-stu-id="d1200-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="d1200-114">Näihin tietoihin kuuluvat peruskalenterin tiedot kaikista muutoksista projektin resurssikalenterin kapasiteettitaulukkoon.</span><span class="sxs-lookup"><span data-stu-id="d1200-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="d1200-115">Jos projektiin lisätään uusia resursseja, synkronointi auttaa varmistamaan, että päivitetyt kalenteritiedot ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="d1200-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="d1200-116">Synkronoinnin vois suorittaa milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="d1200-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="d1200-117">On suositeltavaa synkronoida erissä.</span><span class="sxs-lookup"><span data-stu-id="d1200-117">We recommend that you use a batch.</span></span> <span data-ttu-id="d1200-118">Asetukset ovat käytettävissä kapasiteettivarausten synkronoinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="d1200-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="d1200-119">Valitse **Projektinhallinta ja kirjanpito** &gt; **Jaksoittainen** &gt; **Kapasiteetin synkronointi** &gt; **Synkronoi resurssikapasiteettien koonnit**.</span><span class="sxs-lookup"><span data-stu-id="d1200-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="d1200-120">Määritä seuraavan taulukon asetukset.</span><span class="sxs-lookup"><span data-stu-id="d1200-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="d1200-121">Asetus</span><span class="sxs-lookup"><span data-stu-id="d1200-121">Option</span></span>      | <span data-ttu-id="d1200-122">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="d1200-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="d1200-123">Jaksokoodi</span><span class="sxs-lookup"><span data-stu-id="d1200-123">Period code</span></span> | <span data-ttu-id="d1200-124">Voit myös valita pääkirjan päivämäärävälin koodin määrittääksesi resurssikapasiteettien koontien synkronointiprosessin alkamis- ja päättymispäivät.</span><span class="sxs-lookup"><span data-stu-id="d1200-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="d1200-125">Alkamispäivä</span><span class="sxs-lookup"><span data-stu-id="d1200-125">Start date</span></span>  | <span data-ttu-id="d1200-126">Syötä resurssikapasiteettien koontien synkronointiprosessin alkamispäivä.</span><span class="sxs-lookup"><span data-stu-id="d1200-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="d1200-127">Päättymispäivä</span><span class="sxs-lookup"><span data-stu-id="d1200-127">End date</span></span>    | <span data-ttu-id="d1200-128">Syötä resurssikapasiteettien koontien synkronointiprosessin päättymispäivä.</span><span class="sxs-lookup"><span data-stu-id="d1200-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="d1200-129">[![Synkronointiprosessi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="d1200-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]