---
title: Projektin palvelusopimuksen vahvistaminen
description: Tämä aihe tarjoaa tietoja sopimuksen vahvistamisesta Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128279"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="ff5d3-103">Projektin palvelusopimuksen vahvistaminen</span><span class="sxs-lookup"><span data-stu-id="ff5d3-103">Confirm a project contract</span></span>

<span data-ttu-id="ff5d3-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="ff5d3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ff5d3-105">Dynamics 365 Project Operationsin projektisopimus voi olla aktiivinen ja sen syy on **vahvistettu** tai suljettu syyllä **Hävitty**.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="ff5d3-106">Kun vahvistat projektisopimuksen, tila päivittyy **luonnoksesta** **aktiiviseksi** ja tilan syy **vahvistetaan**.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="ff5d3-107">Aktiivista tai suljettua palvelusopimusta ei voi muokata eikä avata uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="ff5d3-108">Projektisopimuksen vahvistamisen taloudellinen vaikutus</span><span class="sxs-lookup"><span data-stu-id="ff5d3-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="ff5d3-109">Kun projektisopimus on vahvistettu, sovellus laskee kustannukset uudelleen peruuttaen vanhat toteutuneet kustannukset ja luoden uudelleen uudet toteutuneet kustannukset.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="ff5d3-110">Uudet kustannuslaskelmat käsitellään sitten liittyvän projektisopimusrivin laskutustavan perusteella.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="ff5d3-111">Jos todelliset kustannukset viittaavat aika- ja materiaalisopimusriviin, sovellus luo automaattisesti uudelleen vastaavat laskuttamattomat toteutuneet myynnit.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="ff5d3-112">Jos kustannusten todelliset tiedot viittaavat kiinteään hintasopimusriviin, sovellus lopettaa kustannusten uudelleenkäsittelyn.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="ff5d3-113">Arvot, joita ei voida ylittää, sekä toteutuneiden hintojen ja kustannuslaskennan arvot arvioidaan ja päivitetään sitten osana vahvistuksia.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="ff5d3-114">Palvelusopimuksen sulkeminen hävittynä</span><span class="sxs-lookup"><span data-stu-id="ff5d3-114">Close a project contract as lost</span></span>

<span data-ttu-id="ff5d3-115">Kun suljet projektisopimuksen hävittynä, palvelusopimuksen tilaksi päivittyy **Suljettu** ja tilan syyksi **Hävitty**.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="ff5d3-116">Projektisopimus muuttuu vain luku -tilaan.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-116">The project contract becomes read-only.</span></span> <span data-ttu-id="ff5d3-117">Vahvistusikkuna on käytettävissä, ennen kuin muutokset ovat valmiina, koska suljettua projektisopimusta ei voi avata uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="ff5d3-118">Jos menetetty projektisopimus viittaa sen riveillä olevaan projektiin, kyseinen projekti merkitään myös suljetuksi.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="ff5d3-119">Kaikki kyseisestä päivästä eteenpäin tehdyt varaukset peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="ff5d3-120">Kaikki projektisopimuksen laskuttamattomat myynnin todelliset arvot, joita ei vielä ole laskussa, peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="ff5d3-121">Dynamics 365 Project Operationsissa projektisopimuksen sulkeminen hävittynä ei vaikuta liittyvän mahdollisuuden tilaan.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="ff5d3-122">Mahdollisuus säilyy avoimena, ja se täytyy sulkea manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="ff5d3-122">The opportunity will remain open and must be manually closed.</span></span>
