---
title: Project Operationsin kentät hinnoitteludimensioiksi
description: Tämä aihe tarjoaa tietoja Dynamics 365 Project Operationsin kenttien käyttämisestä hinnoitteludimensioina.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 56ff45169058d96d7ef81a710de309eec698a75f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075411"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="a91e6-103">Project Operationsin kentät hinnoitteludimensioiksi</span><span class="sxs-lookup"><span data-stu-id="a91e6-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="a91e6-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="a91e6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a91e6-105">**Todelliset arvot** -entiteetillä on useita kenttiä, joita voidaan käyttää hinnoitteludimensioina resurssiperustaisessa hinnoittelussa.</span><span class="sxs-lookup"><span data-stu-id="a91e6-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="a91e6-106">Esimerkiksi yksi yhteinen kenttä on **Varattavissa oleva resurssi**.</span><span class="sxs-lookup"><span data-stu-id="a91e6-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="a91e6-107">Pienemmät yritykset, joissa on alle 20-30 laskutettavaa resurssia, voivat huomata, että laskutus- ja kustannushintojen määrittely erikseen kullekin resurssille on yksinkertaisempaa.</span><span class="sxs-lookup"><span data-stu-id="a91e6-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="a91e6-108">Koska laskutettavan henkilöstön määrä kasvaa, resurssikohtaiset hintoja voi olla liikaa ylläpidettäväksi.</span><span class="sxs-lookup"><span data-stu-id="a91e6-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="a91e6-109">Resurssin kustannukset ja laskumäärät alkavat vaihdella, kun resursseja mainostetaan ja taitoja ja kokemusta tulee lisää.</span><span class="sxs-lookup"><span data-stu-id="a91e6-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="a91e6-110">Toinen esimerkki on tapahtumaluokka.</span><span class="sxs-lookup"><span data-stu-id="a91e6-110">Another example is that of transaction category.</span></span> <span data-ttu-id="a91e6-111">Asiakkaat ja toteuttajat ovat käyttäneet tapahtumaluokkaa työn luokittelussa. He käyttävät kenttää työn luokan hinnan ja kustannusten perusteella</span><span class="sxs-lookup"><span data-stu-id="a91e6-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
