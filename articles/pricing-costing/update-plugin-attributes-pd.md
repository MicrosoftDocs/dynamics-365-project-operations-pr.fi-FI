---
title: Uusien hinnoitteludimensioiden päivittäminen laajennusmääritteisiin
description: Tässä aiheessa on tietoja laajennusmääritteiden päivittämisestä hinnoitteludimensioille.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643214"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="3e3a5-103">Uusien hinnoitteludimensioiden päivittäminen laajennusmääritteisiin</span><span class="sxs-lookup"><span data-stu-id="3e3a5-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="3e3a5-104">Tässä aiheessa on tietoja laajennusmääritteiden päivittämisestä hinnoitteludimensioille.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="3e3a5-105">Tämä aihe koskee vain tarjous- ja sopimusominaisuuksia Dynamics 365 Project Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3e3a5-106">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="3e3a5-106">Prerequisites</span></span>
<span data-ttu-id="3e3a5-107">Ennen kuin suoritat tässä aiheessa kuvatut vaiheet, seuravissa aiheissa kuvattujen toimintosarjojen on oltava suoritettuina:</span><span class="sxs-lookup"><span data-stu-id="3e3a5-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="3e3a5-108">Mukautettujen kenttien ja entiteettien luominen</span><span class="sxs-lookup"><span data-stu-id="3e3a5-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="3e3a5-109">Mukautettujen kenttien lisääminen hintamääritys- ja tapahtumaentiteetteihin </span><span class="sxs-lookup"><span data-stu-id="3e3a5-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="3e3a5-110">[Mukautettujen kenttien määrittäminen hinnoitteludimensioiksi](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="3e3a5-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="3e3a5-111">Jos et ole suorittanut näitä toimintosarjoja loppuun, suorita ne ja palaa sen jälkeen tähän aiheeseen.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="3e3a5-112">Laajennuksen rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="3e3a5-112">Register a plug-in</span></span>
<span data-ttu-id="3e3a5-113">Kun tarjousrivin tieto luodaan **Tarjousrivi**-sivulla projektin tarjouriville, järjestelmä luo kaksi arvioriviä.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="3e3a5-114">Yksi rivi on arvion kustannuspuolelle, ja toinen rivi on myyntipuolelle.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="3e3a5-115">Tämä on sama projektin sopimusriveille.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="3e3a5-116">Kun teet muutoksen määrään tai kenttään kustannuspuolelle, muutos tehdään myös myyntipuolelle.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="3e3a5-117">Tämä on mahdollista siksi, että PreOperation-laajennukset, jotka liittyvät Quotelinedetail- ja contractline detail - entiteetteihin, yhdistävät erityiset määritteet kustannuspuolella tapahtuman myyntipuoleen.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="3e3a5-118">Jos myyntipuolen hinnoitteludimensioihin tehtyjen muutosten on tultava tehdyiksi myös kustannuspuolelle, seuraavat laajennuksen on rekisteröitävä uudelleen hinnoitteludimensioihin tehtyjen muutosten jälkeen.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="3e3a5-119">Nämä laajennukset on päivitettävä ja rekisteröitävä uudelleen:</span><span class="sxs-lookup"><span data-stu-id="3e3a5-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="3e3a5-120">PreOperationContractLineDetailUpdate - **Päivitä msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="3e3a5-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="3e3a5-121">PreOperationQuoteLineDetailUpdate - **Päivittää msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="3e3a5-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="3e3a5-122">Päivitä laajennukset ja rekisteröi ne uudelleen suorittamalla seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="3e3a5-123">Avaa **PluginRegistrationTool** ja muodosta yhteys Project Operations Dataverse -ympäristöösi.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="3e3a5-124">Valitse **Haku** ja kirjoita päivitettävän laajennuksen ensimmäiset kirjaimet.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="3e3a5-125">Kun laajennus löytyy, valitse se ja napauta sitten **Valitse päälomakkeessa**.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="3e3a5-126">Valitse **Päivitä msdyn_orderlinetransaction** -vaihe, napauta oikealla hiiren painikkeella ja valitse sitten **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="3e3a5-127">Vailtse **Päivitä**-dialogisivulla kolme pistettä (**...**) suodatusmääritteistä.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="3e3a5-128">Näkyviin tulee suodatusmääritteet-ikkuna, jossa on luettelo kaikista entiteetin määritteistä ja hinnoitteludimensioista.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="3e3a5-129">Valitse hinnoitteludimension määritteiden valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="3e3a5-130">Valitse **OK** sulkeaksesi sivun ja valitse sitten **Päivitysvaihe**.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="3e3a5-131">Toista vaiheet 2–7 toiselle laajennukselle, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="3e3a5-132">Tätä laajennusta varten on päivitettävä **Päivitä msdyn_quotelinetransaction** -vaihe.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="3e3a5-133">Sulje **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="3e3a5-133">Close **PluginRegistrationTool**.</span></span>
