---
title: Resurssien hallinta
description: Tässä aiheessa on tietoja resurssien hallinnasta.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 37377367751592fc533447748b80b124cb6548ad
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151339"
---
# <a name="manage-resources"></a><span data-ttu-id="ad1fb-103">Resurssien hallinta</span><span class="sxs-lookup"><span data-stu-id="ad1fb-103">Manage resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ad1fb-104">Dynamics 365 Project Service Automation sisältää resurssipäällikön koontinäytön, joka tarjoaa visuaalisen yleiskuvan resurssien kysynnöistä ja käytöstä koko organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="ad1fb-105">Tämän koontinäytön kaavioita voidaan käyttää seuraavien tietojen visualisointiin:</span><span class="sxs-lookup"><span data-stu-id="ad1fb-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="ad1fb-106">**Resurssin kysyntä** – Kaaviossa **Aktiivinen resurssipyyntö** näkyvät resurssit, jotka on lähetetty.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="ad1fb-107">Resurssit koostetaan joko roolin tai projektin perusteella.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="ad1fb-108">**Lähettämätön resurssin kysyntä** – Kaaviossa **Kohdentamaton resurssin kysyntä** näkyvät kaikki resurssitarpeet, joita ei ole lähetetty.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="ad1fb-109">Se auttaa resurssipäällikköitä tarkastelemaan kysyntää, joka ei ole vakaa ja joka voidaan lähettää resurssipyynnön kautta.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="ad1fb-110">**Kuluneen viikon laskutettava käyttö** – Kaaviossa **Roolikohtainen käyttö** näkyy organisaation todellisen roolikohtaisen laskutettavan käytön prosenttiosuus tavoitteena olevasta roolikohtaisesta laskutettavasta käytöstä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ad1fb-111">Kaavio **Roolikohtainen käyttö** saadaan käyttöön luomalla työ, jossa suoritetaan UpdateRoleUtilization-työnkulku.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="ad1fb-112">Tämä toistuva työ suoritetaan seitsemän päivän välein seitsemän edellisen päivän laskutettavan käytön laskemista varten.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="ad1fb-113">Tulokset koostetaan roolikohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="ad1fb-114">Projektiryhmän jäsenten hallinta</span><span class="sxs-lookup"><span data-stu-id="ad1fb-114">Manage project team members</span></span>

<span data-ttu-id="ad1fb-115">Projektipäälliköt voivat käyttää resurssipäällikön koontinäyttöä projektien resurssien hallintaan.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="ad1fb-116">He voivat esimerkiksi lisätä ryhmän jäsenen suoraan projektiin ja varata ryhmän jäsenen täyttämään resurssitarpeet, jotka yleinen resurssi on tallentanut.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="ad1fb-117">Ryhmän jäsenen lisääminen suoraan projektiin</span><span class="sxs-lookup"><span data-stu-id="ad1fb-117">Add a team member directly to a project</span></span>

<span data-ttu-id="ad1fb-118">Ryhmän jäsen lisätään suoraan projektiin valitsemalla **Projektit**-sivun **Ryhmä**-välilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="ad1fb-119">Näkyviin tulee **Pikaluonti: projektiryhmän jäsen** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="ad1fb-120">Tässä valintaikkunassa voidaan suorittaa seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="ad1fb-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="ad1fb-121">**Varaa nimetty resurssi** – Valitse resurssin nimi kentässä **Varattavissa oleva resurssi**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="ad1fb-122">Valitse sitten rooli, määritä ajanjakso ja valitse kohdennustapa.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="ad1fb-123">Valittu nimetty resurssi lisätään projektiin valittua kohdennustapaa ja resurssikalenteria käyttäen.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="ad1fb-124">**Lisää yleinen resurssi** – Jätä **Varattavissa oleva resurssi** -kenttä tyhjäksi ja valitse rooli, määritä ajanjakso ja valitse ensisijainen kohdennustapa.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="ad1fb-125">Ryhmään lisätään yleinen resurssi paikkamerkiksi säilyttämään kysyntämalli, jota käytetään nimettyjen resurssien varaamiseen ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="ad1fb-126">Tarve luodaan projektikalenterin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="ad1fb-127">**Lisää ryhmään nimetty resurssi ilman resurssikapasiteetin käyttöä** – Valitse resurssi kentässä **Varattavissa oleva resurssi**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="ad1fb-128">Määritä sitten ajanjakso ja valitse kohdennustavaksi **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="ad1fb-129">Resurssi lisätään ryhmään, mutta resurssin kapasiteettia ei käytetä varauksella.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="ad1fb-130">Ryhmän jäsenen varaaminen yleisen resurssin resurssitarpeen täyttämiseen</span><span class="sxs-lookup"><span data-stu-id="ad1fb-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="ad1fb-131">PSA:ssa voit varata projektiryhmän yleisen resurssin ja määrittää roolin, tarvitun kapasiteetin ja kapasiteetin jaon.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="ad1fb-132">Resurssin kysynnässä voit määrittää määritteitä, jotka yhdistetään yleiseen resurssiin.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="ad1fb-133">Näitä määritteitä ovat tarvittavat osaamisalueet, ensisijainen organisaatioyksikkö ja ensisijaiset resurssit.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="ad1fb-134">Noudata näitä vaiheita määrittääksesi kehittäjän yleisen resurssin tarvittavat osaamisalueet.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="ad1fb-135">Varaa yleinen resurssi valitsemalla **Projektit**-sivun **Ryhmä**-välilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Ryhmässä varattu yleinen resurssi](media/Resource-Management-image9.png)

