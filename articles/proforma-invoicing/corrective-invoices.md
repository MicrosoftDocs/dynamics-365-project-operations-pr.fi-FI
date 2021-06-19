---
title: Korjaavat projektipohjaiset laskut
description: Tässä aiheessa on tietoja korjaavien projektipohjaisten laskujen luomisesta ja vahvistamisesta Project Operationsissa.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012267"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="cf0dc-103">Korjaavat projektipohjaiset laskut</span><span class="sxs-lookup"><span data-stu-id="cf0dc-103">Corrective project-based invoices</span></span>

<span data-ttu-id="cf0dc-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="cf0dc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cf0dc-105">Vahvistettu projektilasku voidaan korjata käsittelemään muutoksia tai hyvityksiä neuvoteltuna asiakkaan ja projektipäällikön kanssa.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="cf0dc-106">Voit tehdä muokkauksia vahvistettuun laskuun avaamalla vahvistetun laskun ja valitsemalla **Korjaa tämä lasku**.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="cf0dc-107">Valinta ei ole käytettävissä, ellei projektilaskua ole vahvistettu tai projektipohjaisessa laskussa on ennakkoja tai ennakkomaksuja tai ennakoiden tai ennakkomaksujen täsmäytyksiä.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="cf0dc-108">Uusi laskuluonnos luodaan vahvistetusta laskusta.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="cf0dc-109">Kaikki aiemmin vahvistetun laskun laskurivin tiedot kopioidaan uuteen luonnokseen.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="cf0dc-110">Seuraavassa on joitakin tärkeitä tietoja uuden korjatun laskun rivitiedoista:</span><span class="sxs-lookup"><span data-stu-id="cf0dc-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="cf0dc-111">Kaikki määrät päivitetään nollaksi.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-111">All quantities are updated to zero.</span></span> <span data-ttu-id="cf0dc-112">Dynamics 365 Project Operations olettaa, että kaikki laskutetut nimikkeet hyvitetään kokonaan.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="cf0dc-113">Voit tarvittaessa päivittää nämä määrät manuaalisesti niin, että ne vastaavat laskutettavaa määrää eikä hyvitettävän määrän määrää.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="cf0dc-114">Sovellus laskee hyvitetyn määrän syöttämiesi määrien perusteella.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="cf0dc-115">Tämä summa heijastuu todellisiin arvoihin, jotka luodaan korjatun laskun vahvistuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="cf0dc-116">Jos teet verosummaan muutoksia, sinun täytyy syöttää oikea verosumma eikä hyvitettävää verosummaa.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="cf0dc-117">Välitavoitekorjaukset käsitellään aina täysinä hyvityksinä.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="cf0dc-118">Jos laskurivin tiedot ovat korjauksia muihin jo laskutettuihin kuluihin, **Korjaus**-kentän arvoksi määritetään **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="cf0dc-119">Jos laskurivin tiedot ovat korjauksia, **Onko korjaus**-kentän arvoksi määritetään **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="cf0dc-120">Toteutuneet arvot, jotka luodaan, kun korjauslasku vahvistetaan</span><span class="sxs-lookup"><span data-stu-id="cf0dc-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="cf0dc-121">Seuraavassa taulukossa on esitetty toteutuneet arvot, jotka luodaan korjauslaskun vahvistuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="cf0dc-122">
                    <strong>Skenaario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cf0dc-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="cf0dc-123">
                    <strong>Vahvistuksen yhteydessä luodut toteutuneet arvot</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cf0dc-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cf0dc-124">Aiemmin laskutetun ajan tapahtuman täyden hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-125">Laskutetun myynnin peruutus tunnille ja summalle alkuperäisen ajan laskurivitiedon perusteella.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-126">Uusi laskuttamattoman todellinen myynti tunnille ja summalle alkuperäisen ajan laskurivitiedon perusteella.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="cf0dc-127">Osittaisen hyvityksen laskuttaminen aikatapahtumasta.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-128">Laskutettu myynnin peruutus tunneista ja summista, joka laskutetaan alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-129">Uusi laskuttamaton todellinen myynti, joka veloitetaan muokatun laskurivin tiedoissa olevista tunneista ja summasta, tämän palautus ja vastaava laskutetun myynnin toteutuma.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-130">Uusi laskuttamaton toteutunut myynti, joka on veloitettavissa jäljellä olevista työajoista ja määrästä, kun laskun rivitiedoista on vähennetty korjatut luvut.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cf0dc-131">Aiemmin laskutetun kulun tapahtuman täyden hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-132">Laskutettu myynnin peruutus määrästä ja summista kulun alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-133">Uusi laskuttamaton myynnin todellinen määrä ja summista kulun alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="cf0dc-134">Aiemmin laskutetun kulun tapahtuman osittaisen hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-135">Laskutettu myynnin peruutus laskutetusta määrästä ja summista kulun alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-136">Uusi laskuttamaton todellinen myynti, joka veloitetaan korjatun laskurivin tiedoissa olevista määristä ja summasta, tämän palautus ja vastaava laskutetun myynnin toteutuma.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-137">Uusi laskuttamaton toteutunut myynti, joka on veloitettavissa jäljellä olevista määristä ja summista, kun laskun rivitiedoista on vähennetty korjatut luvut.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cf0dc-138">Aiemmin laskutettujen materiaalitapahtumien täydellisen hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-139">Laskutetun myynnin peruutus määrälle ja summalle alkuperäisen materiaalin laskutusrivin tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-140">Uusi laskuttamattoman myynnin toteutunut arvo määrälle ja summalle alkuperäisen materiaalin laskutusrivin tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="cf0dc-141">Materiaalitapahtuman osittaisen hyvityksen laskutus.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-142">Laskutetun myynnin peruutus määrälle ja summalle, jotka on laskutettu alkuperäisen materiaalin laskutusrivin tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-143">Uusi laskuttamaton myynnin todellinen arvo, joka on laskutettava muokatun laskun rivin määrälle ja summalle, tämän peruutus ja vastaava laskutettu myynnin toteutunut arvo.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-144">Uusi laskuttamaton toteutunut myynti, joka on veloitettavissa jäljellä olevista määristä ja summista, kun laskun rivitiedoista on vähennetty korjatut luvut.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cf0dc-145">Aiemmin laskutetun palkkion tapahtuman täyden hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-146">Laskutettu myynnin peruutus määrästä ja summista palkkion alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-147">Uusi laskuttamaton myynnin todellinen määrä ja summista palkkion alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cf0dc-148">Aiemmin laskutetun palkkion tapahtuman osittaisen hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-149">Laskutettu myynnin peruutus määrästä ja summista palkkion alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-150">Uusi laskuttamaton todellinen myynti, joka veloitetaan muokatun ja korjatun laskurivin tiedoissa olevista määristä ja summasta, tämän palautus ja vastaava laskutetun myynnin toteutuma.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="cf0dc-151">Aiemmin laskutetun virstanpylvään täyden hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-152">Laskutetun myynnin peruutus summalle alkuperäisen virstanpylvään laskurivitiedon perusteella.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="cf0dc-153">Välitavoitteen laskun tila päivittyy arvosta <b>Kirjattu asiakaslasku</b> tilaksi <b>Valmis laskutettavaksi</b>.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="cf0dc-154">Aiemmin laskutetun virstanpylvään osittaisen hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cf0dc-155">Tätä skenaariota ei tueta.</span><span class="sxs-lookup"><span data-stu-id="cf0dc-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
