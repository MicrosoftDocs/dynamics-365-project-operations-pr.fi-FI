---
title: Tarjouksen sulkeminen
description: Tämä aihe tarjoaa tietoja tarjousten sulkemisesta Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c429fa14b4b95420c67a91a6a59af7db2660f68
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075246"
---
# <a name="close-a-quote"></a><span data-ttu-id="a6367-103">Tarjouksen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="a6367-103">Close a quote</span></span>

<span data-ttu-id="a6367-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="a6367-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a6367-105">Projektitarjous voidaan sulkea voitettuna tai hävittynä.</span><span class="sxs-lookup"><span data-stu-id="a6367-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="a6367-106">Koska tarjousten Aktivoi- ja Tarkista-toimintoja ei tueta Microsoft Dynamics 365 Project Operationsissa, voit sulkea tarjousluonnoksen.</span><span class="sxs-lookup"><span data-stu-id="a6367-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="a6367-107">Tarjouksen sulkeminen voitettuna</span><span class="sxs-lookup"><span data-stu-id="a6367-107">Close a quote as Won</span></span>

<span data-ttu-id="a6367-108">Projektitarjouksen sulkeminen voitettuna sulkee määrittää tilaksi **Suljettu** ja tilan syyksi **Voitettu**.</span><span class="sxs-lookup"><span data-stu-id="a6367-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="a6367-109">Kun suljet tarjouksen, projektitarjous on vain luku -muodossa ja luo kaikki tarjoustiedot sisältävän projektisopimusluonnoksen.</span><span class="sxs-lookup"><span data-stu-id="a6367-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="a6367-110">Koska suljettua tarjousta ei voi avata uudelleen, ennen kuin suljet tarjouksen, vahvistusikkuna vahvistaa tekemäsi muutokset.</span><span class="sxs-lookup"><span data-stu-id="a6367-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="a6367-111">Projektitarjouksesta luotu projektisopimus on myös käytettävissä Project Operationsin Projektinhallinta ja kirjanpito -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="a6367-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="a6367-112">Jos projektisopimusta ei ole yhdistetty projektiin millään sen rivillä, tämä projektisopimus on käytettävissä passiivisena projektisopimuksena, ja se aktivoituu heti, kun projekti on yhdistetty vähintään yhteen sen sopimusriveistä.</span><span class="sxs-lookup"><span data-stu-id="a6367-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="a6367-113">Jos tarjous liitetään mahdollisuuteen, kaikki muut mahdollisuuteen liittyvät projektitarjoukset suljetaan automaattisesti hävittyinä.</span><span class="sxs-lookup"><span data-stu-id="a6367-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="a6367-114">Taloudellinen vaikutus, kun tarjous suljetaan voitettuna</span><span class="sxs-lookup"><span data-stu-id="a6367-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="a6367-115">Jos projektiin on tallennettu ajan toteutuneita arvoja, kun se on vielä liitetty tarjousluonnokseen, vain ajan tai kulun kustannukset tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="a6367-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="a6367-116">Kun tarjous on suljettu voitettuna, sovellus määrittää kustannukset uudelleen peruuttaen vanhat toteutuneet kustannukset ja luoden uudelleen uudet toteutuneet kustannukset.</span><span class="sxs-lookup"><span data-stu-id="a6367-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="a6367-117">Sovellus käsittelee nämä toteutuneet kustannukset liitetyn projektisopimusrivin laskutusmenetelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="a6367-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="a6367-118">Jos toteutuneet kustannukset viittaavat aika- ja materiaalisopimusriviin, järjestelmä luo automaattisesti vastaavat laskuttamattomat myynnin toteutuneet arvot, kun tarjous suljetaan ja projektisopimus luodaan.</span><span class="sxs-lookup"><span data-stu-id="a6367-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="a6367-119">Jos kustannusten todelliset tiedot viittaavat kiinteähintaiseen sopimusriviin, sovellus lopettaa kustannusten uudelleenkäsittelyn projektisopimusasiakkaiden laskutuksen jakamisen sääntöjen perusteella.</span><span class="sxs-lookup"><span data-stu-id="a6367-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="a6367-120">Kaikki uudelleenkäsitellyt todelliset arvot ovat käytettävissä Projektinhallinta ja kirjanpito -moduulissa, jotta projektin kirjanpitäjä voi tarkastella, päivittää ja kirjata kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="a6367-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="a6367-121">Tarjouksen sulkeminen hävittynä</span><span class="sxs-lookup"><span data-stu-id="a6367-121">Close a quote as Lost</span></span>

<span data-ttu-id="a6367-122">Jos projektitarjous suljetaan hävittynä, tilaksi tulee **Suljettu** ja tilan syyksi **Hävitty**.</span><span class="sxs-lookup"><span data-stu-id="a6367-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="a6367-123">Kun tarjous suljetaan, se on vain luku -tilassa.</span><span class="sxs-lookup"><span data-stu-id="a6367-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="a6367-124">Koska suljettua tarjousta ei voi avata uudelleen, ennen kuin suljet tarjouksen, vahvistusikkuna vahvistaa tekemäsi muutokset.</span><span class="sxs-lookup"><span data-stu-id="a6367-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="a6367-125">Jos hävittynä suljetulla projektitarjouksella on projekti, johon on viitattu jossakin tarjouksen riveillä, projekti merkitään myös suljetuiksi ja kaikki kyseisestä päivästä eteenpäin tehdyt resurssivaraukset peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="a6367-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="a6367-126">Project Operationsissa tarjouksen sulkeminen voitettuna tai hävittynä ei vaikuta mahdollisuuden tilaan, joka säilyy avoimena, kunnes se suljetaan manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="a6367-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
