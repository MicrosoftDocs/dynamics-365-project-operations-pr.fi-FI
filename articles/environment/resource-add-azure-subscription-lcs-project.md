---
title: Azure-tilauksen lisääminen LCS-projektiin
description: Tässä aiheessa on tietoja siitä, miten Azure-tilauksen voi yhdistää LCS-projektiin.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6daa86d453ec5022cdd75dff0394c8818292406c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000612"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="2e261-103">Azure-tilauksen lisääminen LCS-projektiin</span><span class="sxs-lookup"><span data-stu-id="2e261-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="2e261-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="2e261-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2e261-105">Pilvipalvelussa isännöidyt ympäristöt on otettava käyttöön aiemmin luodun Azure-tilauksen avulla.</span><span class="sxs-lookup"><span data-stu-id="2e261-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="2e261-106">Tässä aiheessa on tietoja siitä, miten olemassa olevan Azure-tilauksen voi yhdistää LCS-projektiin.</span><span class="sxs-lookup"><span data-stu-id="2e261-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="2e261-107">Myönnä järjestelmänvalvojan suostumus</span><span class="sxs-lookup"><span data-stu-id="2e261-107">Grant admin consent</span></span>

1. <span data-ttu-id="2e261-108">Valitse LCS-projektissa **Ympäristöt**-osassa **Microsoft Azure -asetukset**.</span><span class="sxs-lookup"><span data-stu-id="2e261-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Microsoft Azure -asetukset](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="2e261-110">Valitse **Projektin asetukset**-sivun **Azure-yhdistimet** -välilehdessä **Valtuuta**.</span><span class="sxs-lookup"><span data-stu-id="2e261-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="2e261-111">Näin ympäristöt voidaan ottaa käyttöön tässä projektissa.</span><span class="sxs-lookup"><span data-stu-id="2e261-111">This allows environments to be deployed to this project.</span></span>

![Azure-yhdistimet](./media/2AzureConnectors.png)

3. <span data-ttu-id="2e261-113">Anna järjestelmänvalvojan suostumus valitsemalla uudelleen **Valtuuta**.</span><span class="sxs-lookup"><span data-stu-id="2e261-113">Select **Authorize** again to provide admin consent.</span></span>

![Myönnä järjestelmänvalvojan suostumus](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="2e261-115">Hyväksy käyttöoikeuspyyntö.</span><span class="sxs-lookup"><span data-stu-id="2e261-115">Accept the permissions request.</span></span>

![Hyväksy käyttöoikeuspyyntö](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="2e261-117">Valtuutus on nyt valmis.</span><span class="sxs-lookup"><span data-stu-id="2e261-117">The authorization is now complete.</span></span> 

![Valtuutus onnistui](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="2e261-119">Dynamics Deployment Services -käyttöoikeuksien antaminen Azure-tilaukselle</span><span class="sxs-lookup"><span data-stu-id="2e261-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="2e261-120">Siirry kohtaan [Microsoft Azure -laskutus](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) ja valitse tilaus.</span><span class="sxs-lookup"><span data-stu-id="2e261-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="2e261-121">Dynamics Deployment Services -palveluiden on voitava käyttää tätä tilausta, jotta se voi ottaa ympäristöjä käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2e261-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Azure-tilauksen tiedot](./media/6AzureSubscription.png)

2. <span data-ttu-id="2e261-123">Valitse siirtymisruudusta **Käyttöoikeuksien hallinta (IAM)** ja valitse sitten **Lisää roolin delegointi**.</span><span class="sxs-lookup"><span data-stu-id="2e261-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="2e261-124">Valitse oikealla puolella olevasta liukusäätimestä **Osallistuja-rooli**  etsi ja valitse näkyviin tulevasta luettelosta **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="2e261-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="2e261-125">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2e261-125">Select **Save**.</span></span>

![Tilauksen käyttöoikeudet](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="2e261-127">Tilausyhdistimen lisääminen LCS-projektiin</span><span class="sxs-lookup"><span data-stu-id="2e261-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="2e261-128">Voit lisätä uuden yhdistimen valitsemalla LCS-projektissa **Microsoft Azure -asetukset** -sivulla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="2e261-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="2e261-129">Anna Azure-tilaustunnuksesi.</span><span class="sxs-lookup"><span data-stu-id="2e261-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="2e261-130">Voit etsiä Azure-tilaustunnuksen [Azure-portaalista](https://ms.portal.azure.com/) näytön vasemmassa alakulmassa olevasta **Asetukset**-kohdasta.</span><span class="sxs-lookup"><span data-stu-id="2e261-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="2e261-131">Valitse **Määritä käyttämään Azure Resource Manageria** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="2e261-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="2e261-132">Varmista, että Azuren tilauksen AAD-vuokraajan toimialue vastaa käytettyä toimialueen omistavan Azure-tilausksen toimialuetta ja valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="2e261-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="2e261-133">Vahvista valitsemalla **Microsoft Azure -määritys** -näytössä **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="2e261-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="2e261-134">Jos näyttöön tulee virhe tässä näytössä, palaa tämän aiheen osaan [Dynamics Deployment Services -käyttöoikeuksien antaminen Azure-tilaukselle](#provide) javarmista, että olet suorittanut kaikki vaiheet.</span><span class="sxs-lookup"><span data-stu-id="2e261-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="2e261-135">Lataa Azure-hallintavarmenne tietokoneesi paikalliseen kansioon.</span><span class="sxs-lookup"><span data-stu-id="2e261-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="2e261-136">Pyydä Azure-tilausjärjestelmänvalvoja lataamaan varmenne Azure-hallintaportaaliin valitsemalla tilaus ja valitsemalla **Asetukset** > **Hallinnan varmenteet**.</span><span class="sxs-lookup"><span data-stu-id="2e261-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="2e261-137">Tämän varmenteen avulla LCS voi olla yhteydessä Azureen puolestasi.</span><span class="sxs-lookup"><span data-stu-id="2e261-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="2e261-138">Voit ohittaa tämän vaiheen, jos käyttäjälläsi on tilauksen käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="2e261-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="2e261-139">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="2e261-139">Select  **Next**.</span></span>
8. <span data-ttu-id="2e261-140">Valitse Azure-alue, johon otetaan käyttöön, ja valitse sitten palvelinkeskus, joka on lähellä sijaintia, jossa aiot käyttää tätä järjestelmää.</span><span class="sxs-lookup"><span data-stu-id="2e261-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="2e261-141">Valitse **Yhdistä**.</span><span class="sxs-lookup"><span data-stu-id="2e261-141">Select  **Connect**.</span></span>

<span data-ttu-id="2e261-142">Olet yhdistänyt Azure-tilauksen onnistuneesti.</span><span class="sxs-lookup"><span data-stu-id="2e261-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="2e261-143">Voit nyt ottaa käyttöön Dynamics 365 Financen pilvi-isännöidyt ympäristöt.</span><span class="sxs-lookup"><span data-stu-id="2e261-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
