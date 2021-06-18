---
title: Tarjouksen sulkeminen – lite
description: Tämä aihe tarjoaa tietoja tarjousten sulkemisesta Project Operationsissa.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994132"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="731ab-103">Tarjouksen sulkeminen – lite</span><span class="sxs-lookup"><span data-stu-id="731ab-103">Close a quote - lite</span></span>

<span data-ttu-id="731ab-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="731ab-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="731ab-105">Projektitarjous voidaan sulkea voitettuna tai hävittynä.</span><span class="sxs-lookup"><span data-stu-id="731ab-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="731ab-106">Tarjousluonnos voidaan sulkea, koska Microsoft Dynamics 365 Project Operations ei tue tarjousten Aktivoi- ja Muuta-toimintoja.</span><span class="sxs-lookup"><span data-stu-id="731ab-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="731ab-107">Tarjouksen sulkeminen voitettuna</span><span class="sxs-lookup"><span data-stu-id="731ab-107">Close a quote as Won</span></span>

<span data-ttu-id="731ab-108">Kun suljet projektitarjouksen voitettuna, sen tilaksi tulee Suljettu ja tilan syy on Voitettu.</span><span class="sxs-lookup"><span data-stu-id="731ab-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="731ab-109">Kun suljet tarjouksen, projektitarjous on vain luku -muodossa ja luo tarjoustiedot sisältävän projektisopimusluonnoksen.</span><span class="sxs-lookup"><span data-stu-id="731ab-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="731ab-110">Suljettua tarjousta ei voi avata uudelleen, joten vahvistusikkuna vahvistaa tekemäsi muutokset.</span><span class="sxs-lookup"><span data-stu-id="731ab-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="731ab-111">Jos tarjous liitetään mahdollisuuteen, kaikki muut mahdollisuuteen liittyvät projektitarjoukset suljetaan automaattisesti hävittyinä.</span><span class="sxs-lookup"><span data-stu-id="731ab-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="731ab-112">Taloudellinen vaikutus, kun tarjous suljetaan voitettuna</span><span class="sxs-lookup"><span data-stu-id="731ab-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="731ab-113">Jos projektissa on vielä toteutuneita aikatietoja, jotka on vielä liitetty tarjousluonnokseen, vain ajan tai kulujen kustannukset tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="731ab-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="731ab-114">Kun tarjous on suljettu voitettuna, sovellus määrittää kustannukset uudelleen peruuttaen vanhat toteutuneet kustannukset ja luoden uudelleen uudet toteutuneet kustannukset.</span><span class="sxs-lookup"><span data-stu-id="731ab-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="731ab-115">Sovellus käsittelee nämä toteutuneet kustannukset liitetyn projektisopimusrivin laskutusmenetelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="731ab-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="731ab-116">Jos toteutuneet kustannukset liittyvät ajan ja materiaalin sopimusriviin, vastaavat laskuttamattomat toteutuneet myynnit luodaan, kun tarjous suljetaan ja projektisopimus luodaan.</span><span class="sxs-lookup"><span data-stu-id="731ab-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="731ab-117">Jos toteutuneet kustannukset liittyvät kiinteän hinnan sopimusriviin, sovellus lopettaa sellaisten toteutuneiden kustannusten uudelleenkäsittelyn, jotka perustuvat projektisopimusasiakkaita koskevien jaetun laskutuksen sääntöihin.</span><span class="sxs-lookup"><span data-stu-id="731ab-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="731ab-118">Tarjouksen sulkeminen hävittynä:</span><span class="sxs-lookup"><span data-stu-id="731ab-118">Closing a quote as lost:</span></span>

<span data-ttu-id="731ab-119">Kun suljet projektitarjouksen hävittynä, sen tilaksi tulee Suljettu ja tilan syy on Hävitty.</span><span class="sxs-lookup"><span data-stu-id="731ab-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="731ab-120">Kun tarjous suljetaan, projektitarjous siirtyy vain luku -tilaan.</span><span class="sxs-lookup"><span data-stu-id="731ab-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="731ab-121">Koska suljettua tarjousta ei voi avata uudelleen, ennen kuin suljet tarjouksen, vahvistusikkuna vahvistaa tekemäsi muutokset.</span><span class="sxs-lookup"><span data-stu-id="731ab-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="731ab-122">Jos hävittynä suljettu projektitarjous viittaa projektiin riveillään, myös se projekti merkitään suljetuksi.</span><span class="sxs-lookup"><span data-stu-id="731ab-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="731ab-123">Kaikki kyseisestä päivästä eteenpäin tehdyt varaukset peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="731ab-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="731ab-124">Project Operationsissa tarjouksen sulkeminen voitettuna tai hävittynä ei vaikuta mahdollisuuden tilaan, joka säilyy avoimena, kunnes se suljetaan manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="731ab-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]