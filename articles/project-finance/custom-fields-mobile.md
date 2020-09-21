---
title: Ota Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen mukautetut kentät käyttöön iOS:ssä ja Androidissa
description: Tässä aiheessa on yleisiä ohjeita, joiden avulla voit käyttää laajennuksia mukautettujen kenttien toteuttamiseen.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: 4564bbda-34ea-4647-a9bc-f6ef17b1038b
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 16c3b79dcaaf8c5c491587618256694f82f44753
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751135"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="cc18a-103">Ota Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen mukautetut kentät käyttöön iOS:ssä ja Androidissa</span><span class="sxs-lookup"><span data-stu-id="cc18a-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc18a-104">Tässä aiheessa on yleisiä ohjeita, joiden avulla voit käyttää laajennuksia mukautettujen kenttien toteuttamiseen.</span><span class="sxs-lookup"><span data-stu-id="cc18a-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="cc18a-105">Käsiteltäviä aiheita ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="cc18a-105">The following topics are covered:</span></span>

- <span data-ttu-id="cc18a-106">Tietolajit, joita mukautettu kenttäkehys tukee</span><span class="sxs-lookup"><span data-stu-id="cc18a-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="cc18a-107">Miten näyttää vain luku- tai muokkauskentät työaikaraportin merkinnöissä ja tallentaa käyttäjän antamat arvot tietokantaan</span><span class="sxs-lookup"><span data-stu-id="cc18a-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="cc18a-108">Vain luku -muotoisten kenttien näyttäminen työaikaraportin otsikossa</span><span class="sxs-lookup"><span data-stu-id="cc18a-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="cc18a-109">Muiden mukautettujen liiketoimintalogiikkojen integroiminen kenttien oletusarvojen syöttämiseksi ja lisätarkistuksen tekemiseksi</span><span class="sxs-lookup"><span data-stu-id="cc18a-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="cc18a-110">Yleisö</span><span class="sxs-lookup"><span data-stu-id="cc18a-110">Audience</span></span>

