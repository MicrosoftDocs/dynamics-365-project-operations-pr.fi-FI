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
ms.openlocfilehash: ad03f5f7c1c9e93ca12a8c8d48ffbd2f80b1511f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281564"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="c4367-103">Käytä aiemmin luotua kenttää Project Servicessa hinnoitteludimensiona</span><span class="sxs-lookup"><span data-stu-id="c4367-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c4367-104">Project Service Automation (PSA) sisältää monta kenttää **Nykyarvot**-entiteetissä, joita voidaan käyttää hinnoitteludimensioina resurssipohjaisessa hinnoittelussa projektiorganisaatioissa.</span><span class="sxs-lookup"><span data-stu-id="c4367-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="c4367-105">Esimerkiksi yksi yhteinen kenttä on **Varattavissa oleva resurssi**.</span><span class="sxs-lookup"><span data-stu-id="c4367-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="c4367-106">Pienemmät yritykset, joissa on alle 20-30 laskutettavaa resurssia, voivat huomata, että laskutus- ja kustannushintojen määrittely erikseen kullekin resurssille on yksinkertaisempaa.</span><span class="sxs-lookup"><span data-stu-id="c4367-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="c4367-107">Koska laskutettava työvoima kuitenkin kasvaa, tietyt hinnat voivat muuttua epärealistisiksi ylläpitää, kun resurssien kustannukset ja laskutushinnat alkavat vaihdella, kun resursseja ylennetään, he kerryttävät lisää kokemusta, tai saavat uusia taitoja.</span><span class="sxs-lookup"><span data-stu-id="c4367-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="c4367-108">Koska tämä lähestymistapa toimii edelleen tietyn kokoisia yrityksiä varten, katso [Käytä varattavaa resurssia hinnoitteludimensiona](bookable-resource-pricing-dimension.md) ymmärtääksesi, kuinka olemassa olevaa Project Service -kenttää voidaan käyttää hinnoitteludimensiona.</span><span class="sxs-lookup"><span data-stu-id="c4367-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="c4367-109">Toinen esimerkki on tapahtumaluokka.</span><span class="sxs-lookup"><span data-stu-id="c4367-109">Another example is that of transaction category.</span></span> <span data-ttu-id="c4367-110">Asiakkaat ja toteuttajat ovat käyttäneet PSA:N tapahtumaluokkaa työn luokittelemiseksi ja hinnan sekä kustannusten määrittelyä varten työn luokan perusteella.</span><span class="sxs-lookup"><span data-stu-id="c4367-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="c4367-111">Lisätietoja on aiheessa [Tapahtumaluokan käyttäminen hinnoitteludimensiona](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="c4367-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]