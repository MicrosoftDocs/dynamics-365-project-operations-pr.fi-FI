---
title: Projektitarjousten analysointi
description: Tässä aiheessa on tietoja projektitarjousten analysoinnista.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751116"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="f96ad-103">Projektitarjousten analysointi</span><span class="sxs-lookup"><span data-stu-id="f96ad-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f96ad-104">Dynamics 365 Project Service Automation analysoi projektitarjouksia kannattavuuden arvioimiseksi.</span><span class="sxs-lookup"><span data-stu-id="f96ad-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="f96ad-105">Se analysoi myös, kuinka hyvin tarjous vastaa asiakkaan odotuksia toimituspäivän tai valmistumispäivän sekä budjetoinnin osalta.</span><span class="sxs-lookup"><span data-stu-id="f96ad-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="f96ad-106">Kannattavuusanalyysi</span><span class="sxs-lookup"><span data-stu-id="f96ad-106">Profitability analysis</span></span>

<span data-ttu-id="f96ad-107">Project Service Automation analysoi kannattavuutta käyttämällä käyttökatetta ja korjattua käyttökatetta.</span><span class="sxs-lookup"><span data-stu-id="f96ad-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="f96ad-108">Käyttökatteet lasketaan seuraavalla kaavalla:</span><span class="sxs-lookup"><span data-stu-id="f96ad-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="f96ad-109">Korjattu käyttökate lasketaan seuraavalla kaavalla:</span><span class="sxs-lookup"><span data-stu-id="f96ad-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="f96ad-110">Jos käyttökatteen ja korjatun käyttökatteen arvoissa on suuri ero, suuri osa tarjouksen työstä on luokiteltu ei-veloitettavaksi.</span><span class="sxs-lookup"><span data-stu-id="f96ad-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="f96ad-111">Analyysi asiakkaan odotuksista</span><span class="sxs-lookup"><span data-stu-id="f96ad-111">Analysis of customer expectations</span></span>

<span data-ttu-id="f96ad-112">Voit analysoida tarjouksia ja luoda kaavioita asiakkaan odotuksista aikataulun ja budjetin suhteen, jos syötät arvot seuraaville kentille:</span><span class="sxs-lookup"><span data-stu-id="f96ad-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="f96ad-113">Tarjouksen otsikon **Pyydetty toimituspäivä** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="f96ad-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="f96ad-114">Kunkin tarjousrivin **Asiakasbudjetti** (projektiperusteisilla ja tuoteperusteisilla riveillä).</span><span class="sxs-lookup"><span data-stu-id="f96ad-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="f96ad-115">Asiakkaan odotukset aikataulun suhteen analysoidaan vertaamalla tarjousrivin tietojen myöhäisintä päättymispäivää pyydettyyn toimituspäivään kaikilla tarjouksen tarjousriveillä.</span><span class="sxs-lookup"><span data-stu-id="f96ad-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="f96ad-116">Asiakkaan odotukset budjetin osalta analysoidaan vertaamalla asiakkaan kokonaisbudjetin summaa tarjottuun summaan kaikilla tarjousriveillä.</span><span class="sxs-lookup"><span data-stu-id="f96ad-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