<span data-ttu-id="cc18a-111">Tämä aihe on tarkoitettu sovelluskehittäjille, jotka integroivat mukautettuja kenttiä Microsoft Dynamics 365 Project Timesheet -mobiilisovellukseen, joka on saatavilla Apple iOS- ja Google Android -sovelluksiin.</span><span class="sxs-lookup"><span data-stu-id="cc18a-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="cc18a-112">Oletuksena on, että lukijat tuntevat X++-kehitystyön ja projektin työaikaraportin toiminnot.</span><span class="sxs-lookup"><span data-stu-id="cc18a-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="cc18a-113">Tietosopimus – TSTimesheetCustomField X++-luokka</span><span class="sxs-lookup"><span data-stu-id="cc18a-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="cc18a-114">**TSTimesheetCustomField**-luokka on X++-tietosopimusluokka, joka edustaa tietoja mukautetusta kentästä työaikaraportin toiminnallisuuteen.</span><span class="sxs-lookup"><span data-stu-id="cc18a-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="cc18a-115">Mukautettujen kenttäobjektien luettelot välitetään sekä TSTimesheetDetails-palvelusopimuksessa että TSTimesheetEntry-tietosopimuksessa mukautettujen kenttien näyttämistä varten mobiilisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="cc18a-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="cc18a-116">**TSTimesheetDetails** - Työaikaraportin otsikkosopimus.</span><span class="sxs-lookup"><span data-stu-id="cc18a-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="cc18a-117">**TSTimesheetEntry** - Työaikaraportin tapahtumasopimus.</span><span class="sxs-lookup"><span data-stu-id="cc18a-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="cc18a-118">Näiden objektien ryhmät, joilla on samat projektitiedot ja **timesheetLineRecId**-arvo, muodostavat rivin.</span><span class="sxs-lookup"><span data-stu-id="cc18a-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="cc18a-119">fieldBaseType (Lajit)</span><span class="sxs-lookup"><span data-stu-id="cc18a-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="cc18a-120">**TsTimesheetCustom**-objektin **FieldBaseType**-ominaisuus määrittää sovelluksessa näkyvän kentän tyypin.</span><span class="sxs-lookup"><span data-stu-id="cc18a-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="cc18a-121">Seuraavat **Tyypit**-arvot ovat tuettuja.</span><span class="sxs-lookup"><span data-stu-id="cc18a-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="cc18a-122">Tyypin arvo</span><span class="sxs-lookup"><span data-stu-id="cc18a-122">Types value</span></span> | <span data-ttu-id="cc18a-123">Laji</span><span class="sxs-lookup"><span data-stu-id="cc18a-123">Type</span></span>              | <span data-ttu-id="cc18a-124">Muistiinpanot</span><span class="sxs-lookup"><span data-stu-id="cc18a-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="cc18a-125">0</span><span class="sxs-lookup"><span data-stu-id="cc18a-125">0</span></span>           | <span data-ttu-id="cc18a-126">Merkkijono (ja Enum)</span><span class="sxs-lookup"><span data-stu-id="cc18a-126">String (and Enum)</span></span> | <span data-ttu-id="cc18a-127">Kenttä näkyy tekstikenttänä.</span><span class="sxs-lookup"><span data-stu-id="cc18a-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="cc18a-128">1</span><span class="sxs-lookup"><span data-stu-id="cc18a-128">1</span></span>           | <span data-ttu-id="cc18a-129">Integer</span><span class="sxs-lookup"><span data-stu-id="cc18a-129">Integer</span></span>           | <span data-ttu-id="cc18a-130">Arvo näkyy numerona, jossa ei ole desimaaleja.</span><span class="sxs-lookup"><span data-stu-id="cc18a-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="cc18a-131">2</span><span class="sxs-lookup"><span data-stu-id="cc18a-131">2</span></span>           | <span data-ttu-id="cc18a-132">Reaali</span><span class="sxs-lookup"><span data-stu-id="cc18a-132">Real</span></span>              | <span data-ttu-id="cc18a-133">Arvo näkyy numerona, jossa on desimaaleja.</span><span class="sxs-lookup"><span data-stu-id="cc18a-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="cc18a-134">Jos haluat näyttää sovelluksessa todellisen arvon valuuttana, käytä **fieldExtenededType**-ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="cc18a-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="cc18a-135">**numberOfDecimals**-ominaisuuden avulla voit määrittää näytettävien desimaalien määrän.</span><span class="sxs-lookup"><span data-stu-id="cc18a-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="cc18a-136">3</span><span class="sxs-lookup"><span data-stu-id="cc18a-136">3</span></span>           | <span data-ttu-id="cc18a-137">Päivä</span><span class="sxs-lookup"><span data-stu-id="cc18a-137">Date</span></span>              | <span data-ttu-id="cc18a-138">Päivämäärämuodot määräytyvät **Käyttäjän asetukset** -kohdassa **kieli ja maa/alue** -asetuksen mukaan määräytyvien käyttäjien **päivämäärä-, kellonaika- ja lukumuoto** -asetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="cc18a-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="cc18a-139">4</span><span class="sxs-lookup"><span data-stu-id="cc18a-139">4</span></span>           | <span data-ttu-id="cc18a-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="cc18a-140">Boolean</span></span>           | |
| <span data-ttu-id="cc18a-141">15</span><span class="sxs-lookup"><span data-stu-id="cc18a-141">15</span></span>          | <span data-ttu-id="cc18a-142">GUID</span><span class="sxs-lookup"><span data-stu-id="cc18a-142">GUID</span></span>              | |
| <span data-ttu-id="cc18a-143">16</span><span class="sxs-lookup"><span data-stu-id="cc18a-143">16</span></span>          | <span data-ttu-id="cc18a-144">Int64</span><span class="sxs-lookup"><span data-stu-id="cc18a-144">Int64</span></span>             | |

