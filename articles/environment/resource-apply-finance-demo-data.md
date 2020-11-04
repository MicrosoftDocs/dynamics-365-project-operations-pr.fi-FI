---
title: Project Operations -esittelytietojen käyttäminen Finance-pilvipalveluympäristössä
description: Tässä aiheessa kerrotaan, miten Project Operations -esittelytietoja käytetään pilvipalvelussa isännöidyssä Dynamics 365 Finance -ympäristössä.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b9af6c71b61840f4ffdf2892d8e7e5bbf0f8df67
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096618"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="c9702-103">Project Operations -esittelytietojen käyttäminen Finance-pilvipalveluympäristössä</span><span class="sxs-lookup"><span data-stu-id="c9702-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="c9702-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="c9702-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9702-105">Tämä aihe koskee vain Microsoft Dynamics 365 Finance -versiota 10.0.13, ja se voidaan suorittaa vain pilvipohjaisessa ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="c9702-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="c9702-106">Suorita tämän aiheen vaiheet, **ENNEN** kuin otat käyttöön ympäristön laatupäivitykset.</span><span class="sxs-lookup"><span data-stu-id="c9702-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="c9702-107">Avaa LCS-projektissa **Ympäristön tiedot** -sivu.</span><span class="sxs-lookup"><span data-stu-id="c9702-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="c9702-108">Huomaa, että se sisältää tiedot, joita tarvitaan yhteyden muodostamiseen ympäristöön etätyöpöytäprotokollan (RDP) avulla.</span><span class="sxs-lookup"><span data-stu-id="c9702-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![-ympäristön tiedot](./media/1EnvironmentDetails.png)

<span data-ttu-id="c9702-110">Ensimmäiset korostetut tunniste tiedot ovat paikallisten tilien tunnistetietoja, ja niissä on hyperlinkki etätyöpöytäyhteyteen.</span><span class="sxs-lookup"><span data-stu-id="c9702-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="c9702-111">Tunnistetiedoissa on ympäristön järjestelmänvalvojan käyttäjänimi ja salasana.</span><span class="sxs-lookup"><span data-stu-id="c9702-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="c9702-112">Toisen tunnistetietojoukon avulla voit kirjautua SQL Serveriin tässä ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="c9702-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="c9702-113">Voit muodostaa yhteyden ympäristöön **Paikalliset tilit** -kohdan hyperlinkin avulla ja todentautua käyttäen **paikallisen tilin tunnistetietoja**.</span><span class="sxs-lookup"><span data-stu-id="c9702-113">Remote to the environment by the hyperlink in **Local Accounts** , and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="c9702-114">Siirry kohtaan **Internet Information Services** > **Sovellusryhmät** > **AOSService** ja pysäytä palvelu.</span><span class="sxs-lookup"><span data-stu-id="c9702-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="c9702-115">Palvelu pysäytetään tässä vaiheessa, jotta voit jatkaa SQL-tietokannan korvaamista.</span><span class="sxs-lookup"><span data-stu-id="c9702-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Pysäytä AOS-palvelu](./media/2StopAOS.png)

4. <span data-ttu-id="c9702-117">Siirry kohtaan **Palvelut** ja pysäytä seuraavat kaksi kohdetta:</span><span class="sxs-lookup"><span data-stu-id="c9702-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="c9702-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span><span class="sxs-lookup"><span data-stu-id="c9702-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="c9702-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span><span class="sxs-lookup"><span data-stu-id="c9702-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Pysäytä palvelut](./media/3StopServices.png)

5. <span data-ttu-id="c9702-121">Avaa Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="c9702-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="c9702-122">Kirjaudu sisään SQL Server -tunnistetiedoilla ja käytä axdbadmin-käyttäjää ja salasanaa LCS:n **Ympäristöjen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c9702-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="c9702-124">Valitse Object Explorerissa **Tietokannat** ja etsi **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="c9702-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="c9702-125">Korvaat tietokannan uudella tietokannalla, joka sijaitsee [Download Centerissä](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="c9702-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="c9702-126">Kopioi zip-tiedosto yhdistettyyn virtuaalikoneeseen ja pura zip-tiedoston sisältö.</span><span class="sxs-lookup"><span data-stu-id="c9702-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="c9702-127">Napsauta SQL Server Management Studiossa hiiren kakkospainikkeella **AxDB** ja valitse sitten **Tehtävät** > **Palauta** > **Tietokanta**.</span><span class="sxs-lookup"><span data-stu-id="c9702-127">In SQL Server Management Studio, right-click **AxDB** , and then select **Tasks** > **Restore** > **Database**.</span></span>

![Tietokannan palauttaminen](./media/5RestoreDatabase.png)

9. <span data-ttu-id="c9702-129">Valitse **Lähdelaite** ja siirry kopioimastasi zip-tiedostosta purkamaasi tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="c9702-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Lähdelaitteet](./media/6SourceDevice.png)

10. <span data-ttu-id="c9702-131">Valitse **Asetukset** ja valitse sitten **Korvaa aiemmin luotu tietokanta** ja **Sulje aiemmin luodut yhteydet kohdetietokantaan**.</span><span class="sxs-lookup"><span data-stu-id="c9702-131">Select **Options** , and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="c9702-132">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9702-132">Select **OK**.</span></span>

![Asetusten palauttaminen](./media/7RestoreSetting.png)

<span data-ttu-id="c9702-134">Näyttöön tulee vahvistus siitä, että AXDB-palautus onnistui.</span><span class="sxs-lookup"><span data-stu-id="c9702-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="c9702-135">Kun olet saanut tämän vahvistuksen, voit sulkea SQL Services Management Studion.</span><span class="sxs-lookup"><span data-stu-id="c9702-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="c9702-136">Siirry takaisn kohtaan **Internet Information Services** > **Sovellusryhmät** > **AOSService** ja käynnistä AOSService.</span><span class="sxs-lookup"><span data-stu-id="c9702-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="c9702-137">Siirry kohtaan **Palvelut** ja käynnistä kaksi aiemmin pysäytettyä palvelua.</span><span class="sxs-lookup"><span data-stu-id="c9702-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="c9702-138">Etsi tässä virtuaalikoneessa AdminUserProvisioning-työkalu.</span><span class="sxs-lookup"><span data-stu-id="c9702-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="c9702-139">Katso K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="c9702-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="c9702-140">Suorita .exe-tiedosto **Sähköpostiosoite** -kentässä olevan käyttäjäosoitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="c9702-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="c9702-141">Valitse **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="c9702-141">Select **Submit**.</span></span>

![Järjestelmänvalvojakäyttäjän valmistelu](./media/8AdminUserProvisioning.png)

<span data-ttu-id="c9702-143">Tämä kestää muutaman minuutin.</span><span class="sxs-lookup"><span data-stu-id="c9702-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="c9702-144">Saat vahvistusviestin, jonka mukaan järjestelmänvalvojakäyttäjän päivitys onnistui.</span><span class="sxs-lookup"><span data-stu-id="c9702-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="c9702-145">Suorita lopuksi komentokehote järjestelmänvalvojana ja suorita iisreset-komento</span><span class="sxs-lookup"><span data-stu-id="c9702-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS Reset](./media/9IISReset.png)

18. <span data-ttu-id="c9702-147">Sulje etätyöpöytäistunto ja kirjaudu ympäristöön LCS:n **Ympäristön tiedot** -sivulla, jotta voit varmistaa, että se toimii odotetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="c9702-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
