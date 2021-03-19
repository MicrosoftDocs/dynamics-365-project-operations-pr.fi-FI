---
title: Proformalaskun vahvistaminen – lite
description: Tämä aihe tarjoaa tietoja Project Operationsin proformalaskujen vahvistamisesta.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3b1818f20a0d54848939b689f87986154943c57a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274274"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="5cbc1-103">Proformalaskun vahvistaminen – lite</span><span class="sxs-lookup"><span data-stu-id="5cbc1-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="5cbc1-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="5cbc1-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="5cbc1-105">Kun proformalasku on vahvistettu, projektilaskun päivitysten tila on **Vahvistettu**.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="5cbc1-106">Kun lasku on vahvistettu, se on vain luku -tilassa.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="5cbc1-107">Jatkossa lasku voidaan oikaista vain, jos asiakkaalle on aloitettu korjauksia tai hyvityksiä tai jos lasku on merkitty maksetuksi.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="5cbc1-108">Seuraavassa taulukossa on lueteltu järjestelmän luomat toteutuneet arvot.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="5cbc1-109">Nämä toteutuneet arvot luodaan, kun projektilaskulle tehdään tiettyjä toimintoja ennen sen vahvistamista.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="5cbc1-110">
                    <strong>Skenaario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5cbc1-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="5cbc1-111">
                    <strong>Vahvistuksen yhteydessä luodut toteutuneet arvot</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5cbc1-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5cbc1-112">Ennakkomaksun tai ennakkomaksuun perustuvan maksun laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="5cbc1-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-113">Laskutetun todellisen myynnin tyyppi, <strong>Pidätyskohde</strong> luodaan ennakkomaksulle tai pidätyskohteelle.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-114">Täsmäyttämisen yhteydessä käytettävä maksun tai ennakon negatiivinen summa, jota ei ole laskutettu.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5cbc1-115">Sen jälkeen, kun olet täysin täsmäyttänyt laskun pidätyksen tai ennakkomaksun.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-116">Täsmäytystä varten luodun pidätyksen tai ennakkomaksun laskuttamattoman myynnin peruutus.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="5cbc1-117">Tämä summa on positiivinen, koska sen tarkoitus on kumota pidätyksen tai ennakkomaksun yhteydessä luotu negatiivinen tulos.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-118">Laskutetun myynnin todellinen summa laskussa.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="5cbc1-119">Sen jälkeen, kun olet osittain täsmäyttänyt laskun pidätyksen tai ennakkomaksun.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-120">Täsmäytystä varten luodun pidätyksen tai ennakkomaksun laskuttamattoman myynnin peruutus.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="5cbc1-121">Tämä summa on positiivinen, koska sen tarkoitus on kumota pidätyksen tai ennakkomaksun yhteydessä luotu negatiivinen tulos.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-122">Laskutetun myynnin todellinen summa laskussa.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-123">Negatiivisen laskuttamattoman myynnin todellinen jäljellä olevan pidätys tai ennakkomäärä, jota käytetään tulevissa laskuissa.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5cbc1-124">Aikatapahtuman laskuttaminen muokkaamatta laskuluonnokseen.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-125">Laskuttamattoman myynnin peruutus tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-126">Laskutettu toteutunut myynti tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="5cbc1-127">Määrän pienentämiseen muokatun aikatapahtuman laskutus.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-128">Laskuttamattoman myynnin peruutus tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-129">Uusi laskuttamaton todellinen myynti, joka veloitetaan muokatun laskurivin tiedoissa olevista tunneista ja summasta, myynnin tosiasiallinen palautus ja vastaava laskutetun myynnin toteutuma.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-130">Uusi laskuttamaton tosiasiallinen myynti, josta ei veloiteta jäljellä olevia tunteja ja määrää sen jälkeen, kun vähennetään korjatut luvut muokatun laskurivin yksityiskohdissa, tosiasiallisen myynnin palautus ja vastaava laskutettu todellinen myynti.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5cbc1-131">Määrän lisäämiseen muokatun aikatapahtuman laskutus.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-132">Laskuttamattoman myynnin peruutus tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-133">Uusi laskuttamaton todellinen myynti, joka on veloitettavissa laskutettujen laskurivien tiedoille, peruutetun myynnin toteutumiselle ja laskutettavalle myynnille.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5cbc1-134">Kulutapahtuman laskuttaminen muokkaamatta laskuluonnokseen.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-135">Laskuttamattoman myynnin peruutus määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-136">Laskutettu toteutunut myynti määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella</span><span class="sxs-lookup"><span data-stu-id="5cbc1-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="5cbc1-137">Määrän pienentämiseen muokatun kulutapahtuman laskutus.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-138">Laskuttamattoman myynnin peruutus määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-139">Uusi laskuttamaton todellinen myynti, joka on veloitettavissa muokatun laskurivin tiedoissa olevasta määrästä ja summasta, laskuttamattoman tosiasiallisen myynnin palautuksesta ja vastaavan laskutetun myynnin todellisesta arvosta.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-140">Uusi laskuttamaton tosiasiallinen myynti, josta ei veloiteta jäljellä olevaa määrää ja summaa sen jälkeen, kun vähennetään korjatut luvut muokatun laskurivin yksityiskohdissa, laskutetun myynnin tosiasiallisesta palautuksesta ja vastaavasta laskutetusta todellisesta myynnistä.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5cbc1-141">Määrän kasvattamiseen muokatun kulutapahtuman laskutus.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-142">Laskuttamattoman myynnin peruutus määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-143">Uusi laskuttamaton todellinen myynti, joka on veloitettavissa muokatun laskurivin tiedoissa olevasta määrästä ja summasta, laskuttamattoman tosiasiallisen myynnin palautuksesta ja vastaavan laskutetun myynnin todellisesta arvosta.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5cbc1-144">Maksun laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-145">Laskuttamattoman myynnin peruutus maksusummalle alkuperäisellä kirjauskansion rivillä.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-146">Laskutettu toteutunut myynti määrälle ja summalle alkuperäisen palkkion kirjauskansion riville.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="5cbc1-147">Välitavoitteen laskutus.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-148">Välitavoitteen summaa koskeva laskutettu myynti, joka on projektisopimusrivin alkuperäisessä välitavoitteessa.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="5cbc1-149">Tuotepohjaisen sopimusrivin laskuttaminen.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5cbc1-150">Tuoteriviltä laskutettu myynti, jolla on tuotepohjaisen sopimusrivin määrä ja summa.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]