- <span data-ttu-id="cc18a-145">Jos **TSTimesheetCustomField**-objektissa ei ole **stringOptions**-ominaisuutta, käyttäjälle toimitetaan vapaamuotoinen tekstikenttä.</span><span class="sxs-lookup"><span data-stu-id="cc18a-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="cc18a-146">**stringLength**-ominaisuuden avulla voidaan määrittää merkkijonon enimmäispituus, jonka käyttäjät voivat syöttää.</span><span class="sxs-lookup"><span data-stu-id="cc18a-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="cc18a-147">Jos **TSTimesheetCustomField**-objektissa on **stringOptions**-ominaisuus, nämä luetteloelementit ovat ainoat arvot, joita käyttäjät voivat valita valintanappien avulla.</span><span class="sxs-lookup"><span data-stu-id="cc18a-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="cc18a-148">Tässä tapauksessa merkkijonokenttä voi toimia luettelointi-arvona käyttäjämerkintää varten.</span><span class="sxs-lookup"><span data-stu-id="cc18a-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="cc18a-149">Jos haluat tallentaa arvon tietokantaan valintaluettelolla, yhdistä se manuaalisesti uudelleen luettelointiarvoon, ennen kuin tallennat tietokantaan komentoketjulla (lisätietoja on kohdassa "käytä komentoa TSTimesheetEntryService-luokassa, kun haluat tallentaa tuntilomakemerkinnän sovelluksesta uudelleen tietokantaan"-osaan jäljempänä tässä aiheessa).</span><span class="sxs-lookup"><span data-stu-id="cc18a-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="cc18a-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="cc18a-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="cc18a-151">Tämän ominaisuuden avulla voit muotoilla reaaliarvoja valuutalle.</span><span class="sxs-lookup"><span data-stu-id="cc18a-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="cc18a-152">Tämä menetelmä on käytettävissä vain, kun **fieldBaseType**-arvo on **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="cc18a-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="cc18a-153">**TSCustomFieldExtendedType:None** – Muotoilua ei käytetä.</span><span class="sxs-lookup"><span data-stu-id="cc18a-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="cc18a-154">**TSCustomFieldExtendedType::Currency** – Muotoile arvo valuuttana.</span><span class="sxs-lookup"><span data-stu-id="cc18a-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="cc18a-155">Kun valuutan muotoilu on aktiivinen, voit käyttää **stringValue**-kenttää ja siirtää sovelluksessa näkyvän valuuttakoodin.</span><span class="sxs-lookup"><span data-stu-id="cc18a-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="cc18a-156">Arvo on vain luku -arvo.</span><span class="sxs-lookup"><span data-stu-id="cc18a-156">The value is a read-only value.</span></span>

    <span data-ttu-id="cc18a-157">**realValue**-kenttä sisältää rahasummat, jotka tulisi tallentaa tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="cc18a-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="cc18a-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="cc18a-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="cc18a-159">Tämän ominaisuuden avulla voit määrittää, missä mukautetun kentän pitäisi näkyä sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="cc18a-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="cc18a-160">**TSCustomFieldSection::Header** – Kenttä näkyy **Sovelluksen lisätietoja** -osassa.</span><span class="sxs-lookup"><span data-stu-id="cc18a-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="cc18a-161">Nämä kentät ovat aina vain luettavissa.</span><span class="sxs-lookup"><span data-stu-id="cc18a-161">These fields are always read-only.</span></span>
- <span data-ttu-id="cc18a-162">**TSCustomFieldSection::Line** – Kenttä tulee näkyviin, kun kaikki valmiit rivikentät ovat työaikaraportin kentissä.</span><span class="sxs-lookup"><span data-stu-id="cc18a-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="cc18a-163">Nämä kentät voivat olla joko muokattavia tai vain luku -kenttiä.</span><span class="sxs-lookup"><span data-stu-id="cc18a-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="cc18a-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="cc18a-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="cc18a-165">Tämä ominaisuus määrittää kentän, kun sovelluksen arvot tallennetaan tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="cc18a-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="cc18a-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="cc18a-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="cc18a-167">Tämä ominaisuus määrittää kentän, kun sovelluksen arvot tallennetaan tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="cc18a-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="cc18a-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="cc18a-168">isEditable (NoYes)</span></span>

<span data-ttu-id="cc18a-169">Määrittämällä tämän ominaisuuden arvoksi **Kyllä** voit määrittää, että käyttäjät voivat muokata tuntilomakemerkintäosan kenttää.</span><span class="sxs-lookup"><span data-stu-id="cc18a-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="cc18a-170">Määrittämällä ominaisuuden arvoksi **Ei**, voit määrittää kentän vain luku -tilaan.</span><span class="sxs-lookup"><span data-stu-id="cc18a-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="cc18a-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="cc18a-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="cc18a-172">Määrittämällä tämän ominaisuuden arvoksi **Kyllä** voit määrittää, että tuntilomakemerkintäosan tulisi olla pakollinen.</span><span class="sxs-lookup"><span data-stu-id="cc18a-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="cc18a-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="cc18a-173">label (str)</span></span>

<span data-ttu-id="cc18a-174">Tämä ominaisuus määrittää otsikon, joka näkyy sovelluksen kentän vieressä.</span><span class="sxs-lookup"><span data-stu-id="cc18a-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="cc18a-175">stringOptions (Merkkijonoluettelo)</span><span class="sxs-lookup"><span data-stu-id="cc18a-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="cc18a-176">Tämä ominaisuus on käytettävissä vain, jos **fieldBaseType**-arvoksi on määritetty **merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="cc18a-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="cc18a-177">Jos **stringOptions** on määritetty, valintanappien kautta valittavissa olevat merkkijonoarvot (radiopainikkeet) määritetään luettelon merkkijonojen avulla.</span><span class="sxs-lookup"><span data-stu-id="cc18a-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="cc18a-178">Jos merkkijonoja ei ole, vapaatekstimuotoinen merkintä merkkijonokentässä sallitaan (lisätietoja on kohdassa "Käyttöketjun hallinta TSTimesheetEntryService-luokassa, kun tuntilomakemerkintä tallennetaan sovelluksesta uudelleen tietokantaan" -osaan jäljempänä tässä aiheessa).</span><span class="sxs-lookup"><span data-stu-id="cc18a-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="cc18a-179">strinLength (kokonaisluku)</span><span class="sxs-lookup"><span data-stu-id="cc18a-179">stringLength (int)</span></span>

