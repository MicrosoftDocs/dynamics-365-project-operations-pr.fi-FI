---
title: Päivitä laajennusmääritteet sisältämään uudet hinnoitteludimensiot
description: Tässä aiheessa on tietoja laajennusmääritteiden päivittämisestä hinnoitteludimensioille.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c42e5fda79d51430f4dedf46037e11c86a38c474
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121844"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="b0e4d-103">Päivitä laajennusmääritteet sisältämään uudet hinnoitteludimensiot</span><span class="sxs-lookup"><span data-stu-id="b0e4d-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="b0e4d-104">Jos et käytä Project Service Automationin (PSA) tarjous- ja sopimusominaisuuksia, voit ohittaa tämän aiheen.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="b0e4d-105">Aihe olettaa, että olet suorittanut toimintosarjat aiheissa [Luo mukautettuja kenttiä ja entiteettejä](create-custom-fields-entities.md), [Lisää mukautettuja kenttiä hintojen määrittelyyn ja tapahtumaentiteetteihin](field-references.md) ja [Lisää mukautettuja kenttiä hintadimensioiksi](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="b0e4d-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="b0e4d-106">Jos et ole suorittanut näitä toimintosarjoja loppuun, palaa niihin ja suorita ne, ja palaa sen jälkeen tähän aiheeseen.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="b0e4d-107">Kun tarjousrivin tiedot luodaan **Tarjousrivi**-sivulla projektin tarjousriville, järjestelmä luo kaksi arvioriviä taustalle -- yhden rivin arvion kulupuolelle ja toisen myyntipuolelle.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="b0e4d-108">Tämä on sama projektin sopimusriveille.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="b0e4d-109">Kun teet muutoksen määrään tai kenttään kustannuspuolelle, muutos välitetään myyntipuolelle.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="b0e4d-110">Tämä on mahdollista seuraavien laajennusten vuoksi, jotka on rekisteröitävä uudelleen hinnoitteludimensioiden muutoksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="b0e4d-111">PreOperationContractLineDetailUpdate - Päivitykset **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="b0e4d-112">PreOperationQuoteLineDetailUpdate - Päivitykset **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="b0e4d-113">Seuraavissa vaiheissa selitetään, miten laajennukset rekisteröidään.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="b0e4d-114">Avaa **PluginRegistrationTool** ja muodosta yhteys online-ilmentymään.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="b0e4d-115">Napauta **Hae** ja etsi päivitettävä laajennus.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Kuvakaappaus hakupuusta](media/PRT-1.png)

3. <span data-ttu-id="b0e4d-117">Kun laajennus löytyy, valitse se ja napauta sitten **Valitse päälomakkeessa**.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="b0e4d-118">Valitse päivitettävän laajennuksen vaihe, napsauta hiiren kakkospainiketta ja valitse sitten **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Päivitettävän laajennuksen kuvakaappaus](media/PRT-2.png)
 
5. <span data-ttu-id="b0e4d-120">Napauta päivitysikkunassa painiketta, jossa on kolme pistettä (**...**) suodatusmääritteissä.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Kuvakaappaus määrittelytiedoista Nykyisen vaiheen päivittämiselle](media/PRT-3.png)
 
6. <span data-ttu-id="b0e4d-122">Valitse hinnoittelumääritteiden valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-122">Select the pricing attribute check boxes.</span></span>

 ![Kuvakaappaus, jossa valintaruutu valitaan hinnoittelumääritteille](media/PRT-4.png)

7. <span data-ttu-id="b0e4d-124">Napauta **OK** sulkeaksesi sivun ja valites sitten **Päivitysvaihe**.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Kuvakaappaus, jossa näkyy "Päivitysvaihe"-painike](media/PRT-5.png)
 
8. <span data-ttu-id="b0e4d-126">Toista tämä prosessi toiselle laajennukselle **PreOperationQuoteLineDetail - Päivitä msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="b0e4d-127">Sulje laajennuksen rekisteröintityökalu.</span><span class="sxs-lookup"><span data-stu-id="b0e4d-127">Close the plug-in registration tool.</span></span>
