---
title: Proformamuotoisen projektipohjaisen laskun vahvistaminen
description: Tässä aiheessa on tietoja proformamuotoisen projektipohjaisen laskun vahvistamisesta.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 53c647dca506822312053fb5c9b086a2947974c2
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867126"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="d2a80-103">Proformamuotoisen projektipohjaisen laskun vahvistaminen</span><span class="sxs-lookup"><span data-stu-id="d2a80-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="d2a80-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="d2a80-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d2a80-105">Kun proformalasku on vahvistettu, projektilaskun päivitysten tila on **Vahvistettu**.</span><span class="sxs-lookup"><span data-stu-id="d2a80-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="d2a80-106">Kun lasku on vahvistettu, se on vain luku -tilassa.</span><span class="sxs-lookup"><span data-stu-id="d2a80-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="d2a80-107">Edelleen lasku voidaan korjata vain, jos on asiakkaan aloittamia korjauksia tai hyvityksiä.</span><span class="sxs-lookup"><span data-stu-id="d2a80-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="d2a80-108">Seuraavassa taulukossa on lueteltu järjestelmän luomat toteutuneet arvot.</span><span class="sxs-lookup"><span data-stu-id="d2a80-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="d2a80-109">Nämä toteutuneet arvot luodaan, kun projektilaskulle tehdään tiettyjä toimintoja ennen sen vahvistamista.</span><span class="sxs-lookup"><span data-stu-id="d2a80-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="d2a80-110">
                    <strong>Skenaario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d2a80-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="d2a80-111">
                    <strong>Vahvistuksen yhteydessä luodut toteutuneet arvot</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d2a80-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2a80-112">Ennakkomaksun tai ennakkomaksuun perustuvan maksun laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="d2a80-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-113">Laskutetun todellisen myynnin tyyppi, <strong>Pidätyskohde</strong> luodaan ennakkomaksulle tai pidätyskohteelle.</span><span class="sxs-lookup"><span data-stu-id="d2a80-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-114">Laskuttamaton toteutunut myynti, jonka ennakkomaksun tai ennakkon täsmäytykseen käytettävä summa on negatiivinen.</span><span class="sxs-lookup"><span data-stu-id="d2a80-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2a80-115">Sen jälkeen, kun olet täysin täsmäyttänyt laskun pidätyksen tai ennakkomaksun.</span><span class="sxs-lookup"><span data-stu-id="d2a80-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-116">Täsmäytystä varten luodun pidätyksen tai ennakkomaksun laskuttamattoman myynnin peruutus.</span><span class="sxs-lookup"><span data-stu-id="d2a80-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="d2a80-117">Tämä summa on positiivinen, koska sen tarkoitus on kumota pidätyksen tai ennakkomaksun yhteydessä luotu negatiivinen tulos.</span><span class="sxs-lookup"><span data-stu-id="d2a80-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-118">Laskutetun myynnin todellinen summa laskussa.</span><span class="sxs-lookup"><span data-stu-id="d2a80-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d2a80-119">Sen jälkeen, kun olet osittain täsmäyttänyt laskun pidätyksen tai ennakkomaksun.</span><span class="sxs-lookup"><span data-stu-id="d2a80-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-120">Täsmäytystä varten luodun pidätyksen tai ennakkomaksun laskuttamattoman myynnin peruutus.</span><span class="sxs-lookup"><span data-stu-id="d2a80-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="d2a80-121">Tämä summa on positiivinen, koska sen tarkoitus on kumota pidätyksen tai ennakkomaksun yhteydessä luotu negatiivinen tulos.</span><span class="sxs-lookup"><span data-stu-id="d2a80-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-122">Laskutetun myynnin todellinen summa laskussa.</span><span class="sxs-lookup"><span data-stu-id="d2a80-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-123">Negatiivisen laskuttamattoman myynnin todellinen jäljellä olevan pidätys tai ennakkomäärä, jota käytetään tulevissa laskuissa.</span><span class="sxs-lookup"><span data-stu-id="d2a80-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2a80-124">Aikatapahtuman laskuttaminen muokkaamatta laskuluonnokseen.</span><span class="sxs-lookup"><span data-stu-id="d2a80-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-125">Laskuttamattoman myynnin peruutus tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="d2a80-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-126">Laskutettu toteutunut myynti tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="d2a80-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d2a80-127">Määrän pienentämiseen muokatun aikatapahtuman laskutus.</span><span class="sxs-lookup"><span data-stu-id="d2a80-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-128">Laskuttamattoman myynnin peruutus tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="d2a80-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-129">Uusi laskuttamaton todellinen myynti, joka veloitetaan muokatun laskurivin tiedoissa olevista tunneista ja summasta, myynnin tosiasiallinen palautus ja vastaava laskutetun myynnin toteutuma.</span><span class="sxs-lookup"><span data-stu-id="d2a80-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-130">Uusi laskuttamaton myynnin toteutunut arvo, joka ei ole laskutettava jäljellä olevilta tunneilta ja summalta sen jälkeen, kun muokatun laskurivin tiedot, toteutuneiden myyntien peruutus ja vastaava laskutettu myynti on vähennetty.</span><span class="sxs-lookup"><span data-stu-id="d2a80-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2a80-131">Määrän lisäämiseen muokatun aikatapahtuman laskutus.</span><span class="sxs-lookup"><span data-stu-id="d2a80-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-132">Laskuttamattoman myynnin peruutus tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="d2a80-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-133">Uusi laskuttamaton todellinen myynti, joka on veloitettavissa laskutettujen laskurivien tiedoille, peruutetun myynnin toteutumiselle ja laskutettavalle myynnille.</span><span class="sxs-lookup"><span data-stu-id="d2a80-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2a80-134">Kulutapahtuman laskuttaminen muokkaamatta laskuluonnokseen.</span><span class="sxs-lookup"><span data-stu-id="d2a80-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-135">Laskuttamattoman myynnin peruutus määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="d2a80-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-136">Laskutettu toteutunut myynti määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="d2a80-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d2a80-137">Määrän pienentämiseen muokatun kulutapahtuman laskutus.</span><span class="sxs-lookup"><span data-stu-id="d2a80-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-138">Laskuttamattoman myynnin peruutus määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="d2a80-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-139">Uusi laskuttamaton todellinen myynti, joka on veloitettavissa muokatun laskurivin tiedoissa olevasta määrästä ja summasta, laskuttamattoman tosiasiallisen myynnin palautuksesta ja vastaavan laskutetun myynnin todellisesta arvosta.</span><span class="sxs-lookup"><span data-stu-id="d2a80-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-140">Uusi laskuttamaton tosiasiallinen myynti, josta ei veloiteta jäljellä olevaa määrää ja summaa sen jälkeen, kun vähennetään korjatut luvut muokatun laskurivin yksityiskohdissa, laskutetun myynnin tosiasiallisesta palautuksesta ja vastaavasta laskutetusta todellisesta myynnistä.</span><span class="sxs-lookup"><span data-stu-id="d2a80-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2a80-141">Määrän kasvattamiseen muokatun kulutapahtuman laskutus.</span><span class="sxs-lookup"><span data-stu-id="d2a80-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-142">Laskuttamattoman myynnin peruutus määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="d2a80-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-143">Uusi laskuttamaton todellinen myynti, joka on veloitettavissa muokatun laskurivin tiedoissa olevasta määrästä ja summasta, laskuttamattoman tosiasiallisen myynnin palautuksesta ja vastaavan laskutetun myynnin todellisesta arvosta.</span><span class="sxs-lookup"><span data-stu-id="d2a80-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2a80-144">Materiaalitapahtuman laskutus ilman laskuluonnoksen muokkauksia.</span><span class="sxs-lookup"><span data-stu-id="d2a80-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-145">Laskuttamattoman myynnin peruutus alkuperäisen materiaalin käytön hyväksynnän määrälle ja summalle.</span><span class="sxs-lookup"><span data-stu-id="d2a80-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-146">Laskutetun myynnin todellinen arvo alkuperäisen materiaalin käytön hyväksynnän määrälle ja summalle.</span><span class="sxs-lookup"><span data-stu-id="d2a80-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d2a80-147">Muokatun materiaalitapahtuman laskutus, kun sitä muokattiin määrän pienentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="d2a80-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-148">Laskuttamattoman myynnin peruutus alkuperäisen ajan käytön hyväksynnän määrälle ja summalle.</span><span class="sxs-lookup"><span data-stu-id="d2a80-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-149">Uusi laskuttamaton todellinen myynti, joka on veloitettavissa muokatun laskurivin tiedoissa olevasta määrästä ja summasta, laskuttamattoman tosiasiallisen myynnin palautuksesta ja vastaavan laskutetun myynnin todellisesta arvosta.</span><span class="sxs-lookup"><span data-stu-id="d2a80-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-150">Uusi laskuttamaton tosiasiallinen myynti, josta ei veloiteta jäljellä olevaa määrää ja summaa sen jälkeen, kun vähennetään korjatut luvut muokatun laskurivin yksityiskohdissa, laskutetun myynnin tosiasiallisesta palautuksesta ja vastaavasta laskutetusta todellisesta myynnistä.</span><span class="sxs-lookup"><span data-stu-id="d2a80-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2a80-151">Muokatun materiaalitapahtuman laskutus, kun sitä muokattiin määrän kasvattamiseksi.</span><span class="sxs-lookup"><span data-stu-id="d2a80-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-152">Laskuttamattoman myynnin peruutus alkuperäisen materiaalin käytön hyväksynnän määrälle ja summalle.</span><span class="sxs-lookup"><span data-stu-id="d2a80-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-153">Uusi laskuttamaton todellinen myynti, joka on veloitettavissa muokatun laskurivin tiedoissa olevasta määrästä ja summasta, laskuttamattoman tosiasiallisen myynnin palautuksesta ja vastaavan laskutetun myynnin todellisesta arvosta.</span><span class="sxs-lookup"><span data-stu-id="d2a80-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2a80-154">Maksun laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="d2a80-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-155">Laskuttamattoman myynnin peruutus maksusummalle alkuperäisellä kirjauskansion rivillä.</span><span class="sxs-lookup"><span data-stu-id="d2a80-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-156">Laskutettu toteutunut myynti määrälle ja summalle alkuperäisen palkkion kirjauskansion riville.</span><span class="sxs-lookup"><span data-stu-id="d2a80-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d2a80-157">Välitavoitteen laskutus.</span><span class="sxs-lookup"><span data-stu-id="d2a80-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2a80-158">Välitavoitteen summaa koskeva laskutettu myynti, joka on projektisopimusrivin alkuperäisessä välitavoitteessa.</span><span class="sxs-lookup"><span data-stu-id="d2a80-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