2. <span data-ttu-id="ad1fb-137">Valitse **Kaikki ryhmän jäsenet** -näkymän **Resurssitarve**-sarakkeessa linkki lisätäksesi yleisen resurssin tarvittavat osaamisalueet.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Tarvelinkki](media/Resource-Management-image10.png)

3. <span data-ttu-id="ad1fb-139">Valitse näkyviin tulevan **Resurssitarve**-sivun **Osaamisalueet**-ruudukossa kolme pistettä (**...**) ja sitten **Lisää uusi tarveominaisuus** lisätäksesi kehittäjän tarvittavat osaamisalueet.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Lisää uusi tarveominaisuus -komento](media/Resource-Management-image11.png)

4. <span data-ttu-id="ad1fb-141">Valitse tarvittava osaamisalue näkyviin tulevan **Pikaluonti: tarveominaisuus** -valintaikkunan **Ominaisuus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="ad1fb-142">Valitse sitten **Luokitusarvo** -kentässä kyseisen osaamisalueen pätevyystaso.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="ad1fb-143">Määritä lopuksi **Resurssitarve**-kentässä tarve hakemaan resursseja organisaatioyksiköistä tai jopa nimetyistä resursseista.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="ad1fb-144">Kun olet valmis, valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-144">When you've finished, select **Save**.</span></span>

    ![Pikaluonti: Tarveominaisuus-valintaikkuna](media/Resource-Management-image12.png)

5. <span data-ttu-id="ad1fb-146">Täytä resurssitarve valitsemalla **Resurssitarve**-sivulla **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Resurssitarve-sivun varauspainike](media/Resource-Management-image13.png)

    <span data-ttu-id="ad1fb-148">Voit myös valita yleisen resurssin **Kaikki ryhmän jäsenet** -ruudukossa ja valita sitten **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Varauspainike Kaikki ryhmän jäsenet -ruudukon yläpuolella](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="ad1fb-150">Tässä esimerkissä on 40 tarvittua tuntia, mutta ei yhtään varattuja tunteja, koska yleisillä resursseilla ei ole varauksia.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="ad1fb-151">Lisäksi siinä ei ole kohdennettuja tunteja, koska yleinen resurssi on lisätty suoraan ryhmään.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="ad1fb-152">Sitä ei siis lisätty tehtävien kohdennuksella.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="ad1fb-153">**Ajoitusavustaja**-sivulla voit suodattaa käytettävissä olevia resursseja resurssitarpeessa määritettyjen tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="ad1fb-154">Resurssit lajitellaan aikataulutaulukossa määritettyjen lajitteluparametrien perusteella.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Ajoitusavustaja-sivu](media/Resource-Management-image15.png)

    <span data-ttu-id="ad1fb-156">Seuraavassa esitellään usein käytettyjä suodattimia:</span><span class="sxs-lookup"><span data-stu-id="ad1fb-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="ad1fb-157">**Ominaisuudet ja luokitus** – Suodata osaamisalueiden, sertifiointien ja muiden resurssien ominaisuuksien sekä pätevyysluokitusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="ad1fb-158">**Roolit** – Suodata varattavissa oleville resursseille määritettyjen oletusroolien perusteella.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="ad1fb-159">**Organisaatioyksiköt** – Suodata varattavissa olevia resursseja niille määritettyjen organisaatioyksiköiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="ad1fb-160">Jos et ole tyytyväinen ensimmäisen tarvehaun tuloksiin, voit muuttaa suodatusperusteita.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="ad1fb-161">Laajenna **Suodatinnäkymä**-ruutu ja valitse **Haku** löytääksesi lisää resursseja.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Suodatinnäkymä-ruutu](media/Resource-Management-image16.png)

