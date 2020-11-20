---
title: Kustannus- ja myyntihintojen määrittäminen luettelotuotteille – lite
description: Tässä aiheessa on tietoja siitä, miten tuoteluettelon nimikkeiden kustannus- ja myyntihinnat määritetään.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176697"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="79827-103">Kustannus- ja myyntihintojen määrittäminen luettelotuotteille – lite</span><span class="sxs-lookup"><span data-stu-id="79827-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="79827-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="79827-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="79827-105">Tuoteluettelonimikkeiden hinnoittelun määrittäminen Dynamics 365 Project Operationsissa on sama kuin Dynamics 365 Salesissa.</span><span class="sxs-lookup"><span data-stu-id="79827-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="79827-106">Koska tuotteita ei voi arvioida tai käyttää Project Operationsin projekteissa, tuoteluettelon hintoja ei tarvitse määrittää projektihinnastoissa tarjouksia ja sopimuksia varten.</span><span class="sxs-lookup"><span data-stu-id="79827-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="79827-107">Tuoteluettelon hinnat on määritettävä tarjouksen, palvelusopimuksen tai asiakkuuden **tuotehinta**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="79827-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="79827-108">Älä määritä tuoteluettelon hintoja näiden kohteille projektin hinnastoissa.</span><span class="sxs-lookup"><span data-stu-id="79827-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="79827-109">Projektihinnastot ovat yksinomaisia Project Operationsia varten.</span><span class="sxs-lookup"><span data-stu-id="79827-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="79827-110">Sovelluskohtainen liiketoimintalogiikka kopioi hinnastot tarjouksesta palvelusopimukseen.</span><span class="sxs-lookup"><span data-stu-id="79827-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="79827-111">Tuloksena on palvelussopimuskohtainen hinnasto</span><span class="sxs-lookup"><span data-stu-id="79827-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="79827-112">Kopiointitoiminto voi viivyttää tarjouksen voittoprosessia, jos tarjouksen projektihinnasto muuttuu liian suureksi.</span><span class="sxs-lookup"><span data-stu-id="79827-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="79827-113">Tuotehinnastoja ei kopioida, kun luodaan palvelusopimuksille mukautettuja hinnastoja.</span><span class="sxs-lookup"><span data-stu-id="79827-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="79827-114">Tämä tarkoittaa sitä, että tuotehinnastot eivät vaikuta tarjouksen voittoprosessin tehokkuuteen.</span><span class="sxs-lookup"><span data-stu-id="79827-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
