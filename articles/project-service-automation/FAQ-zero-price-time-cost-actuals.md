---
title: Miksi toteutuneen ajan kustannuksen oletushinta on nolla?
description: Tee vianmääritys ja selvitä, miksi toteutuneen ajan kustannuksen hinnan oletusarvo on 0.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 597d75b7-fadf-4947-8d52-95425ff90324
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 448c6c0569a40e1d7cb133561435811ecedb4356
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751279"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="fdee1-103">Miksi toteutuneen ajan kustannuksen oletushinta on nolla?</span><span class="sxs-lookup"><span data-stu-id="fdee1-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fdee1-104">Nämä usein kysytyt kysymykset koskevat toteutuneita arvoja, joissa tapahtuman luokaksi on määritetty Aika ja tapahtumatyypiksi Kustannus.</span><span class="sxs-lookup"><span data-stu-id="fdee1-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="fdee1-105">Seuraavien kolmen tarkistuksen avulla voit tehdä vianmäärityksen ja selvittää, miksi hinnan oletusarvo on 0 toteutuneen ajan kustannukselle.</span><span class="sxs-lookup"><span data-stu-id="fdee1-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="fdee1-106">Tarkistus 1: Määritä projektin kustannushinnasto</span><span class="sxs-lookup"><span data-stu-id="fdee1-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="fdee1-107">Etsi projekti toteutuneesta projektikentästä ja siirry sitten projektin sivulle.</span><span class="sxs-lookup"><span data-stu-id="fdee1-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="fdee1-108">Valitse kentässä sopimusyksikön linkki.</span><span class="sxs-lookup"><span data-stu-id="fdee1-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="fdee1-109">Tarkista Sopimusyksikkö-sivulla, onko sopimusyksiköllä hinnasto Kustannushinnastot-ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="fdee1-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="fdee1-110">Jos hinnastoja on useita, olet eristänyt ongelman.</span><span class="sxs-lookup"><span data-stu-id="fdee1-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="fdee1-111">Project Service tukee vain yhtä hinnastoa organisaatioyksikköä kohti.</span><span class="sxs-lookup"><span data-stu-id="fdee1-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="fdee1-112">Poista tästä entiteetistä kaikki muut hinnastot paitsi organisaatioyksikön Kustannushinnastot-ruudukon yksi hinnasto.</span><span class="sxs-lookup"><span data-stu-id="fdee1-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="fdee1-113">Jos organisaatioyksikköön ei ole liitetty hinnastoja, merkitse organisaatioyksikön valuutta muistiin.</span><span class="sxs-lookup"><span data-stu-id="fdee1-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="fdee1-114">Siirry Project Service -sovellukseen ja sitten Parametrit-kohtaan. Avaa Hinnastot-välilehti ja tarkista, onko siellä hinnastoja, joiden kontekstiksi on määritetty Kustannus ja valuutaksi organisaatioyksikön valuutta.</span><span class="sxs-lookup"><span data-stu-id="fdee1-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="fdee1-115">Jos ehtoja vastaavia hinnastoja ei ole, olet eristänyt ongelman.</span><span class="sxs-lookup"><span data-stu-id="fdee1-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="fdee1-116">Varmista, että vähintään yhden hinnaston kontekstiksi on määritetty Kustannus ja valuutta on sama kuin organisaatioyksikön valuutta.</span><span class="sxs-lookup"><span data-stu-id="fdee1-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="fdee1-117">Jos ehtoja vastaavia hinnastoja on useita, jatka tämän asiakirjan lukemista ja tee lisätarkistuksia.</span><span class="sxs-lookup"><span data-stu-id="fdee1-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="fdee1-118">Tarkistus 2: Onko jokin yllä määritetyistä hinnastoista sallittu toteutuneen ajan kustannuksen määritettynä päivämääränä?</span><span class="sxs-lookup"><span data-stu-id="fdee1-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="fdee1-119">Project Service -sovelluksessa voidaan käyttää oletushintojen hinnastoa, jos hinnasto on käytössä toteutuneen ajan kustannuksen päivämääränä.</span><span class="sxs-lookup"><span data-stu-id="fdee1-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="fdee1-120">Tarkista seuraavat kohdat ja varmista, ovatko yllä määritetyt hinnastot käytettävissä:</span><span class="sxs-lookup"><span data-stu-id="fdee1-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="fdee1-121">Tarkista, että liitettyjen hinnastojen Yleinen-välilehden alku- ja loppupäivämäärät on määritetty.</span><span class="sxs-lookup"><span data-stu-id="fdee1-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="fdee1-122">Jos yllä määritettyjä hinnastojen alku- ja loppupäivämääriä ei ole määritetty, olet eristänyt ongelman.</span><span class="sxs-lookup"><span data-stu-id="fdee1-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="fdee1-123">Ota toteutuneen ajan kustannuksen päivämääräkentän arvo muistiin ja tarkista, onko mikään hinnastoista käytössä kyseisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="fdee1-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="fdee1-124">Esimerkiksi toteutuneen ajan kustannuksen päivämäärän tulisi olla hinnaston alku- ja loppupäivämäärän välillä.</span><span class="sxs-lookup"><span data-stu-id="fdee1-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="fdee1-125">Jos toteutuneen ajan kustannuksen päivämäärä ei kuulu yhdenkään hinnaston päivämääräväliin, olet eristänyt ongelman.</span><span class="sxs-lookup"><span data-stu-id="fdee1-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="fdee1-126">Muokkaa hinnaston alku- ja loppupäivämääriä varmistaaksesi, että hinnasto kattaa toteutuneen ajan kustannuksen päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="fdee1-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="fdee1-127">Jos toteutuneen ajan kustannuksen päivämäärä kuuluu usean hinnaston päivämääräväliin, olet eristänyt ongelman.</span><span class="sxs-lookup"><span data-stu-id="fdee1-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="fdee1-128">Voit korjata ongelman muokkaamalla hinnastojen alku- ja loppupäivämääriä niin, että vain yksi hinnasto kattaa toteutuneen ajan kustannuksen päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="fdee1-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="fdee1-129">Jos toteutuneen ajan kustannuksen päivämäärän kattavia hinnastoja on vain yksi, siirry asiakirjassa seuraavaan tarkistukseen.</span><span class="sxs-lookup"><span data-stu-id="fdee1-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="fdee1-130">Kun olet tehnyt vaaditut korjaukset, voit luoda aikamerkinnän uudelleen ja hyväksyä sen. Tarkista, että toteutuneen ajan kustannuksella on sallittu hinta.</span><span class="sxs-lookup"><span data-stu-id="fdee1-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="fdee1-131">Tarkistus 3: Onko hinnastossa hinta toteutuneen ajan kustannuksen hinnoitteludimensioille?</span><span class="sxs-lookup"><span data-stu-id="fdee1-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="fdee1-132">Jos olet tarkistuksen 1 ja 2 suoritus onnistui, sinulla pitäisi olla nyt vain yksi hinnasto, joka käsittää toteutuneen ajan kustannuksen päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="fdee1-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="fdee1-133">Avaa tämä hinnasto ja siirry Roolin hinnat -välilehteen. Varmista, että toteutuneen ajan kustannuksen hinnoitteludimensioilla on rivi ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="fdee1-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="fdee1-134">Jos toteutuneen ajan kustannuksen hinnoitteludimensioiden roolin hinnan ruudukossa ei ole riviä, olet eristänyt ongelman.</span><span class="sxs-lookup"><span data-stu-id="fdee1-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="fdee1-135">Luo toteutuneen ajan kustannuksen hinnoitteludimensioiden Roolin hinnat -ruudukolle rivi.</span><span class="sxs-lookup"><span data-stu-id="fdee1-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="fdee1-136">Kun olet tehnyt tämän, voit luoda aikamerkinnän uudelleen ja hyväksyä sen. Tarkista, että toteutuneen ajan kustannuksen hinta on sallittu.</span><span class="sxs-lookup"><span data-stu-id="fdee1-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="fdee1-137">Jos toteutuneen ajan kustannuksella ei ole sallittua hintaa näiden kolmen edellä mainitun tarkistuksen jälkeen ole sallittu, kirjaa tukipyyntö.</span><span class="sxs-lookup"><span data-stu-id="fdee1-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