<span data-ttu-id="cc18a-180">Tämä ominaisuus määrittää merkkijonokentän enimmäispituuden.</span><span class="sxs-lookup"><span data-stu-id="cc18a-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="cc18a-181">Se on käytettävissä vain, jos **fieldBaseType**-arvoksi on määritetty **merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="cc18a-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="cc18a-182">numberOfDecimals (kokonaisluku)</span><span class="sxs-lookup"><span data-stu-id="cc18a-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="cc18a-183">Tämä ominaisuus määrittää todelliselle kentälle näytettävien desimaalien määrän.</span><span class="sxs-lookup"><span data-stu-id="cc18a-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="cc18a-184">Se on käytettävissä vain, jos **fieldBaseType**-arvoksi on määritetty **todellinen**.</span><span class="sxs-lookup"><span data-stu-id="cc18a-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="cc18a-185">orderSequence (kokonaisluku)</span><span class="sxs-lookup"><span data-stu-id="cc18a-185">orderSequence (int)</span></span>

<span data-ttu-id="cc18a-186">Tämä ominaisuus määrittää, missä järjestyksessä mukautetut kentät näkyvät sovelluksessa, kun määritettynä on useampi kuin yksi mukautettu kenttä.</span><span class="sxs-lookup"><span data-stu-id="cc18a-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="cc18a-187">Kentät, joiden luvut ovat alemmat, näytetään ensin.</span><span class="sxs-lookup"><span data-stu-id="cc18a-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="cc18a-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="cc18a-188">booleanValue (boolean)</span></span>

<span data-ttu-id="cc18a-189">**Boolean**-tyypin kentissä tämä ominaisuus siirtää kentän totuusarvon palvelimen ja sovelluksen välille.</span><span class="sxs-lookup"><span data-stu-id="cc18a-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="cc18a-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="cc18a-190">guidValue (guid)</span></span>

<span data-ttu-id="cc18a-191">**GUID**-tyypin kentissä tämä ominaisuus siirtää GUID-arvon palvelimen ja sovelluksen välille.</span><span class="sxs-lookup"><span data-stu-id="cc18a-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="cc18a-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="cc18a-192">int64Value (int64)</span></span>

<span data-ttu-id="cc18a-193">**Int64**-tyypin kentissä tämä ominaisuus siirtää kentän Int64-arvon palvelimen ja sovelluksen välille.</span><span class="sxs-lookup"><span data-stu-id="cc18a-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="cc18a-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="cc18a-194">intValue (int)</span></span>

<span data-ttu-id="cc18a-195">**Int**-tyypin kentissä tämä ominaisuus siirtää kentän Int-arvon palvelimen ja sovelluksen välille.</span><span class="sxs-lookup"><span data-stu-id="cc18a-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="cc18a-196">realValue (todellinen)</span><span class="sxs-lookup"><span data-stu-id="cc18a-196">realValue (real)</span></span>

<span data-ttu-id="cc18a-197">**Todellinen**-tyypin kentissä tämä ominaisuus siirtää kentän Todellinen-arvon palvelimen ja sovelluksen välille.</span><span class="sxs-lookup"><span data-stu-id="cc18a-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="cc18a-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="cc18a-198">stringValue (str)</span></span>

<span data-ttu-id="cc18a-199">**Merkkijono**-tyypin kentissä tämä ominaisuus siirtää kentän merkkijonoarvon palvelimen ja sovelluksen välille.</span><span class="sxs-lookup"><span data-stu-id="cc18a-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="cc18a-200">Sitä käytetään myös **todellinen**-tyypin kentissä, jotka on muotoiltu valuutaksi.</span><span class="sxs-lookup"><span data-stu-id="cc18a-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="cc18a-201">Näiden kenttien osalta ominaisuutta käytetään valuuttakoodin välittämiseen sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="cc18a-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="cc18a-202">dateValue (päivämäärä)</span><span class="sxs-lookup"><span data-stu-id="cc18a-202">dateValue (date)</span></span>

