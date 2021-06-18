---
title: Raportoinnin kotisivu
description: Tässä aiheessa on tietoja raportoinnista sovelluksessa Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 6c35729e51b7439a74446641af3feace5c7751ac
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998092"
---
# <a name="reporting-home-page"></a><span data-ttu-id="5a1c1-103">Raportoinnin aloitussivu</span><span class="sxs-lookup"><span data-stu-id="5a1c1-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5a1c1-104">Microsoft Dynamics 365 Project Service Automation mahdollistaa projektiperusteisille organisaatioille niiden liiketoimintojen tehokkaan hallinnan.</span><span class="sxs-lookup"><span data-stu-id="5a1c1-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="5a1c1-105">Ryhmän jäsenten on kaikissa projekteissa hallinnnoitava mahdollisuuksia ja tarjouksia sekä suunniteltava työ, resursoitava projektit, hallittava työtä suunnitelman mukaan, laskutettava työstä ja tehtävä työ projektin valmistumiseksi.</span><span class="sxs-lookup"><span data-stu-id="5a1c1-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="5a1c1-106">Kyky raportoida toiminnoista on avainasemassa organisaation terveyden määrittämistä varten ja mahdollisesti tarvittavien korjaavien toimenpiteiden suorittamiseksi.</span><span class="sxs-lookup"><span data-stu-id="5a1c1-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="5a1c1-107">PSA käyttää Microsoft Dynamics 365 -raportointimenetelmää ja -teknologiaa kaikkeen raportointiinsa.</span><span class="sxs-lookup"><span data-stu-id="5a1c1-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="5a1c1-108">Lisätietoja raportointivaihtoehdoista on [Dynamics 365 Customer Engagement (on-premises) -version 9 raportinkirjoitusoppaassa](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="5a1c1-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="5a1c1-109">Ohjattu raportin luominen</span><span class="sxs-lookup"><span data-stu-id="5a1c1-109">Report Wizard</span></span>

<span data-ttu-id="5a1c1-110">Ohjatun raportin luomisen avulla ei-kehittäjät voivat luoda yksinkertaisia raportteja.</span><span class="sxs-lookup"><span data-stu-id="5a1c1-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="5a1c1-111">Koska sovellus on luotu olemassa olevalle alustalle, käyttökokemus on sama kuin oppaassa [Luo tai muokkaa raporttia ohjatun raportointitoiminnon avulla](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard) kuvattu.</span><span class="sxs-lookup"><span data-stu-id="5a1c1-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="5a1c1-112">Siinä käytetään kuitenkin Project Service Automation -kohtaisia entiteettejä.</span><span class="sxs-lookup"><span data-stu-id="5a1c1-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="5a1c1-113">Mukautetut SQL Server Reporting Services -raportit</span><span class="sxs-lookup"><span data-stu-id="5a1c1-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="5a1c1-114">Jos yrityksesi edellyttää tiettyä raporttia, jota ei voi luoda ohjatulla raportinluontitoiminnolla, voit luoda mukautetun raportin.</span><span class="sxs-lookup"><span data-stu-id="5a1c1-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="5a1c1-115">Microsoft Visual Studio on oltava asennettuna, samoin kuin soveltuvat Microsoft SQL Server Data Tools ja Report Authoring Extensions.</span><span class="sxs-lookup"><span data-stu-id="5a1c1-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="5a1c1-116">Lisätietoja työkaluista ja versioista on aiheessa [Raporttien kirjoitusympäristö työkalua SQL Server Data Tools käyttäen](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="5a1c1-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="5a1c1-117">Lisätietoja mukautetun raportin luomisesta on aiheessa [Uuden raportin luominen työkalua SQL Server Data Tools käyttäen](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools)</span><span class="sxs-lookup"><span data-stu-id="5a1c1-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="5a1c1-118">Power BI Insights -sovellukset</span><span class="sxs-lookup"><span data-stu-id="5a1c1-118">Power BI insights apps</span></span>

<span data-ttu-id="5a1c1-119">Yhdessä Microsoft Power BI ja Dynamics 365 antavat sinulle tehokkaan tavan käsitellä tietojasi Insights-sovellusten muodossa.</span><span class="sxs-lookup"><span data-stu-id="5a1c1-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="5a1c1-120">Tietoja Insights-sovellusten saatavuudesta on [Power BI Insights -sovellussivulla.](https://powerbi.microsoft.com/power-bi-insights-apps/)</span><span class="sxs-lookup"><span data-stu-id="5a1c1-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="5a1c1-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5a1c1-121">Additional resources</span></span>
<span data-ttu-id="5a1c1-122">Katso lisätietoja raportoinnista PSA:ssa seuraavista aiheista:</span><span class="sxs-lookup"><span data-stu-id="5a1c1-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="5a1c1-123">Project Service -tietomallin käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="5a1c1-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="5a1c1-124">Koontinäytöt</span><span class="sxs-lookup"><span data-stu-id="5a1c1-124">Dashboards</span></span>](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]