7. <span data-ttu-id="ad1fb-163">Voit muuttaa tulosten lajittelutapaa valitsemalla **Lajittele.**</span><span class="sxs-lookup"><span data-stu-id="ad1fb-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Lajittelukomento](media/Resource-Management-image17.png)

8. <span data-ttu-id="ad1fb-165">Valitse resursseja tarpeessa määritetyn ja ruudukon yläosassa näkyvän kysynnän mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="ad1fb-166">Voit tyhjentää ruudukon solujen valinnan ja jättää kyseisen resurssikapasiteetin avoimeksi.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="ad1fb-167">Varatuksi voidaan valita vain yksi resurssi kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="ad1fb-168">Varaa valittu resurssi valitsemalla **Varaa** ja jätä aikataulutaulukko avoimeksi, jotta voit valita lisää resursseja.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="ad1fb-169">Voit myös valita **Varaa ja poistu** varataksesi valitun resurssin ja sulkeaksesi aikataulutaulukon.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Varattava resurssi](media/Resource-Management-image19.png)

    <span data-ttu-id="ad1fb-171">Saat ilmoituksen varatuista tunneista.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="ad1fb-172">Kysynnän ilmaisimet näyttävät, kuinka suuri osa tarpeesta on täytetty ja kuinka paljon sitä on jäljellä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="ad1fb-173">Voit myös katsoa, kuinka paljon valitun resurssin kapasiteetista on käytetty.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="ad1fb-174">Lisätietoja resurssin varauksista saat valitsemalla **Laajenna**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="ad1fb-175">Palaa **Kaikki ryhmän jäsenet** -näkymään.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="ad1fb-176">Huomaa, että yleinen resurssi on ruudukossa korvattu nimetyllä resurssilla ja että kyseiselle resurssille on merkitty 40 tuntia varatuksi.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Päivitetty Kaikki ryhmän jäsenet -ruudukko](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="ad1fb-178">Kohdennettuja tunteja ei näytetä, koska ne varattiin suoraan ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="ad1fb-179">Niitä ei varattu tehtävien kohdennuksella.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="ad1fb-180">Yleisten resurssien kohdennus tehtäville ja resurssitarpeiden luominen</span><span class="sxs-lookup"><span data-stu-id="ad1fb-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="ad1fb-181">PSA:ssa voit luoda tehtäviä ja sitten kohdentaa niille yleisiä resursseja.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="ad1fb-182">Tällöin paikkamerkit voivat edustaa resurssin kysyntää, kun arvioit aikatauluasi ja talouslukujasi.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="ad1fb-183">Tämän jälkeen voit luoda resurssitarpeita yleisille resursseille ja täyttää ne.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="ad1fb-184">Luo tehtävä valitsemalla **Projektit**-sivun **Aikataulut**-välilehdeltä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Uusi tehtävä on luotu](media/Resource-Management-image21.png)

2. <span data-ttu-id="ad1fb-186">Valitse **Resurssit**-kentässä **Resurssivalitsin**-symboli.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="ad1fb-187">Resurssivalitsin tulee näkyviin ja näyttää projektin olemassa olevat ryhmän jäsenet.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Resurssivalitsin](media/Resource-Management-image22.png)

3. <span data-ttu-id="ad1fb-189">Kirjoita uuden yleisen resurssin nimi ja valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Uuden yleisen resurssin nimi on annettu](media/Resource-Management-image23.png)

4. <span data-ttu-id="ad1fb-191">Valitse yleisen resurssin rooli näkyviin tulevan **Pikaluonti: projektiryhmän jäsen** -valintaikkunan **Rooli**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="ad1fb-192">Valitse yleiselle resurssille organisaatioyksikkö **Resursointiyksikkö**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="ad1fb-193">Valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-193">Then select **Save**.</span></span>

    ![Pikaluonti: projektiryhmän jäsen -valintaikkuna.](media/Resource-Management-image24.png)

    <span data-ttu-id="ad1fb-195">Yleinen ryhmän jäsen on nyt kohdennettu tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-195">The generic team member is now assigned to the task.</span></span>

    ![Yleinen ryhmän jäsen on kohdennettu tehtävälle](media/Resource-Management-image25.png)

    <span data-ttu-id="ad1fb-197">Uusi yleinen ryhmän jäsen näkyy **Ryhmä**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="ad1fb-198">Huomaa, että jäsenellä on vain kohdennettuja tunteja.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="ad1fb-199">Nämä tunnit ovat yhteismäärä kaikista yleiselle ryhmän jäsenelle kohdennetuista tehtävistä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="ad1fb-200">Yleisellä ryhmän jäsenellä ei vielä ole tarvittuja tunteja tai resurssitarvetta.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Yleinen ryhmän jäsen Ryhmä-välilehdessä](media/Resource-Management-image26.png)

