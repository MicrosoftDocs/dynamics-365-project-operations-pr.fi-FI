---
title: Myyntiprosessit
description: Tämä aihe sisältää tietoja perustason myyntiprosesseista.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 38e02018e46943f53680babd12c7bede0a5d19de
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129314"
---
# <a name="sales-processes"></a><span data-ttu-id="d004f-103">Myyntiprosessit</span><span class="sxs-lookup"><span data-stu-id="d004f-103">Sales processes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d004f-104">Projektiperusteisessa organisaatiossa käytettävät myyntiprosessit eroavat tuoteperusteisessa organisaatiossa käytettävistä myyntiprosesseista.</span><span class="sxs-lookup"><span data-stu-id="d004f-104">The sales processes that are used in a project-based organization differ from the sales processes that are used in a product-based organization.</span></span> <span data-ttu-id="d004f-105">Tämä ero johtuu siitä, että projektiperusteisten organisaatioiden myyntisyklit ovat pidempiä ja edellyttävät mukautettuja arviointimenetelmiä tarjousten analysoimiseksi ja luomiseksi kullekin kaupalle.</span><span class="sxs-lookup"><span data-stu-id="d004f-105">This difference occurs because the sales cycles for project-based organizations are longer and require customized estimation techniques to analyze and create quotes for each deal.</span></span> <span data-ttu-id="d004f-106">Dynamics 365 Project Service Automationissa käytetään joitakin samoja toimintoja kuin Dynamics 365 Salesin myyntiprosesseissa.</span><span class="sxs-lookup"><span data-stu-id="d004f-106">Dynamics 365 Project Service Automation uses some of the same functionality that is used in the sales process for Dynamics 365 Sales.</span></span> <span data-ttu-id="d004f-107">Seuraavassa on joitakin esimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="d004f-107">Here are some examples:</span></span>

- <span data-ttu-id="d004f-108">Myyntiprosessin seurantaan käytetään Liidi-entiteettiä.</span><span class="sxs-lookup"><span data-stu-id="d004f-108">A Lead entity is used to track the sales process.</span></span>
- <span data-ttu-id="d004f-109">Hyväksyttyjä liidejä seurataan mahdollisuuksina.</span><span class="sxs-lookup"><span data-stu-id="d004f-109">Qualifying leads are tracked as opportunities.</span></span> <span data-ttu-id="d004f-110">Myyntiprosessi voi alkaa myös mahdollisuudesta.</span><span class="sxs-lookup"><span data-stu-id="d004f-110">The sales process can also start with opportunity.</span></span>
- <span data-ttu-id="d004f-111">Kaikkia mahdollisuuteen liittyviä artefakteja käytetään.</span><span class="sxs-lookup"><span data-stu-id="d004f-111">All related artifacts for an opportunity are accessed.</span></span> <span data-ttu-id="d004f-112">Näitä artefakteja ovat esimerkiksi myyntiryhmä, sidosryhmät, todennäköisyys, luokitus, myyntivaiheet ja liiketoimintaprosessit.</span><span class="sxs-lookup"><span data-stu-id="d004f-112">These artifacts include the sales team, stakeholders, probability, rating, sales stages, and business processes.</span></span>
- <span data-ttu-id="d004f-113">Mahdollisuudelle luodaan useita tarjouksia.</span><span class="sxs-lookup"><span data-stu-id="d004f-113">Multiple quotes are created for an opportunity.</span></span>
- <span data-ttu-id="d004f-114">Myyntitilaus luodaan asettamalla tarjouksen tilaksi **Suljettu voitettuna**.</span><span class="sxs-lookup"><span data-stu-id="d004f-114">A quote is marked **Closed as Won** to create a sales order.</span></span> <span data-ttu-id="d004f-115">PSA:ssa myyntitarjous on muokattu, ja sitä kutsutaan projektisopimukseksi.</span><span class="sxs-lookup"><span data-stu-id="d004f-115">In PSA, the sales order is customized and is called a project contract.</span></span>

<span data-ttu-id="d004f-116">Seuraavassa kuvassa näkyy projektiperusteisen organisaation tyypillinen myyntiprosessi.</span><span class="sxs-lookup"><span data-stu-id="d004f-116">The following illustration shows a typical sales process in a project-based organization.</span></span>

