---
title: Uusien mukautettujen entiteettilomakkeiden lisääminen (Project Service Automation 2. x)
description: Tämä aihe sisältää tietoja mukautettujen entiteettilomakkeiden lisäämisestä mahdollisuuksille, tarjouksille tai laskuille Dynamics 365 Project Service Automationin versiossa 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9eb9fc5e-4c7d-466c-9362-fdb0faa30506
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 2bd955ad3eb26d31676ac4ad387baccaee913cd2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751086"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="bd10c-103">Uusien mukautettujen entiteettilomakkeiden lisääminen (Project Service Automation 2. x)</span><span class="sxs-lookup"><span data-stu-id="bd10c-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="bd10c-104">Tyyppikenttä</span><span class="sxs-lookup"><span data-stu-id="bd10c-104">Type field</span></span> 

<span data-ttu-id="bd10c-105">Dynamics 365 Project Service Automation käyttää entiteettien Mahdollisuus, Tarjous, Tilaus ja Lasku **Tyyppi** (**msdyn\_ordertype**) -kenttää erottaakseen kyseisten entiteettien **työperusteiset** versiot **nimikeperusteisista** ja **palveluperusteisista** versioista.</span><span class="sxs-lookup"><span data-stu-id="bd10c-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="bd10c-106">PSA käsittelee kyseisten entiteettien työperusteiset versiot.</span><span class="sxs-lookup"><span data-stu-id="bd10c-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="bd10c-107">Suuri määrä ratkaisun asiakas- ja palvelinpuolen liiketoimintalogiikasta perustuu **Tyyppi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="bd10c-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="bd10c-108">Siksi on tärkeää, että kenttä valmistellaan oikealla arvolla, kun entiteetit luodaan.</span><span class="sxs-lookup"><span data-stu-id="bd10c-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="bd10c-109">Virheellinen arvo voi aiheuttaa virheellistä toimintaa, ja osa liiketoimintalogiikasta saatetaan suorittaa virheellisesti.</span><span class="sxs-lookup"><span data-stu-id="bd10c-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="bd10c-110">Automaattinen lomakkeenvaihto</span><span class="sxs-lookup"><span data-stu-id="bd10c-110">Automatic form switching</span></span>

