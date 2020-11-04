---
title: Luo aikamerkintöjä
description: Tässä aiheessa on tietoja aikamerkintöjen luomisesta.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 878413a24baa340b745a045a6991a63a00851c8b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075439"
---
# <a name="create-time-entries"></a><span data-ttu-id="9b360-103">Luo aikamerkintöjä</span><span class="sxs-lookup"><span data-stu-id="9b360-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9b360-104">Aiemmissa Dynamics 365 Project Service Automation-versioissa aikamerkinnät on syötetty viikoittain.</span><span class="sxs-lookup"><span data-stu-id="9b360-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="9b360-105">Project Service Automationin versiossa 3 aikamerkinnät syötetään päivittäin.</span><span class="sxs-lookup"><span data-stu-id="9b360-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="9b360-106">Voit kuitenkin luoda tai kopioida aikamerkintöjä useita kerrallaan sen jälkeen, kun muutama aikamerkintä on luotu.</span><span class="sxs-lookup"><span data-stu-id="9b360-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="9b360-107">Luo aikamerkintä</span><span class="sxs-lookup"><span data-stu-id="9b360-107">Create a time entry</span></span>

<span data-ttu-id="9b360-108">Luo aikamerkintä seuraavien vaiheiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="9b360-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="9b360-109">Valitse **Aikamerkinnät** -sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9b360-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="9b360-110">Kirjoita **Pikaluonti: aikamerkintä** -valintaikkunaan aikamerkinnän kesto minuutteina, tunteina tai päivinä.</span><span class="sxs-lookup"><span data-stu-id="9b360-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="9b360-111">Kesto on ilmoitettava seuraavassa muodossa: *x* minuuttia, *x* tuntia tai *x* päivää.</span><span class="sxs-lookup"><span data-stu-id="9b360-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="9b360-112">Tunnit ja päivät voidaan ilmoittaa myös desimaalilukuina, kuten *x.x* tuntia tai *x.x* päivää.</span><span class="sxs-lookup"><span data-stu-id="9b360-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="9b360-113">Valitse aikamerkinnän tyyppi ja projekti, jolle olet syöttämässä aikamerkintää.</span><span class="sxs-lookup"><span data-stu-id="9b360-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="9b360-114">Etsi **Projektitehtävä** -kentässä tämän aikamerkinnän tehtävä.</span><span class="sxs-lookup"><span data-stu-id="9b360-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9b360-115">Jos olet luomassa aikamerkintää tehtävälle, jota ei ole kohdennettu käyttäjälle **Projektitehtävä** -kentässä, valitse **Etsi** -painike, valitse **Muuta näkymää** ja valitse sen jälkeen **Kaikki aktiiviset projektitehtävät** nähdäksesi listan tehtävistä.</span><span class="sxs-lookup"><span data-stu-id="9b360-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View** , and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="9b360-116">Kirjoita kuvaus, jos kuvaus on pakollinen, ja valitse sitten **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="9b360-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="9b360-117">Kun aikamerkintä on luotu ja tallennettu, voit muokata sitä ajansyöttöruudukossa.</span><span class="sxs-lookup"><span data-stu-id="9b360-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="9b360-118">Ajansyöttöruudukko tukee kahta muotoa:</span><span class="sxs-lookup"><span data-stu-id="9b360-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="9b360-119">Voit kirjoittaa aikamerkinnät muodossa **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="9b360-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="9b360-120">Tämä muoto muunnetaan sitten tunneiksi ja murtoluvuiksi.</span><span class="sxs-lookup"><span data-stu-id="9b360-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="9b360-121">Voit määrittää tunnit ja murtoluvut suoraan.</span><span class="sxs-lookup"><span data-stu-id="9b360-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="9b360-122">Huomaa, että tunnin murto-osat eivät ole minuutteja.</span><span class="sxs-lookup"><span data-stu-id="9b360-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="9b360-123">1,5 tunnin osuus on siis 1 tunti ja 30 minuuttia.</span><span class="sxs-lookup"><span data-stu-id="9b360-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="9b360-124">Sama sääntö koskee päivien murto-osia.</span><span class="sxs-lookup"><span data-stu-id="9b360-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="9b360-125">Yksi päivä on 24 tuntia, ja 0,5 päivää on 12 tuntia.</span><span class="sxs-lookup"><span data-stu-id="9b360-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="9b360-126">Luo useita aikamerkintöjä kerralla</span><span class="sxs-lookup"><span data-stu-id="9b360-126">Bulk create time entries</span></span>

<span data-ttu-id="9b360-127">Sen jälkeen, kun muutama aikamerkintä on luotu, voit kopioida niitä luodaksesi kerralla useita aikamerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="9b360-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="9b360-128">Valitse **Aikamerkinnät** -sivulla **Kopioi viikko**.</span><span class="sxs-lookup"><span data-stu-id="9b360-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="9b360-129">Määritä **Lähdejakso** -kenttäryhmässä **Alkamispäivä** ja **Päättymispäivä** -kentissä päivämääräväli, jolta aikamerkinnät kopioidaan.</span><span class="sxs-lookup"><span data-stu-id="9b360-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="9b360-130">Määritä **Kohdejakso** -kenttäryhmässä **Alkamispäivä** -kentässä päivämäärä, jolle luodaan aikamerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="9b360-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="9b360-131">Valitse **Kopioi** , jos haluat luoda kopion aikakiertauksista, jotka vastaavat sitä viikonpäivää, joka on määritelty **Kohdejakso** -kenttäryhmässä.</span><span class="sxs-lookup"><span data-stu-id="9b360-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="9b360-132">Esimerkiksi edellisen viikon maanantain aikakirjaus kopioidaan sen viikon maanantaille, joka on määritetty **Kohdejakso** -kenttäryhmässä.</span><span class="sxs-lookup"><span data-stu-id="9b360-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="9b360-133">Aikamerkintöjen tuontitiedot</span><span class="sxs-lookup"><span data-stu-id="9b360-133">Import data for time entries</span></span>

<span data-ttu-id="9b360-134">Voit tuoda tietoja projektin varauksista ja kohdennuksista.</span><span class="sxs-lookup"><span data-stu-id="9b360-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="9b360-135">Kun tuot tietoja, voit määrittää tuotavien varausten päivämäärävälin ja valita sitten erikseen varaukset, jotka luodaan **Luonnos** -tyyppisinä aikakirjauksina.</span><span class="sxs-lookup"><span data-stu-id="9b360-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="9b360-136">Ryhmittely-, lajittelu-, haku- ja suodatusominaisuudet</span><span class="sxs-lookup"><span data-stu-id="9b360-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="9b360-137">Voit ryhmitellä ja suodattaa aikakirjauksia sarakkeissa määritettyjen dimensioiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="9b360-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="9b360-138">Valitse **Ryhmittelyperuste** -kentässä aikamerkintöjen suodatuksessa käytettävä dimensio.</span><span class="sxs-lookup"><span data-stu-id="9b360-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="9b360-139">Voit myös lajitella aikamerkintätietueita nousevaan tai laskevaan järjestykseen käyttämällä sarakeotsikoiden lajittelunuolta.</span><span class="sxs-lookup"><span data-stu-id="9b360-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="9b360-140">Lisäksi voit näyttää tai piilottaa kirjauksia valitsemalla sarakeotsikoista **Suodatin** -painikkeen ja kirjoittamalla sitten **Haku** -ruutuun tekstin, jota käytetään haettaessa aikamerkintöjä projektin nimen, projektitehtävän, aikakirjauksen tai resurssin perusteella.</span><span class="sxs-lookup"><span data-stu-id="9b360-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
