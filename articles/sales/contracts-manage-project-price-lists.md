---
title: Projektihinnastojen hallinta projektisopimuksissa
description: Tässä aiheessa on tietoja projektisopimusten projektihinnastojen hallinnasta.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3313eef74b5e7a0624b32d2a336cd986dfdda839
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010377"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="38823-103">Projektihinnastojen hallinta projektisopimuksissa</span><span class="sxs-lookup"><span data-stu-id="38823-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="38823-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="38823-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="38823-105">Dynamics 365 Project Operationsin projektisopimukset on suunniteltu tukemaan sopimuksessa useita voimassaolopäiviä käyttäviä myyntihinnastoja.</span><span class="sxs-lookup"><span data-stu-id="38823-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="38823-106">Project Operationsissa on uusi **Projektihinnastot**-niminen liitetty entiteetti.</span><span class="sxs-lookup"><span data-stu-id="38823-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="38823-107">Tällä entiteetillä on yksi moneen -suhde projektisopimukseen.</span><span class="sxs-lookup"><span data-stu-id="38823-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="38823-108">Projektin hinnastoilla hinnoitellaan aikaa, materiaalia ja kulutapahtumia projektissa.</span><span class="sxs-lookup"><span data-stu-id="38823-108">Project price lists are used to price time, material, and expense transactions on a project.</span></span> <span data-ttu-id="38823-109">Kun sopimuksessa on yksi tai useampi projektihinnasto, näitä hinnastoja käytetään ajan, materiaalinen, kuluarvioiden ja toteutuneiden arvojen hinnoitteluun projekteissa, jotka liittyvät sopimukseen sopimusrivin kautta.</span><span class="sxs-lookup"><span data-stu-id="38823-109">When a contract has one or more project price lists, these price lists are used to price for time, material, expense estimates, and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="38823-110">Kun projektisopimuksessa ei ole projektihinnastoja, näkyviin tulee varoitus siitä, että projektihinnastoja ei ole, ja arvioitasi, projektin todellista työtä, materiaalia ja kirjattuja kuluja ei hinnoitella.</span><span class="sxs-lookup"><span data-stu-id="38823-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, material, and expenses logged will not be priced.</span></span> <span data-ttu-id="38823-111">Myyntiarvoilla ei ole hintaa.</span><span class="sxs-lookup"><span data-stu-id="38823-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="38823-112">Projektihinnaston liittäminen projektisopimukseen tai tämän liitoksen poistaminen</span><span class="sxs-lookup"><span data-stu-id="38823-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a><span data-ttu-id="38823-113">Tietyn hinnaston luominen tai liittäminen projektipohjaisen työn, materiaalin ja kulujen arvioimista varten</span><span class="sxs-lookup"><span data-stu-id="38823-113">Create or associate a specific price list for estimating project-based work, material, and expenses</span></span>

1. <span data-ttu-id="38823-114">Valitse projektisopimuksessa **Projektihinnastot**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="38823-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="38823-115">Valitse aliruudukossa **+ Lisää uusi projektihinnasto**.</span><span class="sxs-lookup"><span data-stu-id="38823-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="38823-116">Valitse hinnasto **Pikaluonti**-liukusäätimessä.</span><span class="sxs-lookup"><span data-stu-id="38823-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="38823-117">Avattavassa luettelossa on kaikki hinnastot, joiden kontekstiksi on määritetty **Myynti** ja joiden valutta vastaa sopimuksen valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="38823-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="38823-118">Annan projektihinnaston liitoksen kuvaus, valitse **Tallenna** ja sulje sitten **Pikaluonti**-liukusäädin.</span><span class="sxs-lookup"><span data-stu-id="38823-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="38823-119">Projektihinnaston liitos luodaan.</span><span class="sxs-lookup"><span data-stu-id="38823-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="38823-120">Jos haluat lisätä useita projektihinnastoja projektisopimukseen toista vaiheet 1–4.</span><span class="sxs-lookup"><span data-stu-id="38823-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="38823-121">Luo useita projektihinnastoja vain, jos kullakin liitetyllä projektihinnastolla on eri voimassaolopäivä.</span><span class="sxs-lookup"><span data-stu-id="38823-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="38823-122">Project Operations ei tue projektihinnastoja, joissa on päällekkäiset voimassaolopäivät.</span><span class="sxs-lookup"><span data-stu-id="38823-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="38823-123">Jos tietyn päivämäärän tapahtumalla on useita projektihinnastoja, kyseisen tapahtuman hinta palautetaan oletusarvoon nolla.</span><span class="sxs-lookup"><span data-stu-id="38823-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="38823-124">Projektihinnaston liitoksen poistaminen</span><span class="sxs-lookup"><span data-stu-id="38823-124">Remove a project price list association</span></span>

