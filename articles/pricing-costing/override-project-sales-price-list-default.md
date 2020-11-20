---
title: Projektin myyntihinnastojen ohittaminen
description: Tässä aiheessa on tietoja mukautettujen myyntihinnastojen luomisesta.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c97dca8685c2db7d256017cf4442416feb0e005b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130844"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="66106-103">Projektin myyntihinnastojen ohittaminen</span><span class="sxs-lookup"><span data-stu-id="66106-103">Override project sales price lists</span></span>

<span data-ttu-id="66106-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="66106-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="66106-105">Asiakaskohtaiset projektihinnastot</span><span class="sxs-lookup"><span data-stu-id="66106-105">Customer-specific project price lists</span></span>

<span data-ttu-id="66106-106">Asiakaskohtaiset hintasopimukset voidaan määrittää projektihinnastoina Dynamics 365 Project Operationsin tilitietueessa.</span><span class="sxs-lookup"><span data-stu-id="66106-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="66106-107">Määritä asiakaskohtainen projektihinnasto siirtymällä **Myynti**-alueella tilitietueeseen.</span><span class="sxs-lookup"><span data-stu-id="66106-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="66106-108">Avaa **Tilit**-luettelosivu.</span><span class="sxs-lookup"><span data-stu-id="66106-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="66106-109">Avaa **Tilit**-tietosivu etsimällä asiakastietue ja kaksoisnapsauttamalla sitä.</span><span class="sxs-lookup"><span data-stu-id="66106-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="66106-110">Valitse **Projektihinnastot**-välilehdessä \*\*+ Uusi projektihinnasto^^.</span><span class="sxs-lookup"><span data-stu-id="66106-110">On the **Project Price lists** tab, select \*\*+ New Project Price List^^.</span></span>
4. <span data-ttu-id="66106-111">Valitse **Uusi projektihinnasto** -sivulla hinnasto avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="66106-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="66106-112">Vain hinnastot, joiden kontekstiksi on määritetty **Myynti** ja joiden valuutta vastaa tilivaluuttaa, ovat tässä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="66106-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="66106-113">Anna liitoksen nimi valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="66106-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="66106-114">Asiakaskohtainen projektihinnasto luodaan.</span><span class="sxs-lookup"><span data-stu-id="66106-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="66106-115">Tätä hinnastoa käytetään projektihintojen oletuksena tälle asiakkaalle projektitarjouksissa tai -sopimuksissa, joissa tarjouksen tai projektin sopimuksen luontipäivä on hinnaston voimassaolopäivänä.</span><span class="sxs-lookup"><span data-stu-id="66106-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="66106-116">Projektitarjousten mukautettu hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="66106-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="66106-117">Projektitarjouksissa projektin hinnoittelu voi alkaa oletusarvoisesti vakiohinnastosta, joka saadaan oletuksena asiakkaalta tai projektiparametreista.</span><span class="sxs-lookup"><span data-stu-id="66106-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="66106-118">Jos tarvitset projektiin liittyvään työhön mukautetun hinnoittelun jossakin tarjouksessa, saat sen projektihinnastoon liitetystä entiteetistä.</span><span class="sxs-lookup"><span data-stu-id="66106-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="66106-119">Määritä tarjouskohtainen projektin hinnoittelu seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="66106-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="66106-120">Avaa projektitarjous ja valitse **Projektihinnastot**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="66106-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="66106-121">Valitse aliruudukossa **Luo mukautettu hinnoittelu**.</span><span class="sxs-lookup"><span data-stu-id="66106-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="66106-122">Kaikki tarjoukseen liitetyt projektihinnastot kopioidaan uusiin hinnastoihin.</span><span class="sxs-lookup"><span data-stu-id="66106-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="66106-123">Uusien hinnastojen nimet vastaavat tarjouksen nimeä, ja niissä on päivämäärä- ja aikaleima, joka ilmaisee hinnastojen luontiajankohdan.</span><span class="sxs-lookup"><span data-stu-id="66106-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="66106-124">Voit käyttää näitä hinnastoja ja päivittää työn (roolin hinta) ja kulujen (luokkahinta) hinnat.</span><span class="sxs-lookup"><span data-stu-id="66106-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="66106-125">Näitä hintoja käytetään vain kyseisessä projektitarjouksessa.</span><span class="sxs-lookup"><span data-stu-id="66106-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="66106-126">Projektisopimuksen hinnastot</span><span class="sxs-lookup"><span data-stu-id="66106-126">Price lists on a project contract</span></span>

<span data-ttu-id="66106-127">Projektisopimuksen projektihinnoittelun oletusarvona on aina mukautettu hinnasto, jossa on sopimuksen nimi ja jonka nimeen on lisätty luontipäivä- ja aikaleima.</span><span class="sxs-lookup"><span data-stu-id="66106-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="66106-128">Tämä pitää paikkansa riippumatta siitä. luontiinko sopimus silloin, kun tarjous voitettiin, vai luotiinko sopimus alusta alkaen.</span><span class="sxs-lookup"><span data-stu-id="66106-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="66106-129">Voit tarvittaessa poistaa tämän liitoksen mukautettuun hinnastoon ja liittää sen sijaan vakiohinnaston projektisopimukseen.</span><span class="sxs-lookup"><span data-stu-id="66106-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="66106-130">Jos liität vakiohinnaston tarjouksen tai sopimuksen projektihinnastoihin, hinnaston hintoihin tehdyt muutokset vaikuttavat kaikkiin hinnastoa käyttäviin tarjouksiin ja sopimuksiin.</span><span class="sxs-lookup"><span data-stu-id="66106-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
