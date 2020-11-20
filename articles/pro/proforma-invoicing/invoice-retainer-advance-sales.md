---
title: Ennakkomaksun tai ennakkomaksuun perustuvan maksun laskuttaminen
description: Tässä aiheessa on tietoja siitä, miten pidätyksiä tai ennakoita laskutetaan Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ed3b71d5f0ac035403de9fa213f3f45d14038e0
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087892"
---
# <a name="invoice-a-retainer-or-an-advance"></a><span data-ttu-id="ab6fa-103">Ennakkomaksun tai ennakkomaksuun perustuvan maksun laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="ab6fa-103">Invoice a retainer or an advance</span></span>

<span data-ttu-id="ab6fa-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="ab6fa-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ab6fa-105">Dynamics 365 Project Operations tukee pidätykseen perustuvia palvelusopimuksia ja kertaennakoita.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-105">Dynamics 365 Project Operations supports retainer-based contracts and one-time advances.</span></span> <span data-ttu-id="ab6fa-106">Projektisopimuksessa voit kirjata maksuaikataulun tai kertaennakon.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-106">On a project contract, you can record a schedule of retainers or a one-time advance.</span></span> <span data-ttu-id="ab6fa-107">Projektisopimustasolla kirjaaminen ei kuitenkaan heti tee pidätystä tai ennakkoa käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-107">However, recording at the project contract level doesn't immediately make a retainer or advance available for use.</span></span> <span data-ttu-id="ab6fa-108">Jos haluat käyttää pidätystä tai ennakkomaksua laskulle, joka tosiasiassa laskuttaa asiakasta, pidätyksen tai ennakon on oltava ensin laskutettuna.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-108">To use a retainer or advance on an invoice that actually charges the customer, the retainer or advance must be invoiced first.</span></span>

<span data-ttu-id="ab6fa-109">Pidätyksen tai ennakon laskutus tapahtuu suorittamalla seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-109">Complete the following steps to invoice a retainer or an advance.</span></span>

1. <span data-ttu-id="ab6fa-110">Valitse **myynti** > **laskutus** > **pidätykset ja ennakot**.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-110">Select **Sales** > **Billing** > **Retainers and Advances**.</span></span> 
2. <span data-ttu-id="ab6fa-111">**Valitse ennakot ja pidätykset** -sivulla suodattimesta tietty pidätys tai ennakkomaksu ja merkitse se **valmiiksi laskutettavaksi**.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-111">On the **Advances and Retainers** page, use the filter to select the specific retainer or advance to invoice and mark it as **Ready to Invoice**.</span></span>
3. <span data-ttu-id="ab6fa-112">Luo lasku joko manuaalisesti **Projektisopimus** -luettelosta tai tietosivulta.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-112">Create an invoice either manually from the **Project Contract** list or detail page.</span></span> <span data-ttu-id="ab6fa-113">Pidätyksen tai ennakon esitys näkyy **lasku** -sivun **ennakko ja pidätys** -osassa.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-113">The retainer or advance is shown on the draft invoice in the **Advances and Retainers** section on the **Invoice** page.</span></span>
4. <span data-ttu-id="ab6fa-114">Vahvista lasku.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-114">Confirm the invoice.</span></span> <span data-ttu-id="ab6fa-115">Tämä tekee pidätyksen tai ennakon käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-115">This will make the retainer or advance available for use.</span></span> <span data-ttu-id="ab6fa-116">Voit tarkistaa laskun **pidätykset ja ennakot** -luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-116">You can verify the invoice on the **Retainers and Advances** list page.</span></span> <span data-ttu-id="ab6fa-117">Jos kyseessä on laskutettu ennakko tai pidätys, käytettävissä oleva summa näkyy ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-117">For an invoiced Advance or Retainer, the available amount is shown in the grid.</span></span>

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a><span data-ttu-id="ab6fa-118">Pidätyksen tai ennakon luominen laskun ruudukosta</span><span class="sxs-lookup"><span data-stu-id="ab6fa-118">Create a retainer or advance from the Invoice grid</span></span>

