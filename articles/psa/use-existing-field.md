---
title: Käytä aiemmin luotua kenttää Project Servicessa hinnoitteludimensiona
description: Tässä aiheessa on tietoja aiemmin luotujen Project Service -kenttien käyttämisestä hinnoitteludimensioina.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075426"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="f4ae9-103">Käytä aiemmin luotua kenttää Project Servicessa hinnoitteludimensiona</span><span class="sxs-lookup"><span data-stu-id="f4ae9-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="f4ae9-104">Project Service Automation (PSA) sisältää monta kenttää **Nykyarvot** -entiteetissä, joita voidaan käyttää hinnoitteludimensioina resurssipohjaisessa hinnoittelussa projektiorganisaatioissa.</span><span class="sxs-lookup"><span data-stu-id="f4ae9-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="f4ae9-105">Esimerkiksi yksi yhteinen kenttä on **Varattavissa oleva resurssi**.</span><span class="sxs-lookup"><span data-stu-id="f4ae9-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="f4ae9-106">Pienemmät yritykset, joissa on alle 20-30 laskutettavaa resurssia, voivat huomata, että laskutus- ja kustannushintojen määrittely erikseen kullekin resurssille on yksinkertaisempaa.</span><span class="sxs-lookup"><span data-stu-id="f4ae9-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="f4ae9-107">Koska laskutettava työvoima kuitenkin kasvaa, se voi muuttua epärealistiseksi ylläpitää, kun resurssien kustannukset ja laskutushinnat alkavat vaihdella, kun resursseja ylennetään, he kerryttävät lisää kokemusta, tai saavat uusia taitoja.</span><span class="sxs-lookup"><span data-stu-id="f4ae9-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="f4ae9-108">Koska tämä lähestymi tapa toimii edelleen tietyn kokoisia yrityksiä varten, katso aihetta [Käytä varattavaa resurssia hinnoitteludimensiona](bookable-resource-pricing-dimension.md) ymmärtääksesi, kuinka olemassa olevaa Project Service -kenttää voidaan käyttää hinnoitteludimensiona.</span><span class="sxs-lookup"><span data-stu-id="f4ae9-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="f4ae9-109">Toinen esimerkki on tapahtumaluokka.</span><span class="sxs-lookup"><span data-stu-id="f4ae9-109">Another example is that of transaction category.</span></span> <span data-ttu-id="f4ae9-110">Asiakkaat ja toteuttajat ovat käyttäneet PSA:N tapahtumaluokkaa työn luokittelemiseksi ja hinnan sekä kustannusten määrittelyä varten työn luokan perusteella.</span><span class="sxs-lookup"><span data-stu-id="f4ae9-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="f4ae9-111">Lisätietoja on aiheessa [Tapahtumaluokan käyttäminen hinnoitteludimensiona](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="f4ae9-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
