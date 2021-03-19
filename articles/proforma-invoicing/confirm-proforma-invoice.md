---
title: Proformalaskun vahvistaminen
description: Tässä aiheessa on tietoja proformalaskun vahvistamisesta.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287864"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="9aef4-103">Proformalaskun vahvistaminen</span><span class="sxs-lookup"><span data-stu-id="9aef4-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="9aef4-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="9aef4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9aef4-105">Kun proformalasku on vahvistettu, projektilaskun päivitysten tila on **Vahvistettu**.</span><span class="sxs-lookup"><span data-stu-id="9aef4-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="9aef4-106">Kun lasku on vahvistettu, se on vain luku -tilassa.</span><span class="sxs-lookup"><span data-stu-id="9aef4-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="9aef4-107">Jatkossa lasku voidaan oikaista vain, jos asiakkaalle on aloitettu korjauksia tai hyvityksiä tai kun se on merkitty maksetuksi.</span><span class="sxs-lookup"><span data-stu-id="9aef4-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="9aef4-108">Seuraavassa taulukossa on lueteltu järjestelmän luomat toteutuneet arvot.</span><span class="sxs-lookup"><span data-stu-id="9aef4-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="9aef4-109">Nämä toteutuneet arvot luodaan, kun projektilaskulle tehdään tiettyjä toimintoja ennen sen vahvistamista.</span><span class="sxs-lookup"><span data-stu-id="9aef4-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="9aef4-110">
                    <strong>Skenaario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9aef4-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="9aef4-111">
                    <strong>Vahvistuksen yhteydessä luodut toteutuneet arvot</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9aef4-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9aef4-112">Aikatapahtuman laskuttaminen muokkaamatta laskuluonnokseen.</span><span class="sxs-lookup"><span data-stu-id="9aef4-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-113">Laskuttamattoman myynnin peruutus tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="9aef4-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-114">Laskutettu toteutunut myynti tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="9aef4-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9aef4-115">Määrän pienentämiseen muokatun aikatapahtuman laskutus.</span><span class="sxs-lookup"><span data-stu-id="9aef4-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-116">Laskuttamattoman myynnin peruutus tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="9aef4-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-117">Uusi laskuttamaton todellinen myynti, joka on veloitettavissa laskutettujen laskurivien tiedoille, peruutetun myynnin toteutumiselle ja laskutettavalle myynnille.</span><span class="sxs-lookup"><span data-stu-id="9aef4-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-118">Uusi laskuttamaton tosiasiallinen myynti, josta ei veloiteta jäljellä olevia tunteja ja määrää sen jälkeen, kun vähennetään korjatut luvut muokatun laskurivin yksityiskohdissa, laskutetun myynnin tosiasiallinen palautus ja vastaava laskutettu todellinen myynti.</span><span class="sxs-lookup"><span data-stu-id="9aef4-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9aef4-119">Määrän lisäämiseen muokatun aikatapahtuman laskutus.</span><span class="sxs-lookup"><span data-stu-id="9aef4-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-120">Laskuttamattoman myynnin peruutus tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="9aef4-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-121">Uusi laskuttamaton todellinen myynti, joka on veloitettavissa laskutettujen laskurivien tiedoille, peruutetun myynnin toteutumiselle ja laskutettavalle myynnille.</span><span class="sxs-lookup"><span data-stu-id="9aef4-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9aef4-122">Kulutapahtuman laskuttaminen muokkaamatta laskuluonnokseen.</span><span class="sxs-lookup"><span data-stu-id="9aef4-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-123">Laskuttamattoman myynnin peruutus määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="9aef4-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-124">Laskutettu toteutunut myynti määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="9aef4-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9aef4-125">Määrän pienentämiseen muokatun kulutapahtuman laskutus.</span><span class="sxs-lookup"><span data-stu-id="9aef4-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-126">Laskuttamattoman myynnin peruutus määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="9aef4-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-127">Uusi laskuttamaton todellinen myynti, joka on veloitettavissa muokatun laskurivin tiedoissa olevasta määrästä ja summasta, laskuttamattoman tosiasiallisen myynnin palautuksesta ja vastaavan laskutetun myynnin todellisesta arvosta.</span><span class="sxs-lookup"><span data-stu-id="9aef4-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-128">Uusi laskuttamaton tosiasiallinen myynti, josta ei veloiteta jäljellä olevaa määrää ja summaa sen jälkeen, kun vähennetään korjatut luvut muokatun laskurivin yksityiskohdissa, laskutetun myynnin tosiasiallisesta palautuksesta ja vastaavasta laskutetusta todellisesta myynnistä.</span><span class="sxs-lookup"><span data-stu-id="9aef4-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9aef4-129">Määrän kasvattamiseen muokatun kulutapahtuman laskutus.</span><span class="sxs-lookup"><span data-stu-id="9aef4-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-130">Laskuttamattoman myynnin peruutus määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="9aef4-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-131">Uusi laskuttamaton todellinen myynti, joka on veloitettavissa muokatun laskurivin tiedoissa olevasta määrästä ja summasta, muokkaamattoman tosiasiallisen myynnin palautuksesta ja vastaavan laskutetun myynnin todellisesta arvosta.</span><span class="sxs-lookup"><span data-stu-id="9aef4-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9aef4-132">Maksun laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="9aef4-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-133">Laskuttamattoman myynnin peruutus maksusummalle alkuperäisellä kirjauskansion rivillä.</span><span class="sxs-lookup"><span data-stu-id="9aef4-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-134">Laskutettu toteutunut myynti määrälle ja summalle alkuperäisen palkkion kirjauskansion riville.</span><span class="sxs-lookup"><span data-stu-id="9aef4-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9aef4-135">Välitavoitteen laskutus.</span><span class="sxs-lookup"><span data-stu-id="9aef4-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9aef4-136">Välitavoitteen summaa koskeva laskutettu myynti, joka on projektisopimusrivin alkuperäisessä välitavoitteessa.</span><span class="sxs-lookup"><span data-stu-id="9aef4-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]