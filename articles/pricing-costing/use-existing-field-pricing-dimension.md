---
title: Project Operationsin kentät hinnoitteludimensioiksi
description: Tässä aiheessa on tietoja kenttien käytöstä hinnoitteludimensioina Dynamics 365 Project Operationsissa.
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
ms.openlocfilehash: 04b823e8237590a294ed0706e64d0ecb9d2cf56f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274634"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="deea3-103">Project Operationsin kentät hinnoitteludimensioina</span><span class="sxs-lookup"><span data-stu-id="deea3-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="deea3-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="deea3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="deea3-105">**Todelliset arvot** -entiteetillä on useita kenttiä, joita voidaan käyttää hinnoitteludimensioina resurssiperustaisessa hinnoittelussa.</span><span class="sxs-lookup"><span data-stu-id="deea3-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="deea3-106">Esimerkiksi yksi yhteinen kenttä on **Varattavissa oleva resurssi**.</span><span class="sxs-lookup"><span data-stu-id="deea3-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="deea3-107">Pienemmät yritykset, joissa on alle 20-30 laskutettavaa resurssia, voivat huomata, että laskutus- ja kustannushintojen määrittely erikseen kullekin resurssille on yksinkertaisempaa.</span><span class="sxs-lookup"><span data-stu-id="deea3-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="deea3-108">Koska laskutettavan henkilöstön määrä kasvaa, resurssikohtaiset hintoja voi olla liikaa ylläpidettäväksi.</span><span class="sxs-lookup"><span data-stu-id="deea3-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="deea3-109">Resurssin kustannukset ja laskumäärät alkavat vaihdella, kun resursseja mainostetaan ja taitoja ja kokemusta tulee lisää.</span><span class="sxs-lookup"><span data-stu-id="deea3-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="deea3-110">Toinen esimerkki on tapahtumaluokka.</span><span class="sxs-lookup"><span data-stu-id="deea3-110">Another example is that of transaction category.</span></span> <span data-ttu-id="deea3-111">Asiakkaat ja toteuttajat ovat käyttäneet tapahtumaluokkaa työn luokittelussa. He käyttävät kenttää työn luokan hinnan ja kustannusten perusteella</span><span class="sxs-lookup"><span data-stu-id="deea3-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]