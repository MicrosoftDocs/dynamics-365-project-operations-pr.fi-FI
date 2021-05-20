---
title: Tuotepohjaiset mahdollisuusrivit – lite
description: Tässä aiheessa on tietoja tuotepohjaisista mahdollisuusrivinimikkeistä Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f7dfabd068e180c7122ede0f79aaebfe220250a1
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949540"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="565e3-103">Tuotepohjaiset mahdollisuusrivit – lite</span><span class="sxs-lookup"><span data-stu-id="565e3-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="565e3-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="565e3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="565e3-105">Tuotepohjaiset mahdollisuusrivit ovat mahdollisuuden rivinimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="565e3-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="565e3-106">Nämä erilliset rivinimikkeet ovat asiakkaalle toimitettavassa laskussa.</span><span class="sxs-lookup"><span data-stu-id="565e3-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="565e3-107">Lasku ei sisällä mitään muita lisäpalveluita.</span><span class="sxs-lookup"><span data-stu-id="565e3-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="565e3-108">Liittyvää kulutusta ei seurata liittyvien projektien tehtävissä.</span><span class="sxs-lookup"><span data-stu-id="565e3-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="565e3-109">Tuotepohjaiset rivit voivat olla luettelonimikkeitä tai käsin lisättyjä tuotteita.</span><span class="sxs-lookup"><span data-stu-id="565e3-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="565e3-110">Suurin osa mahdollisuuden tuotepohjaisten rivien ominaisuuksista noudattaa Dynamics 365 Sales -sovelluksen tarjoamia toimintoja.</span><span class="sxs-lookup"><span data-stu-id="565e3-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="565e3-111">Lisätietoja tuotepohjaisista mahdollisuusriveistä on aiheessa [Tuotteiden lisääminen mahdollisuuteen](/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="565e3-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="565e3-112">**Asiakasbudjetti** on konsepti, joka liittyy projektipohjaisiin mahdollisuusriveihin.</span><span class="sxs-lookup"><span data-stu-id="565e3-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="565e3-113">**Asiakasbudjetti**-kenttä seuraa summaa, jonka asiakas on valmis maksamaan nimikkeestä.</span><span class="sxs-lookup"><span data-stu-id="565e3-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="565e3-114">Kun mahdollisuuden yhteenvedon tuottomenetelmä on **Järjestelmän laskema**, asiakkaan budjettiarvot mahdollisuusriveillä lasketaan yhteen arvioidun tuoton laskemiseksi.</span><span class="sxs-lookup"><span data-stu-id="565e3-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]