5. <span data-ttu-id="ad1fb-202">Voit nyt kohdentaa yleisen ryhmän jäsenen muihin tehtäviin resurssivalitsimen avulla.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Yleinen ryhmän jäsen resurssivalitsimessa](media/Resource-Management-image27.png)

    <span data-ttu-id="ad1fb-204">Kun olet kohdentanut yleisen resurssin haluamiisi tehtäviin, voit luoda resurssitarpeen yleiselle resurssille.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="ad1fb-205">Valitse yleinen resurssi **Ryhmä**-välilehdessä ja valitse sitten **Luo tarve**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Luo tarve -komento](media/Resource-Management-image28.png)

    <span data-ttu-id="ad1fb-207">Kun tarve on luotu, yleisellä ryhmän jäsenellä on tarvitut tunnit sekä linkki resurssitarpeeseen.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Resurssitarpeen linkki](media/Resource-Management-image29.png)

    <span data-ttu-id="ad1fb-209">Kun olet varannut nimetyn resurssin, yleinen resurssi poistetaan ryhmästä ja korvataan nimetyllä resurssilla.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Nimetyllä resurssilla korvattu yleinen resurssi](media/Resource-Management-image30.png)

    <span data-ttu-id="ad1fb-211">**Aikataulut**-välilehdellä yleisen resurssin kohdennukset poistetaan ja korvataan nimetyllä resurssilla.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Yleisen resurssin kohdennukset korvataan nimetyllä resurssilla Aikataulut-välilehdessä](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="ad1fb-213">Tämä tapahtuu vain, kun nimetty resurssi on täysin varattu yleiselle resurssitarpeelle.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="ad1fb-214">Kun nimetty resurssi korvaa yleisen resurssitarpeen osittain tai useat nimetyt resurssit korvaavat resurssitarpeen, yleinen resurssi pysyy kohdennettuna tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="ad1fb-215">Seuraavassa kuvassa 80-tuntinen tehtävä on suunniteltu viiden päivän kestolle (16 tuntia päivässä viiden päivän ajan) ja kohdennettu yleiselle resurssille nimeltään **Toiminnallinen** (Functional).</span><span class="sxs-lookup"><span data-stu-id="ad1fb-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![80-tuntinen ja viisipäiväinen tehtävä kohdennettuna yleiselle resurssille Toiminnallinen](media/Resource-Management-image32.png)

    <span data-ttu-id="ad1fb-217">Kun luot tarpeen, se käsittää 80 tuntia viiden päivän aikana.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Tarve luotu 80 tunnille viiden päivän aikana](media/Resource-Management-image33.png)

    <span data-ttu-id="ad1fb-219">Koska käytettävissä olevat resurssit työskentelevät vain kahdeksan tuntia päivässä, tarpeen täyttämiseen tarvitaan kaksi resurssia.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Toinen resurssi](media/Resource-Management-image35.png)

    <span data-ttu-id="ad1fb-221">**Ryhmä**-välilehdessä näkyy nyt, että yleisellä resurssilla ei ole tarvittuja tunteja, mutta kohdennetut tunnit näkyvät yhä niiden kahden nimetyn resurssin kanssa, jotka täyttävät tarpeen.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Kaksi nimettyä resurssia Ryhmä-välilehdessä](media/Resource-Management-image36.png)

    <span data-ttu-id="ad1fb-223">**Aikataulut**-välilehdessä yleinen resurssi on edelleen kohdennettuna tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Yleisiä resursseja Aikataulut-välilehdessä](media/Resource-Management-image37.png)

<span data-ttu-id="ad1fb-225">PSA ei kohdenna molempia resursseja tehtävälle, koska silloin aikataulu olisi huonommin ennustettavissa.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="ad1fb-226">Tässä yksinkertaisessa esimerkissä tunnit on helppo jakaa tasan kahden resurssin kesken.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="ad1fb-227">Monimutkaisemmissa skenaarioissa, joihin liittyy useita tehtäviä ja useita resursseja, PSA:n on tehtävä oletuksia siitä, miten useille resursseille useissa tehtävissä tehdyt varaukset kohdennetaan.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="ad1fb-228">Siksi projektipäällikkö on näissä skenaarioissa vastuussa useiden varausten jäsentelystä ja tarpeenmukaisesta kohdennuksesta.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="ad1fb-229">Varausten kohdistamiseksi projektipäällikkö siirtää tehtävät yleisiltä resursseilta nimetyille resursseille ja varmistaa **Täsmäytys**-näkymän avulla, että kohdistus toimii varausten kanssa.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="ad1fb-230">Resurssitarpeen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="ad1fb-230">Edit a resource requirement</span></span>

