---
title: Kulukäytäntöjen määrittäminen
description: Voit määrittää kulukäytäntöjä, joita työntekijöiden on seurattava kuluraporttien ja matkustusehdotusten syöttämisessä ja lähettämisessä Microsoft Dynamics 365 Financessa.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c014b0593a87ce50f09175b77d9cf498a65391e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271259"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="af81a-103">Kulukäytäntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="af81a-103">Set up expense policies</span></span>

<span data-ttu-id="af81a-104">Voit määrittää kulukäytäntöjä, joita työntekijöiden on noudatettava kuluraporttien ja matkustusehdotusten syöttämisessä ja lähettämisessä.</span><span class="sxs-lookup"><span data-stu-id="af81a-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="af81a-105">Kulukäytäntöjen käyttäminen voi olla avuksi kulujen tehokkaassa hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="af81a-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="af81a-106">Voit määrittää esimerkiksi New Yorkin hotellikuluille käytännön, jonka mukaan yökohtainen kulu saa olla enintään 250 dollaria.</span><span class="sxs-lookup"><span data-stu-id="af81a-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="af81a-107">Jos työntekijä lähettää kuluraportin tai matkustusehdotuksen, jossa huoneen hinta ylitää tämän summan, järjestelmä ilmoittaa</span><span class="sxs-lookup"><span data-stu-id="af81a-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="af81a-108">työntekijälle, että kulun summa ylittää käytännön määrittämän summan.</span><span class="sxs-lookup"><span data-stu-id="af81a-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="af81a-109">Voit määrittää viestin, jonka työntekijä saa, kun</span><span class="sxs-lookup"><span data-stu-id="af81a-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="af81a-110">määrität käytännön.</span><span class="sxs-lookup"><span data-stu-id="af81a-110">define the policy.</span></span>      
        
<span data-ttu-id="af81a-111">Voit määrittää seuraavia kolmentyyppisiä käytäntöjä:</span><span class="sxs-lookup"><span data-stu-id="af81a-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="af81a-112">Varoitus – Antaa työntekijälle mahdollisuuden lähettää kuluraportin tai matkustusehdotuksen, mutta kulu merkitään kaikille hyväksyjille ja</span><span class="sxs-lookup"><span data-stu-id="af81a-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="af81a-113">myöhempää raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="af81a-113">for later reporting.</span></span>        

- <span data-ttu-id="af81a-114">Virhe – Vaatii työntekijää tarkistamaan, että kulu noudattaa käytäntöä, ennen kuin kuluraportti tai matkustusehdotus lähetetään.</span><span class="sxs-lookup"><span data-stu-id="af81a-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="af81a-115">Peruste – Vaatii työntekijää tai esimiestä antamaan perustelun käytäntösumman ylittämiselle ennen kuluraportin tai matkustusehdotuksen lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="af81a-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="af81a-116">Käytäntöä koskevat vihjeet</span><span class="sxs-lookup"><span data-stu-id="af81a-116">Policy tips</span></span>
<span data-ttu-id="af81a-117">Seuraavassa kerrotaan muutamia ehdotuksia, jotka voivat auttaa kulujen hallinnan uusien käytäntöjen luomisessa.</span><span class="sxs-lookup"><span data-stu-id="af81a-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="af81a-118">Käytännöt ovat voimassa voimaantulopäivänä, eivätkä ne tule voimaan, jos käytäntö luodaan kulutuspäivän jälkeen.</span><span class="sxs-lookup"><span data-stu-id="af81a-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="af81a-119">Jos olet esimerkiksi luomassa uutta käytäntöä, jonka mukaan 50 $ on mahdollisimman paljon ateriakuluja, kaikkia eilisestä lähtien määritettyjä kuluja ei voi tarkistaa tästä käytännöstä.</span><span class="sxs-lookup"><span data-stu-id="af81a-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="af81a-120">Kun eriteltävälle kululuokalle luodaan käytäntö, voit lisätä kulurivin tyypille ehdon.</span><span class="sxs-lookup"><span data-stu-id="af81a-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="af81a-121">Joissakin sellaisissa käytännöissä, kuten kuittauksen vaatiminen, ei ehkä kannata määrittää eriteltyjä rivejä, vaan ne tulisi kohdistaa vain otsikkoriville tai ei-eritellylle riville.</span><span class="sxs-lookup"><span data-stu-id="af81a-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="af81a-122">Kulujen hallintakäytännöt arvioidaan lähde-entiteetin perusteella oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="af81a-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="af81a-123">Voit määrittää konsernin skenaarioiden käytännön niin, että se arvioidaan sen sijaan kohde-entiteetin (lainaava entiteetti) avulla.</span><span class="sxs-lookup"><span data-stu-id="af81a-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="af81a-124">Jos haluat suorittaa käytäntöjä kohde-entiteetin avulla, ota käyttöön Arvioi kulukäytäntö lainaavan yrityksen entiteetin avulla -ominaisuus **Ominaisuuksien hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="af81a-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="af81a-125">Käytäntöjen arvioimisajankohta</span><span class="sxs-lookup"><span data-stu-id="af81a-125">When to evaluate policies</span></span>

<span data-ttu-id="af81a-126">Kustannushallintaparametreissa on mahdollisuus joko arvioida kustannusten hallintakäytännöt, kun rivi tallennetaan tai kun kustannusraportti lähetetään.</span><span class="sxs-lookup"><span data-stu-id="af81a-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="af81a-127">Jos päätät arvioida, kun rivi tallennetaan, se varmistaa, että käyttäjillä on aikaisempi näkyvyys siitä, mitä heidän on tehtävä, jotta kuluraportti voidaan täydentää kerralla.</span><span class="sxs-lookup"><span data-stu-id="af81a-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="af81a-128">Muussa tapauksessa voit viivästyttää käytännön arviointia ja säästää aikaa suorittamalla tarkistuksen lopussa työnkulun lähettämisen aikana.</span><span class="sxs-lookup"><span data-stu-id="af81a-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]