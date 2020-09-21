---
title: Päivityksen kotisivu
description: Tässä aiheessa kerrotaan, mistä löytää tärkeitä tietoja Dynamics 365 Project Service Automationin uusista ja muuttuneista ominaisuuksista, ja uuteen versioon päivittämisen prosessista.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751210"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="ede4f-103">Päivityksen kotisivu</span><span class="sxs-lookup"><span data-stu-id="ede4f-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="ede4f-104">Päivitä PSA-versiosta 2.x tai 1.x versioon 3.x</span><span class="sxs-lookup"><span data-stu-id="ede4f-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="ede4f-105">Uudet esiintymät</span><span class="sxs-lookup"><span data-stu-id="ede4f-105">New instances</span></span>

<span data-ttu-id="ede4f-106">Kun Project Service Automation valitaan uuden esiintymän valmistelun aikana, 17. toukokuuta 2019 alkaen versio 3. x asennetaan oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="ede4f-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="ede4f-107">Käytössä olevat esiintymät</span><span class="sxs-lookup"><span data-stu-id="ede4f-107">Existing instances</span></span>

<span data-ttu-id="ede4f-108">Aiemmin asiakkaiden, joilla on PSA-version 2.x, esiintymä ja joiden täytyi päivittää versioon 3.x, joka on Unified client interface -perustainen (UCI) versio PSA:sta, täytyi ottaa yhteyttä Microsoft-tukeen ja antaa tiedot esiintymästään, jotta tuki pystyi ottamaan esiintymän käyttöön versioon 3.x päivittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="ede4f-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="ede4f-109">1. maaliskuuta 2020 alkaen asiakkaat, joilla on PSA-version 2.x esiintymä ja joiden täytyy päivittää versioon 3.x, voivat päivittää esiintymänsä suoraan hallintaportaalista ottamatta yhteyttä Microsoft-tukeen.</span><span class="sxs-lookup"><span data-stu-id="ede4f-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="ede4f-110">PSA-versio 3.x sisältää merkittäviä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="ede4f-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="ede4f-111">Se on luotu Unified Interface -kehykseen, joka auttaa parantamaan käyttökokemusta.</span><span class="sxs-lookup"><span data-stu-id="ede4f-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="ede4f-112">Uudistettu sovellus tarjoaa yhdenmukaisen ja yhtenäisen käyttöliittymän, ja se noudattaa joustavia suunnitteluperiaatteita, jotka takaavat optimaalisen katselun missä tahansa näytön koossa tai laitteessa.</span><span class="sxs-lookup"><span data-stu-id="ede4f-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="ede4f-113">Sovelluksessa on tehty muitakin muutoksia.</span><span class="sxs-lookup"><span data-stu-id="ede4f-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="ede4f-114">Muuttuneisiin alueisiin kuuluvat hinnoittelu, varaukset ja resurssien kohdentaminen, aika, kulut ja hyväksynnät.</span><span class="sxs-lookup"><span data-stu-id="ede4f-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="ede4f-115">Suosittelemme, että suoritat seuraavat tehtävät ennen päivitysprosessin aloittamista:</span><span class="sxs-lookup"><span data-stu-id="ede4f-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="ede4f-116">Tarkista, ovatko sekä Dynamics 365 Field Service että Project Service Automation asennettu tunnistettuun esiintymään.</span><span class="sxs-lookup"><span data-stu-id="ede4f-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="ede4f-117">Jos molemmat ratkaisut on asennettu, sinun on päivitettävä molemmat, ennen kuin voit jatkaa esiintymän säännöllistä käyttöä.</span><span class="sxs-lookup"><span data-stu-id="ede4f-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="ede4f-118">Tutustu seuraaviin aiheisiin huolellisesti.</span><span class="sxs-lookup"><span data-stu-id="ede4f-118">Carefully review the following topics.</span></span> <span data-ttu-id="ede4f-119">Versioiden välisten muutosten tiedostaminen ja ymmärtäminen auttaa päivitysprosessissa.</span><span class="sxs-lookup"><span data-stu-id="ede4f-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="ede4f-120">Nämä aiheet sisältävät tietoja PSA:N merkittävistä muutoksista sekä huomioista ja suosituksista, jotka koskevat päivityksen suunnittelua versioon 3. x.</span><span class="sxs-lookup"><span data-stu-id="ede4f-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="ede4f-121">Uutuudet ja muutokset Project Service Automation -versiossa 3</span><span class="sxs-lookup"><span data-stu-id="ede4f-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="ede4f-122">Päivitykseen liittyviä huomioita - Project Service Automation versio 2.x tai 1.x versioon 3</span><span class="sxs-lookup"><span data-stu-id="ede4f-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="ede4f-123">Päivitä Sandbox-esiintymä arvioidaksesi muutoksia toteutukseesi ennen kuin päivität tuotantoesiintymän.</span><span class="sxs-lookup"><span data-stu-id="ede4f-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="ede4f-124">Kun olet tarkistanut aiemmin mainitut aiheet ja olet valmis päivittämään PSA-versioon 3. x tai UCI-pohjaiseen versioon, lähetä pyyntö Microsoftin tuelle, jotta päivitys voidaan asettaa saataville hallintakeskuksesta.</span><span class="sxs-lookup"><span data-stu-id="ede4f-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="ede4f-125">Anna pyynnössäsi esiintymäsi tiedot.</span><span class="sxs-lookup"><span data-stu-id="ede4f-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="ede4f-126">Vanhemmat PSA:n versiot (PSA versio 2.x) äskettäin luodussa esiintymässä</span><span class="sxs-lookup"><span data-stu-id="ede4f-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="ede4f-127">17. toukokuuta 2019 alkaen kaikissa uusissa ilmentymissä on käytössä UCI oletusasiakasohjelmana.</span><span class="sxs-lookup"><span data-stu-id="ede4f-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="ede4f-128">Jotta muutos olisi linjassa tämän muutoksen kanssa, PSA-versio 3.x ja Field Service versio 8.x tarjotaan oletusarvoisesti, koska nämä versiot on suunniteltu käytettäviksi UCI-asiakasohjelman kanssa.</span><span class="sxs-lookup"><span data-stu-id="ede4f-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="ede4f-129">1. maaliskuuta 2020 alkaen Dynamics PSA:n asiakkaat eivät voi enää luoda uusia ympäristöjä PSA:n vanhemmilla versioilla, kuten PSA-versiolla 2.x tai sitä vanhemmilla.</span><span class="sxs-lookup"><span data-stu-id="ede4f-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="ede4f-130">Kaikki uudet ympäristöt saavat vain PSA:n version 3.x.</span><span class="sxs-lookup"><span data-stu-id="ede4f-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="ede4f-131">Saadaksesi parhaan käyttökokemuksen vanhemmista Field Service - ja PSA-sovelluksista, siirry sivulle **Järjestelmäasetukset**, ja valitse kentälle **Käytä vain uutta Unified Interfacea** arvoksi **Ei**, sillä näitä versioita ei ole suunniteltu ladattavaksi oikein UCI:n.</span><span class="sxs-lookup"><span data-stu-id="ede4f-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="ede4f-132">Kun olet poistanut UCI:n käytöstä, voit avata ja suorittaa nämä Field Service - ja PSA-versiot käyttämällä vanhaa www-asiakasohjelmaa.</span><span class="sxs-lookup"><span data-stu-id="ede4f-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> <span data-ttu-id="ede4f-133">Tietoja UCI-asiakkaan poistamisesta käytöstä on aiheessa [Ota käyttöön ainoastaan unified interface](../admin/enable-unified-interface-only.md).</span><span class="sxs-lookup"><span data-stu-id="ede4f-133">For instructions about how to turn off the UCI client, see [Enable unified interface only](../admin/enable-unified-interface-only.md).</span></span>
