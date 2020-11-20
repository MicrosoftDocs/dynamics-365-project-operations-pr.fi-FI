---
title: Project Operationsin kentät hinnoitteludimensioiksi
description: Tämä aihe tarjoaa tietoja Dynamics 365 Project Operationsin kenttien käyttämisestä hinnoitteludimensioina.
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
ms.openlocfilehash: 59367b35f15f806b109f606e912edc487d9e7685
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119234"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="2035b-103">Project Operationsin kentät hinnoitteludimensioiksi</span><span class="sxs-lookup"><span data-stu-id="2035b-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="2035b-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="2035b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2035b-105">**Todelliset arvot** -entiteetillä on useita kenttiä, joita voidaan käyttää hinnoitteludimensioina resurssiperustaisessa hinnoittelussa.</span><span class="sxs-lookup"><span data-stu-id="2035b-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="2035b-106">Esimerkiksi yksi yhteinen kenttä on **Varattavissa oleva resurssi**.</span><span class="sxs-lookup"><span data-stu-id="2035b-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="2035b-107">Pienemmät yritykset, joissa on alle 20-30 laskutettavaa resurssia, voivat huomata, että laskutus- ja kustannushintojen määrittely erikseen kullekin resurssille on yksinkertaisempaa.</span><span class="sxs-lookup"><span data-stu-id="2035b-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="2035b-108">Koska laskutettavan henkilöstön määrä kasvaa, resurssikohtaiset hintoja voi olla liikaa ylläpidettäväksi.</span><span class="sxs-lookup"><span data-stu-id="2035b-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="2035b-109">Resurssin kustannukset ja laskumäärät alkavat vaihdella, kun resursseja mainostetaan ja taitoja ja kokemusta tulee lisää.</span><span class="sxs-lookup"><span data-stu-id="2035b-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="2035b-110">Toinen esimerkki on tapahtumaluokka.</span><span class="sxs-lookup"><span data-stu-id="2035b-110">Another example is that of transaction category.</span></span> <span data-ttu-id="2035b-111">Asiakkaat ja toteuttajat ovat käyttäneet tapahtumaluokkaa työn luokittelussa. He käyttävät kenttää työn luokan hinnan ja kustannusten perusteella</span><span class="sxs-lookup"><span data-stu-id="2035b-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