<span data-ttu-id="ab6fa-119">Voit luoda pidätyksen tai ennakon suoraan laskuun.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-119">You can create a retainer or an advance directly on an invoice.</span></span>

1. <span data-ttu-id="ab6fa-120">Jos haluat luoda uuden **pidätyksen tai ennakon** , valitse laskun ennakkomaksut ja lisäasetukset -aliruudukossa **uusi**.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-120">On a draft invoice, on the **Advances and Retainers** subgrid, select **New** to create a new retainer or advance.</span></span> 
2. <span data-ttu-id="ab6fa-121">Lisää tarvittavat tiedot **Pikaluonti** -sivulla ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-121">On the **Quick Create** page, add the necessary information, and then select **Save**.</span></span> <span data-ttu-id="ab6fa-122">Pidätys tai ennakkomaksu luodaan laskuun liittyvässä projektisopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-122">The retainer or advance is created on the project contract related to the invoice.</span></span> <span data-ttu-id="ab6fa-123">Pidätys tai ennakko merkitään automaattisesti **valmiiksi laskutettavaksi** ja lisätään sitten **Laskut** -sivun **Ennakot ja pidätykset** -aliruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-123">The retainer or advance is automatically marked as **Ready to Invoice** and then added to the **Advances and Retainers** subgrid on the **Invoice** page.</span></span>

## <a name="reconcile-an-invoiced-retainer-or-advance"></a><span data-ttu-id="ab6fa-124">Yhdistä laskutettu pidätys tai ennakko</span><span class="sxs-lookup"><span data-stu-id="ab6fa-124">Reconcile an invoiced retainer or advance</span></span>

<span data-ttu-id="ab6fa-125">Kun pidätys tai ennakko on laskutettu, sitä voidaan käyttää tai täsmäyttää laskuun ajan, kulujen, välitavoitteiden tai muiden projektipohjaisten kulujen perusteella.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-125">After a retainer or advance is invoiced, they can be used or reconciled on an invoice with time, expenses, milestones, or other project-based charges.</span></span> <span data-ttu-id="ab6fa-126">Asiakas näkee laskunsa laskun summalla, jota vähennetään laskussa käytetyn pidätyksen tai ennakon perusteella.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-126">The customer will see their invoice amount reduced by the retainer or advance amount used on this invoice.</span></span>

<span data-ttu-id="ab6fa-127">Kun projektisopimukselle, jolle on laskutettu pidätykset tai ennakot, luodaan lasku, projektitoiminto ottaa automaattisesti käyttöön laskun pidätyksen tai ennakon.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-127">On every invoice that is generated for a project contract that has invoiced retainers or advances, Project Operation automatically applies the retainer or advance to the invoice.</span></span>

<span data-ttu-id="ab6fa-128">Tämän voi nähdä **Kohdistetut pidätykset ja ennakot** -ruudukossa **lasku** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-128">This can be seen in the **Applied Retainers and Advances** grid on the **Invoice** page.</span></span> <span data-ttu-id="ab6fa-129">Seuraavassa taulukossa on tietoja **Projektilasku** -sivun **Käytössä olevat pidätykset ja ennakot** -ruudukon kentistä.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-129">The following table provides information about the fields on the **Applied Retainers and Advances** grid of the **Project Invoice** page.</span></span>

