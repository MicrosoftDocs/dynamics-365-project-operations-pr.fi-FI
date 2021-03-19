---
title: Äkillisen ennakon luominen palvelusopimuksessa
description: Tässä aiheessa on tietoja ennakon luomisesta sopimuksessa tarpeen mukaan.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f0a6391a3bf6dd39d21504a6f286e4ff1954183
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273593"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a><span data-ttu-id="6cb38-103">Äkillisen ennakon luominen palvelusopimuksessa</span><span class="sxs-lookup"><span data-stu-id="6cb38-103">Creating an ad hoc advance on a contract</span></span>

<span data-ttu-id="6cb38-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="6cb38-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6cb38-105">Microsoft Dynamics 365 Project Operations tukee laskutusskenaarioita, joissa on ennakkomaksuja ja maksuennakoita.</span><span class="sxs-lookup"><span data-stu-id="6cb38-105">Microsoft Dynamics 365 Project Operations supports invoicing scenarios that involve pre-payments and advances.</span></span> <span data-ttu-id="6cb38-106">**Ennakoiden** käyttö **Project Operationsissa** muistuttaa sopimusten **ennakkomaksuja**.</span><span class="sxs-lookup"><span data-stu-id="6cb38-106">The process for using **Advances** in **Project Operations** is similar to **Retainer** contracts.</span></span> 

<span data-ttu-id="6cb38-107">Laskuta ennakko asiakkaalta seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6cb38-107">Complete the following steps to invoice the customer for an advance.</span></span>

1. <span data-ttu-id="6cb38-108">Siirry **Projektisopimus**-riville ja valitse sitten **Ennakot ja ennakkomaksut**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6cb38-108">Go to the **Project Contract** page, and then select the **Advances and Retainers** tab.</span></span>
2. <span data-ttu-id="6cb38-109">Valitse alaruudukossa, jossa on luettelo kaikista aiemmin kirjatuista ennakoista ja ennakkomaksuista, **+ Uusi projektisopimuksen ennakkomaksu**.</span><span class="sxs-lookup"><span data-stu-id="6cb38-109">In the subgrid that lists all the previously recorded advances and prepayments, select **+ New Project contract retainer**.</span></span> 

    <span data-ttu-id="6cb38-110">**Pikaluonti**-lomake avautuu ennakkomaksun tai ennakon kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="6cb38-110">The **Quick Create** form opens for recording a prepayment or advance.</span></span>
    
