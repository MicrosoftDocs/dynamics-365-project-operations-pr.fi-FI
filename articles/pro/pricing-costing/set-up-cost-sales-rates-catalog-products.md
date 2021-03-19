---
title: Kustannus- ja myyntihintojen määrittäminen luettelotuotteille – lite
description: Tässä aiheessa on tietoja siitä, miten tuoteluettelon nimikkeiden kustannus- ja myyntihinnat määritetään.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274454"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="8711a-103">Kustannus- ja myyntihintojen määrittäminen luettelotuotteille – lite</span><span class="sxs-lookup"><span data-stu-id="8711a-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="8711a-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="8711a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="8711a-105">Tuoteluettelonimikkeiden hinnoittelu määritetään Dynamics 365 Project Operationsissa samoin kuin Dynamics 365 Salesissa.</span><span class="sxs-lookup"><span data-stu-id="8711a-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="8711a-106">Project Operationsissa tuotteita ei voi arvioida tai käyttää projekteissa, joten tuoteluettelohintoja ei tarvitse määrittää tarjousten ja sopimusten projektihinnastoihin.</span><span class="sxs-lookup"><span data-stu-id="8711a-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="8711a-107">Määritä tuoteluettelohinnat tarjouksen, sopimuksen tai tilin **Tuotehinta**-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="8711a-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="8711a-108">Älä määritä tuoteluettelohintoja projektin hinnastoihin.</span><span class="sxs-lookup"><span data-stu-id="8711a-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="8711a-109">Projektihinnastot ovat yksinomaisia Project Operationsia varten.</span><span class="sxs-lookup"><span data-stu-id="8711a-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="8711a-110">Sovelluskohtainen liiketoimintalogiikka kopioi hinnastot tarjouksesta sopimukseen.</span><span class="sxs-lookup"><span data-stu-id="8711a-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="8711a-111">Tuloksena on palvelussopimuskohtainen hinnasto</span><span class="sxs-lookup"><span data-stu-id="8711a-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="8711a-112">Kopiointitoiminto voi viivyttää tarjouksen voittoprosessia, jos tarjouksen projektihinnasto muuttuu liian suureksi.</span><span class="sxs-lookup"><span data-stu-id="8711a-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="8711a-113">Tuotehinnastoja ei kopioida, kun luodaan palvelusopimuksille mukautettuja hinnastoja.</span><span class="sxs-lookup"><span data-stu-id="8711a-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="8711a-114">Koska kopiointia ei tehdä, tämä ei vaikuta tarjousprosessin suorituskykyyn.</span><span class="sxs-lookup"><span data-stu-id="8711a-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]