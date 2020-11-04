---
title: Project Operations -integroinnin määrittäminen oikeushenkilöä kohden
description: Tämä aihe sisältää tietoja integroinnin määrittämisestä yrityksen mukaan Project Operationsissa.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096748"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="0f589-103">Project Operations -integroinnin määrittäminen oikeushenkilöä kohden</span><span class="sxs-lookup"><span data-stu-id="0f589-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="0f589-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="0f589-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0f589-105">Tässä aihe käy läpi vaiheet, joita tarvitaan Dynamics 365 Project Operationsin määrittämiseen yrityksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="0f589-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="0f589-106">Ota käyttöön ominaisuusavaimet Dynamics 365 Financessa</span><span class="sxs-lookup"><span data-stu-id="0f589-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="0f589-107">Ota tarvittavat ominaisuudet käyttöön tekemällä seuraavat toimet.</span><span class="sxs-lookup"><span data-stu-id="0f589-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="0f589-108">Siirry Dynamics 365 Financessa **Tietojen hallinta** -työtilaan.</span><span class="sxs-lookup"><span data-stu-id="0f589-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="0f589-109">Etsi **ominaisuusluettelosta** seuraavat ominaisuudet ja ota ne käyttöön:</span><span class="sxs-lookup"><span data-stu-id="0f589-109">In **Feature list** , find and enable the following features:</span></span>
  
    - <span data-ttu-id="0f589-110">**Projektin useiden sopimusrivien ottaminen käyttöön**</span><span class="sxs-lookup"><span data-stu-id="0f589-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="0f589-111">**Ota käyttöön Project Operations Dynamics 365 Customer Engagementissa**</span><span class="sxs-lookup"><span data-stu-id="0f589-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="0f589-112">Jos **toimintonäppäimiä** ei näy luettelossa, tarkista, että taloushallinnon versio on vähimmäisversiovaatimus (sovelluksen versio 10.0.13, jossa on käytössä kaikki laatupäivitykset tai uudempi).</span><span class="sxs-lookup"><span data-stu-id="0f589-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="0f589-113">Päivitä ominaisuusluettelo valitsemalla **Tarkista päivitykset**.</span><span class="sxs-lookup"><span data-stu-id="0f589-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="0f589-114">Project Operationsin käyttöönoton skenaarion määrittäminen yritykselle</span><span class="sxs-lookup"><span data-stu-id="0f589-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="0f589-115">Voit ottaa Project Operationsin käyttöön Dynamics 365 Customer Engagementissa yritystasolla.</span><span class="sxs-lookup"><span data-stu-id="0f589-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="0f589-116">Sinulla voi olla yksi yritys, joka käyttää Project Operationsia Dynamics 365 Customer Engagementissa resurssilla/ei-varastoitavien skenaarioiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="0f589-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="0f589-117">Samassa ympäristössä voi olla toinen yritys, joka käyttää projektitoimintoja varastoitujen/tuotantotilausten skenaarioita varten.</span><span class="sxs-lookup"><span data-stu-id="0f589-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="0f589-118">Valitse Dynamics 365 Financessa **Projektinhallinta ja kirjanpito** > **Määritys** > **Globaalin projektinhallinnan ja kirjanpidon parametrit**.</span><span class="sxs-lookup"><span data-stu-id="0f589-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="0f589-119">Valitse käytettävissä olevien yritysten luettelosta kohteet, joihin on otettu käyttöön useita sopimusrivejä ja projektitoimintoja Dynamics 365 Customer Engagementissa.</span><span class="sxs-lookup"><span data-stu-id="0f589-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="0f589-120">Jätä yritykset, jotka käyttävät projektitoimintoja varastoitujen/tuotantotilausten skenaarioita varten.</span><span class="sxs-lookup"><span data-stu-id="0f589-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="0f589-121">Yritys voidaan valita vain, jos sillä ei ole aiemmin luotuja projekteja.</span><span class="sxs-lookup"><span data-stu-id="0f589-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="0f589-122">Projektinhallinnan ja kirjanpidon parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0f589-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="0f589-123">Jokainen yritys, joka käyttää projektitoimintoja Dynamics 365 Customer Engagementissa tarvitsee oletusparametrien joukon.</span><span class="sxs-lookup"><span data-stu-id="0f589-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="0f589-124">Nämä parametrit määritetään **projektinhallinta ja kirjanpidon parametrit** -sivun **projektitoiminnot** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="0f589-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="0f589-125">Parametrit ovat:</span><span class="sxs-lookup"><span data-stu-id="0f589-125">The parameters are:</span></span>

  - <span data-ttu-id="0f589-126">**Laskutustyyppioletukset** : Project Operations käyttää kiinteää joukkoa laskutustyyppioletusarvoja, jotka on yhdistettävä rivin ominaisuuksiin Financessa.</span><span class="sxs-lookup"><span data-stu-id="0f589-126">**Billing type defaults** : Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="0f589-127">Tietueen luominen kullekin laskutustyypille: **ei määritetty** , **Laskutettava** , **Ei-laskutettava** , **maksuton** ja **ei käytettävissä**.</span><span class="sxs-lookup"><span data-stu-id="0f589-127">Create a record for each billing type: **Not specified** , **Chargeable** , **Non-chargeable** , **Complimentary** , and **Not available**.</span></span>
  - <span data-ttu-id="0f589-128">**Projektiluokan oletusarvot** : Valitse kullekin tapahtumatyypille käytettävät oletusprojektiluokat.</span><span class="sxs-lookup"><span data-stu-id="0f589-128">**Project category defaults** : Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="0f589-129">Näitä oletusarvoja käytetään **Projektitoimintojen integrointikirjauskansiossa** ja arvioissa, joissa projektin toteutumiselle ei ole määritetty tapahtumaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="0f589-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="0f589-130">**Ennusteet** : Valitse ennustemalli, jota käytetään aika- ja kuluarvioille.</span><span class="sxs-lookup"><span data-stu-id="0f589-130">**Forecasts** : Select the forecast model to be used for time and expense estimates.</span></span>