3. <span data-ttu-id="6cb38-111">Seuraavassa taulukossa on luettelo kentistä, joilla ennakko kirjataan, ja seikoista, jotka on otettava huomioon uusia ennakoita luotaessa:</span><span class="sxs-lookup"><span data-stu-id="6cb38-111">The table below lists the fields for recording an advance and the considerations to keep in mind as you create new ones:</span></span>

    | <span data-ttu-id="6cb38-112">Field</span><span class="sxs-lookup"><span data-stu-id="6cb38-112">Field</span></span> | <span data-ttu-id="6cb38-113">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="6cb38-113">Description</span></span> | <span data-ttu-id="6cb38-114">Loppupään vaikutus</span><span class="sxs-lookup"><span data-stu-id="6cb38-114">Downstream impact</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="6cb38-115">**Projektisopimuksen asiakas**</span><span class="sxs-lookup"><span data-stu-id="6cb38-115">**Project Contract Customer**</span></span> | <span data-ttu-id="6cb38-116">Tämä kenttä ilmaisee, miltä sopimuksen asiakkaalta tämä ennakko laskutetaan.</span><span class="sxs-lookup"><span data-stu-id="6cb38-116">This field indicates which customer on the contract will be invoiced for this advance.</span></span> | <span data-ttu-id="6cb38-117">Jos sopimuksessa on useita asiakkaita ja niistä jokaiselta halutaan laskuttaa tietty ennakkomaksu- tai ennakkosumma, luo ennakko erikseen kullekin asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="6cb38-117">If you have multiple customers on the contract and want to invoice each of them for a specific retainer or advance amount, create an advance for each customer individually.</span></span> |
    | <span data-ttu-id="6cb38-118">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="6cb38-118">**Description**</span></span> | <span data-ttu-id="6cb38-119">Ennakon tarkoituksen tai ajoituksen kuvaus auttaa tunnistamaan ennakon.</span><span class="sxs-lookup"><span data-stu-id="6cb38-119">The description of the purpose or timing of the advance to help identify this advance.</span></span> | <span data-ttu-id="6cb38-120">Kuvaus näytetään ennakon laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="6cb38-120">This description is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="6cb38-121">**Summa**</span><span class="sxs-lookup"><span data-stu-id="6cb38-121">**Amount**</span></span> | <span data-ttu-id="6cb38-122">Ennakkomaksun tai ennakon summa.</span><span class="sxs-lookup"><span data-stu-id="6cb38-122">The amount for the pre-payment or advance.</span></span> | <span data-ttu-id="6cb38-123">Summa näytetään ennakon laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="6cb38-123">This amount is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="6cb38-124">**Laskun pvm**</span><span class="sxs-lookup"><span data-stu-id="6cb38-124">**Invoice Date**</span></span> | <span data-ttu-id="6cb38-125">Päivämäärä, jolloin ennakko laskutetaan asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="6cb38-125">The date on which this advance is invoiced to the customer.</span></span> | <span data-ttu-id="6cb38-126">Tämä on päivämäärä, jolloin automatisoitu laskun luontiprosessi luo ennakon laskurivin.</span><span class="sxs-lookup"><span data-stu-id="6cb38-126">This is the date for the automated invoice creation process to create an invoice line for this advance.</span></span> |
    | <span data-ttu-id="6cb38-127">**Laskun tila**</span><span class="sxs-lookup"><span data-stu-id="6cb38-127">**Invoice Status**</span></span> | <span data-ttu-id="6cb38-128">Tämä asetusjoukko ilmaisee, lisätäänkö ennakko tämän asiakkaan luonnoslaskuun.</span><span class="sxs-lookup"><span data-stu-id="6cb38-128">This is an option setting that indicates whether this advance is added to a draft invoice for this customer.</span></span> <span data-ttu-id="6cb38-129">Mahdolliset arvot:</span><span class="sxs-lookup"><span data-stu-id="6cb38-129">The possible values are:</span></span></br><span data-ttu-id="6cb38-130">- **Ei valmis laskuttamista varten**</span><span class="sxs-lookup"><span data-stu-id="6cb38-130">- **Not ready to invoice**</span></span></br><span data-ttu-id="6cb38-131">- **Valmis laskuttamista varten**</span><span class="sxs-lookup"><span data-stu-id="6cb38-131">- **Ready to invoice**</span></span> | <span data-ttu-id="6cb38-132">Jos ennakon tai ennakkomaksun merkintänä on **Valmis laskutettavaksi**, se lisätään rivien aikana luonnoslaskuun.</span><span class="sxs-lookup"><span data-stu-id="6cb38-132">When an advance or pre-payment is marked as **Ready to invoice**, it is added as a line time on a draft invoice.</span></span> <span data-ttu-id="6cb38-133">Vain täysin laskutettua ennakkoa voidaan käyttää täsmäyttämään seuraavan laskukauden projektikustannuksia.</span><span class="sxs-lookup"><span data-stu-id="6cb38-133">Only a fully invoiced advance can be used to reconcile against project costs for the next invoice period.</span></span> |

4. <span data-ttu-id="6cb38-134">Kirjaa ennakko tai ennakkomaksu valitsemalla **Tallenna ja sulje** pikaluonti-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="6cb38-134">Select **Save and close** on the quick create dialog to record the advance or the pre-payment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]