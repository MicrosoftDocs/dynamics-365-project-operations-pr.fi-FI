---
title: Miten voin mukauttaa Projektin vaiheet -liiketoimintaprosessin?
description: Yleiskatsaus Projektin vaiheet -liiketoimintaprosessin mukauttamiseen.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d0168f187e6b0880713aac04bd87dbc2209197d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148999"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="0610a-103">Miten voin mukauttaa Projektin vaiheet -liiketoimintaprosessin?</span><span class="sxs-lookup"><span data-stu-id="0610a-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="0610a-104">Project Service -sovelluksen aiemmissa versioissa on rajoitus, jonka vuoksi Projektin vaiheet -liiketoimintaprosessin vaiheiden nimien on vastattava täsmälleen englanninkielisiä nimiä (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="0610a-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="0610a-105">Muussa tapauksessa englanninkielisiin vaiheiden nimiin tukeutuva liiketoimintalogiikka ei toimi odotetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="0610a-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="0610a-106">Tämän vuoksi projektilomakkeessa ei ole tuttuja toimintoja, kuten **Vaihda prosessia** tai **Muokkaa prosessia**, eikä liiketoimintaprosessin mukautusta suositella.</span><span class="sxs-lookup"><span data-stu-id="0610a-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="0610a-107">Tämä rajoitus on otettu huomioon versiossa 2.4.5.48 ja sitä uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="0610a-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="0610a-108">Tämä artikkeli sisältää ehdotetut ratkaisut sitä varten, että aiempien versioiden oletusliiketoimintaprosessia on mukautettava.</span><span class="sxs-lookup"><span data-stu-id="0610a-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="0610a-109">Liiketoimintalogiikkaa varten on annettava englanninkielisten vaiheiden nimien täsmälliset vastineet</span><span class="sxs-lookup"><span data-stu-id="0610a-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="0610a-110">Projektin vaiheet -liiketoimintaprosessi sisältää liiketoimintalogiikan, joka ohjaa sovelluksen seuraavaa toimintaa:</span><span class="sxs-lookup"><span data-stu-id="0610a-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="0610a-111">Kun projekti on liitetty tarjoukseen, koodi määrittää liiketoimintaprosessin vaiheeksi **Quote**.</span><span class="sxs-lookup"><span data-stu-id="0610a-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="0610a-112">Kun projekti on liitetty sopimukseen, koodi määrittää liiketoimintaprosessin vaiheeksi **Plan**.</span><span class="sxs-lookup"><span data-stu-id="0610a-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="0610a-113">Kun liiketoimintaprosessi on edennyt **Close**-vaiheeseen, projektitietueen aktivointi poistetaan.</span><span class="sxs-lookup"><span data-stu-id="0610a-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="0610a-114">Kun projektin aktivointi poistetaan, projektilomake ja työrakenne määritetään Vain luku -tilaan, nimetyt resurssin varaukset vapautetaan ja kaikkien liittyvien hinnastojen aktivoinnit poistetaan.</span><span class="sxs-lookup"><span data-stu-id="0610a-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="0610a-115">Tämä liiketoimintalogiikka edellyttää englanninkielisiä nimiä projektin vaiheissa.</span><span class="sxs-lookup"><span data-stu-id="0610a-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="0610a-116">Riippuvuus englanninkielisistä vaiheiden nimistä on pääsyy sille, miksi Projektin vaiheet -liiketoimintaprosessin mukauttamista ei suositella. Se on syy myös siihen, miksi projektin entiteetissä ei näy yleisiä liiketoimintaprosessien toimintoja, kuten **Vaihda prosessia** tai **Muokkaa prosessia**.</span><span class="sxs-lookup"><span data-stu-id="0610a-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="0610a-117">Mitä tapahtuu, jos vaiheiden nimet eivät vastaa englanninkelisiä nimiä?</span><span class="sxs-lookup"><span data-stu-id="0610a-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="0610a-118">Jos Project Service -sovelluksen versiossa 1.x ympäristössä 8.2 liiketoimintaprosessin vaiheiden nimet eivät vastaa täysin englanninkielisiä vaiheiden nimiä, liiketoimintalogiikka, joka määrittää tarjousten ja sopimusten oikean vaiheen ja sulkee projektin, ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="0610a-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="0610a-119">Virhesanomia ei näytetä.</span><span class="sxs-lookup"><span data-stu-id="0610a-119">No error messages are displayed.</span></span> <span data-ttu-id="0610a-120">Tämän vuoksi vaikuttaa siltä, että Projektin vaiheet -liiketoimintaprosessin mukauttaminen toimii.</span><span class="sxs-lookup"><span data-stu-id="0610a-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="0610a-121">Automaattiset prosessit eivät kuitenkaan toimi tarjouksissa, sopimuksissa ja projektin sulkemisessa.</span><span class="sxs-lookup"><span data-stu-id="0610a-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="0610a-122">Project Service -sovelluksen versiossa 2.4.4.30 tai aiemmassa versiossa ympäristössä 9.0 oli merkittävä arkkitehtuurimuutos liiketoimintaprosesseissa. Muutoksen vuoksi liiketoimintaprosessin liiketoimintalogiikka piti kirjoittaa uudelleen.</span><span class="sxs-lookup"><span data-stu-id="0610a-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="0610a-123">Jos projektin vaiheiden nimet eivät vastaa odotettuja englanninkielisiä nimiä, virhesanomaa ei näytetä.</span><span class="sxs-lookup"><span data-stu-id="0610a-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="0610a-124">Jos siis haluat mukauttaa projektin entiteetin Projektin vaiheet -liiketoimintaprosessia, voit lisätä vain aivan uusia vaiheita projektin entiteetin oletusliiketoimintaprosessiin. **Quote**-, **Plan**- ja **Close**-vaiheita ei saa muuttaa.</span><span class="sxs-lookup"><span data-stu-id="0610a-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="0610a-125">Rajoitus varmistaa sen, että liiketoimintaprosessi ei aiheuta virheitä. Liiketoimintaprosessi vaatii englanninkieliset vaiheiden nimet.</span><span class="sxs-lookup"><span data-stu-id="0610a-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="0610a-126">Tässä artikkelissa kuvattu liiketoimintalogiikka on poistettu versiossa 2.4.5.48 tai sitä uudemmissa versioissa projektin entiteetin oletusliiketoimintaprosessista.</span><span class="sxs-lookup"><span data-stu-id="0610a-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="0610a-127">Kun otat käyttöön kyseisen version tai myöhemmän version, voit mukauttaa oletusliiketoimintaprosessia tai korvata sen omalla prosessilla.</span><span class="sxs-lookup"><span data-stu-id="0610a-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="0610a-128">Aiempien versioiden ratkaisuehdotukset</span><span class="sxs-lookup"><span data-stu-id="0610a-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="0610a-129">Jos version päivittäminen ei ole vaihtoehto, voit mukauttaa projektin entiteetin Projektin vaiheet -liiketoimintaprosessin jommallakummalla seuraavista tavoista:</span><span class="sxs-lookup"><span data-stu-id="0610a-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="0610a-130">Lisää oletusmääritykseen vaiheita samalla, kun säilytät englanninkieliset nimet **Quote**-, **Plan**- ja **Close**-vaiheille.</span><span class="sxs-lookup"><span data-stu-id="0610a-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Oletusmäärityksen vaiheiden lisäämisen näyttökuva](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="0610a-132">Luo oma liiketoimintaprosessi ja tee siitä projektin entiteetin ensisijainen liiketoimintaprosessi. Tällöin voit antaa vaiheille haluamasi nimet.</span><span class="sxs-lookup"><span data-stu-id="0610a-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="0610a-133">Jos kuitenkin haluat käyttää samoja projektin vakiovaiheita eli **Quote**-, **Plan**- ja **Close**-vaiheita, sinun on tehtävä joitakin mukautuksia, jotka saadaan mukautetuista vaiheiden nimistä.</span><span class="sxs-lookup"><span data-stu-id="0610a-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="0610a-134">Projektin sulkeminen sisältää monimutkaisempaa logiikkaa. Voit kuitenkin käynnistää sen poistamalla projektitietueen aktivoinnin.</span><span class="sxs-lookup"><span data-stu-id="0610a-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Liiketoimintaprosessin mukauttaminen](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="0610a-136">Erityisiä huomioita Project Service -sovelluksen versiosta 2.4.4.30 tai aiemmista versioista ympäristössä 9.0</span><span class="sxs-lookup"><span data-stu-id="0610a-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="0610a-137">Mukautetun liiketoimintaprosessin omaavassa Project Service -versiossa 2.4.4.30 tai aiemmassa versiossa ympäristössä 9.0 projektin entiteetin **Vaiheen nimi** -kenttä, jota käytetään **Projekti vaiheen mukaan** -kaaviossa ja projektiluettelonäkymissä, ei päivity, koska se on yhdistetty Projektin vaiheet -oletusliiketoimintaprosessiin.</span><span class="sxs-lookup"><span data-stu-id="0610a-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="0610a-138">Tämä ongelma voidaan ratkaista seuraavien vaiheiden avulla:</span><span class="sxs-lookup"><span data-stu-id="0610a-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="0610a-139">Lisää mukautettu kenttä, joka sieppaa nykyisen liiketoimintaprosessin vaiheen, joka päivitetään samalla kun käyttäjä siirtyy mukautetussa liiketoimintaprosessissa.</span><span class="sxs-lookup"><span data-stu-id="0610a-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="0610a-140">Muokkaa **Projekti vaiheen mukaan** kaaviota niin, että sitä voi käyttää mukautetun kentän kanssa oletusmäärityksen sijaan.</span><span class="sxs-lookup"><span data-stu-id="0610a-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="0610a-141">Vaiheet, joiden avulla luodaan oma liiketoimintaprosessi projektin entiteettiä varten</span><span class="sxs-lookup"><span data-stu-id="0610a-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="0610a-142">Voit luoda oman liiketoimintaprosessin projektin entiteettiä varten seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="0610a-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="0610a-143">Siirry kohtaan **Asetukset** > **Prosessikeskus**.</span><span class="sxs-lookup"><span data-stu-id="0610a-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="0610a-144">Älä kopioi Projektin vaiheet -liiketoimintaprosessia, koska silloin myös Project Service -sovelluksen liiketoimintalogiikka kopioidaan.</span><span class="sxs-lookup"><span data-stu-id="0610a-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Luo prosessi](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="0610a-146">Luo haluamasi vaiheiden nimet prosessin suunnitteluohjelman avulla.</span><span class="sxs-lookup"><span data-stu-id="0610a-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="0610a-147">Jos haluat samat toiminnot kuin **Quote**-, **Plan**- ja **Close**-oletusvaiheissa on, luonnin on perustuttava mukautetun liiketoimintaprosessin vaiheiden nimiin.</span><span class="sxs-lookup"><span data-stu-id="0610a-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Liiketoimintaprosessin mukautuksessa käytettävän prosessin suunnitteluohjelman näyttökuva](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="0610a-149">Tee mukautetusta liiketoimintaprosessista projektin entiteetin ensisijainen liiketoimintaprosessi valitsemalla prosessin suunnitteluohjelmassa **Prosessin järjestys** -kohta. Siirrä projektin entiteetti Projektin vaiheet -liiketoimintaprosessin yläpuolelle luettelon yläosaan.</span><span class="sxs-lookup"><span data-stu-id="0610a-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="0610a-150">Prosessin järjestyksen käyttämisen näyttökuva</span><span class="sxs-lookup"><span data-stu-id="0610a-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="0610a-151">Seuraavat vaiheet koskevat Project Service -sovelluksen versiota 2.4.4.30 tai aiempaa versiota ympäristössä 9.0</span><span class="sxs-lookup"><span data-stu-id="0610a-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="0610a-152">Lisää uusi mukautettu kenttä projektin entiteettiin ja sieppaa mukautetut vaiheet mukautettuun liiketoimintaprosessiin.</span><span class="sxs-lookup"><span data-stu-id="0610a-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="0610a-153">Lisää liiketoimintalogiikka (laajennus/työnkulku) ja päivitä tämä kenttä, kun mukautetun liiketoimintaprosessin vaihe päivitetään.</span><span class="sxs-lookup"><span data-stu-id="0610a-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Projektin entiteetin mukautuksen näyttökuva](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="0610a-155">Muokkaa **Projekti vaiheen mukaan** -kaaviota, kun haluat käyttää vaiheiden uutta mukautettua kenttää.</span><span class="sxs-lookup"><span data-stu-id="0610a-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Projekti vaiheen mukaan -kaavion käyttämisen näyttökuva](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="0610a-157">Muokkaa projektin entiteetin näkymiä ja sisällytä vaiheiden uusi mukautettu kenttä.</span><span class="sxs-lookup"><span data-stu-id="0610a-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Projektin entiteetin näkymien muokkaamisen näyttökuva](media/FAQ-Customize-BPF-8-720.png)

