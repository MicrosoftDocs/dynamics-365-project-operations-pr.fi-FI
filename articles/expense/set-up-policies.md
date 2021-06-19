---
title: Kulukäytäntöjen määrittäminen
description: Voit määrittää kulukäytäntöjä, joita työntekijöiden on seurattava kuluraporttien ja matkustusehdotusten syöttämisessä ja lähettämisessä.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001872"
---
# <a name="define-expense-policies"></a><span data-ttu-id="03458-103">Kulukäytäntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="03458-103">Define expense policies</span></span>

<span data-ttu-id="03458-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="03458-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="03458-105">Voit määrittää kulukäytäntöjä, joita työntekijöiden on noudatettava kuluraporttien ja matkustusehdotusten syöttämisessä ja lähettämisessä.</span><span class="sxs-lookup"><span data-stu-id="03458-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="03458-106">Kulukäytäntöjen käyttäminen voi olla avuksi kulujen tehokkaassa hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="03458-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="03458-107">Voit määrittää esimerkiksi New Yorkin hotellikuluille käytännön, jonka mukaan yökohtainen kulu saa olla enintään 250 dollaria.</span><span class="sxs-lookup"><span data-stu-id="03458-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="03458-108">Jos työntekijä lähettää kuluraportin tai matkustusehdotuksen, jossa huoneen hinta ylitää tämän summan, järjestelmä ilmoittaa</span><span class="sxs-lookup"><span data-stu-id="03458-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="03458-109">työntekijälle, että kulun summa ylittää käytännön määrittämän summan.</span><span class="sxs-lookup"><span data-stu-id="03458-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="03458-110">Voit määrittää viestin, jonka työntekijä saa, kun</span><span class="sxs-lookup"><span data-stu-id="03458-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="03458-111">määrität käytännön.</span><span class="sxs-lookup"><span data-stu-id="03458-111">define the policy.</span></span>      
        
<span data-ttu-id="03458-112">Voit määrittää seuraavia kolmentyyppisiä käytäntöjä:</span><span class="sxs-lookup"><span data-stu-id="03458-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="03458-113">**Varoitus** : Antaa työntekijälle mahdollisuuden lähettää kuluraportin tai matkustusehdotuksen, mutta kulu merkitään kaikille hyväksyjille ja</span><span class="sxs-lookup"><span data-stu-id="03458-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="03458-114">myöhempää raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="03458-114">for later reporting.</span></span>        

- <span data-ttu-id="03458-115">**Virhe**: Vaatii työntekijää tarkistamaan, että kulu noudattaa käytäntöä, ennen kuin kuluraportti tai matkustusehdotus lähetetään.</span><span class="sxs-lookup"><span data-stu-id="03458-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="03458-116">**Peruste**: Vaatii työntekijää tai esimiestä antamaan perustelun käytäntösumman ylittämiselle ennen kuluraportin tai matkustusehdotuksen lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="03458-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="03458-117">Käytäntöä koskevat vihjeet</span><span class="sxs-lookup"><span data-stu-id="03458-117">Policy tips</span></span>
<span data-ttu-id="03458-118">Seuraavassa kerrotaan muutamia ehdotuksia, jotka voivat auttaa kulujen hallinnan uusien käytäntöjen luomisessa:</span><span class="sxs-lookup"><span data-stu-id="03458-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="03458-119">Käytännöt ovat voimassa tiettynä ajankohtana. Se tarkoittaa sitä, että käytäntö ei ole voimassa, jos se on luotu kulun tapahtumisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="03458-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="03458-120">Voit esimerkiksi luoda uuden käytännön, jonka mukaan suurin mahdollinen ateriakulu on 50 dollaria.</span><span class="sxs-lookup"><span data-stu-id="03458-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="03458-121">Aiemmin syötettyjä kuluja ei tarkisteta tämän käytännön perusteella.</span><span class="sxs-lookup"><span data-stu-id="03458-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="03458-122">Kun eriteltävälle kululuokalle luodaan käytäntö, voit lisätä kulurivin tyypille ehdon.</span><span class="sxs-lookup"><span data-stu-id="03458-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="03458-123">Jotkin käytännöt, kuten kuitin vaatiminen, eivät toimi eriteltävien rivien kohdalla.</span><span class="sxs-lookup"><span data-stu-id="03458-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="03458-124">Tässä tilanteessa käytäntö kohdistetaan vain otsikkoriviin tai muihin kuin eriteltyihin riveihin.</span><span class="sxs-lookup"><span data-stu-id="03458-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="03458-125">Kulujen hallintakäytännöt arvioidaan lähde-entiteetin perusteella oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="03458-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="03458-126">Voit määrittää konsernin skenaarioiden käytännön niin, että se arvioidaan sen sijaan kohde-entiteetin (lainaava entiteetti) avulla.</span><span class="sxs-lookup"><span data-stu-id="03458-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="03458-127">Jos haluat suorittaa käytäntöjä kohde-entiteetin avulla, ota käyttöön **Arvioi kulukäytäntö lainaaavan yrityksen entiteetin avulla** -ominaisuus **Ominaisuuksien hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="03458-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="03458-128">Käytäntöjen arvioimisajankohta</span><span class="sxs-lookup"><span data-stu-id="03458-128">When to evaluate policies</span></span>

<span data-ttu-id="03458-129">Voit valita kulujen hallinnan parametreissa kulujen hallintakäytäntöjen arvioimisen, kun rivi on tallennettu tai kun kuluraportti on lähetetty.</span><span class="sxs-lookup"><span data-stu-id="03458-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="03458-130">Jos haluat tehdä arvioinnin rivin tallennuksen yhteydessä, käyttäjät näkevät suoritettavat toiminnot aiemmin ja voivat viimeistellä kuluraportin kerralla.</span><span class="sxs-lookup"><span data-stu-id="03458-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="03458-131">Muussa tapauksessa voit viivästyttää käytännön arviointia ja säästää aikaa suorittamalla tarkistuksen lopussa työnkulun lähettämisen aikana.</span><span class="sxs-lookup"><span data-stu-id="03458-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]