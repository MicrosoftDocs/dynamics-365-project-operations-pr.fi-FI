---
title: Rekisteröi resurssien/ei-varastoitavien skenaarioiden Project Operations -esiversiotilaus
description: Tässä aiheessa on tietoja siitä, miten tilataan ja otetaan käyttöön Project Operations resurssien/ei-varastoitavien skenaarioille.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4c2cd4c5d4dfbb95398932d432864cf0d4d5d54d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276839"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="82dac-103">Rekisteröi resurssien/ei-varastoitavien skenaarioiden Project Operations -esiversiotilaus</span><span class="sxs-lookup"><span data-stu-id="82dac-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="82dac-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="82dac-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="82dac-105">Tässä aiheessa kerrotaan, miten voit tilata esiversio-/kumppanitarjouksen ja ottaa käytöön Project Operations -ympäristön resurssien/ei-varastoitavien skenaarioille.</span><span class="sxs-lookup"><span data-stu-id="82dac-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="82dac-106">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="82dac-106">Prerequisites</span></span>

- <span data-ttu-id="82dac-107">Saat sähköpostiviestin, jossa saat kutsun osallistumaan esiversioon.</span><span class="sxs-lookup"><span data-stu-id="82dac-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="82dac-108">Voit pyytää esiversiota [Project Operations -sivustossa](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="82dac-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="82dac-109">Esiversion käyttöön ottavalla käyttäjällä on oltava Azure-vuokraajaan yleisen järjestelmänvalvojan oikeudet.</span><span class="sxs-lookup"><span data-stu-id="82dac-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="82dac-110">Finance-ympäristön käyttöönotto edellyttää voimassaolevaa Azure-tilausta, joka laskutetaan ympäristökohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="82dac-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="82dac-111">Voit aloittaa käyttämällä organisaatiosi olemassa olevaa tilausta tai [Azure-kokeiluversiota](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="82dac-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="82dac-112">CDS-ympäristö on maksuton rajoitetulle 30 päivän jaksolle.</span><span class="sxs-lookup"><span data-stu-id="82dac-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="82dac-113">Tilaa</span><span class="sxs-lookup"><span data-stu-id="82dac-113">Subscribe</span></span>

<span data-ttu-id="82dac-114">Kun [esiversiopyyntösi](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) hyväksytään, saat kolme Microsoftin tarjousta sähköpostitse.</span><span class="sxs-lookup"><span data-stu-id="82dac-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="82dac-115">Näiden tarjousten avulla voit ottaa käyttöön Project Operationsin esikatselun:</span><span class="sxs-lookup"><span data-stu-id="82dac-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="82dac-116">Dynamics 365 Project Operations (CRM) - Esiversion kokeiluversio</span><span class="sxs-lookup"><span data-stu-id="82dac-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="82dac-117">Office 365 Project Operationsin esiversion kokeilu</span><span class="sxs-lookup"><span data-stu-id="82dac-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="82dac-118">Dynamics 365 Finance – esiversion kokeilu</span><span class="sxs-lookup"><span data-stu-id="82dac-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82dac-119">Vain yksi henkilö, vuokraajan järjestelmänvalvoja, voi suorittaa tämän tehtävän organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="82dac-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="82dac-120">Jos et ole tämän version tilaaja, odota, kunnes organisaatiosi on rekisteröitynyt ja olet saanut käyttäjätietosi.</span><span class="sxs-lookup"><span data-stu-id="82dac-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="82dac-121">Dynamics 365 Project Operations (CRM) - Esiversion kokeiluversio</span><span class="sxs-lookup"><span data-stu-id="82dac-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="82dac-122">Ennen kuin aloitat, varmista, että olet kirjautunut selaimeen, jossa on käyttäjän työtili, siinä vuokraajan kohdassa, jossa haluat projektin toimintojen esikatselun.</span><span class="sxs-lookup"><span data-stu-id="82dac-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="82dac-123">Lunasta ensimmäinen tarjouskoodi, **Dynamics 365 Project Operations (CRM) – Esiversion kokeiluversio** liittämällä se selaimen URL-osoitekenttään.</span><span class="sxs-lookup"><span data-stu-id="82dac-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Lunasta tarjous](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="82dac-125">Vahvista tilaus.</span><span class="sxs-lookup"><span data-stu-id="82dac-125">Confirm your order.</span></span>

![Vahvista tilaus](./media/17ConfirmOrderNew.png)

<span data-ttu-id="82dac-127">Näkyviin tulee vahvistus siitä, että tarjouksen lunastaminen onnistui.</span><span class="sxs-lookup"><span data-stu-id="82dac-127">You will see confirmation offer was successfully redeemed.</span></span>

![Varmistus](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="82dac-129">Office 365 Project Operationsin esiversion kokeilu</span><span class="sxs-lookup"><span data-stu-id="82dac-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="82dac-130">Toista samat vaiheet kuin ensimmäisellä tarjouskoodilla.</span><span class="sxs-lookup"><span data-stu-id="82dac-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="82dac-131">Muista lisätä toinen tarjouskoodi käyttämällä samaa käyttäjätiliä, jota käytettiin ensimmäisen tarjouskoodin kanssa.</span><span class="sxs-lookup"><span data-stu-id="82dac-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="82dac-132">Dynamics 365 Finance – esiversion kokeilu</span><span class="sxs-lookup"><span data-stu-id="82dac-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="82dac-133">Toista samat vaiheet viimeiselle Tervetuloa-viestin tarjoukselle.</span><span class="sxs-lookup"><span data-stu-id="82dac-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="82dac-134">Käyttöoikeuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="82dac-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82dac-135">Tarvitset järjestelmänvalvojan käyttöoikeudet organisaatiosi Microsoft 365 -portaaliin, jotta voit suorittaa seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="82dac-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="82dac-136">Siirry [Microsoft 365 -hallintakeskukseen](https://portal.office.com/) ja määritä käyttöoikeudet käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="82dac-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Hallintakeskuksen aloitussivu](./media/14AdminPortal.png)

2. <span data-ttu-id="82dac-138">Valitse **Aktiiviset käyttäjät** -sivulla käyttäjät, joille haluat määrittää käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="82dac-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Käyttöoikeuksien määrittäminen](./media/15AssignLicenses.png)

3. <span data-ttu-id="82dac-140">Tarkista, että **Dynamics 365 Project Operations (CRM) Esiversio** ja **Office 365 Project Operations - Esiversio** -lisenssit on valittu, ja valitse **Tallenna muutokset**.</span><span class="sxs-lookup"><span data-stu-id="82dac-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="82dac-141">Finance-kokeilun tarjousta ei tarvitse delegoida käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="82dac-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="82dac-142">Aloita uusi projekti LCS:ssä</span><span class="sxs-lookup"><span data-stu-id="82dac-142">Start a new project in LCS</span></span>

<span data-ttu-id="82dac-143">Luo uusi LCS-projekti aiheessa [Aloita uusi projekti LCS:ssä](create-lcs-project.md) kuvatulla tavalla</span><span class="sxs-lookup"><span data-stu-id="82dac-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="82dac-144">Azure-tilauksen lisääminen LCS-projektiin</span><span class="sxs-lookup"><span data-stu-id="82dac-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="82dac-145">Voit suorittaa tämän tehtävän noudattamalla ohjeitaaiheessa [Lisää Azure-tilaus LCS-projektiin](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="82dac-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="82dac-146">Finance-esittely-ympäristön käyttöönotto Project Operationsin resurssien/ei-varastoitavien skenaarioille</span><span class="sxs-lookup"><span data-stu-id="82dac-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="82dac-147">Noudata ohjeita aiheessa [Uuden ympäristön valmistelu](resource-provision-new-environment.md) vimeistelläksesi käyttöönoton.</span><span class="sxs-lookup"><span data-stu-id="82dac-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="82dac-148">Käytä [esittely-ympäristö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) -käyttöönottotyyppiä esiversiossa.</span><span class="sxs-lookup"><span data-stu-id="82dac-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="82dac-149">Asenna CDS:n määritys- ja konfiguraatiotiedot</span><span class="sxs-lookup"><span data-stu-id="82dac-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="82dac-150">Asenna CDS:n määritys- ja konfiguraatiotiedot aiheessa [Konfiguraatiotietojen määritys ja käyttöönotto Common Data Servicessa](resource-apply-pro-setup-config-data.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="82dac-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="82dac-151">Suorita tämä vaihe vasta sen jälkeen, kun Financen demoympäristö on otettu käyttöön ja esittelytiedot ovat valmiina.</span><span class="sxs-lookup"><span data-stu-id="82dac-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]