<span data-ttu-id="cc18a-203">**Päivämäärä**-tyypin kentissä tämä ominaisuus siirtää kentän päivämääräarvon palvelimen ja sovelluksen välille.</span><span class="sxs-lookup"><span data-stu-id="cc18a-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="cc18a-204">Mukautetun kentän näyttäminen ja tallentaminen tuntilomakemerkinnän osassa</span><span class="sxs-lookup"><span data-stu-id="cc18a-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="cc18a-205">Alla on kuvakaappaus tuntilomakemerkinnän luomisesta mobiilisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="cc18a-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="cc18a-206">Siinä näkyy valmiit kentät ja mukautettu kenttä tuntimerkintäosassa nimeltään Test String ja luettelointiarvo Second Option jo asetettu.</span><span class="sxs-lookup"><span data-stu-id="cc18a-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Testimerkkijonon mukautettu kenttä sovelluksessa](media/timesheet-entry.jpg)



<span data-ttu-id="cc18a-208">Alla on näyttökuva, joka on käyttäjän mobiilisovelluksessa, kun valitaan jokin "testimerkkijonon" mukautetulle kentälle käytettävissä olevista luettelointivaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="cc18a-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="cc18a-209">Kaksi vaihtoehtoa ovat ensimmäinen vaihtoehto ja toinen vaihtoehto, joka näkyy valintapainikkeina.</span><span class="sxs-lookup"><span data-stu-id="cc18a-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="cc18a-210">Toinen vaihtoehto on tällä hetkellä valittuna.</span><span class="sxs-lookup"><span data-stu-id="cc18a-210">The second option is currently selected.</span></span>