| <span data-ttu-id="ab6fa-130">Field</span><span class="sxs-lookup"><span data-stu-id="ab6fa-130">Field</span></span> | <span data-ttu-id="ab6fa-131">Sijainti</span><span class="sxs-lookup"><span data-stu-id="ab6fa-131">Location</span></span> | <span data-ttu-id="ab6fa-132">Relevanssi, tarkoitus ja opastus</span><span class="sxs-lookup"><span data-stu-id="ab6fa-132">Relevance, purpose, and guidance</span></span> | <span data-ttu-id="ab6fa-133">Loppupään vaikutus</span><span class="sxs-lookup"><span data-stu-id="ab6fa-133">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="ab6fa-134">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="ab6fa-134">Description</span></span> | <span data-ttu-id="ab6fa-135">**Kohdistetut ennakot ja pidätykset** -ruudukossa **projektilasku** -sivulla</span><span class="sxs-lookup"><span data-stu-id="ab6fa-135">**Applied Advances and Retainers** grid on the **Project Invoice** page</span></span> |<span data-ttu-id="ab6fa-136">Tässä vain luku -kentässä on tässä laskussa käytetyn maksun tai ennakon kuvaus.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-136">This read-only field provides a description of the retainer or advance used on this invoice.</span></span> <span data-ttu-id="ab6fa-137">Tätä arvoa ei voi muuttaa laskussa.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-137">This value can't be changed on the invoice.</span></span> <span data-ttu-id="ab6fa-138">Tämä arvo voidaan päivittää **projektisopimus** -sivun aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-138">This value can be updated on the subgrid on the **Project Contract** page.</span></span> | <span data-ttu-id="ab6fa-139">Tämä kenttä voidaan näyttää asiakkaalle tulostetussa laskussa, joka ilmaisee, mitä pidätystä tai ennakkoa käytetään laskussa.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-139">This field can be displayed to the customer on the printed invoice to indicate which retainer or advance is applied on the invoice.</span></span> |
| <span data-ttu-id="ab6fa-140">Toimituspäivä</span><span class="sxs-lookup"><span data-stu-id="ab6fa-140">Delivered On</span></span> | <span data-ttu-id="ab6fa-141">**Kohdistetut ennakot ja pidätykset** -ruudukossa **projektilasku** -sivulla</span><span class="sxs-lookup"><span data-stu-id="ab6fa-141">**Applied Advances and Retainers** grid on the **Project Invoice** page</span></span>  | <span data-ttu-id="ab6fa-142">Tässä vain luku -kentässä on tässä laskussa käytetyn pidätyksen tai ennakon laskupäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-142">This read-only field provides the invoice date of the retainer or advance used on this invoice.</span></span> <span data-ttu-id="ab6fa-143">Tätä arvoa ei voi muuttaa laskussa.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-143">This value can't be changed on the invoice.</span></span> <span data-ttu-id="ab6fa-144">Tämä arvo voidaan päivittää **projektisopimus** -sivun aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-144">This value can be updated on the subgrid on the **Project Contract** page.</span></span> | <span data-ttu-id="ab6fa-145">Tämä kenttä voidaan näyttää asiakkaalle painetussa laskussa ilmoittamaan päivämäärä, jolloin pidätys tai ennakko laskutettiin ensimmäisen kerran asiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-145">This field can be displayed to the customer on the printed invoice to indicate the date when the retainer or advance was first invoiced to the customer.</span></span> |
| <span data-ttu-id="ab6fa-146">Summa</span><span class="sxs-lookup"><span data-stu-id="ab6fa-146">Amount</span></span> | <span data-ttu-id="ab6fa-147">**Kohdistetut ennakot ja pidätykset** -ruudukossa **projektilasku** -sivulla</span><span class="sxs-lookup"><span data-stu-id="ab6fa-147">**Applied Advances and Retainers** grid on the **Project Invoice** page</span></span>  | <span data-ttu-id="ab6fa-148">Tässä vain luku -kentässä on tässä laskussa käytetyn pidätyksen tai ennakon määrä.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-148">This read-only field provides the amount of the retainer or advance used on this invoice.</span></span> <span data-ttu-id="ab6fa-149">Tätä arvoa ei voi muuttaa laskussa.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-149">This value can't be changed on the invoice.</span></span> <span data-ttu-id="ab6fa-150">Tämä arvo voidaan päivittää **projektisopimus** -sivun aliruudukossa.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-150">This value can be updated on the subgrid on the **Project Contract** page.</span></span> | <span data-ttu-id="ab6fa-151">Tämä kenttä voidaan näyttää asiakkaalle painetussa laskussa ilmoittamaan pidätyksen tai ennakon alkuperäinen määrä, jonka asiakas maksoi.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-151">This field can be displayed to the customer on the printed invoice to indicate the original amount of retainer or advance that was paid by the customer.</span></span> |
| <span data-ttu-id="ab6fa-152">Käytetty summa</span><span class="sxs-lookup"><span data-stu-id="ab6fa-152">Used Amount</span></span> | <span data-ttu-id="ab6fa-153">**Kohdistetut ennakot ja pidätykset** -ruudukossa **projektilasku** -sivulla</span><span class="sxs-lookup"><span data-stu-id="ab6fa-153">**Applied Advances and Retainers** grid on the **Project Invoice** page</span></span>  | <span data-ttu-id="ab6fa-154">Tässä vain luku -kentässä on laskettu arvo, joka sisältää yhteenvedon siitä, kuinka paljon ennakkomaksua on käytetty.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-154">This read-only field provides the calculated value that summarizes how much of the retainer or advance has been used.</span></span> | <span data-ttu-id="ab6fa-155">Tämä kenttä voidaan näyttää asiakkaalle painetussa laskussa ilmoittamaan pidätyksen tai ennakon määrä, joka on jo käytetty.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-155">This field can be displayed to the customer on the printed invoice to indicate the amount from this retainer or advance that was already used.</span></span> |
| <span data-ttu-id="ab6fa-156">Koko summa</span><span class="sxs-lookup"><span data-stu-id="ab6fa-156">Extended Amount</span></span> | <span data-ttu-id="ab6fa-157">**Kohdistetut ennakot ja pidätykset** -ruudukossa **projektilasku** -sivulla</span><span class="sxs-lookup"><span data-stu-id="ab6fa-157">**Applied Advances and Retainers** grid on the **Project Invoice** page</span></span>  | <span data-ttu-id="ab6fa-158">Tässä muokattavassa kentässä on tässä projektilaskussa käytössä oleva pidätyksen tai ennakon määrä.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-158">This editable field provides the amount of the retainer or advance that is being used on this project invoice.</span></span> <span data-ttu-id="ab6fa-159">Tämä summa ei voi olla suurempi kuin se, joka on käytettävissä etukäteen.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-159">This amount can't be more that what is available on the advance.</span></span> <span data-ttu-id="ab6fa-160">Järjestelmä laskee tämän automaattisesti ruudukon **summa** - ja **käytetty summa** -kenttien erotuksena.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-160">The system automatically calculates this as the difference between the **Amount** and **Used Amount** fields on the grid.</span></span> <span data-ttu-id="ab6fa-161">Voit pienentää tätä määrää, jos haluat käyttää vähemmän kuin mitä on käytettävissä, mutta et voi kasvattaa määrää, joka käyttää enemmän kuin mitä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-161">You can decrease this amount to use less than what is available but you can't increase the amount to use more than what is available.</span></span> | <span data-ttu-id="ab6fa-162">Tämä kenttä voidaan näyttää asiakkaalle painetussa laskussa ilmoittamaan pidätyksen tai ennakon määrä, joka on jo käytössä laskussa.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-162">This field can be displayed to the customer on the printed invoice to indicate the amount from this retainer or advance that being used on the invoice.</span></span> |
| <span data-ttu-id="ab6fa-163">Saldon ennakkomaksusumma.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-163">Balance Retainer Amount.</span></span> | <span data-ttu-id="ab6fa-164">**Kohdistetut ennakot ja pidätykset** -ruudukossa **projektilasku** -sivulla</span><span class="sxs-lookup"><span data-stu-id="ab6fa-164">**Applied Advances and Retainers** grid on the **Project Invoice** page</span></span>  | <span data-ttu-id="ab6fa-165">Tämä vain luku -kenttä sisältää arvon siitä, kuinka paljon maksun pidätystä tai ennakkoa jää laskun vahvistuksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-165">This read-only field provides the value of how much of the retainer or advance will be left after the invoice is confirmed.</span></span> | <span data-ttu-id="ab6fa-166">Tämä kenttä voidaan näyttää asiakkaalle painetussa laskussa ilmoittamaan summa, joka jää jäljelle tästä pidätyksestä tai ennakosta laskun vahvistamisen ja maksamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="ab6fa-166">This field can be displayed to the customer on the printed invoice to indicate the amount that will be left from this retainer or advance after the invoice is confirmed and paid.</span></span> |