- <span data-ttu-id="38823-125">Valitse projektihinnasto ja valitse sitten aliruudukossa **Poista sopimuksen hinnasto**.</span><span class="sxs-lookup"><span data-stu-id="38823-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="38823-126">Hinnasto poistetaan sopimuksen projektihinnastoista.</span><span class="sxs-lookup"><span data-stu-id="38823-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="38823-127">Itse hinnastoa ei poisteta.</span><span class="sxs-lookup"><span data-stu-id="38823-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="38823-128">Sen sijaan vain liitos sopimukseen poistetaan.</span><span class="sxs-lookup"><span data-stu-id="38823-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="38823-129">Sopimuksen projektihinnaston automaattisten oletusarvojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="38823-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="38823-130">Projektihinnasto voidaan määrittää projektin oletushinnastoksi.</span><span class="sxs-lookup"><span data-stu-id="38823-130">A project price list can be set up as the default project price list.</span></span> <span data-ttu-id="38823-131">Tämä määritys varmistaa, että kaikki organisaation sopimukset alkavat aina vakiomuotoisella projektihinnastolla kyseiselle ajanjaksolle.</span><span class="sxs-lookup"><span data-stu-id="38823-131">This setup ensures that all contracts in your organization always start with a standard project price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="38823-132">Organisaation oletusprojektihinnaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="38823-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="38823-133">Valitse ensin **Asetukset** > **Yleiset** ja sitten **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="38823-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="38823-134">Valitse **Aktiiviset parametrit** -luettelosivulla tietue ja avaa se kaksoisnapsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="38823-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="38823-135">Kun kaksoisnapsautat tietuetta, varmista, ettet napsauta sellaista kentän arvo, joka on hyperlinkki.</span><span class="sxs-lookup"><span data-stu-id="38823-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="38823-136">Valitse **Aktiiviset parametrit** -sivulla **Hinnasto**-luettelo. Oletushinnastojen luettelo näkyy aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="38823-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="38823-137">Kyseinen luettelo on vakiokustannusten ja myyntihinnastojen luettelo.</span><span class="sxs-lookup"><span data-stu-id="38823-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="38823-138">**Myynti**-hinnaston liittäminen tässä kohdassa jokaiseen valuuttaan, jolla myyntiä tehdään, varmistaa, että myyntihinnasto on oletushinnasto jokaisessa sopimuksessa, joka luodaan kyseistä valuuttaa käyttävälle asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="38823-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="38823-139">Asiakaskohtaisen projektihinnaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="38823-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="38823-140">Asiakaskohtainen projektihinnasto voidaan määrittää, kun asiakkaiden kanssa on neuvoteltu hinnoittelun pääsopimus.</span><span class="sxs-lookup"><span data-stu-id="38823-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="38823-141">Valitse **Myynti** > **Asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="38823-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="38823-142">Valitse aktiivisten asiakkaiden luettelosta asiakas, jolla on erikoishinnasto.</span><span class="sxs-lookup"><span data-stu-id="38823-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="38823-143">Avaa asiakastietue valitsemalla se ja valitse sitten **Projektihinnastot**-välilehti. Aliruudukossa on näkyvissä kyseisen asiakkaan hinnastot.</span><span class="sxs-lookup"><span data-stu-id="38823-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="38823-144">Luo kyseisestä asiakasta koskeva projektihinnasto luomalla tässä kohdassa uusi hinnastoliitos.</span><span class="sxs-lookup"><span data-stu-id="38823-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="38823-145">Projektisopimuksen mukautettu hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="38823-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="38823-146">Kun organisaation oletusprojektihinnastot ja asiakaskohtaiset projektihinnastot ovat käytettävissä, luotavissa projektisopimuksissa käytetään automaattisesti näitä projektihinnastoliitoksia.</span><span class="sxs-lookup"><span data-stu-id="38823-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="38823-147">Projektisopimuksen projektihinnastot kuitenkin kopioidaan aina siten, että niihin on liitetty päivämäärä ja sopimuksen nimi.</span><span class="sxs-lookup"><span data-stu-id="38823-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="38823-148">Tili- ja projektipäälliköt voivat sitten muokata hintoja näissä kopioiduissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="38823-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="38823-149">Tällä tavoin muutettuja hintoja käytetään vain kyseisessä projektisopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="38823-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