![Valintanappi (radionappi) testimerkkijonon mukautetulle kentälle](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="cc18a-212">TSTimesheetLine-taulukon laajentaminen siten, että siinä on mukautettu kenttä</span><span class="sxs-lookup"><span data-stu-id="cc18a-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="cc18a-213">Tyypillisissä skenaarioissa on todennäköistä, että tuntilomakkeen merkintäosan mukautetun kentän tiedot tallennetaan TSTimesheetLine-tauluun.</span><span class="sxs-lookup"><span data-stu-id="cc18a-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="cc18a-214">Muita taulukoita voidaan kuitenkin käyttää, jos tiedot voidaan hakea annetun TSTimesheetTrans-tietueen perusteella tai jos niissä ei ole tiettyä tietuekontekstia (jos esimerkiksi kenttä on määritetty vain luku -tilaan projektiparametreissa).</span><span class="sxs-lookup"><span data-stu-id="cc18a-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="cc18a-215">Huomaa, että mukautettujen kenttien ei tarvitse olla tukitietokannan tietueita.</span><span class="sxs-lookup"><span data-stu-id="cc18a-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="cc18a-216">Ne voidaan luoda dynaamisesti X++-logiikan perusteella.</span><span class="sxs-lookup"><span data-stu-id="cc18a-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="cc18a-217">Tästä lähestymistavasta voi olla hyötyä vain luku -tilassa (lisätietoja on kohdassa Komentoketju TSTimesheetDetails-luokassa, buildCustomFieldListForHeader-menetelmä, joka täyttää työaikaraportin tiedot-osassa, joka on esimerkki dynaamisesti luoduista mukautettujen kenttien arvoista.)</span><span class="sxs-lookup"><span data-stu-id="cc18a-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="cc18a-218">Alla on Visual Studio -sovellusobjektipuusta otettu näyttökuva.</span><span class="sxs-lookup"><span data-stu-id="cc18a-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="cc18a-219">Se näyttää TSTimesheetLine-taulukon laajennuksen, jossa TestLineString-kenttä on lisätty mukautettuna kenttänä.</span><span class="sxs-lookup"><span data-stu-id="cc18a-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Rivimerkkijono](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="cc18a-221">Käytä komentoketjua TSTimesheetSettings-luokan buildCustomFieldList-menetelmässä, kun haluat näyttää kentän tuntilomakemerkinnän osassa</span><span class="sxs-lookup"><span data-stu-id="cc18a-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="cc18a-222">Tämä koodi määrittää sovelluksen kentän näyttöasetukset.</span><span class="sxs-lookup"><span data-stu-id="cc18a-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="cc18a-223">Se esimerkiksi määrittää kenttätyypin, otsikon, sen, onko kenttä pakollinen, ja missä osassa kenttä näkyy.</span><span class="sxs-lookup"><span data-stu-id="cc18a-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="cc18a-224">Seuraavassa esimerkissä näkyy aikamerkintöjen merkkijonokenttä.</span><span class="sxs-lookup"><span data-stu-id="cc18a-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="cc18a-225">Tässä kentässä on kaksi vaihtoehtoa, **Ensimmäinen vaihtoehto** ja **Toinen vaihtoehto**, jotka ovat käytettävissä valintanappien kautta (radionapit).</span><span class="sxs-lookup"><span data-stu-id="cc18a-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="cc18a-226">Sovelluksen kenttä liitetään **TestLineString**-kenttään, joka on lisätty TSTimesheetLine-tauluun.</span><span class="sxs-lookup"><span data-stu-id="cc18a-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="cc18a-227">Huomaa kohtien **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** ja **numberOfDecimals** käyttö.</span><span class="sxs-lookup"><span data-stu-id="cc18a-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="cc18a-228">Voit myös määrittää nämä parametrit manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="cc18a-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="cc18a-229">Käytä komentoketjua TSTimesheetEntry-luokan buildCustomFieldListForEntry-menetelmässä, kun haluat syöttää tuntilomakemerkinnän arvot</span><span class="sxs-lookup"><span data-stu-id="cc18a-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="cc18a-230">**buildCustomFieldListForEntry**-menetelmällä syötetään arvoja mobiilisovelluksen tallennettujen työaikaraporttien riveille.</span><span class="sxs-lookup"><span data-stu-id="cc18a-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="cc18a-231">Se vie TSTimesheetTrans-tietueen parametriksi.</span><span class="sxs-lookup"><span data-stu-id="cc18a-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="cc18a-232">Tietueen kenttien avulla voit täyttää mukautetun kentän arvon sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="cc18a-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="cc18a-233">Käytä komentoketjua TSTimesheetEntryService-luokassa, kun haluat tallentaa tuntilomakemerkinnän sovelluksesta uudelleen tietokantaan</span><span class="sxs-lookup"><span data-stu-id="cc18a-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="cc18a-234">Jos haluat tallentaa mukautetun kentän tietokantaan tavalliseen käyttöön, sinun täytyy laajentaa useita menetelmiä:</span><span class="sxs-lookup"><span data-stu-id="cc18a-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="cc18a-235">**timesheetLineNeedsUpdating**-menetelmällä määritetään, onko käyttäjä muuttanut rivitietuetta sovelluksessa, ja se on tallennettava tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="cc18a-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="cc18a-236">Jos tehokkuus ei ole ongelma, tätä menetelmää voidaan yksinkertaistaa niin, että se palauttaa aina **tosi**-arvon.</span><span class="sxs-lookup"><span data-stu-id="cc18a-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="cc18a-237">**populateTimesheetLineFromEntryDuringCreate**- ja **populateTimesheetLineFromEntryDuringUpdate**-menetelmien avulla voi lisätä arvoja TSTimesheetLine tietokantatietueeseen.</span><span class="sxs-lookup"><span data-stu-id="cc18a-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="cc18a-238">Seuraavassa esimerkissä määritetään, miten tietokantakentän ja syöttökentän välinen yhdistämismääritys tehdään manuaalisesti X++-koodin kautta.</span><span class="sxs-lookup"><span data-stu-id="cc18a-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="cc18a-239">**populateTimesheetWeekFromEntry**-menetelmää voidaan myös laajentaa, jos **TSTimesheetEntry**-objektiin yhdistettävän mukautetun kentän täytyy kirjoittaa uudelleen TSTimesheetLineweek-tietokantataulukkoon.</span><span class="sxs-lookup"><span data-stu-id="cc18a-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="cc18a-240">Seuraavassa esimerkissä tallennetaan **firstOption**- tai **seconnOption**-arvo, jonka käyttäjä valitsee tietokantaan raakamerkkijonoarvona.</span><span class="sxs-lookup"><span data-stu-id="cc18a-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="cc18a-241">Jos tietokannan kenttä on **Enum**-tyypin kenttä, arvot voidaan yhdistää manuaalisesti luettelointiarvoon ja tallentaa sitten tietokantataulukon luettelointikenttään.</span><span class="sxs-lookup"><span data-stu-id="cc18a-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="cc18a-242">Mukautetun kentän näyttäminen tuntilomakeotsikon osassa</span><span class="sxs-lookup"><span data-stu-id="cc18a-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="cc18a-243">Alla on kuvakaappaus mobiilisovelluksesta, jossa käyttäjä tarkastelee tuntilomaketta.</span><span class="sxs-lookup"><span data-stu-id="cc18a-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="cc18a-244">Lisätietoja-painike on valittu oikeassa yläkulmassa, jotta näkyviin tulee Näytä lisätiedot -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="cc18a-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Näytä lisätietoja -komento](media/show-more.png)