<span data-ttu-id="ad1fb-231">Kun resurssitarve on luotu, projektipäällikkö tai resurssipäällikkö voi haluta muokata tietoja tarkentaakseen hakuehtoja, kun käytetään aikataulutaulukkoa.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="ad1fb-232">Resurssitarvetta muokataan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="ad1fb-233">Valitse **Projektit**-sivun **Ryhmä**-välilehdestä linkki mihin tahansa yleisen resurssin tarpeeseen.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="ad1fb-234">Näkyviin tulevalla **Resurssitarve**-sivulla voit päivittää useita määritteitä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="ad1fb-235">Seuraavassa on joitakin esimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-235">Here are some examples:</span></span>

    - <span data-ttu-id="ad1fb-236">Nimi</span><span class="sxs-lookup"><span data-stu-id="ad1fb-236">Name</span></span>
    - <span data-ttu-id="ad1fb-237">Päivämäärästä</span><span class="sxs-lookup"><span data-stu-id="ad1fb-237">From Date</span></span>
    - <span data-ttu-id="ad1fb-238">Päivämäärään</span><span class="sxs-lookup"><span data-stu-id="ad1fb-238">To Date</span></span>
    - <span data-ttu-id="ad1fb-239">Kesto</span><span class="sxs-lookup"><span data-stu-id="ad1fb-239">Duration</span></span>
    - <span data-ttu-id="ad1fb-240">Resurssityyppi</span><span class="sxs-lookup"><span data-stu-id="ad1fb-240">Resource Type</span></span>

<span data-ttu-id="ad1fb-241">**Resurssitarve**-sivulla projektipäällikkö tai resurssipäällikkö voi määrittää myös seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="ad1fb-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="ad1fb-242">Osaamisalueet</span><span class="sxs-lookup"><span data-stu-id="ad1fb-242">Skills</span></span>
- <span data-ttu-id="ad1fb-243">Roolit</span><span class="sxs-lookup"><span data-stu-id="ad1fb-243">Roles</span></span>
- <span data-ttu-id="ad1fb-244">Resurssin asetukset</span><span class="sxs-lookup"><span data-stu-id="ad1fb-244">Resource preferences</span></span>
- <span data-ttu-id="ad1fb-245">Ensisijainen organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="ad1fb-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="ad1fb-246">Resurssivarausten päivittäminen, kun ne on varattu projektille</span><span class="sxs-lookup"><span data-stu-id="ad1fb-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="ad1fb-247">Kun olet lisännyt projektiryhmään yleisen tai nimetyn resurssin, voit muuttaa resurssin varauksia.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="ad1fb-248">Valitse ryhmän jäsen **Projektit**-sivun **Ryhmä**-välilehdessä ja valitse sitten **Ylläpidä varauksia**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Valitun ryhmän jäsenen aikataulutaulukko avattuna](media/Resource-Management-image40.png)

    <span data-ttu-id="ad1fb-250">Aikataulutaulukko tulee näkyviin, ja siinä näkyvät projektiryhmän jäsenen varaukset.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="ad1fb-251">Laajentamalla ryhmän jäsenen tietueen näet tunnit, jotka on varattu tälle projektille ja muille projekteille, joissa käytetään ryhmän jäsenen kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="ad1fb-252">Voit pidentää tai lyhentää varausta valitsemalla sen ja vetämällä sitä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="ad1fb-253">Näkyviin tulee **Luo resurssivaraus**-valintaikkuna, jossa voit muokata varausta.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Luo resurssivaraus -valintaikkuna](media/Resource-Management-image41.png)

3. <span data-ttu-id="ad1fb-255">Napsauta varausta hiiren kakkospainikkeella.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-255">Right-click the booking.</span></span> <span data-ttu-id="ad1fb-256">Voit käyttää tätä pikavalikkoa seuraaviin toimiin:</span><span class="sxs-lookup"><span data-stu-id="ad1fb-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="ad1fb-257">Varauksen tilan muuttaminen.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-257">Change the booking status.</span></span>
    - <span data-ttu-id="ad1fb-258">Varauksen muokkaaminen.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-258">Edit the booking.</span></span>
    - <span data-ttu-id="ad1fb-259">Projektiryhmän resurssin korvaaminen.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="ad1fb-260">Varauksen tilan muuttaminen</span><span class="sxs-lookup"><span data-stu-id="ad1fb-260">Change the booking status</span></span>

<span data-ttu-id="ad1fb-261">Voit muuttaa mitä tahansa oletusarvoista tai muokattua varauksen tilaa.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-261">You can change any default or custom booking status.</span></span>

