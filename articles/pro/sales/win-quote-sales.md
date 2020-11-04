---
title: Tarjouksien sulkeminen
description: Tämä aihe tarjoaa tietoja tarjousten sulkemisesta Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075269"
---
# <a name="close-quotes"></a><span data-ttu-id="7553f-103">Tarjouksien sulkeminen</span><span class="sxs-lookup"><span data-stu-id="7553f-103">Close quotes</span></span> 

<span data-ttu-id="7553f-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="7553f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7553f-105">Projektitarjous voidaan sulkea voitettuna tai hävittynä.</span><span class="sxs-lookup"><span data-stu-id="7553f-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="7553f-106">Tarjousten Aktivoi- ja Tarkista-toimintoja ei tueta Microsoft Dynamics 365 Project Operationsissa, joten tarjousluonnos voidaan sulkea.</span><span class="sxs-lookup"><span data-stu-id="7553f-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="7553f-107">Tarjouksen sulkeminen voitettuna</span><span class="sxs-lookup"><span data-stu-id="7553f-107">Close a quote as Won</span></span>

<span data-ttu-id="7553f-108">Projektitarjouksen sulkeminen voitettuna sulkee tarjouksen määrittäen tilaksi Suljettu ja tilan syyksi Voitettu.</span><span class="sxs-lookup"><span data-stu-id="7553f-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="7553f-109">Kun suljet tarjouksen, projektitarjous on vain luku -muodossa ja luo tarjoustiedot sisältävän projektisopimusluonnoksen.</span><span class="sxs-lookup"><span data-stu-id="7553f-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="7553f-110">Koska suljettua tarjousta ei voi avata uudelleen, näkyviin tulee vahvistusikkuna ennen muutosten tekemistä – muutokset ovat peruuttamattomia.</span><span class="sxs-lookup"><span data-stu-id="7553f-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="7553f-111">Jos tarjous liitetään mahdollisuuteen, kaikki muut mahdollisuuteen liittyvät projektitarjoukset suljetaan automaattisesti hävittyinä.</span><span class="sxs-lookup"><span data-stu-id="7553f-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="7553f-112">Taloudellinen vaikutus, kun tarjous suljetaan voitettuna</span><span class="sxs-lookup"><span data-stu-id="7553f-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="7553f-113">Jos projektiin on tallennettu ajan toteutuneita arvoja, kun se on vielä liitetty tarjousluonnokseen, vain ajan tai kulun kustannukset tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="7553f-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="7553f-114">Kun tarjous on suljettu voitettuna, sovellus määrittää kustannukset uudelleen peruuttaen vanhat toteutuneet kustannukset ja luoden uudelleen uudet toteutuneet kustannukset.</span><span class="sxs-lookup"><span data-stu-id="7553f-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="7553f-115">Sovellus käsittelee nämä toteutuneet kustannukset liitetyn projektisopimusrivin laskutusmenetelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="7553f-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="7553f-116">Jos toteutuneet kustannukset viittaavat aika- ja materiaalisopimusriviin, järjestelmä luo automaattisesti vastaavat laskuttamattomat myynnin toteutuneet arvot, kun tarjous suljetaan ja projektisopimus luodaan.</span><span class="sxs-lookup"><span data-stu-id="7553f-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="7553f-117">Jos kustannusten todelliset tiedot viittaavat kiinteähintaiseen sopimusriviin, sovellus lopettaa kustannusten uudelleenkäsittelyn projektisopimusasiakkaiden laskutuksen jakamisen sääntöjen perusteella.</span><span class="sxs-lookup"><span data-stu-id="7553f-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="7553f-118">Tarjouksen sulkeminen hävittynä:</span><span class="sxs-lookup"><span data-stu-id="7553f-118">Closing a quote as lost:</span></span>

<span data-ttu-id="7553f-119">Jos projektitarjous suljetaan hävittynä, tilaksi tulee Suljettu ja tilan syyksi Hävitty.</span><span class="sxs-lookup"><span data-stu-id="7553f-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="7553f-120">Kun tarjous suljetaan, projektitarjous siirtyy vain luku -tilaan.</span><span class="sxs-lookup"><span data-stu-id="7553f-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="7553f-121">Koska suljettua tarjousta ei voi avata uudelleen, ennen kuin suljet tarjouksen, vahvistusikkuna vahvistaa tekemäsi muutokset.</span><span class="sxs-lookup"><span data-stu-id="7553f-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="7553f-122">Jos hävittynä suljetulla projektitarjouksella on projekti, johon on viitattu jossakin tarjouksen riveillä, projekti merkitään myös suljetuiksi ja kaikki kyseisestä päivästä eteenpäin tehdyt resurssivaraukset peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="7553f-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="7553f-123">Project Operationsissa tarjouksen sulkeminen voitettuna tai hävittynä ei vaikuta mahdollisuuden tilaan, joka säilyy avoimena, kunnes se suljetaan manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="7553f-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