<span data-ttu-id="cc18a-246">Alla on kuvakaappaus mobiilisovelluksen tuntilomakkeen Lisää-osasta.</span><span class="sxs-lookup"><span data-stu-id="cc18a-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="cc18a-247">Työaikaraportin otsikko-osaan on lisätty mukautettu kenttä, jonka nimi on tämän tuntilomakkeen käyttöaste (laskettu mukautettu kenttä).</span><span class="sxs-lookup"><span data-stu-id="cc18a-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="cc18a-248">Mukautettu kenttä määrittää vain luku -arvon 0.667.</span><span class="sxs-lookup"><span data-stu-id="cc18a-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Lisää-osa](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="cc18a-250">TSTimesheetTable-taulukon laajentaminen siten, että siinä on mukautettu kenttä</span><span class="sxs-lookup"><span data-stu-id="cc18a-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="cc18a-251">Tyypillisissä skenaarioissa on todennäköistä, että otsikko-osan tiedot saadaan TSTimesheetHeader-taulusta.</span><span class="sxs-lookup"><span data-stu-id="cc18a-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="cc18a-252">Muita taulukoita voidaan kuitenkin käyttää, jos tiedot voidaan hakea annetun TSTimesheetTable-tietueen perusteella tai jos niissä ei ole tiettyä tietuekontekstia (jos esimerkiksi kenttä on määritetty vain luku -tilaan projektiparametreissa).</span><span class="sxs-lookup"><span data-stu-id="cc18a-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="cc18a-253">Huomaa, että mukautettujen kenttien ei tarvitse olla tukitietokannan tietueita.</span><span class="sxs-lookup"><span data-stu-id="cc18a-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="cc18a-254">Ne voidaan luoda dynaamisesti X++-logiikan perusteella.</span><span class="sxs-lookup"><span data-stu-id="cc18a-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="cc18a-255">Seuraava esimerkki osoittaa tämän lähestymistavan.</span><span class="sxs-lookup"><span data-stu-id="cc18a-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="cc18a-256">Otsikko-osan kentät ovat aina vain luku -tilassa sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="cc18a-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="cc18a-257">Käytä komentoketjua TSTimesheetSettings-luokan buildCustomFieldList-menetelmässä, kun haluat näyttää kentän otsikko-osassa</span><span class="sxs-lookup"><span data-stu-id="cc18a-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="cc18a-258">Tämä koodi määrittää sovelluksen kentän näyttöasetukset.</span><span class="sxs-lookup"><span data-stu-id="cc18a-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="cc18a-259">Se esimerkiksi määrittää kenttätyypin, otsikon, sen, onko kenttä pakollinen, ja missä osassa kenttä näkyy.</span><span class="sxs-lookup"><span data-stu-id="cc18a-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="cc18a-260">Seuraava esimerkki näyttää lasketun arvon sovelluksen otsikko-osassa.</span><span class="sxs-lookup"><span data-stu-id="cc18a-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="cc18a-261">Käytä komentoketjua TSTimesheetDetails-luokan buildCustomFieldListForHeader-menetelmässä, kun haluat täyttää tuntilomakemerkinnän tiedot</span><span class="sxs-lookup"><span data-stu-id="cc18a-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="cc18a-262">**buildCustomFieldListForHeader**-menetelmää käytetään täyttämään tuntilomakkeen otsikkotiedot mobiilisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="cc18a-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="cc18a-263">Se vie TSTimesheetTable-tietueen parametriksi.</span><span class="sxs-lookup"><span data-stu-id="cc18a-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="cc18a-264">Tietueen kenttien avulla voit täyttää mukautetun kentän arvon sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="cc18a-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="cc18a-265">Seuraavassa esimerkissä ei lue tietokannan arvoja.</span><span class="sxs-lookup"><span data-stu-id="cc18a-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="cc18a-266">Sen sijaan se luo X++-logiikan avulla lasketun arvon, joka näkyy sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="cc18a-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="cc18a-267">Muut konfiguroitavuus-/laajennettavuus-mahdollisuudet</span><span class="sxs-lookup"><span data-stu-id="cc18a-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="cc18a-268">Sovelluksen lisätarkistuksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="cc18a-268">Adding additional validation for the app</span></span>