![Muuta tilaa -komento](media/Resource-Management-image42.png)

<span data-ttu-id="ad1fb-263">PSA:ssa voidaan käyttää seuraavia tiloja:</span><span class="sxs-lookup"><span data-stu-id="ad1fb-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="ad1fb-264">**Peruttu** – Tämä tila peruu resurssin varauksen ja vapauttaa resurssin kapasiteetin.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="ad1fb-265">**Sitova varaus** – Tämä tila käyttää resurssin kapasiteetin.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="ad1fb-266">Varauksella on yleensä tämä tila, kun **Ylläpidä varauksia** avataan **Kaikki ryhmän jäsenet** -ruudukossa **Projektit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="ad1fb-267">**Alustava varaus** – Tämä tila lisää resurssin ryhmälle, mutta ei käytä resurssin kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="ad1fb-268">Se ilmaisee, että resurssi on varattu mahdollista työtä varten ja että sillä on tästä huolimatta tarvittaessa kapasiteettia muita töitä varten.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="ad1fb-269">Resurssien kokonaiskäytettävyyden näkymässä alustavilla varauksilla on eri tila kuin sitovilla varauksilla.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="ad1fb-270">**Ehdotettu** – Tämä tila ilmaisee resurssipäällikön tai projektipäällikön resurssiehdotusta.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="ad1fb-271">Ehdotukset eivät käytä resurssin kapasiteettia, eikä resurssia lisätä projektiryhmään.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="ad1fb-272">Resurssin sitovaksi varaamiseksi ryhmälle projektipäällikön on hyväksyttävä ehdotus.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="ad1fb-273">Lähetä resurssipyyntöjä</span><span class="sxs-lookup"><span data-stu-id="ad1fb-273">Submit resource requests</span></span>

<span data-ttu-id="ad1fb-274">Resurssipyyntöjä käytetään siirtämään kysyntöjä (resurssitarpeita), jotka resurssipäällikön on täytettävä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="ad1fb-275">Jos kyse on ryhmällä jo olevasta yleisestä resurssista, resurssipyyntö voidaan lähettää suoraan.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="ad1fb-276">Resurssipyyntö voidaan täyttää kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="ad1fb-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="ad1fb-277">Resurssipäällikkö täyttää pyynnön suoraan.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="ad1fb-278">Tällöin yleinen resurssi korvataan sitovalla varauksella, jolla on nimetty resurssi.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="ad1fb-279">Resurssipäällikkö ehdottaa projektipäällikölle resurssia, ja projektipäällikkö hyväksyy tai hylkää ehdotetun resurssin.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="ad1fb-280">Resurssipyyntöjen suora täyttäminen</span><span class="sxs-lookup"><span data-stu-id="ad1fb-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="ad1fb-281">Kun resurssitarve luodaan, projektipäällikkö voi lähettää yleistä resurssia koskevan resurssipyynnön valitsemalla resurssin ja sitten **Lähetä pyyntö**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Lähetä pyyntö -painike](media/Resource-Management-image45.png)

<span data-ttu-id="ad1fb-283">Resursseja koskevia kommentteja voi antaa pyynnön täyttävälle resurssipäällikölle.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="ad1fb-284">Kun pyyntö on lähetetty, ryhmän jäsenen **Tila** -kentän arvoksi vaihtuu **Lähetetty**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Valinnaisten kommenttien antaminen](media/Resource-Management-image46.png)

