---
title: Kustannus- ja myyntihintojen määrittäminen luettelotuotteille
description: Tässä aiheessa on tietoja siitä, miten tuoteluettelon nimikkeiden kustannus- ja myyntihinnat määritetään.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075415"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="d9be2-103">Kustannus- ja myyntihintojen määrittäminen luettelotuotteille</span><span class="sxs-lookup"><span data-stu-id="d9be2-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="d9be2-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="d9be2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d9be2-105">Tuoteluettelonimikkeiden hinnoittelun määrittäminen Dynamics 365 Project Operationsissa on sama kuin Dynamics 365 Salesissa.</span><span class="sxs-lookup"><span data-stu-id="d9be2-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="d9be2-106">Koska tuotteita ei voi arvioida tai käyttää Project Operationsin projekteissa, tuoteluettelon hintoja ei tarvitse määrittää projektihinnastoissa tarjouksia ja sopimuksia varten.</span><span class="sxs-lookup"><span data-stu-id="d9be2-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="d9be2-107">Tuoteluettelon hinnat on määritettävä tarjouksen, palvelusopimuksen tai asiakkuuden **tuotehinta** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="d9be2-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="d9be2-108">Älä määritä tuoteluettelon hintoja näiden kohteille projektin hinnastoissa.</span><span class="sxs-lookup"><span data-stu-id="d9be2-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="d9be2-109">Projektihinnastot ovat yksinomaisia Project Operationsia varten.</span><span class="sxs-lookup"><span data-stu-id="d9be2-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="d9be2-110">Sovelluskohtainen liiketoimintalogiikka kopioi hinnastot tarjouksesta palvelusopimukseen.</span><span class="sxs-lookup"><span data-stu-id="d9be2-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="d9be2-111">Tuloksena on palvelussopimuskohtainen hinnasto</span><span class="sxs-lookup"><span data-stu-id="d9be2-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="d9be2-112">Kopiointitoiminto voi viivyttää tarjouksen voittoprosessia, jos tarjouksen projektihinnasto muuttuu liian suureksi.</span><span class="sxs-lookup"><span data-stu-id="d9be2-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="d9be2-113">Tuotehinnastoja ei kopioida, kun luodaan palvelusopimuksille mukautettuja hinnastoja.</span><span class="sxs-lookup"><span data-stu-id="d9be2-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="d9be2-114">Tämä tarkoittaa sitä, että tuotehinnastot eivät vaikuta tarjouksen voittoprosessin tehokkuuteen.</span><span class="sxs-lookup"><span data-stu-id="d9be2-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
