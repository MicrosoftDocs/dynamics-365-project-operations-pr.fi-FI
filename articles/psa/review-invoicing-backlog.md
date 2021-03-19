---
title: Laskutusjonon tarkasteleminen projekteissa ja projektisopimuksissa
description: Tässä aiheessa on tietoja ajan, kulujen ja tuotteiden jonojen tarkastelusta sekä siitä, miten ne voidaan merkitä laskutusvalmiiksi.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bdeeb100614cda78d0ba536310bb6b411c863b71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282779"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="563e4-103">Laskutusjonon tarkasteleminen projekteissa ja projektisopimuksissa</span><span class="sxs-lookup"><span data-stu-id="563e4-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="563e4-104">Kun tapahtuma on valmis laskun luomista ja käsittelyä varten, tapahtuma tulisi merkitä **Laskutusvalmiiksi**.</span><span class="sxs-lookup"><span data-stu-id="563e4-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="563e4-105">Tässä aiheessa kuvataan, minkä tyyppisiä tapahtumia voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="563e4-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="563e4-106">Tarkastele aika-ja materiaalipohjaisen laskutuksen jonoa</span><span class="sxs-lookup"><span data-stu-id="563e4-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="563e4-107">Kun aika- tai kulumerkintä lähetetään ja hyväksytään projektille, PSA luo projektin nykyarvon.</span><span class="sxs-lookup"><span data-stu-id="563e4-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="563e4-108">Jos projektin ja tapahtumaluokan yhdistelmä on yhdistetty aika- ja materiaaliprojektin sopimu riviin, luodaan kaksi todellista arvoa, kun tapahtuma hyväksytään:</span><span class="sxs-lookup"><span data-stu-id="563e4-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="563e4-109">Kulujen nykyarvo</span><span class="sxs-lookup"><span data-stu-id="563e4-109">Cost actual</span></span> 
- <span data-ttu-id="563e4-110">Laskuttamattoman myynnin nykyarvo</span><span class="sxs-lookup"><span data-stu-id="563e4-110">Unbilled sales actual</span></span>

<span data-ttu-id="563e4-111">Laskuttamattoman myynnin nykyarvot edustavat laskutusjonoa, ja niiden laskutustilaksi on asetettava **Laskutusvalmis**.</span><span class="sxs-lookup"><span data-stu-id="563e4-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="563e4-112">Projektilaskua luotaessa laskuttamattomat myynnin nykyarvot, jotka on merkitty **Laskutusvalmiiksi** kopioidaan laskurivien tiedoiksi.</span><span class="sxs-lookup"><span data-stu-id="563e4-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="563e4-113">Tarkastellaksesi laskutusjonoa aikaa ja materiaaleja varten, siirry kohtaan **Myynti** \> **Laskutus** \> **Ajan ja materiaalien laskutuksen jono**.</span><span class="sxs-lookup"><span data-stu-id="563e4-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="563e4-114">Valitse kaikki laskuttamattomat myynnin nykyarvot, jotka ovat valmiita laskutettaviksi, ja valitse sitten **Laskutusvalmis**.</span><span class="sxs-lookup"><span data-stu-id="563e4-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="563e4-115">Näiden nykyarvojen laskutustilaksi vaihtuu **Laskutusvalmis**.</span><span class="sxs-lookup"><span data-stu-id="563e4-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Ajan ja materiaalien laskutuksen jono](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="563e4-117">Tarkastele tuotteiden laskutuksen jonoa</span><span class="sxs-lookup"><span data-stu-id="563e4-117">Review the product billing backlog</span></span>

<span data-ttu-id="563e4-118">Kun projekti opimuksessa on PSA-järjestelmässä tuotepohjaisia sopimusrivejä, kyseiset rivit katsotaan laskutettaviksi aina, kun projekti opimukselle luodaan lasku.</span><span class="sxs-lookup"><span data-stu-id="563e4-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="563e4-119">Mikä tahansa tuote, jolla on sopimusrivejä, jotka on merkitty **Laskutusvalmiiksi** kopioidaan projektilaskuun projektilaskun riveiksi.</span><span class="sxs-lookup"><span data-stu-id="563e4-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="563e4-120">Jos haluat tarkastella tuotteiden laskutusjonoa, siirry kohtaan **Myynti**\>**Laskutus**\>**Tuotteiden laskutuksen jono**.</span><span class="sxs-lookup"><span data-stu-id="563e4-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="563e4-121">Valitse kaikki tuotepohjaiset sopimusrivit, jotka ovat valmiita laskutettaviksi, ja valitse sitten **Laskutusvalmis**.</span><span class="sxs-lookup"><span data-stu-id="563e4-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="563e4-122">Näiden rivien laskutustilaksi vaihtuu **Laskutusvalmis**.</span><span class="sxs-lookup"><span data-stu-id="563e4-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Tuotteiden laskutuksen jono](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="563e4-124">Kiinteähintaisten palvelusopimusten laskutuksen välitavoitteiden tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="563e4-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="563e4-125">Jokaiselle projektisopimusrivin, jolla on kiinteähintainen laskutusmenetelmä, on määritettävä sopimuksen välitavoitteet.</span><span class="sxs-lookup"><span data-stu-id="563e4-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="563e4-126">Nämä sopimuksen välitavoitteet voidaan laskuttaa vain, jos ne on merkitty **Laskutusvalmiiksi**.</span><span class="sxs-lookup"><span data-stu-id="563e4-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="563e4-127">Voit tarkastella laskutuksen välitavoitteita siirtymällä kohtaan **Myynti**\> **Laskutus**\> **Kiinteän hinnan välitavoitteet**.</span><span class="sxs-lookup"><span data-stu-id="563e4-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="563e4-128">Valitse kaikki välitavoitteet, jotka ovat valmiita laskutettaviksi, ja valitse sitten **Laskutusvalmis**.</span><span class="sxs-lookup"><span data-stu-id="563e4-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="563e4-129">Näiden välitavoitteiden laskutustilaksi vaihtuu **Laskutusvalmis**.</span><span class="sxs-lookup"><span data-stu-id="563e4-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Kiinteän hinnan välitavoitteet](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]