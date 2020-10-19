---
title: Rekisteröi resurssien/ei-varastoitavien skenaarioiden Project Operations -esiversiotilaus
description: Tässä aiheessa on tietoja siitä, miten tilataan ja otetaan käyttöön Project Operations resurssien/ei-varastoitavien skenaarioille.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948842"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="38a56-103">Rekisteröi resurssien/ei-varastoitavien skenaarioiden Project Operations -esiversiotilaus</span><span class="sxs-lookup"><span data-stu-id="38a56-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="38a56-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="38a56-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="38a56-105">Tässä aiheessa kerrotaan, miten voit tilata esiversio-/kumppanitarjouksen ja ottaa käytöön Project Operations -ympäristön resurssien/ei-varastoitavien skenaarioille.</span><span class="sxs-lookup"><span data-stu-id="38a56-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="38a56-106">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="38a56-106">Prerequisites</span></span>

- <span data-ttu-id="38a56-107">Saat sähköpostiviestin, jossa saat kutsun osallistumaan esiversioon.</span><span class="sxs-lookup"><span data-stu-id="38a56-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="38a56-108">Voit pyytää esiversiota [Project Operations -sivustossa](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="38a56-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="38a56-109">Esiversion käyttöön ottavalla käyttäjällä on oltava Azure-vuokraajaan yleisen järjestelmänvalvojan oikeudet.</span><span class="sxs-lookup"><span data-stu-id="38a56-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="38a56-110">Finance-ympäristön käyttöönotto edellyttää voimassaolevaa Azure-tilausta, joka laskutetaan ympäristökohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="38a56-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="38a56-111">Voit aloittaa käyttämällä organisaatiosi olemassa olevaa tilausta tai [Azure-kokeiluversiota](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="38a56-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="38a56-112">CDS-ympäristö on maksuton rajoitetulle 30 päivän jaksolle.</span><span class="sxs-lookup"><span data-stu-id="38a56-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="38a56-113">Tilaa</span><span class="sxs-lookup"><span data-stu-id="38a56-113">Subscribe</span></span>

<span data-ttu-id="38a56-114">Kun [esiversiopyyntösi](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) hyväksytään, saat kaksi Microsoftin tarjousta sähköpostitse.</span><span class="sxs-lookup"><span data-stu-id="38a56-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="38a56-115">Näiden tarjousten avulla voit ottaa käyttöön Project Operationsin esikatselun:</span><span class="sxs-lookup"><span data-stu-id="38a56-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="38a56-116">Dynamics 365 Project Operations – esiversion kokeilu</span><span class="sxs-lookup"><span data-stu-id="38a56-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="38a56-117">Dynamics 365 for Finance and Operations – esiversion kokeilu</span><span class="sxs-lookup"><span data-stu-id="38a56-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="38a56-118">Vain yksi henkilö, vuokraajan järjestelmänvalvoja, voi suorittaa tämän tehtävän organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="38a56-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="38a56-119">Jos et ole tämän version tilaaja, odota, kunnes organisaatiosi on rekisteröitynyt ja olet saanut käyttäjätietosi.</span><span class="sxs-lookup"><span data-stu-id="38a56-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="38a56-120">Dynamics 365 Project Operations – esiversion kokeilu</span><span class="sxs-lookup"><span data-stu-id="38a56-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="38a56-121">Lunasta ensimmäinen tarjous, **Dynamics 365 Project Operations -kokeilu** käyttämällä URL-osoitetta Tervetuloa-sähköpostista.</span><span class="sxs-lookup"><span data-stu-id="38a56-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Ensimmäinen tarjous](./media/1FirstOffer.png)

2. <span data-ttu-id="38a56-123">Varmista, että olet kirjautuneena sisään käyttäjänä, joka kuuluu palvelun tilanneeseen organisaatioon.</span><span class="sxs-lookup"><span data-stu-id="38a56-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="38a56-124">Jatka tarjouksen lunastamista.</span><span class="sxs-lookup"><span data-stu-id="38a56-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="38a56-125">Valitse **Kyllä, lisää se tiliini**.</span><span class="sxs-lookup"><span data-stu-id="38a56-125">Select **Yes, add it to my account**.</span></span>

![Lunasta tarjous](./media/2RedeemFirstOffer.png)

![Tarjouksen vahvistaminen](./media/3ConfirmFirstOffer.png)

![Tarjous lunastettu](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="38a56-129">Dynamics 365 Finance – esiversion kokeilu</span><span class="sxs-lookup"><span data-stu-id="38a56-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="38a56-130">Toista samat vaiheet toiselle Tervetuloa-viestin tarjoukselle.</span><span class="sxs-lookup"><span data-stu-id="38a56-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="38a56-131">Käyttöoikeuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="38a56-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="38a56-132">Tarvitset järjestelmänvalvojan käyttöoikeudet organisaatiosi Office 365 -portaaliin, jotta voit suorittaa seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="38a56-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="38a56-133">Siirry [Microsoft 365 -hallintakeskukseen](https://portal.office.com/) ja määritä käyttöoikeudet käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="38a56-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Office-hallintaportaali](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="38a56-135">Valitse **Aktiiviset käyttäjät** -sivulla käyttäjät, joille haluat määrittää käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="38a56-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Käyttöoikeuksien määrittäminen](./media/6AssignLicenses.png)

3. <span data-ttu-id="38a56-137">Tarkista, että Project Operations -käyttöoikeus on valittu, ja valitse sitten **Tallenna muutokset**.</span><span class="sxs-lookup"><span data-stu-id="38a56-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="38a56-138">Finance-kokeilun tarjousta ei tarvitse delegoida käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="38a56-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="38a56-139">Aloita uusi projekti LCS:ssä</span><span class="sxs-lookup"><span data-stu-id="38a56-139">Start a new project in LCS</span></span>

<span data-ttu-id="38a56-140">Luo uusi LCS-projekti aiheessa [Aloita uusi projekti LCS:ssä](create-lcs-project.md) kuvatulla tavalla</span><span class="sxs-lookup"><span data-stu-id="38a56-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="38a56-141">Azure-tilauksen lisääminen LCS-projektiin</span><span class="sxs-lookup"><span data-stu-id="38a56-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="38a56-142">Voit suorittaa tämän tehtävän noudattamalla ohjeitaaiheessa [Lisää Azure-tilaus LCS-projektiin](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="38a56-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="38a56-143">Finance-esittely-ympäristön käyttöönotto Project Operationsin resurssien/ei-varastoitavien skenaarioille</span><span class="sxs-lookup"><span data-stu-id="38a56-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="38a56-144">Noudata ohjeita aiheessa [Uuden ympäristön valmistelu](resource-provision-new-environment.md) vimeistelläksesi käyttöönoton.</span><span class="sxs-lookup"><span data-stu-id="38a56-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="38a56-145">Käytä [esittely-ympäristö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) -käyttöönottotyyppiä esiversiossa.</span><span class="sxs-lookup"><span data-stu-id="38a56-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="38a56-146">Asenna CDS:n määritys- ja konfiguraatiotiedot</span><span class="sxs-lookup"><span data-stu-id="38a56-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="38a56-147">Asenna CDS:n määritys- ja konfiguraatiotiedot aiheessa [Konfiguraatiotietojen määritys ja käyttöönotto Common Data Servicessa](resource-apply-pro-setup-config-data.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="38a56-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

