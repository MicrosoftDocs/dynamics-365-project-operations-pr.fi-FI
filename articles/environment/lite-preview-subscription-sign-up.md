---
title: Rekisteröityminen esiversion tilaajaksi – lite
description: Tässä aiheessa on tietoja siitä, miten voit tilata ja ottaa käyttöön Project Operationsin lite – kauppa proformalaskutukseen -käyttöönoton.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334778"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="04c07-103">Rekisteröityminen esiversion tilaajaksi – lite</span><span class="sxs-lookup"><span data-stu-id="04c07-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="04c07-104">Tässä aiheessa selostetaan kokeilutarjouksen tilaamista ja Dynamics 365 Project Operations -lite-käyttöönottoa kaupasta proformalaskutukseen.</span><span class="sxs-lookup"><span data-stu-id="04c07-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="04c07-105">Tämä prosessi muuttuu Project Operationsin tulevissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="04c07-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="04c07-106">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="04c07-106">Prerequisites</span></span>
- <span data-ttu-id="04c07-107">Esiversion käyttöön ottavalla käyttäjällä on oltava Azure-vuokraajaan yleisen järjestelmänvalvojan oikeudet.</span><span class="sxs-lookup"><span data-stu-id="04c07-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="04c07-108">Voit luoda vuokraajan ensimmäisen tarjouksen aikana.</span><span class="sxs-lookup"><span data-stu-id="04c07-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04c07-109">Vain yksi henkilö, vuokraajan järjestelmänvalvoja, voi suorittaa tämän tehtävän organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="04c07-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="04c07-110">Jos et ole tämän version tilaaja, odota, kunnes organisaatiosi on rekisteröitynyt ja olet saanut käyttäjätietosi.</span><span class="sxs-lookup"><span data-stu-id="04c07-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="04c07-111">Kokeiluversiot ovat kertakäyttöisiä vuokraajalle.</span><span class="sxs-lookup"><span data-stu-id="04c07-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="04c07-112">Voit suorittaa kokeiluversion vain kerran.</span><span class="sxs-lookup"><span data-stu-id="04c07-112">You can only run a trial one time.</span></span> <span data-ttu-id="04c07-113">On suositeltavaa luoda uusi vuokraaja kokeilua varten.</span><span class="sxs-lookup"><span data-stu-id="04c07-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="04c07-114">Dynamics 365 Project Operations-kokeiluversio</span><span class="sxs-lookup"><span data-stu-id="04c07-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="04c07-115">Ennen kuin aloitat, varmista, että olet kirjautunut selaimeen, jossa on käyttäjän työtili, siinä vuokraajan kohdassa, jossa haluat projektin toimintojen esikatselun.</span><span class="sxs-lookup"><span data-stu-id="04c07-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="04c07-116">Siirry [Project Operations -kokeiluversioon](https://aka.ms/try-po) lunastaaksesi ensimmäisen tarjouskoodin, **Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="04c07-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="04c07-117">Vahvista tilaus.</span><span class="sxs-lookup"><span data-stu-id="04c07-117">Confirm your order.</span></span>

  <span data-ttu-id="04c07-118">Näet vahvistuksen, että tarjous on nyt onnistuneesti lunastettu.</span><span class="sxs-lookup"><span data-stu-id="04c07-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="04c07-119">Käyttöoikeuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="04c07-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04c07-120">Tarvitset järjestelmänvalvojan käyttöoikeudet organisaatiosi Microsoft 365 -portaaliin, jotta voit suorittaa seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="04c07-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="04c07-121">Siirry [Microsoft 365 -hallintakeskukseen](https://portal.office.com/) ja määritä käyttöoikeudet käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="04c07-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="04c07-122">Valitse **Aktiiviset käyttäjät** -sivulla käyttäjät, joille haluat määrittää käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="04c07-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="04c07-123">Tarkista, että **Dynamics 365 Project Operations** -käyttöoikeus on valittu.</span><span class="sxs-lookup"><span data-stu-id="04c07-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="04c07-124">Valitse **Tallenna muutokset**.</span><span class="sxs-lookup"><span data-stu-id="04c07-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="04c07-125">Uuden Dataverse -ympäristön luominen</span><span class="sxs-lookup"><span data-stu-id="04c07-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="04c07-126">Valmistele uusi Project Operations Dataverse -käyttöönottoympäristö noudattamalla aiheen [Dataverse-käyttöönoton malli](lite-deployment.md) -ohjeita.</span><span class="sxs-lookup"><span data-stu-id="04c07-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="04c07-127">Kun valitset ympäristötyypin, varmista, että käytät **kokeiluversiota (tilaukseen perustuva)**.</span><span class="sxs-lookup"><span data-stu-id="04c07-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![Uusi ympäristö](./media/19CreateEnvironment.png)

2. <span data-ttu-id="04c07-129">Valitse **Ota käyttöön Dynamics 365 -sovellukset** -asetus ja jätä **näiden sovellusten automaattinen käyttöönotto** tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="04c07-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="04c07-130">Valitse **Tallenna** luodaksesi ympäristön.</span><span class="sxs-lookup"><span data-stu-id="04c07-130">Select **Save** to create the environment.</span></span>

  ![Lisää tietokanta](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="04c07-132">Kun ympäristö on luotu, asenna **Microsoft Dynamics 365 Project Operations** -ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="04c07-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Asenna ratkaisu](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="04c07-134">Asenna CDS-määritys ja määritä esittelytiedot</span><span class="sxs-lookup"><span data-stu-id="04c07-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="04c07-135">Asenna CDS-määritykset ja määritä esittelytiedot noudattamalla ohjeita aiheessa [Ota käyttöön esittelyn määritystiedot](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="04c07-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
