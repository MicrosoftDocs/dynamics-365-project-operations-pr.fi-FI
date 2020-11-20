---
title: Tuotepohjaiset mahdollisuusrivit – lite
description: Tässä aiheessa on tietoja tuotepohjaisista mahdollisuusrivinimikkeistä Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd32bedb94cf36f706c112a845f342d9dde19805
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176318"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="c2ea6-103">Tuotepohjaiset mahdollisuusrivit – lite</span><span class="sxs-lookup"><span data-stu-id="c2ea6-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="c2ea6-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="c2ea6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c2ea6-105">Tuotepohjaiset mahdollisuusrivit ovat mahdollisuuden rivinimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="c2ea6-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="c2ea6-106">Nämä rivit toimitetaan asiakkaalle erillisinä rivinimikkeinä lopullisessa laskussa ilman muita lisäarvopalveluja.</span><span class="sxs-lookup"><span data-stu-id="c2ea6-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="c2ea6-107">Liittyvää kulutusta ei seurata liittyvien projektien tehtävissä.</span><span class="sxs-lookup"><span data-stu-id="c2ea6-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="c2ea6-108">Tuotepohjaiset rivit voivat olla luettelonimikkeitä tai käsin lisättyjä tuotteita.</span><span class="sxs-lookup"><span data-stu-id="c2ea6-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="c2ea6-109">Suurin osa mahdollisuuden tuotepohjaisten rivien ominaisuuksista noudattaa Dynamics 365 Sales -sovelluksen tarjoamia toimintoja.</span><span class="sxs-lookup"><span data-stu-id="c2ea6-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="c2ea6-110">Lisätietoja tuotepohjaisista mahdollisuusriveistä on aiheessa [Tuotteiden lisääminen mahdollisuuteen](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="c2ea6-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="c2ea6-111">Yksi käsite tuotepohjaisista mahdollisuusriveissä liittyy projektipohjaisiin mahdollisuuksiin, nimittäin käsite **Asiakasbudjetti**.</span><span class="sxs-lookup"><span data-stu-id="c2ea6-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="c2ea6-112">Tämän kentän avulla voit seurata summaa, jonka asiakas on valmis maksamaan rivinimikkeestä.</span><span class="sxs-lookup"><span data-stu-id="c2ea6-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="c2ea6-113">Jos mahdollisuuden yhteenvedon tuottomenetelmäksi on määritetty **Järjestelmän laskema**, asiakasbudjetin arvot sekä tuote- että projektipohjaisilla riveillä on koottu yhteen arvioidun tuoton laskemiseksi.</span><span class="sxs-lookup"><span data-stu-id="c2ea6-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
