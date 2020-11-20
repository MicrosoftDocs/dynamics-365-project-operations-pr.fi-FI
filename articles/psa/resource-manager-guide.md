---
title: Resurssipäällikön opas
description: Resurssienhallintaopas Project Servicessä
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 04ee87e5b1a2cf96434f4862e07d2b85bad9eace
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124004"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="dcfcf-103">Resurssipäällikön opas (Project Service)</span><span class="sxs-lookup"><span data-stu-id="dcfcf-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="dcfcf-104">[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] -ratkaisun [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -toiminnoilla voit etsiä oikeat resurssit oikeaan aikaan tietylle projektille ja varmistaa resurssien tehokkaan käytön.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="dcfcf-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -toimintojen avulla saat yrityksen konsultit tehokkaaseen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="dcfcf-106">Saat käyttöösi työkalut, jotka tarvitset resurssien aikatauluttamiseen konsultointiprojektien edellytyksien ja aikataulujen sekä konsulttien taitojen ja saatavuuden perusteella.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="dcfcf-107">Löydät nopeasti pätevimmät asiantuntijat, jotka voivat työskennellä projekteissa, ja voit helposti nähdä miten ne aikataulutetaan parhaiten kunkin projektin aikana.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="dcfcf-108">Resurssien aikataulutuksen avulla voit tehdä seuraavaa:</span><span class="sxs-lookup"><span data-stu-id="dcfcf-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="dcfcf-109">Täsmäytä resurssit projektien kanssa, sen perusteella kuinka hyvin taidot ja pätevyystasot vastaavat projektin resurssivaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="dcfcf-110">Täsmäytä resurssin aikataulu projektikalenterin kanssa käytettävyyden ja aikataulutetun poissaoloajan perusteella.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="dcfcf-111">Värikoodattu kalenteri antaa graafisia tietoja resurssin käytettävyydestä.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="dcfcf-112">Tarkista kunkin konsultin kapasiteetti ja selvitä, miten kyseinen kapasiteetti on tällä hetkellä käytössä.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="dcfcf-113">Tämä voi auttaa sinua havaitsemaan, onko konsultti ali- tai ylikuormitettu tai onko hänen kapasiteettinsa käytössä.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="dcfcf-114">Määritä prosenttiarvo tai työntekijän kapasiteetti projektia varten tuntimääränä.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="dcfcf-115">Tee ryhmän resurssivaraukset.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="dcfcf-116">Varaa resurssit alustavasti tai sitovasti ja muunna alustavasti varatut tunnit sitovasti varatuiksi tunneiksi yhdessä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="dcfcf-117">Muodosta automaattisesti projektiryhmän työrakenne projektiin määritettyjen resurssien perusteella.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="dcfcf-118">Täytä resurssipyynnöt (varaa, ehdota, etsiä korvaavia resursseja).</span><span class="sxs-lookup"><span data-stu-id="dcfcf-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="dcfcf-119">Delegoi resursseja keskitetyn (resurssipäällikkö delegoi) tai hybridimallin (resurssipäällikkö ja muut päälliköt voivat delegoida).</span><span class="sxs-lookup"><span data-stu-id="dcfcf-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="dcfcf-120">Lisätietoja resurssinhallinnan keskitetystä vs. hybridimallista on kohdassa [Lisäparametrien asetusten määrittäminen (Project Service)](../psa/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="dcfcf-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="dcfcf-121">Voit hallita projektien resursseja tehokkaasti ja varmistaa, että projektit on resursoitu asianmukaisesti.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="dcfcf-122">Sinun on suoritettava seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="dcfcf-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="dcfcf-123">[Hallitse resurssipyyntöjä](../psa/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="dcfcf-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="dcfcf-124">Täsmäytä konsulttien osaamisalueet ja pätevyydet oikeiden projektien kanssa.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="dcfcf-125">[Näytä resurssin saatavuus](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="dcfcf-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="dcfcf-126">Tarkista konsulttien saatavuus Kalenteri-näkymässä.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="dcfcf-127">[Näytä resurssin käytetty aika](../psa/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="dcfcf-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="dcfcf-128">Näet prosenttiosuuden ajasta, jona konsultit ovat tällä hetkellä varattuja.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="dcfcf-129">[Projektin resurssien aikatauluttaminen](../psa/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="dcfcf-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="dcfcf-130">Projektin konsulttien aikatauluttaminen.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="dcfcf-131">Katso lisätietoja yksittäisten projektien resurssipyyntöjen lähettämisestä [Lähetä resurssipyyntöjä](../psa/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="dcfcf-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="dcfcf-132">Katso myös</span><span class="sxs-lookup"><span data-stu-id="dcfcf-132">See Also</span></span>  
 <span data-ttu-id="dcfcf-133">[Project Servicen yleiskuvaus](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="dcfcf-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="dcfcf-134">[Järjestelmänvalvojan opas](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="dcfcf-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="dcfcf-135">[Asiakaspäällikön opas](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="dcfcf-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="dcfcf-136">[Projektipäällikön opas](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="dcfcf-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="dcfcf-137">Aika-, kulu- ja yhteistyöopas</span><span class="sxs-lookup"><span data-stu-id="dcfcf-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
