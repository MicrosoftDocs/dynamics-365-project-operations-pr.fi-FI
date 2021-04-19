---
title: Korjaavien projektipohjaisten laskujen luominen
description: Tässä aiheessa on tietoja korjauslaskuista Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788850"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="324f5-103">Korjaavien projektipohjaisten laskujen luominen</span><span class="sxs-lookup"><span data-stu-id="324f5-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="324f5-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="324f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="324f5-105">Vahvistettu projektilasku voidaan korjata käsittelemään muutoksia tai hyvityksiä neuvoteltuna asiakkaan ja projektipäällikön kanssa.</span><span class="sxs-lookup"><span data-stu-id="324f5-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="324f5-106">Voit tehdä muokkauksia vahvistettuun laskuun avaamalla vahvistetun laskun ja valitsemalla **Korjaa tämä lasku**.</span><span class="sxs-lookup"><span data-stu-id="324f5-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="324f5-107">Tämä valinta ei ole käytettävissä, ellei projektilaskua vahvisteta.</span><span class="sxs-lookup"><span data-stu-id="324f5-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="324f5-108">Uusi laskuluonnos luodaan vahvistetusta laskusta.</span><span class="sxs-lookup"><span data-stu-id="324f5-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="324f5-109">Kaikki aiemmin vahvistetun laskun laskurivin tiedot kopioidaan uuteen luonnokseen.</span><span class="sxs-lookup"><span data-stu-id="324f5-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="324f5-110">Seuraavassa on joitakin tärkeitä seikkoja, jotka auttavat ymmärtämään paremmin uuden korjatun laskun rivin tiedot:</span><span class="sxs-lookup"><span data-stu-id="324f5-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="324f5-111">Kaikki määrät päivitetään nollaksi.</span><span class="sxs-lookup"><span data-stu-id="324f5-111">All quantities are updated to zero.</span></span> <span data-ttu-id="324f5-112">Oletetaan, että kaikki laskutetut nimikkeet hyvitetään kokonaan.</span><span class="sxs-lookup"><span data-stu-id="324f5-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="324f5-113">Voit tarvittaessa päivittää nämä määrät manuaalisesti niin, että ne vastaavat laskutettavaa määrää eikä hyvitettävän määrän määrää.</span><span class="sxs-lookup"><span data-stu-id="324f5-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="324f5-114">Sovellus laskee hyvitetyn määrän syöttämiesi määrien perusteella.</span><span class="sxs-lookup"><span data-stu-id="324f5-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="324f5-115">Tämä summa heijastuu todellisiin arvoihin, jotka luodaan korjatun laskun vahvistuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="324f5-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="324f5-116">Jos teet verosummaan muutoksia, sinun täytyy syöttää oikea verosumma eikä hyvitettävää verosummaa.</span><span class="sxs-lookup"><span data-stu-id="324f5-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="324f5-117">Välitavoitekorjaukset käsitellään aina täysinä hyvityksinä.</span><span class="sxs-lookup"><span data-stu-id="324f5-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="324f5-118">Pidätys- tai ennakkosummat voidaan oikaista, jos asiakasta on laskutettu virheellisen määrän takia.</span><span class="sxs-lookup"><span data-stu-id="324f5-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="324f5-119">Pidätysmaksujen ja ennakoiden täsmäytykset voidaan oikaista, jos aiemmin vahvistetun laskun kulujen täsmäyttämiseen käytettiin virheellistä määrää.</span><span class="sxs-lookup"><span data-stu-id="324f5-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="324f5-120">Jos laskurivin tiedot ovat korjauksia muihin jo laskutettuihin kuluihin, määritä **Korjaus**-kentän arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="324f5-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="324f5-121">Laskuilla, joiden laskurivitiedot on korjattu on kenttä nimeltä **korjaukset**, joiden arvo on myös **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="324f5-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="324f5-122">Korjaavan laskun vahvistuksessa luodut toteutuneet arvot</span><span class="sxs-lookup"><span data-stu-id="324f5-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="324f5-123">Seuraavassa taulukossa on esitetty toteutuneet arvot, jotka luodaan korjauslaskun vahvistuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="324f5-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="324f5-124">
                    <strong>Skenaario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="324f5-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="324f5-125">
                    <strong>Vahvistuksen yhteydessä luodut toteutuneet arvot</strong>
                </span><span class="sxs-lookup"><span data-stu-id="324f5-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="324f5-126">Vahvista laskutettu ennakko tai pidätys.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="324f5-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-127">Täsmäytystä varten luodun pidätyksen tai ennakkomaksun laskuttamattoman myynnin peruutus.</span><span class="sxs-lookup"><span data-stu-id="324f5-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="324f5-128">Tämä summa on positiivinen, koska sen tarkoitus on kumota pidätyksen tai ennakkomaksun yhteydessä luotu negatiivinen tulos.</span><span class="sxs-lookup"><span data-stu-id="324f5-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-129">Laskutetun myynnin peruutuksen todellinen arvo luodaan ennakkomaksun tai ennakon peruutuksesta alkuperäistä laskutettavaa myyntiä varten.</span><span class="sxs-lookup"><span data-stu-id="324f5-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-130">Korjatulle summalle luodaan uusi laskutettu myyntiennuste pidätykselle tai ennakkoon perustuvalle korjatulle laskuriville.</span><span class="sxs-lookup"><span data-stu-id="324f5-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-131">Laskuttamattoman myynnin todellisen negatiivisen määrän pidätys tai ennakkoon perustuva korjattu laskurivi, jota käytetään täsmäytykseen.</span><span class="sxs-lookup"><span data-stu-id="324f5-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="324f5-132">Vahvistus korjauksesta, joka on aiemmin täsmäytetyn pidätys- tai ennakkomaksun korjaus.</span><span class="sxs-lookup"><span data-stu-id="324f5-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-133">Täsmäytystä varten luodun pidätyksen tai ennakkomaksun laskuttamattoman myynnin peruutus.</span><span class="sxs-lookup"><span data-stu-id="324f5-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="324f5-134">Tämä summa on positiivinen ja sen tarkoitus on kumota aiemman täsmäytyksen yhteydessä luotu negatiivinen tulos.</span><span class="sxs-lookup"><span data-stu-id="324f5-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-135">Laskutetun myynnin peruutuksen todellinen summa aiemmassa laskussa.</span><span class="sxs-lookup"><span data-stu-id="324f5-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-136">Todellinen uusi laskutettu myynti korjatulle pidätyssummalle, joka otetaan käyttöön korjatussa laskussa.</span><span class="sxs-lookup"><span data-stu-id="324f5-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-137">Laskuttamaton todellinen myynti negatiivisella summalla korjatusta jäljellä olevasta pidätyksestä tai ennakosta, jota käytetään myöhempien laskujen täsmäytykseen.</span><span class="sxs-lookup"><span data-stu-id="324f5-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="324f5-138">Aiemmin laskutetun ajan tapahtuman täyden hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="324f5-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-139">Laskutetun myynnin peruutus tunnille ja summalle alkuperäisen ajan laskurivitiedon perusteella.</span><span class="sxs-lookup"><span data-stu-id="324f5-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-140">Uusi laskuttamattoman todellinen myynti tunnille ja summalle alkuperäisen ajan laskurivitiedon perusteella.</span><span class="sxs-lookup"><span data-stu-id="324f5-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="324f5-141">Osittaisen hyvityksen laskuttaminen aikatapahtumasta.</span><span class="sxs-lookup"><span data-stu-id="324f5-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-142">Laskutettu myynnin peruutus tunneista ja summista, joka laskutetaan alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="324f5-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-143">Uusi laskuttamaton todellinen myynti, joka veloitetaan muokatun laskurivin tiedoissa olevista tunneista ja summasta, tämän palautus ja vastaava laskutetun myynnin toteutuma.</span><span class="sxs-lookup"><span data-stu-id="324f5-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-144">Uusi laskuttamaton toteutunut myynti, joka on veloitettavissa jäljellä olevista työajoista ja määrästä, kun laskun rivitiedoista on vähennetty korjatut luvut.</span><span class="sxs-lookup"><span data-stu-id="324f5-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="324f5-145">Aiemmin laskutetun kulun tapahtuman täyden hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="324f5-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-146">Laskutettu myynnin peruutus määrästä ja summista kulun alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="324f5-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-147">Uusi laskuttamaton myynnin todellinen määrä ja summista kulun alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="324f5-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="324f5-148">Aiemmin laskutetun kulun tapahtuman osittaisen hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="324f5-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-149">Laskutettu myynnin peruutus laskutetusta määrästä ja summista kulun alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="324f5-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-150">Uusi laskuttamaton todellinen myynti, joka veloitetaan korjatun laskurivin tiedoissa olevista määristä ja summasta, tämän palautus ja vastaava laskutetun myynnin toteutuma.</span><span class="sxs-lookup"><span data-stu-id="324f5-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-151">Uusi laskuttamaton toteutunut myynti, joka on veloitettavissa jäljellä olevista määristä ja summista, kun laskun rivitiedoista on vähennetty korjatut luvut.</span><span class="sxs-lookup"><span data-stu-id="324f5-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="324f5-152">Aiemmin laskutetun palkkion tapahtuman täyden hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="324f5-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-153">Laskutettu myynnin peruutus määrästä ja summista palkkion alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="324f5-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-154">Uusi laskuttamaton myynnin todellinen määrä ja summista palkkion alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="324f5-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="324f5-155">Aiemmin laskutetun palkkion tapahtuman osittaisen hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="324f5-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-156">Laskutettu myynnin peruutus määrästä ja summista palkkion alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="324f5-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-157">Uusi laskuttamaton todellinen myynti, joka veloitetaan muokatun ja korjatun laskurivin tiedoissa olevista määristä ja summasta, tämän palautus ja vastaava laskutetun myynnin toteutuma.</span><span class="sxs-lookup"><span data-stu-id="324f5-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="324f5-158">Aiemmin laskutetun virstanpylvään täyden hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="324f5-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-159">Laskutetun myynnin peruutus summalle alkuperäisen virstanpylvään laskurivitiedon perusteella.</span><span class="sxs-lookup"><span data-stu-id="324f5-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="324f5-160">Välitavoitteen laskun tila päivittyy arvosta <b>Kirjattu asiakaslasku</b> tilaksi <b>Valmis laskutettavaksi</b>.</span><span class="sxs-lookup"><span data-stu-id="324f5-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="324f5-161">Aiemmin laskutetun virstanpylvään osittaisen hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="324f5-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="324f5-162">Ei tuettu</span><span class="sxs-lookup"><span data-stu-id="324f5-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
