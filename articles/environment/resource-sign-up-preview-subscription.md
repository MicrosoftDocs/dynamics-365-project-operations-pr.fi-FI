---
title: Rekisteröi resurssien/ei-varastoitavien skenaarioiden Project Operations -esiversiotilaus
description: Tässä aiheessa on tietoja siitä, miten tilataan ja otetaan käyttöön Project Operations resurssien/ei-varastoitavien skenaarioille.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334823"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="f7fd1-103">Rekisteröi resurssien/ei-varastoitavien skenaarioiden Project Operations -esiversiotilaus</span><span class="sxs-lookup"><span data-stu-id="f7fd1-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="f7fd1-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="f7fd1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f7fd1-105">Tässä aiheessa kerrotaan, miten kokeilutarjouksen tilaaminen ja Project Operations -ympäristön käyttöönotto resurssi- tai ei-varastopohjaisissa skenaarioissa suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f7fd1-106">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="f7fd1-106">Prerequisites</span></span>
- <span data-ttu-id="f7fd1-107">Esiversion käyttöön ottavalla käyttäjällä on oltava Azure-vuokraajaan yleisen järjestelmänvalvojan oikeudet.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="f7fd1-108">Voit luoda vuokraajan ensimmäisen tarjouksen aikana.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="f7fd1-109">Finance-ympäristön käyttöönotto edellyttää voimassaolevaa Azure-tilausta, joka laskutetaan ympäristökohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="f7fd1-110">Voit aloittaa käyttämällä organisaatiosi olemassa olevaa tilausta tai [Azure-kokeiluversiota](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="f7fd1-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="f7fd1-111">CDS-ympäristö on maksuton rajoitetulle 30 päivän jaksolle.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7fd1-112">Vain yksi henkilö, vuokraajan järjestelmänvalvoja, voi suorittaa tämän tehtävän organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="f7fd1-113">Jos et ole tämän version tilaaja, odota, kunnes organisaatiosi on rekisteröitynyt ja olet saanut käyttäjätietosi.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="f7fd1-114">Kokeiluversiot ovat kertakäyttöisiä vuokraajalle.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="f7fd1-115">Voit suorittaa kokeiluversion vain kerran.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-115">You can only run a trial one time.</span></span> <span data-ttu-id="f7fd1-116">On suositeltavaa luoda uusi vuokraaja kokeilua varten.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="f7fd1-117">Dynamics 365 Project Operations (CE) – esikatselun kokeiluversio</span><span class="sxs-lookup"><span data-stu-id="f7fd1-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="f7fd1-118">Ennen kuin aloitat, varmista, että olet kirjautunut selaimeen, jossa on käyttäjän työtili, siinä vuokraajan kohdassa, jossa haluat projektin toimintojen esikatselun.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="f7fd1-119">Lunasta ensimmäinen tarjouskoodi, **Dynamics 365 Project Operations** täällä [Project Operations -kokeiluversio](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="f7fd1-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="f7fd1-120">Vahvista tilaus.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-120">Confirm your order.</span></span>

  <span data-ttu-id="f7fd1-121">Näkyviin tulee vahvistus siitä, että tarjouksen lunastaminen onnistui.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="f7fd1-122">Dynamics 365 Finance – esiversion kokeilu</span><span class="sxs-lookup"><span data-stu-id="f7fd1-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="f7fd1-123">Siirry [Dynamics 365 for Finance Preview -kokeiluversioon](https://aka.ms/trypoche) ja toista edellisen osan vaiheet tarjoukselle. Rekisteröidy pilvipalvelussa isännöityyn ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="f7fd1-124">Käyttöoikeuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f7fd1-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7fd1-125">Tarvitset järjestelmänvalvojan käyttöoikeudet organisaatiosi Microsoft 365 -portaaliin, jotta voit suorittaa seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="f7fd1-126">Siirry [Microsoft 365 -hallintakeskukseen](https://portal.office.com/) ja määritä käyttöoikeudet käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="f7fd1-127">Valitse **Aktiiviset käyttäjät** -sivulla käyttäjät, joille haluat määrittää käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="f7fd1-128">Tarkista, että **Dynamics 365 Project Operations** -lisenssi on valittu, ja valitse **Tallenna muutokset**.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="f7fd1-129">Finance-kokeilun tarjousta ei tarvitse delegoida käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="f7fd1-130">Aloita uusi projekti LCS:ssä</span><span class="sxs-lookup"><span data-stu-id="f7fd1-130">Start a new project in LCS</span></span>

<span data-ttu-id="f7fd1-131">Luo uusi LCS-projekti aiheessa [Aloita uusi projekti LCS:ssä](create-lcs-project.md) kuvatulla tavalla</span><span class="sxs-lookup"><span data-stu-id="f7fd1-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="f7fd1-132">Azure-tilauksen lisääminen LCS-projektiin</span><span class="sxs-lookup"><span data-stu-id="f7fd1-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="f7fd1-133">Voit suorittaa tämän tehtävän noudattamalla ohjeitaaiheessa [Lisää Azure-tilaus LCS-projektiin](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="f7fd1-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="f7fd1-134">Finance-esittely-ympäristön käyttöönotto Project Operationsin resurssien/ei-varastoitavien skenaarioille</span><span class="sxs-lookup"><span data-stu-id="f7fd1-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="f7fd1-135">Noudata ohjeita aiheessa [Uuden ympäristön valmistelu](resource-provision-new-environment.md) vimeistelläksesi käyttöönoton.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="f7fd1-136">Käytä [esittely-ympäristö](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) -käyttöönottotyyppiä esiversiossa.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="f7fd1-137">Asenna CDS:n määritys- ja konfiguraatiotiedot</span><span class="sxs-lookup"><span data-stu-id="f7fd1-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="f7fd1-138">Asenna CDS:n määritys- ja konfiguraatiotiedot aiheessa [Konfiguraatiotietojen määritys ja käyttöönotto Common Data Servicessa](resource-apply-pro-setup-config-data.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="f7fd1-139">Suorita tämä vaihe vasta, kun Finance-esittely-ympäristö on otettu käyttöön ja esittelytiedot ovat käyttövalmiita.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