> ![Myyntiprosessi projektiperusteisessa organisaatiossa](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a><span data-ttu-id="d004f-118">Myynnin arviointi</span><span class="sxs-lookup"><span data-stu-id="d004f-118">Estimating a sale</span></span>
<span data-ttu-id="d004f-119">Myynnin arvo voidaan arvioida aiemmin toimitettujen projektien ja projektin monimutkaisuuden perusteella.</span><span class="sxs-lookup"><span data-stu-id="d004f-119">The value of a sale can be estimated based on projects that have previously been delivered and the complexity of projects.</span></span> <span data-ttu-id="d004f-120">Jos projektiin liittyy laajennuksia aiempaan projektiin tai projektin toimittajan asiantuntemus on korkeatasoista ja siinä käytetään tuttuja työmalleja, voidaan käyttää yksinkertaisempaa arviointiprosessia.</span><span class="sxs-lookup"><span data-stu-id="d004f-120">For projects that involve extensions to previous projects, or projects where the vendor's expertise is high and well-known work templates are used, you can use a simpler estimation process.</span></span> <span data-ttu-id="d004f-121">Monimutkaisissa projekteissa ostoprosessi on yleensä pidempi.</span><span class="sxs-lookup"><span data-stu-id="d004f-121">More complex projects usually have a longer purchase process.</span></span> <span data-ttu-id="d004f-122">Siksi myös myynninarviointiprosessissa on enemmän vaiheita.</span><span class="sxs-lookup"><span data-stu-id="d004f-122">Therefore, there are more stages in the sales estimation process.</span></span> <span data-ttu-id="d004f-123">Projektin alussa myyntiryhmä käyttää asiakkuuspäällikköjen ja aihealueen asiantuntijoiden panosta päästäkseen alkuun ylätason arvioinnin luomisessa kullekin erilliselle tarjoukseen sisältyvälle työkomponentille.</span><span class="sxs-lookup"><span data-stu-id="d004f-123">Early in the process, the sales team uses the input of account managers and subject matter experts (SMEs) to start to create a high-level estimate for each distinct component of work that is quoted.</span></span> <span data-ttu-id="d004f-124">Tarjousrivit edustavat näitä työkomponentteja.</span><span class="sxs-lookup"><span data-stu-id="d004f-124">These components of work are represented by quote lines.</span></span> 

<span data-ttu-id="d004f-125">Vuot luoda tarjoukselle ylätason arvioinnin.</span><span class="sxs-lookup"><span data-stu-id="d004f-125">You can create a high-level estimate of the quote.</span></span> <span data-ttu-id="d004f-126">Tämä ylätason arviointi korvataan myöhemmin yksityiskohtaisemmalla arvioinnilla, joka perustuu vakioitujen projektimallien avulla luotavaan projektisuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="d004f-126">Eventually, this high-level estimate will be replaced by a more detailed estimate that is based on a project plan that you create by using the standardized project templates.</span></span> <span data-ttu-id="d004f-127">Näiden mallien avulla voit laatia aikataulun ja määrittää rahallisia arvoja tarjoukselle ja sen komponenteille (tarjousriveille).</span><span class="sxs-lookup"><span data-stu-id="d004f-127">These templates help you build a schedule and determine monetary values on the quote and its components (quote lines).</span></span> 

<span data-ttu-id="d004f-128">Voit luoda projektille useita tarjouksia ja koota ne yksittäisen mahdollisuusentiteettityypin alle.</span><span class="sxs-lookup"><span data-stu-id="d004f-128">You can create multiple quotes for a project and group them under a single opportunity entity type.</span></span> <span data-ttu-id="d004f-129">Lopulta jokin näistä tarjouksista asetetaan tilaan **Suljettu voitettuna** ja projektisopimus tai työnkuvaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="d004f-129">Eventually, one of those quotes is marked **Closed as Won**, and a project contract or statement of work (SOW) is created.</span></span> <span data-ttu-id="d004f-130">Projektisopimus sisältää sovitun arvon kullekin komponentille (sopimusrivi), jonka asiakas hyväksyy toimitettavaksi.</span><span class="sxs-lookup"><span data-stu-id="d004f-130">A project contract holds the contracted value for each component (contract line) that is accepted by the customer for delivery.</span></span> <span data-ttu-id="d004f-131">Työnkuvaus luodaan yleensä Microsoft Word -asiakirjana.</span><span class="sxs-lookup"><span data-stu-id="d004f-131">An SOW is usually created as a Microsoft Word document.</span></span> <span data-ttu-id="d004f-132">Kaikki asiakkaalle projektin toimittamisen aikana lähetettävät laskut viittaavat projektisopimukseen tai työnkuvaukseen.</span><span class="sxs-lookup"><span data-stu-id="d004f-132">All invoices that are sent to the customer over the course of the project's delivery reference the project contract or SOW.</span></span>

<span data-ttu-id="d004f-133">Voit myös luoda vaihtoehtoisia tarjouksia yhden mahdollisuusentiteettityypin alle tai määrittää järjestelmän siten, että projektisopimus luodaan, kun tarjous voitetaan.</span><span class="sxs-lookup"><span data-stu-id="d004f-133">You can also create alternate quotes under one opportunity entity type or set up the system so that a project contract is created when a quote is won.</span></span> <span data-ttu-id="d004f-134">Tällöin voit liittää projektisopimuksen tietueeseen Word-asiakirjan, joka edustaa työnkuvausta.</span><span class="sxs-lookup"><span data-stu-id="d004f-134">In this case, you can attach a Word document that represents the SOW to the project contract record.</span></span>

![Tarjouksen sulkeminen projektisopimuksen luomista varten](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a><span data-ttu-id="d004f-136">Myyntiprosessin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d004f-136">Configuring the sales process</span></span>
<span data-ttu-id="d004f-137">Voit määrittää myyntiprosessisi käyttämällä Microsoft Dynamics 365:n liiketoimintaprosesseja.</span><span class="sxs-lookup"><span data-stu-id="d004f-137">You can use business process flows (BPFs) in Microsoft Dynamics 365 to configure your sales process.</span></span> <span data-ttu-id="d004f-138">Liiketoimintaprosessit tarjoavat myyntihenkilöstölle opastetun visuaalisen liittymän, jota se voi käyttää siirtääkseen kauppoja yrityksellesi tyypillisten vaiheiden läpi.</span><span class="sxs-lookup"><span data-stu-id="d004f-138">BPFs give your sales staff a guided visual interface that they can use to move deals forward through the stages that are typical for your company.</span></span>

<span data-ttu-id="d004f-139">Yrityksen myyntiprosessissa voi olla esimerkiksi seuraavat kuusi vaihetta:</span><span class="sxs-lookup"><span data-stu-id="d004f-139">For example, your company might have the following six stages in the sales process:</span></span>

1. <span data-ttu-id="d004f-140">Hyväksy</span><span class="sxs-lookup"><span data-stu-id="d004f-140">Qualify</span></span>
2. <span data-ttu-id="d004f-141">Arvio</span><span class="sxs-lookup"><span data-stu-id="d004f-141">Estimate</span></span>
3. <span data-ttu-id="d004f-142">Sisäinen arviointi</span><span class="sxs-lookup"><span data-stu-id="d004f-142">Internal review</span></span>
4. <span data-ttu-id="d004f-143">Palvelusopimus</span><span class="sxs-lookup"><span data-stu-id="d004f-143">Contract</span></span>
5. <span data-ttu-id="d004f-144">Toimita</span><span class="sxs-lookup"><span data-stu-id="d004f-144">Deliver</span></span>
6. <span data-ttu-id="d004f-145">Sulje</span><span class="sxs-lookup"><span data-stu-id="d004f-145">Close</span></span>

<span data-ttu-id="d004f-146">Nuolenkärkipainikkeet (\>), jotka valitaan laajennettavaksi kussakin luotavassa mahdollisuusentiteettityypissä, edustavat näitä kuutta vaihetta.</span><span class="sxs-lookup"><span data-stu-id="d004f-146">These six stages are represented by chevrons (\>) that you select to expand in each opportunity entity type that you create.</span></span>

![Liiketoimintaprosessien määritys Dynamics 365:ssä](media/basic-guide-3.png)
 
<span data-ttu-id="d004f-148">Organisaatiossasi saatetaan käyttää eri entiteettejä edustamaan samaa kauppaa sen muuttuessa.</span><span class="sxs-lookup"><span data-stu-id="d004f-148">Your organization might use different entities to represent the same deal as it evolves.</span></span> <span data-ttu-id="d004f-149">Aikaisin myyntiprosessissa kauppaa edustaa Mahdollisuus-entiteetti.</span><span class="sxs-lookup"><span data-stu-id="d004f-149">Early in the sales process, a deal is represented by the Opportunity entity.</span></span> <span data-ttu-id="d004f-150">Ajan myötä ja kaupan tarkentuessa saatetaan käyttää ylätason arvioita yhden tai useamman tarjouksen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="d004f-150">As time passes and more details emerge, you might use high-level estimates to create one or more quotes.</span></span> <span data-ttu-id="d004f-151">Jos sisäiset ja asiakkaan sidosryhmät tarkistavat yhden näistä tarjouksista, kauppaa edustaa Tarjous-entiteetti.</span><span class="sxs-lookup"><span data-stu-id="d004f-151">If one of these quotes is reviewed by internal and customer stakeholders, the Quote entity represents the deal.</span></span> <span data-ttu-id="d004f-152">Kun asiakas on hyväksynyt tarjouksen, kauppaa edustaa projektisopimus tai työnkuvaus.</span><span class="sxs-lookup"><span data-stu-id="d004f-152">After the customer accepts the quote, a project contract or SOW represents the deal.</span></span> <span data-ttu-id="d004f-153">Näiden toimintojen tukemiseksi jokainen prosessin vaihe on liiketoimintaprosessien rakenteessa linkitetty eri tietokantataulukkoon.</span><span class="sxs-lookup"><span data-stu-id="d004f-153">To support this behavior, BPFs are structured so that each stage in the process is linked to a different database table.</span></span>

<span data-ttu-id="d004f-154">Myyntiprosessin **Hyväksy**-vaihetta voidaan tukea Mahdollisuus-entiteetillä.</span><span class="sxs-lookup"><span data-stu-id="d004f-154">The **Qualify** stage in the sales process can be backed by an Opportunity entity.</span></span> <span data-ttu-id="d004f-155">Vaiheita **Arvio** ja **Sisäinen arviointi** voidaan tukea Tarjous-entiteetillä.</span><span class="sxs-lookup"><span data-stu-id="d004f-155">The **Estimate** and **Internal Review** stages can be backed by a Quote entity.</span></span> <span data-ttu-id="d004f-156">Vaiheita **Sopimus**, **Toimitus** ja **Sulkeminen** voidaan tukea Projektisopimus-entiteetillä.</span><span class="sxs-lookup"><span data-stu-id="d004f-156">The **Contract**, **Delivery**, and **Close** stages can be backed by a Project Contract entity.</span></span>

<span data-ttu-id="d004f-157">Kun siirrät kauppoja vaiheiden läpi, järjestelmä pyytää sinua luomaan asianmukaisen entiteettitietueen auttamaan ja opastamaan sinua prosessissa.</span><span class="sxs-lookup"><span data-stu-id="d004f-157">As you move deals through the stages, you're prompted to create the appropriate entity record to help and guide you through the process.</span></span> <span data-ttu-id="d004f-158">Vaiheet voivat olla ehdollisia.</span><span class="sxs-lookup"><span data-stu-id="d004f-158">The stages can be conditional.</span></span> <span data-ttu-id="d004f-159">Jos esimerkiksi tarvitset tarjoukselle sisäisen arvioinnin vain, kun tarjouksessa käytetään mukautettua hinnastoa, voit määrittää kyseisen ehdon vastaavassa liiketoimintaprosessin vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="d004f-159">For example, if you require an internal review of a quote only if the quote uses a custom price list, you can configure that condition in the appropriate stage of the business process.</span></span> <span data-ttu-id="d004f-160">**Sisäinen arviointi** -vaihe näkyy tällöin vain sellaisten tarjousten osalta, joissa käytetään mukautettua hinnastoa.</span><span class="sxs-lookup"><span data-stu-id="d004f-160">The **Internal Review** stage is then shown only for quotes that use a custom price list.</span></span> <span data-ttu-id="d004f-161">Kaikissa muissa kaupoissa ja tarjouksissa **Arvio** -vaihetta seuraa **Sopimus**-vaihe.</span><span class="sxs-lookup"><span data-stu-id="d004f-161">For all other deals and quotes, the **Estimate** stage is followed by the **Contract** stage.</span></span>

> [!NOTE]
> <span data-ttu-id="d004f-162">PSA:ssa on omat sivunsa entiteeteille Mahdollisuus, Tarjous, Tilaus ja Lasku.</span><span class="sxs-lookup"><span data-stu-id="d004f-162">PSA has specific pages for the Opportunity, Quote, Order, and Invoice entities.</span></span> <span data-ttu-id="d004f-163">Sinun on luotava projektipalvelun mahdollisuuksia, tarjouksia, tilauksia ja laskuja käyttämällä näiden entiteettien projektitietosivuja.</span><span class="sxs-lookup"><span data-stu-id="d004f-163">You must create project service opportunities, quotes, orders, and invoices using the project information pages for these entities.</span></span> <span data-ttu-id="d004f-164">Jos käytät tietueen luonnissa muuta sivua, et voi avata tietuetta **Projektitiedot**-sivun kautta.</span><span class="sxs-lookup"><span data-stu-id="d004f-164">If you use another page to create a record, you won't be able to open the record from the **Project Information** page.</span></span> <span data-ttu-id="d004f-165">Jos haluat avata tietueen **Projektitiedot**-sivulta, sinun on poistettava tietue ja luotava se uudelleen käyttäen **Projektitiedot**-sivua.</span><span class="sxs-lookup"><span data-stu-id="d004f-165">If you want to open a record from the **Project Information** page, you must delete the record and recreate it using the **Project Information** page.</span></span> <span data-ttu-id="d004f-166">**Projektitiedot**-sivulla näiden entiteettityyppien liiketoimintalogiikat varmistavat, että tietueen **Tyyppi**-kenttä määritetään oikein ja että kaikki pakolliset konseptit alustetaan asianmukaisesti.</span><span class="sxs-lookup"><span data-stu-id="d004f-166">On the **Project Information** page, business logic for each of these entity types ensures that the **Type** field of the record is set correctly, and all of the mandatory concepts are properly initialized.</span></span>

> ![Uuden tilauksen projektitiedot](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a><span data-ttu-id="d004f-168">Erot Project Service Automationin ja Salesin välillä</span><span class="sxs-lookup"><span data-stu-id="d004f-168">Differences between Project Service Automation and Sales</span></span>
<span data-ttu-id="d004f-169">Vaikka PSA:n myyntiprosessissa käytetään Salesin myyntiprosessin perusominaisuuksia, niiden välillä on keskeisiä eroja projektiperusteisten organisaatioiden liiketoimintakäytännöissä esiintyvien vaihteluiden vuoksi.</span><span class="sxs-lookup"><span data-stu-id="d004f-169">Although the sales process in PSA uses the basic capabilities of the sales process in Sales, it does have some key differences because of variations in the business practices of project-based organizations.</span></span> <span data-ttu-id="d004f-170">Seuraavassa on joitakin esimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="d004f-170">Here are some examples:</span></span>

- <span data-ttu-id="d004f-171">**Projektitarjoukset** – Project Service Automationissa tarjous suljetaan, kun tarjouksesta on luotu projektisopimus.</span><span class="sxs-lookup"><span data-stu-id="d004f-171">**Project quotes** – In Project Service Automation, a quote is closed after a project contract is created from a quote.</span></span> <span data-ttu-id="d004f-172">Salesissa tarjous voidaan pitää avoimena, kun se on voitettu.</span><span class="sxs-lookup"><span data-stu-id="d004f-172">In Sales, you can keep a quote open after you've won it.</span></span> <span data-ttu-id="d004f-173">Syynä tähän eroon, että tarjouksen ja projektisopimuksen vastaavuus sopii paremmin projektiperusteiselle organisaatiolle.</span><span class="sxs-lookup"><span data-stu-id="d004f-173">The reason for this difference is that a match between a quote and a project contract is better for project-based organizations.</span></span> 
- <span data-ttu-id="d004f-174">**Aktivoinnit ja muutokset** – PSA ei tue projektitarjousten aktivointeja ja muutoksia.</span><span class="sxs-lookup"><span data-stu-id="d004f-174">**Activation and revisions** – In PSA, activation and revisions aren't supported for project quotes.</span></span> <span data-ttu-id="d004f-175">Salesissa tarjous voidaan lukita muokkauksen estämiseksi.</span><span class="sxs-lookup"><span data-stu-id="d004f-175">In Sales, a quote can be locked to prevent additional edits.</span></span>
- <span data-ttu-id="d004f-176">**Tarjouksen sulkeminen hävittynä tai voitettuna** – Kun projektitarjous suljetaan voitettuna tai hävittynä, mahdollisuus pysyy PSA:ssa avoimena.</span><span class="sxs-lookup"><span data-stu-id="d004f-176">**Closing a quote as lost or won** – In PSA, when a project quote is closed as won or lost, the opportunity remains open.</span></span> <span data-ttu-id="d004f-177">Kaikki muut mahdollisuuden tarjoukset suljetaan hävittynä.</span><span class="sxs-lookup"><span data-stu-id="d004f-177">All other quotes on the opportunity are closed as lost.</span></span> <span data-ttu-id="d004f-178">Kun tarjous suljetaan voitettuna tai hävittynä Salesissa, käyttäjää pyydetään toimimaan mahdollisuuden osalta.</span><span class="sxs-lookup"><span data-stu-id="d004f-178">In Sales, when a quote is closed as won or lost, the user is prompted to take an action on the opportunity.</span></span> <span data-ttu-id="d004f-179">Taustalla oleva mahdollisuus suljetaan tai jätetään avoimeksi käyttäjän valinnan perusteella.</span><span class="sxs-lookup"><span data-stu-id="d004f-179">Depending on the user input, the underlying opportunity might be closed or left open.</span></span>

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a><span data-ttu-id="d004f-180">Muutosten jäljittäminen tarjouksiin ja projektisuunnitelmiin myyntisyklin aikana</span><span class="sxs-lookup"><span data-stu-id="d004f-180">Tracking revisions to quotes and project plans in the sales cycle</span></span>
<span data-ttu-id="d004f-181">PSA:ssa tarjoukseen tehtyjä muutoksia ei voi jäljittää.</span><span class="sxs-lookup"><span data-stu-id="d004f-181">In PSA, you can't track revisions that are made to a quote.</span></span> <span data-ttu-id="d004f-182">Sen sijaan kulloisenkin tarjouksen tilaksi on asetettava **Suljettu hävittynä** ja sen jälkeen luotava uusi tarjous.</span><span class="sxs-lookup"><span data-stu-id="d004f-182">Instead, you must mark the existing quote **Closed as Lost** and then create a new quote.</span></span> <span data-ttu-id="d004f-183">PSA:n avulla tarjous voidaan kopioida tai projektiperusteinen tarjous kloonata.</span><span class="sxs-lookup"><span data-stu-id="d004f-183">You can copy a quote or clone a project-based quote by using PSA.</span></span>

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a><span data-ttu-id="d004f-184">Tarjousten ja projektisopimusten kommenttien ja hyväksyntöjen seuraaminen</span><span class="sxs-lookup"><span data-stu-id="d004f-184">Tracking comments and approvals of quotes and project contracts</span></span>
<span data-ttu-id="d004f-185">Voit hallita tarjousten ja projektisopimusten arviointia ja hyväksymistä tietueseinän ja viestien avulla.</span><span class="sxs-lookup"><span data-stu-id="d004f-185">You can manage the review and approval of quotes and project contracts by using the record wall and posts.</span></span> <span data-ttu-id="d004f-186">Organisaatiosi voi luoda mukautettuja työnkulkuja ja laajennuksia kohdentamaan, uudelleenohjaamaan ja hallitsemaan arvioinnin ja hyväksynnän työkohteiden ilmoituksia.</span><span class="sxs-lookup"><span data-stu-id="d004f-186">Your organization can create custom workflows and plug-ins to assign, redirect, escalate, and manage notifications of review and approval work items.</span></span>