<span data-ttu-id="bd10c-111">Myyntientiteettitietueiden virheellisestä valmistelusta ja muokkauksesta aiheutuvan mahdollisen tietojen vaurioitumisen ja odottamattomien toimintojen ehkäisemiseksi PSA sisältää nyt automaattisen lomakkeenvaihdon logiikkaa valmiissa lomakkeissa.</span><span class="sxs-lookup"><span data-stu-id="bd10c-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="bd10c-112">Tämä logiikka vie käyttäjät oikeaan lomakkeeseen työperusteisellä versiolla tai millä tahansa muulla entiteettien Mahdollisuus, Tarjous, Tila tai Lasku tyypillä työskentelyä varten.</span><span class="sxs-lookup"><span data-stu-id="bd10c-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="bd10c-113">Kun käyttäjä avaa entiteetin Mahdollisuus, Tarjous, Tilaus tai Lasku työperusteisen version, lomake vaihtuu lomakkeeksi **Projektitiedot**.</span><span class="sxs-lookup"><span data-stu-id="bd10c-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="bd10c-114">Automaattisessa lomakkeenvaihtologiikassa käytetään arvon **formId** ja kentän **msdyn\_ordertype** välistä yhteyttä.</span><span class="sxs-lookup"><span data-stu-id="bd10c-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="bd10c-115">Tähän yhdistämismääritykseen on lisätty kaikki valmiit lomakkeet.</span><span class="sxs-lookup"><span data-stu-id="bd10c-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="bd10c-116">Mukautetut lomakkeet on kuitenkin lisättävä manuaalisesti ilmaisemaan, missä entiteetin versiossa ne on tarkoitus käsitellä.</span><span class="sxs-lookup"><span data-stu-id="bd10c-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="bd10c-117">Tämä perustuu **msdyn\_ordertype** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="bd10c-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="bd10c-118">Jos lomakkeenvaihto puuttuu yhdistämismäärityksestä, logiikka vaihtaa valmiiseen lomakkeeseen sen arvon perusteella, joka on tallennettu entiteetin **msdyn\_ordertype** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="bd10c-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="bd10c-119">Mukautettujen lomakkeiden lisääminen ja lomakkeenvaihtologiikan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="bd10c-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="bd10c-120">Seuraavassa esimerkissä esitetään mukautetun **Omat projektitiedot** -lomakkeen lisääminen siten, että se toimii työperusteisten mahdollisuuksien kanssa.</span><span class="sxs-lookup"><span data-stu-id="bd10c-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="bd10c-121">Samaa prosessia käytetään mukautettujen lomakkeiden lisäämiseen siten, että ne toimivat yhdessä tarjousten, tilausten ja laskujen kanssa.</span><span class="sxs-lookup"><span data-stu-id="bd10c-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="bd10c-122">Voit luoda mukautetun version **Projektitiedot**-lomakkeesta seuraavalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="bd10c-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="bd10c-123">Avaa Mahdollisuus-entiteetissä lomake **Projektitiedot** ja tallenna kopio siitä nimellä **Omat projektitiedot**.</span><span class="sxs-lookup"><span data-stu-id="bd10c-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="bd10c-124">Avaa uusi lomake ja varmista sitten ominaisuuksissa, että ne sisältävät **Projektitiedot**-lomakkeen lomakkeenvalmistelun komentosarjat.</span><span class="sxs-lookup"><span data-stu-id="bd10c-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="bd10c-125">Älä poista komentosarjoja.</span><span class="sxs-lookup"><span data-stu-id="bd10c-125">Don't remove the scripts.</span></span> <span data-ttu-id="bd10c-126">Muulloin osa tiedoista saatetaan valmistella virheellisesti.</span><span class="sxs-lookup"><span data-stu-id="bd10c-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="bd10c-127">Tarkista, että lomake sisältää**Tyyppi** (**msdyn\_ordertype**)-kentän.</span><span class="sxs-lookup"><span data-stu-id="bd10c-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="bd10c-128">Älä poista tätä kenttää.</span><span class="sxs-lookup"><span data-stu-id="bd10c-128">Don't remove this field.</span></span> <span data-ttu-id="bd10c-129">Muussa tapauksessa valmistelukomentosarjat epäonnistuvat.</span><span class="sxs-lookup"><span data-stu-id="bd10c-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="bd10c-130">Etsi uuden lomakkeen **formId**-arvo.</span><span class="sxs-lookup"><span data-stu-id="bd10c-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="bd10c-131">Voit tehdä tämän kahdella eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="bd10c-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="bd10c-132">Vie **Omat projektitiedot** lomake hallitsemattoman ratkaisun osana ja etsi sitten **formId** -arvo viedyn ratkaisun customization.xml-tiedostosta.</span><span class="sxs-lookup"><span data-stu-id="bd10c-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="bd10c-133">Avaa lomake **Omat projektitiedot** lomake-editorissa ja etsi sitten **fromid** -parametrin vieressä URL-osoitteessa oleva GUID-tunnus seuraavassa kuvassa näkyvällä tavalla.</span><span class="sxs-lookup"><span data-stu-id="bd10c-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Uuden lomakkeen formId-arvo URL-osoitteessa](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="bd10c-135">Luo **msdyn\_ordertype** -yhdistämismääritys **formId**-arvolle muokkaamalla verkkoresurssia msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="bd10c-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="bd10c-136">Poista koodi resurssista ja korvaa se seuraavalla koodilla.</span><span class="sxs-lookup"><span data-stu-id="bd10c-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="bd10c-137">Tallenna ja julkaise mukautukset.</span><span class="sxs-lookup"><span data-stu-id="bd10c-137">Save and then publish the customizations.</span></span>