<span data-ttu-id="cc18a-269">Työaikaraportin toimintojen aiemmin luotu logiikka tietokantatasolla toimii silti odotetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="cc18a-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="cc18a-270">Jos haluat keskeyttää Tallenna- tai Lähetä-toimintojen suorittamisen ja näyttää tietyn virhesanoman, voit lisätä **heittovirheen ("viesti käyttäjälle")** -komentolaajennuksen kautta.</span><span class="sxs-lookup"><span data-stu-id="cc18a-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="cc18a-271">Seuraavassa on kolme hyödyllistä laajennusmenetelmäesimerkkiä:</span><span class="sxs-lookup"><span data-stu-id="cc18a-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="cc18a-272">Jos TSTimesheetLine-taulun **validateWrite** palauttaa arvon **epätosi** aikaraportin rivintallennustoiminnon aikana, mobiilisovelluksessa näkyy virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="cc18a-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="cc18a-273">Jos TSTimesheetTable-taulun **validateSubmit** palauttaa arvon **epätosi**, sovelluksen tuntilomakkeen lähettämisen aikana käyttäjälle näytetään virheilmoitus.</span><span class="sxs-lookup"><span data-stu-id="cc18a-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="cc18a-274">Logiikka, joka täyttää kentät (esimerkiksi **rivin ominaisuus**) **Lisää**-menetelmän aikana TSTimesheetLine-taulussa, suoritetaan edelleen.</span><span class="sxs-lookup"><span data-stu-id="cc18a-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="cc18a-275">Valmiiden kenttien piilottaminen ja merkitseminen vain luku -muodossa määrityksen kautta</span><span class="sxs-lookup"><span data-stu-id="cc18a-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="cc18a-276">Projektiparametreistä voit luoda valmiita kenttiä vain luku -muodossa tai piilotettuina mobiilisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="cc18a-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="cc18a-277">Määritä asetukset **projektinhallinta- ja kirjanpitoparametrit**-sivun **tuntilomake**-välilehden **mobiilituntilomakkeet**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="cc18a-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projektin parametrit](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="cc18a-279">Valintaan käytettävissä olevien aktiviteettien muuttaminen laajennusten kautta</span><span class="sxs-lookup"><span data-stu-id="cc18a-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="cc18a-280">Projektiin valittavissa olevat aktiviteetit täytetään **TsTimesheetProjectService**-luokan **getActivitiesForProject()**- ja **getActivityQuery()**- menetelmien kautta.</span><span class="sxs-lookup"><span data-stu-id="cc18a-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="cc18a-281">Voit muuttaa tätä tapaa käyttämällä komentoketjua, joka vastaa liiketoimintaskenaariota aktiviteeteille, joita voi valita tietylle projektille.</span><span class="sxs-lookup"><span data-stu-id="cc18a-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="cc18a-282">Oletusprojektiluokan syöttäminen työaikaraportin tapahtumille</span><span class="sxs-lookup"><span data-stu-id="cc18a-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="cc18a-283">Oletusprojektiluokan syöttäminen työaikaraportin tapahtumille tapahtuu kolmella tasolla.</span><span class="sxs-lookup"><span data-stu-id="cc18a-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="cc18a-284">Voit käyttää komentoketjua, kun haluat laajentaa käyttäytymistä jollakin tai kaikilla näillä tasoilla halutun käyttäytymisen saavuttamiseksi.</span><span class="sxs-lookup"><span data-stu-id="cc18a-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="cc18a-285">Käytetään seuraavaa hierarkiaa:</span><span class="sxs-lookup"><span data-stu-id="cc18a-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="cc18a-286">Sovellus yrittää asettaa oletusluokan projektiresurssista.</span><span class="sxs-lookup"><span data-stu-id="cc18a-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="cc18a-287">Tämä oletusluokka on määritetty **getCurrentUserResource**- ja **getDelegatedResourcesForCurrentUser**-menetelmille **TSTimesheetSettingsService**-luokassa.</span><span class="sxs-lookup"><span data-stu-id="cc18a-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="cc18a-288">Jos oletusluokkaa ei ole projektiresurssitasolla, sovellus yrittää vetää sen projektiaktiviteetista.</span><span class="sxs-lookup"><span data-stu-id="cc18a-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="cc18a-289">Tämä oletusluokka määritetään **TSTimesheetProjectService**-luokan **getActivitiesForProject**-menetelmässä.</span><span class="sxs-lookup"><span data-stu-id="cc18a-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="cc18a-290">Jos oletuskategoriaa ei anneta projektin aktiviteettitasolla, oletusluokka otetaan projektin parametreista.</span><span class="sxs-lookup"><span data-stu-id="cc18a-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="cc18a-291">Tämä oletusluokka määritetään **TSTimesheetProjectService**-luokan **getProjectDetailsbyRule**-menetelmässä.</span><span class="sxs-lookup"><span data-stu-id="cc18a-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