<span data-ttu-id="ad1fb-286">Kun resurssipäällikkö täyttää pyynnön, yleinen ryhmän jäsen korvataan nimetyllä resurssilla **Kaikki ryhmän jäsenet** -ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Yleinen ryhmän jäsen korvattu nimetyllä resurssilla Kaikki ryhmän jäsenet -ruudukossa](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="ad1fb-288">Resurssiehdotusten käyttäminen resurssipyynnöissä</span><span class="sxs-lookup"><span data-stu-id="ad1fb-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="ad1fb-289">Resurssin suoran resurssipyyntöä varten varaamisen sijaan resurssipäällikkö voi ehdottaa projektipäällikölle resurssia.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="ad1fb-290">Resurssipäällikkö voi käyttää tätä vaihtoehtoa esimerkiksi, kun tarpeille ei ole tarkkaa vastaavuutta.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="ad1fb-291">Kun resurssipäällikkö ehdottaa resurssia, projektipäällikkö näkee, että yleisen ryhmän jäsenen **Tila**-kentän arvoksi vaihtuu **Tarkistettava**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Yleisen ryhmän jäsenen tilaksi vaihtunut Tarkistettava](media/Resource-Management-image48.png)

<span data-ttu-id="ad1fb-293">Voit tarkastella ehdotettua resurssia yhdessä ehdotuksen varauksen vaikutuksen visualisoinnin kanssa kaksoisnapsauttamalla ryhmän jäsentä, jolla on tila **Tarkistettava**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="ad1fb-294">Valitse sitten **Ehdotetut resurssit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-294">Then select the **Proposed Resources** tab.</span></span>

![Ehdotetut resurssit -välilehti](media/Resource-Management-image49.png)

<span data-ttu-id="ad1fb-296">Voit hyväksyä kaikki ehdotukset valitsemalla **Hyväksy kaikki ehdotukset** ja hylätä ne valitsemalla **Hylkää kaikki ehdotukset**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="ad1fb-297">Jos hyväksyt ehdotetut resurssit, ne varataan projektille sitovasti ryhmän jäseniksi ja korvaavat yleiset resurssit.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="ad1fb-298">Kaikki ehdotukset on joko hyväksyttävä tai hylättävä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="ad1fb-299">Niitä ei voi hyväksyä tai hylätä osittain.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="ad1fb-300">Projektiryhmän resurssin korvaaminen</span><span class="sxs-lookup"><span data-stu-id="ad1fb-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="ad1fb-301">Joskus projektipäällikön on korvattava projektille varattu ryhmän jäsen.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="ad1fb-302">Valitse korvattava resurssi **Projektit**-sivun **Ryhmä**-välilehdessä ja valitse sitten **Ylläpidä varauksia**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="ad1fb-303">Näet projektit, joille resurssi on kohdennettu, laajentamalla resurssia.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Laajennettu resurssi, jossa näkyvät sen projektit](media/Resource-Management-image50.png)

3. <span data-ttu-id="ad1fb-305">Napsauta projektia hiiren kakkospainikkeella ja valitse **Korvaa resurssi**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="ad1fb-306">Jos tiedät, millä resurssilla haluat korvata nykyisen resurssin, valitse tai kirjoita resurssin nimi ja valitse **Delegoi uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Korvaavan resurssin määrittäminen](media/Resource-Management-image51.png)

    <span data-ttu-id="ad1fb-308">Vaihtoehtoisesti voit etsiä resurssia seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="ad1fb-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="ad1fb-309">Valitse **Etsi korvaava**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-309">Select **Find Substitution**.</span></span>

        ![Korvaavan resurssin hakeminen](media/Resource-Management-image52.png)

        <span data-ttu-id="ad1fb-311">Aikatauluavustaja palauttaa luettelon käytettävissä olevista korvaavista resursseista.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="ad1fb-312">Voit lisäksi suodattaa käytettävissä olevia resursseja aikatauluavustajassa löytääksesi sopivan korvaavan resurssin.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Käytettävissä olevien korvaavien resurssien luettelo](media/Resource-Management-image53.png)

    2. <span data-ttu-id="ad1fb-314">Korvaa resurssi valitsemalla haluamasi resurssi ja sitten **Korvaava**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Korvaava resurssi valittuna](media/Resource-Management-image54.png)

    <span data-ttu-id="ad1fb-316">Varaukset ja kohdennukset siirretään uudelle resurssille.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Varaukset ja kohdennukset siirretty uudelle resurssille](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="ad1fb-318">Ryhmän jäsenen varausten ja kohdennusten täsmäyttäminen</span><span class="sxs-lookup"><span data-stu-id="ad1fb-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="ad1fb-319">Ryhmän jäsenillä varaukset ja kohdennukset ovat löyhästi sidoksissa.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="ad1fb-320">Toisin sanoen resursseilla voi olla kohdennuksia ilman varauksia ja varauksia ilman kohdennuksia.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="ad1fb-321">Ihannetapauksessa varaukset ja kohdennukset ovat samoja, jotta resurssit ovat sitoutuneet suorittamaan kohdennettuja tehtäviään.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="ad1fb-322">Varaukset saattavat kuitenkin perustua käytettävyyteen ja tehtävien ajoitukset saattavat muuttua projektin edetessä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="ad1fb-323">Siten varausten ja kohdennusten löyhä sidoksisuus luo joustavuutta.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="ad1fb-324">PSA:ssa on **Täsmäytys**-välilehti, jonka avulla projektipäälliköt voivat täsmäyttää ryhmänsä jäsenten varaukset ja kohdennukset projektiryhmille.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Täsmäytys-välilehti](media/Resource-Management-image56.png)

<span data-ttu-id="ad1fb-326">**Täsmäytys**-välilehti näyttää kunkin ryhmän jäsenen varaukset ja kohdennukset yksittäisten tehtävien kohdennusten tasolle asti.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="ad1fb-327">Se näyttää tunnit soluissa, jotka edustavat aikajaksoja kuukausista päiviin asti.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="ad1fb-328">Välilehdissä näkyy myös projektin kokonaissumma yhdessä summasarakkeen kanssa.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="ad1fb-329">Välilehti laskee kunkin resurssin osalta koosteen erosta ryhmän jäsenen varausten ja ryhmän jäsenen kohdennettujen tehtävien välillä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="ad1fb-330">Ihannetapauksessa eron pitäisi olla 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="ad1fb-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="ad1fb-331">Varausten ja kohdennusten välillä ei siis pitäisi olla eroa.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="ad1fb-332">Erot on korostettu väreillä ja varjostuksilla, jotta huomio kiinnittyy kahteen tilanteeseen:</span><span class="sxs-lookup"><span data-stu-id="ad1fb-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="ad1fb-333">**Varauspuute** – Varauspuutteessa on kyse siitä, että resurssilla on enemmän kohdennuksia kuin varauksia.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="ad1fb-334">Koska tätä kapasiteettia ei ole varattu, projektipäällikkö voi halutessaan korjata tämän tilanteen laajentamalla resurssin varauksia kattamaan puutteen.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="ad1fb-335">**Ylimääräiset varaukset** – ylimääräisiä varauksia tapahtuu, kun resurssi on kirjattu projektiin, mutta sitä ei ole kohdennettu tehtäviin.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="ad1fb-336">Tämä tilanne voi olla hyväksyttävä, jos resurssi on varattu projektille ennen tehtävien kohdentamista.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="ad1fb-337">Muissa tapauksissa resurssia ei kuitenkaan ole tarkoitus kohdentaa tehtäville.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="ad1fb-338">Näissä tapauksissa projektipäällikön tulisi harkita resurssin varausten peruuttamista, jotta kapasiteettia voidaan käyttää toisessa projektissa.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="ad1fb-339">Kun aikaa tarkastellaan päivätasoa korkeammalla tasolla (kuten kuukausitasolla), resurssin nettoero voi olla nolla (tällöin varaukset = kohdennukset).</span><span class="sxs-lookup"><span data-stu-id="ad1fb-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="ad1fb-340">Aikaa viikkotasolla tarkasteltaessa voi olla, että kohdennuksia on nolla tuntia, ja varauksia 40 tuntia ensimmäisellä viikolla, mutta 40 tuntia kohdennuksia ja nolla tuntia varauksia toisella viikolla.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="ad1fb-341">Yleisellä tasolla varaukset ja kohdennukset täsmäävät, mutta niiden välillä voi olla viikkokohtaisia eroja.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="ad1fb-342">Aikaa korkeilla tasoilla tarkasteltaessa **Täsmäytys**-välilehden soluissa on ilmaisin, joka ilmoittaa, että alemmilla aikatasoilla on eroja.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="ad1fb-343">Kaksoisnapsauttamalla solua voit lähentää näkymää nähdäksesi eron.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="ad1fb-344">Voit sitten loitontaa näkymää napsauttamalla hiiren kakkospainiketta. Valitsemalla resurssin ja käyttämällä sitten **Seuraava ero** -ohjausobjektia voit siirtyä seuraavaan eroon resurssin varausten ja kohdennusten välillä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="ad1fb-345">Voit myös palata takaisin käyttämällä **Edellinen ero** -ohjausobjektia.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="ad1fb-346">Voit myös poistaa eronilmaisimen ja siirtymistoiminnon käytöstä **Asetukset**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Eronilmaisin](media/Resource-Management-image57.png)

<span data-ttu-id="ad1fb-348">Tilanteissa, joissa resurssille on kohdennuksia mutta ei varauksia, voit valita varauspuutteen **Projektit**-sivun **Täsmäytys**-välilehdessä ja valita sitten **Laajenna varausta**.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="ad1fb-349">Näkyviin tulee **Laajenna varausta** -valintaikkuna, jota tarvitaan resurssin puutteen käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="ad1fb-350">Ikkunassa näkyvät myös resurssin olemassa olevat varaukset kaikissa projekteissa tai muissa ajoitettavissa entiteeteissä.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="ad1fb-351">Jos valitset **OK** luodaksesi varauksen resurssille sen käytettävyydestä riippumatta, voit aiheuttaa ylivarauksen.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Varaus-valintaikkunan laajentaminen](media/Resource-Management-image58.png)

<span data-ttu-id="ad1fb-353">Projektipäällikkö tai resurssipäällikkö voi sitten käyttää aikataulutustaulua hallitakseen tilanteita, joissa resurssin varaukset ylittävät kapasiteetin.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
