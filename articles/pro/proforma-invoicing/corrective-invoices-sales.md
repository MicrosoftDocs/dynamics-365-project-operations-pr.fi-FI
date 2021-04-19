---
title: Oikaisevat projektilaskut
description: Tässä aiheessa on tietoja korjaavien projektipohjaisten laskujen luomisesta Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae6d881e4e68b9f467478afe9735fc3186e6b0a8
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866587"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="f3832-103">Oikaisevat projektilaskut</span><span class="sxs-lookup"><span data-stu-id="f3832-103">Corrective project invoices</span></span>

<span data-ttu-id="f3832-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="f3832-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f3832-105">Vahvistettu projektilasku voidaan korjata käsittelemään muutoksia tai hyvityksiä neuvoteltuna asiakkaan ja projektipäällikön kanssa.</span><span class="sxs-lookup"><span data-stu-id="f3832-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="f3832-106">Voit tehdä muokkauksia vahvistettuun laskuun avaamalla vahvistetun laskun ja valitsemalla **Korjaa tämä lasku**.</span><span class="sxs-lookup"><span data-stu-id="f3832-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="f3832-107">Tämä valinta ei ole käytettävissä, ellei projektilaskua vahvisteta.</span><span class="sxs-lookup"><span data-stu-id="f3832-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="f3832-108">Uusi laskuluonnos luodaan vahvistetusta laskusta.</span><span class="sxs-lookup"><span data-stu-id="f3832-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="f3832-109">Kaikki aiemmin vahvistetun laskun laskurivin tiedot kopioidaan uuteen luonnokseen.</span><span class="sxs-lookup"><span data-stu-id="f3832-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="f3832-110">Seuraavassa on joitakin tärkeitä tietoja uuden korjatun laskun rivitiedoista:</span><span class="sxs-lookup"><span data-stu-id="f3832-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="f3832-111">Kaikki määrät päivitetään nollaksi.</span><span class="sxs-lookup"><span data-stu-id="f3832-111">All quantities are updated to zero.</span></span> <span data-ttu-id="f3832-112">Sovellus olettaa, että kaikki laskutetut nimikkeet hyvitetään kokonaan.</span><span class="sxs-lookup"><span data-stu-id="f3832-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="f3832-113">Voit tarvittaessa päivittää nämä määrät manuaalisesti niin, että ne vastaavat laskutettavaa määrää eikä hyvitettävän määrän määrää.</span><span class="sxs-lookup"><span data-stu-id="f3832-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="f3832-114">Sovellus laskee hyvitetyn määrän syöttämiesi määrien perusteella.</span><span class="sxs-lookup"><span data-stu-id="f3832-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="f3832-115">Tämä summa heijastuu todellisiin arvoihin, jotka luodaan korjatun laskun vahvistuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="f3832-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="f3832-116">Jos teet verosummaan muutoksia, sinun täytyy syöttää oikea verosumma eikä hyvitettävää verosummaa.</span><span class="sxs-lookup"><span data-stu-id="f3832-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="f3832-117">Aiemmin vahvistettuja tuotepohjaisia sopimusrivejä ei kopioida.</span><span class="sxs-lookup"><span data-stu-id="f3832-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="f3832-118">Tuotepohjaisen projektilaskun korjausten käsittelyä ei tueta.</span><span class="sxs-lookup"><span data-stu-id="f3832-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="f3832-119">Välitavoitekorjaukset käsitellään aina täysinä hyvityksinä.</span><span class="sxs-lookup"><span data-stu-id="f3832-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="f3832-120">Pidätys- tai ennakkosummat voidaan oikaista, jos asiakasta on laskutettu virheellisen määrän takia.</span><span class="sxs-lookup"><span data-stu-id="f3832-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="f3832-121">Pidätysmaksujen ja ennakoiden täsmäytykset voidaan oikaista, jos aiemmin vahvistetun laskun kulujen täsmäyttämiseen käytettiin virheellistä määrää.</span><span class="sxs-lookup"><span data-stu-id="f3832-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3832-122">Laskurivin tiedot, jotka ovat korjauksia muihin jo laskutettuihin kuluihin, saavat kentän **korjauksen** arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f3832-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="f3832-123">Laskuilla, joiden laskurivitiedot on korjattu on kenttä nimeltä **korjaukset**, joiden arvo on myös **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f3832-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="f3832-124">Toteutuneet arvot, jotka luodaan, kun korjauslasku vahvistetaan</span><span class="sxs-lookup"><span data-stu-id="f3832-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="f3832-125">Seuraavassa taulukossa on esitetty toteutuneet arvot, jotka luodaan korjauslaskun vahvistuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="f3832-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="f3832-126">
                    <strong>Skenaario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3832-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="f3832-127">
                    <strong>Vahvistuksen yhteydessä luodut toteutuneet arvot</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3832-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="f3832-128">Vahvista laskutettu ennakko tai pidätys.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3832-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-129">Täsmäytystä varten luodun pidätyksen tai ennakkomaksun laskuttamattoman myynnin peruutus.</span><span class="sxs-lookup"><span data-stu-id="f3832-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="f3832-130">Tämä summa on positiivinen, koska sen tarkoitus on kumota pidätyksen tai ennakkomaksun yhteydessä luotu negatiivinen tulos.</span><span class="sxs-lookup"><span data-stu-id="f3832-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-131">Laskutetun myynnin peruutuksen todellinen arvo luodaan ennakkomaksun tai ennakon peruutuksesta alkuperäistä laskutettavaa myyntiä varten.</span><span class="sxs-lookup"><span data-stu-id="f3832-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-132">Korjatulle summalle luodaan uusi laskutettu myyntiennuste pidätykselle tai ennakkoon perustuvalle korjatulle laskuriville.</span><span class="sxs-lookup"><span data-stu-id="f3832-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-133">Laskuttamattoman myynnin todellisen negatiivisen määrän pidätys tai ennakkoon perustuva korjattu laskurivi, jota käytetään täsmäytykseen.</span><span class="sxs-lookup"><span data-stu-id="f3832-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="f3832-134">Vahvistus korjauksesta, joka on aiemmin täsmäytetyn pidätys- tai ennakkomaksun korjaus.</span><span class="sxs-lookup"><span data-stu-id="f3832-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-135">Täsmäytystä varten luodun pidätyksen tai ennakkomaksun laskuttamattoman myynnin peruutus.</span><span class="sxs-lookup"><span data-stu-id="f3832-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="f3832-136">Tämä summa on positiivinen ja sen tarkoitus on kumota aiemman täsmäytyksen yhteydessä luotu negatiivinen tulos.</span><span class="sxs-lookup"><span data-stu-id="f3832-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-137">Laskutetun myynnin peruutuksen todellinen summa aiemmassa laskussa.</span><span class="sxs-lookup"><span data-stu-id="f3832-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-138">Todellinen uusi laskutettu myynti korjatulle pidätyssummalle, joka otetaan käyttöön korjatussa laskussa.</span><span class="sxs-lookup"><span data-stu-id="f3832-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-139">Laskuttamaton todellinen myynti negatiivisella summalla korjatusta jäljellä olevasta pidätyksestä tai ennakosta, jota käytetään myöhempien laskujen täsmäytykseen.</span><span class="sxs-lookup"><span data-stu-id="f3832-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3832-140">Aiemmin laskutetun ajan tapahtuman täyden hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="f3832-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-141">Laskutetun myynnin peruutus tunnille ja summalle alkuperäisen ajan laskurivitiedon perusteella.</span><span class="sxs-lookup"><span data-stu-id="f3832-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-142">Uusi laskuttamattoman todellinen myynti tunnille ja summalle alkuperäisen ajan laskurivitiedon perusteella.</span><span class="sxs-lookup"><span data-stu-id="f3832-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f3832-143">Osittaisen hyvityksen laskuttaminen aikatapahtumasta.</span><span class="sxs-lookup"><span data-stu-id="f3832-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-144">Laskutettu myynnin peruutus tunneista ja summista, joka laskutetaan alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="f3832-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-145">Uusi laskuttamaton todellinen myynti, joka veloitetaan muokatun laskurivin tiedoissa olevista tunneista ja summasta, tämän palautus ja vastaava laskutetun myynnin toteutuma.</span><span class="sxs-lookup"><span data-stu-id="f3832-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-146">Uusi laskuttamaton toteutunut myynti, joka on veloitettavissa jäljellä olevista työajoista ja määrästä, kun laskun rivitiedoista on vähennetty korjatut luvut.</span><span class="sxs-lookup"><span data-stu-id="f3832-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3832-147">Aiemmin laskutetun kulun tapahtuman täyden hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="f3832-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-148">Laskutettu myynnin peruutus määrästä ja summista kulun alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="f3832-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-149">Uusi laskuttamaton myynnin todellinen määrä ja summista kulun alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="f3832-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f3832-150">Aiemmin laskutetun kulun tapahtuman osittaisen hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="f3832-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-151">Laskutettu myynnin peruutus laskutetusta määrästä ja summista kulun alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="f3832-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-152">Uusi laskuttamaton todellinen myynti, joka veloitetaan korjatun laskurivin tiedoissa olevista määristä ja summasta, tämän palautus ja vastaava laskutetun myynnin toteutuma.</span><span class="sxs-lookup"><span data-stu-id="f3832-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-153">Uusi laskuttamaton toteutunut myynti, joka on veloitettavissa jäljellä olevista määristä ja summista, kun laskun rivitiedoista on vähennetty korjatut luvut.</span><span class="sxs-lookup"><span data-stu-id="f3832-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3832-154">Aiemmin laskutettujen materiaalitapahtumien täydellisen hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="f3832-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-155">Laskutetun myynnin peruutus määrälle ja summalle alkuperäisen materiaalin laskutusrivin tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="f3832-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-156">Uusi laskuttamattoman myynnin toteutunut arvo määrälle ja summalle alkuperäisen materiaalin laskutusrivin tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="f3832-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f3832-157">Materiaalitapahtuman osittaisen hyvityksen laskutus.</span><span class="sxs-lookup"><span data-stu-id="f3832-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-158">Laskutetun myynnin peruutus määrälle ja summalle, jotka on laskutettu alkuperäisen materiaalin laskutusrivin tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="f3832-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-159">Uusi laskuttamaton myynnin todellinen arvo, joka on laskutettava muokatun laskun rivin määrälle ja summalle, tämän peruutus ja vastaava laskutettu myynnin toteutunut arvo.</span><span class="sxs-lookup"><span data-stu-id="f3832-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-160">Uusi laskuttamaton toteutunut myynti, joka on veloitettavissa jäljellä olevista määristä ja summista, kun laskun rivitiedoista on vähennetty korjatut luvut.</span><span class="sxs-lookup"><span data-stu-id="f3832-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3832-161">Aiemmin laskutetun palkkion tapahtuman täyden hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="f3832-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-162">Laskutettu myynnin peruutus määrästä ja summista palkkion alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="f3832-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-163">Uusi laskuttamaton myynnin todellinen määrä ja summista palkkion alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="f3832-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3832-164">Aiemmin laskutetun palkkion tapahtuman osittaisen hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="f3832-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-165">Laskutettu myynnin peruutus määrästä ja summista palkkion alkuperäisellä laskurivillä.</span><span class="sxs-lookup"><span data-stu-id="f3832-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-166">Uusi laskuttamaton todellinen myynti, joka veloitetaan muokatun ja korjatun laskurivin tiedoissa olevista määristä ja summasta, tämän palautus ja vastaava laskutetun myynnin toteutuma.</span><span class="sxs-lookup"><span data-stu-id="f3832-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f3832-167">Aiemmin laskutetun virstanpylvään täyden hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="f3832-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-168">Laskutetun myynnin peruutus summalle alkuperäisen virstanpylvään laskurivitiedon perusteella.</span><span class="sxs-lookup"><span data-stu-id="f3832-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="f3832-169">Välitavoitteen laskun tila päivittyy arvosta <b>Kirjattu asiakaslasku</b> tilaksi <b>Valmis laskutettavaksi</b>.</span><span class="sxs-lookup"><span data-stu-id="f3832-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f3832-170">Aiemmin laskutetun virstanpylvään osittaisen hyvityksen laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="f3832-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-171">Ei tuettu</span><span class="sxs-lookup"><span data-stu-id="f3832-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f3832-172">Aiemmin laskutetun tuotepohjaisen sopimusrivin hyvitykset ja korjaukset.</span><span class="sxs-lookup"><span data-stu-id="f3832-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3832-173">Ei tuettu</span><span class="sxs-lookup"><span data-stu-id="f3832-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
