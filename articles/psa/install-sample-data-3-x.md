---
title: Näytetietojen asennus
description: Tässä aiheessa on tietoja näytetietojen asentamisesta Project Service Automationin avulla.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 3c9cca7aa9d85bb38e48820b361ba07923ceddbd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132419"
---
# <a name="sample-data-installation-for-the-project-service-application"></a><span data-ttu-id="6c06f-103">Näytetietojen asennus Project Service -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="6c06f-103">Sample data installation for the Project Service application</span></span>

<span data-ttu-id="6c06f-104">Jos haluat luoda omia esittely-ympäristöjä, voit käyttää Microsoftin ladattavissa olevia näytetietopaketteja, joissa esitellään sovellustesi ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="6c06f-104">To help you build your own demo environments, Microsoft provides downloadable sample data packages that showcase the capabilities of your apps.</span></span> <span data-ttu-id="6c06f-105">Näytetietopaketteja on kahta tyyppiä:</span><span class="sxs-lookup"><span data-stu-id="6c06f-105">There are two types of sample data packages:</span></span>
- <span data-ttu-id="6c06f-106">viite- ja asetustiedot</span><span class="sxs-lookup"><span data-stu-id="6c06f-106">reference/setup data</span></span>
- <span data-ttu-id="6c06f-107">esittelytiedot (viite- ja asetustiedot ja liiketapahtumatiedot, kuten työtilaukset ja projektit)</span><span class="sxs-lookup"><span data-stu-id="6c06f-107">demo data (reference/setup and transactional data such as work orders and projects)</span></span>

<span data-ttu-id="6c06f-108">**Viitteiden** näytetietopaketit ovat ladattavissa kolmessa erillisessä paketissa. Voit siis asentaa vain Project Service- tai vain Field Service -sovelluksen näytetiedot tai molempien sovellusten näytetiedot kerralla.</span><span class="sxs-lookup"><span data-stu-id="6c06f-108">The sample **reference** data packages are downloadable in three different packages, so you can install data only for Project Service, or only for Field Service, or you can install sample data for both applications at once.</span></span>

<span data-ttu-id="6c06f-109">Asetus- ja viitetietojen näytetietopaketit:</span><span class="sxs-lookup"><span data-stu-id="6c06f-109">The sample setup/reference data packages are:</span></span>

- [<span data-ttu-id="6c06f-110">**V902PSMasterData** - vain Project Service -sovelluksen versio 3.x</span><span class="sxs-lookup"><span data-stu-id="6c06f-110">**V902PSMasterData** - Project Service version 3.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [<span data-ttu-id="6c06f-111">**V902FSMasterData** - vain Field Service -sovelluksen versio 8.x</span><span class="sxs-lookup"><span data-stu-id="6c06f-111">**V902FSMasterData** - Field Service version 8.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [<span data-ttu-id="6c06f-112">**V902FPSMasterData** - Field Service -sovelluksen versio 8.x ja Project Service -sovelluksen versio 3.x</span><span class="sxs-lookup"><span data-stu-id="6c06f-112">**V902FPSMasterData** - Field Service 8.x and Project Service 3.x</span></span>](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

<span data-ttu-id="6c06f-113">Uusin **esittelytietojen** tietopaketti:</span><span class="sxs-lookup"><span data-stu-id="6c06f-113">The latest **demo** data package is:</span></span>

 - [<span data-ttu-id="6c06f-114">**FPSDemoData** - Field Service 8.x ja Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="6c06f-114">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span></span>](https://aka.ms/fpsdemodatapackage)

   <span data-ttu-id="6c06f-115">Asennusohjeet poikkeavat hieman sen mukaan, luoko vai määrittääkö käyttäjä osan, mutta muuten ohjeet ovat samat kuin edellisessä [**blogikirjoituksessa**](https://aka.ms/fpsdemodatablog).</span><span class="sxs-lookup"><span data-stu-id="6c06f-115">Installation instructions differ slightly in the users to create and configure section but the rest is the same as in the previous [**blog post**](https://aka.ms/fpsdemodatablog).</span></span> <span data-ttu-id="6c06f-116">Tässä paketissa on rajoitettu esittelytietojoukko, ja sen asentaminen kestää noin 3 tuntia.</span><span class="sxs-lookup"><span data-stu-id="6c06f-116">This package features a reduced demo data set and takes approximately 3 hours to install.</span></span>

<span data-ttu-id="6c06f-117">Nämä näytetietopaketit ovat saatavana vain englanninkielisinä.</span><span class="sxs-lookup"><span data-stu-id="6c06f-117">These sample data packages are available in English only.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c06f-118">**Näytetietojen asennusta ei voi peruuttaa.**</span><span class="sxs-lookup"><span data-stu-id="6c06f-118">**There is no way to uninstall the sample data.**</span></span> <span data-ttu-id="6c06f-119">Nämä paketit tulee asentaa vain esittely-, arviointi-, koulutus- tai testijärjestelmiin.</span><span class="sxs-lookup"><span data-stu-id="6c06f-119">You should only install these packages on demonstration, evaluation, training, or test systems.</span></span> <span data-ttu-id="6c06f-120">Huomaa myös, että yksittäisen paketin asennuksen jälkeen toisen yksittäisen paketin asennusta ei tueta.</span><span class="sxs-lookup"><span data-stu-id="6c06f-120">Also note that installing an individual package, and then installing the other individual package, is not supported.</span></span> <span data-ttu-id="6c06f-121">(Toisin sanoen et voi asentaa **FSMasterData**-pakettia ja sen jälkeen **PSMasterData**-pakettia tai päin vastoin) Jos tarvitset jossakin vaiheessa molempien sovellusten näytetietoja, asennettavan paketin tulee olla **v902FPSMasterData**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-121">(In other words, you can't install **FSMasterData** followed by **PSMasterData**, or vice versa.) If you see yourself needing sample data for both applications at any point in the future, you should install the **v902FPSMasterData** package.</span></span>

<span data-ttu-id="6c06f-122">Kun asennat jonkin näytetietopaketin, asennusprosessi suorittaa seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="6c06f-122">When you install any of the sample data packages, the installation process performs the following actions:</span></span>

- <span data-ttu-id="6c06f-123">Luo tai määrittää oletusparametrit, joiden avulla käytetään Project Service- tai Field Service -sovellusta tai molempia sovelluksia (jos käytettävissä).</span><span class="sxs-lookup"><span data-stu-id="6c06f-123">Creates or sets default parameters for using Project Service, Field Service, or both applications (if applicable).</span></span>

- <span data-ttu-id="6c06f-124">Tuo sovellusten näytetiedot, kuten varattavat resurssit, sovelluskohtaiset roolit, myynti- ja kustannushinnastot, organisaatioyksiköt, myyntiprosessitietueet ja muut entiteetit, joiden avulla esitellään tärkeimpiä ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="6c06f-124">Imports sample data for the applications, such as bookable resources, application-specific roles, sales and cost price lists, organizational units, sales process records, and other entities to demonstrate key capabilities.</span></span>  

<span data-ttu-id="6c06f-125">**Esittelytietopaketti** sisältää edellä olevat ja lisää liiketapahtumatietoja, kuten työtilauksia ja projekteja.</span><span class="sxs-lookup"><span data-stu-id="6c06f-125">With the **demo data** package, you get the above and additional transactional data such as work orders and projects.</span></span>

<span data-ttu-id="6c06f-126">Haluatko tietää, millaisia ominaisuuksia voit esitellä näytetietojen kanssa?</span><span class="sxs-lookup"><span data-stu-id="6c06f-126">Wondering what capabilities you can demo with the sample data?</span></span> <span data-ttu-id="6c06f-127">Katso kuvitteellinen Fabrikam Robotics -skenaario [teknisissä huomautuksissa](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="6c06f-127">See the Fabrikam Robotics fictitious scenario in [Technical notes](#technical-notes).</span></span>

<span data-ttu-id="6c06f-128">Jos sinulla on näiden näytetietopakettien asentamiseen liittyviä kysymyksiä, [lähetä sähköpostiviesti osoitteeseen fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="6c06f-128">If you have questions about installing these sample data packages, [send us an email at fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c06f-129">Vaatimukset</span><span class="sxs-lookup"><span data-stu-id="6c06f-129">Requirements</span></span>

<span data-ttu-id="6c06f-130">Asennustoiminnoissa edellytetään, että kohdeilmentymä (organisaatio) täyttää seuraavat vaatimukset:</span><span class="sxs-lookup"><span data-stu-id="6c06f-130">The installation protocol assumes the following about your target instance (org):</span></span>

- <span data-ttu-id="6c06f-131">Peruskieli on englanti ja perusvaluutta Yhdysvaltain dollari (USD,$).</span><span class="sxs-lookup"><span data-stu-id="6c06f-131">Base language is English and base currency is US dollar (USD,$).</span></span>

- <span data-ttu-id="6c06f-132">Organisaatiolla ei ole Project Service- tai Field Service -tietoja tai sillä on vain oletustiedot, jotka tulevat minkä tahansa uuden organisaation mukana.</span><span class="sxs-lookup"><span data-stu-id="6c06f-132">The org has no Project Service or Field Service data already, or only has barebones default data that comes with any new org.</span></span>

- <span data-ttu-id="6c06f-133">Yrityssovelluksen oikea versio on jo asennettu:</span><span class="sxs-lookup"><span data-stu-id="6c06f-133">The correct version of the business application is already installed:</span></span>
       
    - <span data-ttu-id="6c06f-134">**FPSDemoData tai v902FPSMasterData:** Organisaatioon on asennettu Field Service -sovelluksen versio 8.x ja Project Service -sovelluksen versio 3.x.</span><span class="sxs-lookup"><span data-stu-id="6c06f-134">**For FPSDemoData or v902FPSMasterData:** The org has Field Service version 8.x and Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="6c06f-135">**v902PSMasterData:** Organisaatioon on asennettu Project Service -sovelluksen versio 3.x.</span><span class="sxs-lookup"><span data-stu-id="6c06f-135">**For v902PSMasterData:** The org has Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="6c06f-136">**v902FSMasterData:** Organisaatioon on asennettu Field Service -sovelluksen versio 8.x.</span><span class="sxs-lookup"><span data-stu-id="6c06f-136">**For v902FSMasterData:** The org has Field Service version 8.x installed.</span></span>

> [!NOTE]
> <span data-ttu-id="6c06f-137">Jos näytetiedot on asennettava olemassa olevan Project Service- tai Field Service -kokeilu- tai esittely-ympäristöön, jossa on jo tietoja (ei suositella), asennusohjelman suorittamat turvallisuuteen liittyvät esitarkistukset on poistettava käytöstä tilapäisesti.</span><span class="sxs-lookup"><span data-stu-id="6c06f-137">If you need to install the sample data on top of an existing Project Service and Field Service trial or demo environment that already has data (not recommended), you'll need to suspend the safety prechecks performed by the installer.</span></span> <span data-ttu-id="6c06f-138">Lisätietoja on alla olevissa teknisissä huomautuksissa.</span><span class="sxs-lookup"><span data-stu-id="6c06f-138">For more information, see the technical notes below.</span></span>

## <a name="prepare-for-installation"></a><span data-ttu-id="6c06f-139">Asennuksen valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="6c06f-139">Prepare for installation</span></span>

<span data-ttu-id="6c06f-140">Asennusohjelma on suoritettava tietokoneella, jossa on käytössä Windowsin uusin versio (Windows 10 on suositeltu versio).</span><span class="sxs-lookup"><span data-stu-id="6c06f-140">You need to run the installer on a computer with a recent version of Windows (Windows 10 preferred).</span></span>

<span data-ttu-id="6c06f-141">Tietokoneessa on oltava verkkoyhteys. **Asennus- tai viitetietojen** asentaminen voi kestää **tunnin**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-141">You should plan for the computer to remain connected to a network, and for the installation to run for up to **1 hour** for **setup/reference data**.</span></span> <span data-ttu-id="6c06f-142">(Yleensä **FPSMasterData**-paketin asennus kestää noin 30 minuuttia. Paketti sisältää kummankin sovelluksen mallitiedot.) **FPSDemoData**-paketin asennus kestää noin **3 tuntia**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-142">(Normally the installation takes around 30 minutes for **FPSMasterData**, which includes sample data for both applications.) For the **FPSDemoData**, the installation will take around **3 hours**.</span></span>

<span data-ttu-id="6c06f-143">Tietokoneen näytönsäästäjätoiminto tulee poistaa käytöstä.</span><span class="sxs-lookup"><span data-stu-id="6c06f-143">The computer should have the screen saver function turned off.</span></span> <span data-ttu-id="6c06f-144">Muussa tapauksessa asennuksen istunnon tunnistetiedot menetetään, kun näytönsäästäjä menee päälle (ellet pidä istuntoa aktiivisena koko ajan).</span><span class="sxs-lookup"><span data-stu-id="6c06f-144">Otherwise, session credentials for the installation may be lost when the screen saver engages (unless you keep your session active throughout).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="6c06f-145">![Näytönsäästäjän asetusten näyttökuva, jossa näytönsäästäjä on poistettu käytöstä](media/sample-data-1.png)</span><span class="sxs-lookup"><span data-stu-id="6c06f-145">![Screenshot of screen saver settings, with screen saver turned off](media/sample-data-1.png)</span></span>

## <a name="download-and-unpack"></a><span data-ttu-id="6c06f-146">Lataaminen ja paketin purkaminen</span><span class="sxs-lookup"><span data-stu-id="6c06f-146">Download and unpack</span></span>

<span data-ttu-id="6c06f-147">Project Service- ja Field Service -näytetietojen asennusohjelma jaetaan automaattisesti purkautuvana suoritettavana tiedostona.</span><span class="sxs-lookup"><span data-stu-id="6c06f-147">The Project Service and Field Service sample data installer is distributed as a self-extracting executable.</span></span> <span data-ttu-id="6c06f-148">Tiedostojen nimet voivat vaihdella näytetietopaketin mukaan. Vaiheet ovat kuitenkin samat asennettavasta paketista riippumatta.</span><span class="sxs-lookup"><span data-stu-id="6c06f-148">The file names may vary depending on the sample data package, but otherwise the steps are the same no matter which package you install.</span></span>

<span data-ttu-id="6c06f-149">Kun paketti on ladattu, suorita .exe-tiedosto ja hyväksy pakatun zip-tiedoston purkamisen ehdot.</span><span class="sxs-lookup"><span data-stu-id="6c06f-149">After downloading a package, run the .exe file, and then accept terms and conditions to unpack the compressed zip file.</span></span> <span data-ttu-id="6c06f-150">Tämän jälkeen tiedoston sisältö puretaan tietokoneen kansioon.</span><span class="sxs-lookup"><span data-stu-id="6c06f-150">You then need to extract contents of that file to a folder on the computer.</span></span>

<span data-ttu-id="6c06f-151">Käyttöjärjestelmästä ja suojausasetuksista riippuen zip-tiedoston purkamisen jälkeen on suoritettava seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="6c06f-151">Depending on the operating system and security settings, you may need to perform the following steps after unpacking the zip file:</span></span>

1. <span data-ttu-id="6c06f-152">Etsi **FPSDemoData.dll**-tiedosto **v902FPSMasterData** / **PackageDeployer_FPSDemoData**-kansiossa ja kaksoisnapsauta sitä.</span><span class="sxs-lookup"><span data-stu-id="6c06f-152">Find and right-click the **FPSDemoData.dll** file in the **v902FPSMasterData** / **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="6c06f-153">Valitse **Poista esto**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-153">Choose **Unblock**.</span></span>

3. <span data-ttu-id="6c06f-154">Valitse **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-154">Select **Apply**.</span></span>

4. <span data-ttu-id="6c06f-155">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-155">Select **OK**.</span></span>


## <a name="create-or-configure-users"></a><span data-ttu-id="6c06f-156">Käyttäjien luominen tai määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6c06f-156">Create or configure users</span></span>

<span data-ttu-id="6c06f-157">**FPSDemoData**-paketti edellyttää kuutta käyttäjää, kun taas **FPSMasterData**-paketit edellyttävät yhtä käyttäjää.</span><span class="sxs-lookup"><span data-stu-id="6c06f-157">The **FPSDemoData** package requires six users while **FPSMasterData** packages require one user.</span></span> <span data-ttu-id="6c06f-158">Viittaa oikeaan, näytetietopaketille tarkoitettuun versioon.</span><span class="sxs-lookup"><span data-stu-id="6c06f-158">Refer to the correct one for your sample data package.</span></span>

## <a name="create-or-configure-users---setupreference-data-packages"></a><span data-ttu-id="6c06f-159">Käyttäjien luominen tai määrittäminen – asetus- ja viitetietopaketit</span><span class="sxs-lookup"><span data-stu-id="6c06f-159">Create or configure users - setup/reference data packages</span></span>

<span data-ttu-id="6c06f-160">**FPSMasterData**-paketti on suunniteltu niin, että se asentaa yhden käyttäjän, jonka nimi on Spencer Low, sekä tässä kuvatut asetukset.</span><span class="sxs-lookup"><span data-stu-id="6c06f-160">The **FPSMasterData** package is designed to install with one user named Spencer Low with the settings described here.</span></span> <span data-ttu-id="6c06f-161">Jotta paketti asentuu oikein, ympäristöösi on luotava käyttäjät (tai käyttäjät on nimettävä uudelleen tilapäisesti), jotta ne vastaavat näytetietojen määritystä.</span><span class="sxs-lookup"><span data-stu-id="6c06f-161">To install the package correctly, you need to create (or temporarily rename) users in your environment to match the incoming sample data configuration.</span></span>

<span data-ttu-id="6c06f-162">Voit luoda tai määrittää käyttäjiä siirtymällä kohtaan **Asetukset** > **Suojaus** > **Käyttäjät** ja tekemällä seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="6c06f-162">To create or configure users, go to **Settings** > **Security** > **Users**, and do the following:</span></span>

1. <span data-ttu-id="6c06f-163">Määritä UserFullname="Spencer Low" ja käyttäjätunnukseksi "spencerl" (**pienet kirjaimet**) projektipäällikön ja käytäntöpäällikön rooleihin.</span><span class="sxs-lookup"><span data-stu-id="6c06f-163">Set UserFullname="Spencer Low" with username "spencerl" (**lowercase**) to the Project Manager and Practice Manager roles.</span></span>

2. <span data-ttu-id="6c06f-164">Valitse käyttäjäksi **Spencer Low** ja valitse sitten **Hallitse rooleja**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-164">Select the **Spencer Low** user, and then select **Manage Roles**.</span></span> <span data-ttu-id="6c06f-165">Etsi **järjestelmänvalvojan** rooli ja valitse se. Myönnä Spencer Low'lle täydet järjestelmänvalvojan oikeudet valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-165">Find and select the **System Administrator** role, and then select **OK** to grant full admin rights to Spencer Low.</span></span> <span data-ttu-id="6c06f-166">Tämän vaihe on välttämätön, koska siinä varmistetaan, että näytetiedot luodaan oikean käyttäjän omistuksen kanssa. Näin näkymien täyttäminen tapahtuu oikein.</span><span class="sxs-lookup"><span data-stu-id="6c06f-166">This step is necessary to ensure that sample records are created with the correct user ownership and therefore populate views correctly.</span></span>

3. <span data-ttu-id="6c06f-167">Päivitä ladatun paketin tietojen yhdistämisen tiedostoon oletuskäyttäjän sähköpostiosoitteet.</span><span class="sxs-lookup"><span data-stu-id="6c06f-167">From the downloaded package, you need to update a data mapping file with email addresses of the default user context.</span></span> <span data-ttu-id="6c06f-168">Avaa **PkgFolder**, etsi **ImportUserMapFile.xml** -tiedosto ja avaa se Muistiossa (tai Visual Studiossa tai toisessa XML-editorissa).</span><span class="sxs-lookup"><span data-stu-id="6c06f-168">To do this, open **PkgFolder**, and then find and open the **ImportUserMapFile.xml** file in Notepad (or Visual Studio or another XML editor).</span></span> <span data-ttu-id="6c06f-169">Määritä **DefaultUserToMapTo=**-kenttään käyttäjän Spencer Low sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="6c06f-169">Set the **DefaultUserToMapTo=** field to the email address of the Spencer Low user.</span></span>

4. <span data-ttu-id="6c06f-170">Jos et käytä Spencer Low'n käyttäjätunnusta **spencerl**, sinun on päivitettävä toinen tiedosto.</span><span class="sxs-lookup"><span data-stu-id="6c06f-170">If you aren't using Spencer Low with username **spencerl**, you need to update an additional file.</span></span> <span data-ttu-id="6c06f-171">Avaa **DemoDataPreImportConfig.xml**-tiedosto ja etsi **userstocreateandconfigure**-tunniste.</span><span class="sxs-lookup"><span data-stu-id="6c06f-171">Open the **DemoDataPreImportConfig.xml** file, and then find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="6c06f-172">Päivitä **\<login\>**-tunnisteeksi käyttäjän Spencer Low käyttäjätunnus.</span><span class="sxs-lookup"><span data-stu-id="6c06f-172">Update the **\<login\>** tag with the username of your Spencer Low user.</span></span> <span data-ttu-id="6c06f-173">Lisätietoja on [teknisissä huomautuksissa](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="6c06f-173">For additional details, see [Technical notes](#technical-notes).</span></span>

## <a name="create-or-configure-users---demo-data-package"></a><span data-ttu-id="6c06f-174">Käyttäjien luominen tai muokkaaminen – esittelytietopaketti</span><span class="sxs-lookup"><span data-stu-id="6c06f-174">Create or configure users - demo data package</span></span>

<span data-ttu-id="6c06f-175">Esittelytietopakettia varten tarvitaan kuusi käyttäjää.</span><span class="sxs-lookup"><span data-stu-id="6c06f-175">The demo data package requires six users.</span></span> <span data-ttu-id="6c06f-176">Paketti asennetaan oikein seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6c06f-176">For the package to install correctly, do the following:</span></span>

 1. <span data-ttu-id="6c06f-177">Luo käyttäjiä tai vaihda väliaikaisesti käyttäjien nimet vastaamaan saapuvaa mallitietomääritystä valitsemalla **Asetukset** > **Suojaus** > **Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-177">Create or temporarily rename existing users to match incoming sample data configuration by going to **Settings** > **Security** > **Users**.</span></span>
 
    <span data-ttu-id="6c06f-178">Näitä rooleja tarvitaan vain henkilöpohjaisissa esittelyissä.</span><span class="sxs-lookup"><span data-stu-id="6c06f-178">These roles are only needed for persona-based demos.</span></span>  
    - <span data-ttu-id="6c06f-179">Käytä kenttätyöntekijänä käyttäjää Fullname="David So"</span><span class="sxs-lookup"><span data-stu-id="6c06f-179">User Fullname="David So" as Field Service Technician</span></span>   
    - <span data-ttu-id="6c06f-180">Käytä asiakaspalvelijana ja kenttäpalvelun aikatauluttajana käyttäjää Fullname="Jamie Reding"</span><span class="sxs-lookup"><span data-stu-id="6c06f-180">User Fullname="Jamie Reding" as Customer Service & Field Service Dispatcher</span></span>   
    - <span data-ttu-id="6c06f-181">Käytä asiakaspäällikkönä käyttäjää Fullname="Molly Clark"</span><span class="sxs-lookup"><span data-stu-id="6c06f-181">User Fullname="Molly Clark" as Account Manager</span></span>   
    - <span data-ttu-id="6c06f-182">Käytä käytäntö- ja projektipäällikkönä käyttäjää Fullname="Spencer Low"</span><span class="sxs-lookup"><span data-stu-id="6c06f-182">User Fullname="Spencer Low" as Practice and Project Manager</span></span>  
    - <span data-ttu-id="6c06f-183">Käytä tiimin jäsenenä käyttäjää Fullname="Veronica Quek"</span><span class="sxs-lookup"><span data-stu-id="6c06f-183">User Fullname="Veronica Quek" as Team Member</span></span>   
    - <span data-ttu-id="6c06f-184">Käyttäjä Fullname="William Contoso"</span><span class="sxs-lookup"><span data-stu-id="6c06f-184">User Fullname="William Contoso"</span></span>
  
2. <span data-ttu-id="6c06f-185">Määritä edellä mainituille kuudelle käyttäjälle järjestelmänvalvojan rooli esittelytietojen tuontia varten, jotta näytetiedot tuodaan oikein.</span><span class="sxs-lookup"><span data-stu-id="6c06f-185">For the purposes of demo data import, assign the six users above the Administrator role so sample records import correctly.</span></span> 

3. <span data-ttu-id="6c06f-186">Avaa **PkgFolder** ja etsi ja avaa sitten **ImportUserMapFile.xml**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-186">Open **PkgFolder** and then find and open **ImportUserMapFile.xml**.</span></span> <span data-ttu-id="6c06f-187">Päivitä **New=**-kentät järjestelmän käyttäjiä vastaaviksi sähköpostiosoitteiksi.</span><span class="sxs-lookup"><span data-stu-id="6c06f-187">Update the **New=** fields to the email addresses of corresponding Users in your system.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="6c06f-188">![Näyttökuva UserMapFile-tiedostosta](media/sample-data-7.png)</span><span class="sxs-lookup"><span data-stu-id="6c06f-188">![Screen shot of UserMapFile](media/sample-data-7.png)</span></span>

4. <span data-ttu-id="6c06f-189">Jos "Spencer Low" -nimisen käyttäjän koko nimellä on eri käyttäjätunnus kuin **"spencerl"**, myös lisätiedosto on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="6c06f-189">If your "Spencer Low" full name user has a different user ID than **"spencerl"**, then you need to update an additional file.</span></span> <span data-ttu-id="6c06f-190">Avaa **DemoDataPreImportConfig.xml** ja etsi **userstocreateandconfigure**-tunniste.</span><span class="sxs-lookup"><span data-stu-id="6c06f-190">Open **DemoDataPreImportConfig.xml** and find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="6c06f-191">Päivitä loginId (kirjainkoolla on merkitystä) **\<login\>**-tunnisteeseen.</span><span class="sxs-lookup"><span data-stu-id="6c06f-191">Update the **\<login\>** tag with the loginId (case-sensitive).</span></span> 

5. <span data-ttu-id="6c06f-192">Ensimmäisen käyttäjän kalenterin (joka on **userstocreateandconfigure**-tunnisteessa) avulla lisätään kaikkien varattavien resurssien työtunnit esittelytietoja tuotaessa.</span><span class="sxs-lookup"><span data-stu-id="6c06f-192">The first user's calendar (in the **userstocreateandconfigure** tag) is used to populate the work hours for all bookable resources on import of demo data.</span></span> <span data-ttu-id="6c06f-193">Valitse **Asetukset** > **Suojaus** > **Käyttäjät**, etsi käyttäjä Spencer Low ja avaa Työtunnit-asetus.</span><span class="sxs-lookup"><span data-stu-id="6c06f-193">Navigate to **Settings** > **Security** > **Users**, find your "Spencer Low" user, and open the "Work Hours" option.</span></span> <span data-ttu-id="6c06f-194">Muokkaa nykyisiä työtunteja valitsemalla **Koko viikoittain toistuva aikataulu alusta loppuun** -asetus.</span><span class="sxs-lookup"><span data-stu-id="6c06f-194">Edit the existing work hours, selecting the **Entire recurring weekly schedule from start to end** option.</span></span> <span data-ttu-id="6c06f-195">Varmista, että **työtunneiksi on määritetty 8.00–17.00 (9 tuntia) maanantaista perjantaihin ja aikavyöhykkeeksi on määritetty Tyynenmeren normaaliaika (USA ja Kanada)**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-195">Ensure the **Work hours are set to 8 AM - 5 PM (9 Hours), Monday to Friday and with the Timezone set to Pacific Time (US & Canada)**.</span></span> <span data-ttu-id="6c06f-196">Tällä tavoin varmistaa, että projekti- ja aikataulutaulukko näkyvät odotetusti.</span><span class="sxs-lookup"><span data-stu-id="6c06f-196">This is needed to ensure that the Project and Schedule board show as expected.</span></span>

<span data-ttu-id="6c06f-197">**Suositus:** Organisaatiolle kannattaa luoda varmuuskopio nyt siltä varalta, että asennuksessa on palattava aloituskohtaan. Näin saattaa käydä, jos näytetietojen asennuksen aikana tapahtuu virhe.</span><span class="sxs-lookup"><span data-stu-id="6c06f-197">**Recommendation:** Consider creating a backup of your org now, in case you need to revert to your starting point if something goes wrong during the sample data installation.</span></span> <span data-ttu-id="6c06f-198">Lisätietoja on kohdassa [Ilmentymien varmuuskopiointi ja palautus](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span><span class="sxs-lookup"><span data-stu-id="6c06f-198">For more information, see [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span></span>

## <a name="run-the-package-deployer"></a><span data-ttu-id="6c06f-199">Suorita Package Deployer</span><span class="sxs-lookup"><span data-stu-id="6c06f-199">Run the Package Deployer</span></span>

1. <span data-ttu-id="6c06f-200">Etsi ja suorita **PackageDeployer.exe**. Se on **v902FPSMasterData**- TAI **PackageDeployer_FPSDemoData**-kansiossa.</span><span class="sxs-lookup"><span data-stu-id="6c06f-200">Find and run **PackageDeployer.exe** in the **v902FPSMasterData** OR **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="6c06f-201">Hyväksy ehdot.</span><span class="sxs-lookup"><span data-stu-id="6c06f-201">Accept the terms and conditions.</span></span>

3. <span data-ttu-id="6c06f-202">Seuraava ikkuna:</span><span class="sxs-lookup"><span data-stu-id="6c06f-202">On the next window:</span></span>

   <span data-ttu-id="6c06f-203">a.</span><span class="sxs-lookup"><span data-stu-id="6c06f-203">a.</span></span> <span data-ttu-id="6c06f-204">Valitse **Office 365**:n käyttöönottotyyppi.</span><span class="sxs-lookup"><span data-stu-id="6c06f-204">Select deployment type **Office 365**.</span></span>

   <span data-ttu-id="6c06f-205">b.</span><span class="sxs-lookup"><span data-stu-id="6c06f-205">b.</span></span> <span data-ttu-id="6c06f-206">Käytä järjestelmänvalvojalle Käyttäjien luominen tai määrittäminen -kohdassa luotua käyttäjää ja salasanaa (Spencer Low ja käyttäjätunnus spencerl).</span><span class="sxs-lookup"><span data-stu-id="6c06f-206">Use the user and password of the system administrator user configured in "Create or configure users" ("Spencer Low" with "spencerl" username).</span></span>

   <span data-ttu-id="6c06f-207">c.</span><span class="sxs-lookup"><span data-stu-id="6c06f-207">c.</span></span> <span data-ttu-id="6c06f-208">Varmista, että **Näytä käytettävissä olevien organisaatioiden luettelo** on valittu.</span><span class="sxs-lookup"><span data-stu-id="6c06f-208">Make sure **Display list of available organizations** is selected.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="6c06f-209">![Näyttökuva Package Deployer -ikkunasta, jossa on valittu Näytä käytettävissä olevien organisaatioiden luettelo](media/sample-data-2.png)</span><span class="sxs-lookup"><span data-stu-id="6c06f-209">![Screenshot of Package Deployer window with "Display list of available organizations" selected](media/sample-data-2.png)</span></span>

4. <span data-ttu-id="6c06f-210">Valitse organisaatio, johon haluat asentaa näytetiedot.</span><span class="sxs-lookup"><span data-stu-id="6c06f-210">Select the organization where you want to install the sample data.</span></span>

5. <span data-ttu-id="6c06f-211">Valitse **Seuraava** niin kauan, kunnes näkyviin tulee **Esittelytietojen asetukset** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="6c06f-211">Select **Next** until you see the **Demo Data Setup** dialog.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="6c06f-212">![Esittelytietojen asennusohjelman tilaikkunan näyttökuva](media/sample-data-3.png)</span><span class="sxs-lookup"><span data-stu-id="6c06f-212">![Screenshot of the demo data installer status window](media/sample-data-3.png)</span></span>

6. <span data-ttu-id="6c06f-213">Ennen kuin jatkat, ota huomioon, että näytetietojen asentaminen voi kestää jopa tunnin (yleensä se kestään noin 10 minuuttia).</span><span class="sxs-lookup"><span data-stu-id="6c06f-213">Before proceeding, note that installing sample data could take up to one hour (normally ~10 minutes).</span></span> <span data-ttu-id="6c06f-214">Varmista, että tietokone on päällä, verkkoyhteys säilyy asennusprosessin ajan ja että istunto pysyy aktiivisena.</span><span class="sxs-lookup"><span data-stu-id="6c06f-214">You'll need to make sure the computer remains on and connected to a network throughout the installation process, and that your session remains active.</span></span>   

7. <span data-ttu-id="6c06f-215">Kun olet valmis, valitse **Seuraava** ja aloita näytetietojen asennusprosessi.</span><span class="sxs-lookup"><span data-stu-id="6c06f-215">When you're ready, click **Next** to start the sample data installation process.</span></span> <span data-ttu-id="6c06f-216">Kun näytetiedot on ladattu, valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-216">After the sample data is loaded, click **Finish**.</span></span>

## <a name="verify-the-sample-data-installation"></a><span data-ttu-id="6c06f-217">Näytetietojen asennuksen tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="6c06f-217">Verify the sample data installation</span></span>

<span data-ttu-id="6c06f-218">Tarkista, että Fabrikam Robotics -yrityksen kuvitteellisen skenaarion tietueet ja entiteettityypit näkyvät halutulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="6c06f-218">For a sanity check, verify that the number of records and types of entities listed in Fabrikam Robotics fictitious scenario appear as expected.</span></span>

<span data-ttu-id="6c06f-219">Kun näytetiedot on ladattu kokonaan, kirjaudu sisään käyttäjänä Spencer Low ja vahvista seuraavat kohdat:</span><span class="sxs-lookup"><span data-stu-id="6c06f-219">After the sample data completely loads, sign in as the Spencer Low user and confirm the following:</span></span>

- <span data-ttu-id="6c06f-220">Jos Project Service -sovellus on asennettu, siirry kohtaan **Project Service** > **Asetukset** > **Hinnastot**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-220">If the Project Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="6c06f-221">Vahvista, että tietojoukon jokaiselle maalle/alueelle on määritetty laskutus- ja kustannushinnat soveltuvassa valuutassa.</span><span class="sxs-lookup"><span data-stu-id="6c06f-221">Confirm that bill rates and costs rates exist with the appropriate currency for each country/region in the data set.</span></span>

- <span data-ttu-id="6c06f-222">Jos Project Service -sovellus on asennettu, siirry kohtaan **Universal Resource Scheduling** > **Asetukset** > **Organisaatioyksiköt**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-222">If the Project Service application is installed, go to **Universal Resource Scheduling** > **Settings** > **Organizational Units**.</span></span> <span data-ttu-id="6c06f-223">Vahvista, että jokaiseen organisaatioyksikköön (lukuun ottamatta kaupunkikirjauksia) on liitetty soveltuvassa valuutassa oleva kustannushinnasto.</span><span class="sxs-lookup"><span data-stu-id="6c06f-223">Confirm that a cost price list with the appropriate currency has been associated with each org unit (excluding city entries).</span></span> <span data-ttu-id="6c06f-224">Jos joku puuttuu, etsi oikea kustannushinnasto ja liitä se.</span><span class="sxs-lookup"><span data-stu-id="6c06f-224">If any are missing, find and associate the correct cost price list.</span></span>

- <span data-ttu-id="6c06f-225">Jos Field Service -sovellus on asennettu, siirry kohtaan **Project Service** > **Asetukset** > **Hinnastot**</span><span class="sxs-lookup"><span data-stu-id="6c06f-225">If the Field Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="6c06f-226">Varmista, että laskutus- ja kustannushinnat on määritetty.</span><span class="sxs-lookup"><span data-stu-id="6c06f-226">Confirm that bill rates and costs rates exist.</span></span> <span data-ttu-id="6c06f-227">Siirry kohtaan **Field Service** > **Asetukset** > **Hinnastot** ja tarkista, että tietojoukon jokaiselle maalle/alueelle on määritetty laskutus- ja kustannushinnat soveltuvassa valuutassa.</span><span class="sxs-lookup"><span data-stu-id="6c06f-227">Go to **Field Service** > **Settings** > **Price Lists** and check that bill rates and costs rates exist, with the appropriate currency, for each country/region in the data set.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="6c06f-228">![Aktiivisten hinnastojen näyttökuva](media/sample-data-4.png)</span><span class="sxs-lookup"><span data-stu-id="6c06f-228">![Screenshot of active price lists](media/sample-data-4.png)</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="6c06f-229">![Aktiivisten organisaatioyksiköiden näyttökuva](media/sample-data-5.png)</span><span class="sxs-lookup"><span data-stu-id="6c06f-229">![Screenshot of active organizational units](media/sample-data-5.png)</span></span>

## <a name="technical-notes"></a><span data-ttu-id="6c06f-230">Tekniset huomautukset</span><span class="sxs-lookup"><span data-stu-id="6c06f-230">Technical notes</span></span>

<span data-ttu-id="6c06f-231">Alla on lisää näiden tietojen asennukseen liittyviä teknisiä tietoja.</span><span class="sxs-lookup"><span data-stu-id="6c06f-231">See below for more technical details on the installation of this data.</span></span>

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a><span data-ttu-id="6c06f-232">Näytetietojen asentaminen aiemmin luotujen tietojen päälle (ei suositella)</span><span class="sxs-lookup"><span data-stu-id="6c06f-232">Installing sample data on top of existing data (not recommended)</span></span>

<span data-ttu-id="6c06f-233">Jos näytetiedot on asennettava olemassa olevan Field Service- tai Project Service -kokeilu- tai esittely-ympäristöön, jossa on jo tietoja, asennusohjelman suorittamat turvallisuuteen liittyvät esitarkistukset on poistettava käytöstä tilapäisesti.</span><span class="sxs-lookup"><span data-stu-id="6c06f-233">If you need to install sample data on top of an existing Field Service or Project Service trial or demo environment that already has data, you'll need to suspend the safety prechecks performed by the installer.</span></span>

<span data-ttu-id="6c06f-234">Jos haluat tehdä niin, siirry **PkgFolder**-kansioon, etsi **DemoDataPreImportConfig.xml**-tiedosto ja avaa se Muistiolla (tai toisella XML-editorilla).</span><span class="sxs-lookup"><span data-stu-id="6c06f-234">To do this, go to the **PkgFolder** folder to find and open the **DemoDataPreImportConfig.xml** file with Notepad (or another XML editor).</span></span>

<span data-ttu-id="6c06f-235">Etsi seuraava arvo ja muuta Tosi-arvo Epätosi-arvoksi:</span><span class="sxs-lookup"><span data-stu-id="6c06f-235">Find the following value, and then change the setting from true to false:</span></span>

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

<span data-ttu-id="6c06f-236">Tämän muutoksen vuoksi asennusohjelma ohittaa joitakin tärkeitä turvallisuustarkistuksia, esimerkiksi seuraavat:</span><span class="sxs-lookup"><span data-stu-id="6c06f-236">This change causes the installer to bypass some important safety checks, including:</span></span>

- <span data-ttu-id="6c06f-237">Vahvistetaan, että aktiivisia **organisaatioyksikkötietueita** on vain yksi, ja annetaan sen nimeksi **Fabrikam US**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-237">Confirming that there is no more than one active **Organizational Unit** record, and then renaming it to **Fabrikam US**.</span></span>

- <span data-ttu-id="6c06f-238">Vahvistetaan, että aktiivisia **työmallitietueita** on vain yksi.</span><span class="sxs-lookup"><span data-stu-id="6c06f-238">Confirming that there is no more than one active **Work Template** record.</span></span>

- <span data-ttu-id="6c06f-239">Vahvistetaan, että aktiivisia **projektiparametritietueita** on vain yksi, ja annetaan sen nimeksi **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-239">Confirming that there is no more than one active **Project Parameter** record, and then renaming that entry to **Parameters**.</span></span>

### <a name="configuration-components"></a><span data-ttu-id="6c06f-240">Määrityksen komponentit</span><span class="sxs-lookup"><span data-stu-id="6c06f-240">Configuration components</span></span>

<span data-ttu-id="6c06f-241">Tässä tuontia edeltävässä määritystiedostossa on useita muita määrityksen komponentteja.</span><span class="sxs-lookup"><span data-stu-id="6c06f-241">There are a number of other configuration components in this pre-import configuration file.</span></span> <span data-ttu-id="6c06f-242">Teknisille käyttäjille tiedoksi, että niitä ovat esimerkiksi seuraavat:</span><span class="sxs-lookup"><span data-stu-id="6c06f-242">For technical users, some of these include:</span></span>

- <span data-ttu-id="6c06f-243">**\<RequiredSolutions\>** määrittää ratkaisun edellyttämät asennukset ja niiden versionumerot.</span><span class="sxs-lookup"><span data-stu-id="6c06f-243">**\<RequiredSolutions\>** specifies prerequisite solution installations and their version numbers.</span></span>

- <span data-ttu-id="6c06f-244">**\<InstallSampleData\>** määrittää, onko sovellusten valmiit näytetiedot asennettu.</span><span class="sxs-lookup"><span data-stu-id="6c06f-244">**\<InstallSampleData\>** controls whether out-of-the-box sample data for the apps is installed.</span></span>

    - <span data-ttu-id="6c06f-245">epätosi - ohittaa näiden oletustietojen asennuksen (poistettavissa)</span><span class="sxs-lookup"><span data-stu-id="6c06f-245">false - skips installation of this built-in data (which is removable)</span></span>

    - <span data-ttu-id="6c06f-246">tosi - asentaa oletustiedot yhdessä FS- ja PSA-näytetietojen asennuksen kanssa</span><span class="sxs-lookup"><span data-stu-id="6c06f-246">true - installs the built-in data concurrent with installation of the FS and PSA sample data</span></span>

- <span data-ttu-id="6c06f-247">**\<PreImportDataCollection\>** määrittää vakiotiedoston tietokartat ja liittyvät tietueet, jotka tuodaan ennen päänäytetietojen asennusta.</span><span class="sxs-lookup"><span data-stu-id="6c06f-247">**\<PreImportDataCollection\>** specifies flat-file Data Maps and associated Records to be imported ahead of the main sample data installation.</span></span>

- <span data-ttu-id="6c06f-248">**\<EntitiesToEnableScheduling\>** määrittää, mitkä entiteetit otetaan käyttöön varaukselle Microsoft Dynamics Schedulingissa (eli Universal Resource Schedulingissa).</span><span class="sxs-lookup"><span data-stu-id="6c06f-248">**\<EntitiesToEnableScheduling\>** specifies which entities should be enabled for Booking in Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span></span>

- <span data-ttu-id="6c06f-249">**\<UsersToCreateAndConfigure\>** määrittää varattavissa olevat resurssit, jotka luodaan (jos niitä ei jo ole) ennen näytetietojen tuontia.</span><span class="sxs-lookup"><span data-stu-id="6c06f-249">**\<UsersToCreateAndConfigure\>** specifies Bookable Resources that will be created (if they don't exist already) before the sample data import executes.</span></span> <span data-ttu-id="6c06f-250">Ota huomioon, että lähdejärjestelmän näytetietojen varattavissa oleva resurssi vastaa kohdejärjestelmän varattavissa olevan resurssin tietueita FullName-kohdassa ja kunkin resurssin sisäänkirjauksessa.</span><span class="sxs-lookup"><span data-stu-id="6c06f-250">Note that the source system sample data Bookable Resource match with the target system Bookable Resource records on the FullName and login of each resource.</span></span> <span data-ttu-id="6c06f-251">Tämän vuoksi esimääritystiedoston nimiä EI voi muuttaa, ennen kuin näytetiedot on tuotu kohdejärjestelmään käyttämällä näitä nimiä, varattavissa olevat resurssit ja aktivoitujen käyttäjien tietueet on nimetty uudelleen ja tiedot viety uudelleen tuontia varten lopulliseen kohdejärjestelmään (samalla päivitetään vastaavasti **ImportUserMapFile.xml**-tiedoston vanhat ja uudet merkinnät).</span><span class="sxs-lookup"><span data-stu-id="6c06f-251">Therefore, it is NOT possible to change the names in this preconfiguration file unless you first import sample data into a target system using these names, then rename the Bookable Resources to your desired name set along with the Enabled User records, and then export the data again for import into your final destination system (updating the **ImportUserMapFile.xml** Old and New entries accordingly).</span></span>

- <span data-ttu-id="6c06f-252">**\<PluginsToDisable\>** määrittää nimikkeen laajennukset, jotka on poistettava käytöstä näytetietojen tuonnin aikana. Tämän jälkeen ne otetaan uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6c06f-252">**\<PluginsToDisable\>** specifies very discrete line-item plug-ins that must be disabled during the sample data import and then reenabled afterwards.</span></span>

### <a name="fabrikam-robotics-fictitious-scenario"></a><span data-ttu-id="6c06f-253">Fabrikam Robotics -yrityksen kuvitteellinen skenaario</span><span class="sxs-lookup"><span data-stu-id="6c06f-253">Fabrikam Robotics fictitious scenario</span></span>

<span data-ttu-id="6c06f-254">Field Service- ja Project Service -viitetietojen näytetietopaketit asentavat **Fabrikamin valmistuksen perustiedot (v3.0.0.0) -ratkaisun** sekä noin 4 000 tietuetta ja 40 eri entiteettiä.</span><span class="sxs-lookup"><span data-stu-id="6c06f-254">The Field Service and Project Service sample reference data packages install the **Fabrikam Manufacturing Master Data (v3.0.0.0) solution**, along with approximately 4,000 records and approximately 40 different entities.</span></span> <span data-ttu-id="6c06f-255">Field Service- ja Project Service -sovelluksen erilliset näytetietopaketit sisältävät kyseisen sovelluksen **v902FPSMasterData**-näytetietojen alijoukon.</span><span class="sxs-lookup"><span data-stu-id="6c06f-255">The separate sample data packages for Field Service or Project Service contain a subset of the **v902FPSMasterData** sample data for that application.</span></span> <span data-ttu-id="6c06f-256">**Esittelytietopaketti** asentaa **Fabrikamin valmistuksen perustiedot (v3.0.0.7) -ratkaisun**, jossa on noin 22 000 tietuetta 148 entiteetissä.</span><span class="sxs-lookup"><span data-stu-id="6c06f-256">The **Demo Data** package installs the **Fabrikam Manufacturing Demo Data (v3.0.0.7) solution** with approximately 22,000 records across 148 entities.</span></span>

<span data-ttu-id="6c06f-257">Kuvitteellinen Fabrikam Robotics -yritys valmistaa elektronisten laitteiden kokoonpanolinjan robotteja. Yritys on tunnettu tuotteiden laadusta, innovoinnista ja hyvästä asiakaspalvelusta. Siihen kuuluvat esimerkiksi asennuksen suunnittelu, käyttöönotto ja jatkuva ylläpito.</span><span class="sxs-lookup"><span data-stu-id="6c06f-257">The fictional company, Fabrikam Robotics, is a manufacturer of electronic device assembly line robots and is known for their product quality, innovation, and solid customer service, including installation planning, implementation, and ongoing maintenance services.</span></span> <span data-ttu-id="6c06f-258">Fabrikamin pääkonttori on Yhdysvalloissa (Fabrikam US). Sillä on projektikohtaisia palvelutoimintoja Ranskassa, Intiassa, Isossa-Britanniassa ja Sveitsissä.</span><span class="sxs-lookup"><span data-stu-id="6c06f-258">Fabrikam is headquartered in the United States (Fabrikam US), and has project-based service operations in France, India, the United Kingdom, and Switzerland.</span></span>

<span data-ttu-id="6c06f-259">Kenttäpalvelutoiminnot on keskitetty Yhdysvaltoihin ja siellä enimmäkseen Seattlen alueelle.</span><span class="sxs-lookup"><span data-stu-id="6c06f-259">Field service operations are centered in the United States, mostly in the greater Seattle area.</span></span> <span data-ttu-id="6c06f-260">Yritys hyödyntää esineiden internetiä (IoT), jonka avulla on mahdollista seurata asiakasresurssien suorituskykyä ja tarjota entistäkin proaktiivisempaa asiakaspalvelua asiakkaan tiloissa.</span><span class="sxs-lookup"><span data-stu-id="6c06f-260">The company is focused on leveraging Internet of Things (IoT) connectivity to monitor customer asset performance and deliver increasingly proactive onsite services.</span></span>

<span data-ttu-id="6c06f-261">Näytetietojen korkean tason yleiskatsaus on seuraava:</span><span class="sxs-lookup"><span data-stu-id="6c06f-261">A high-level overview of the sample data is as follows:</span></span>

- <span data-ttu-id="6c06f-262">Yleiset näytetietoelementit (kuuluvat kumpaankin sovellukseen)</span><span class="sxs-lookup"><span data-stu-id="6c06f-262">Common sample data elements (included for both applications)</span></span>

    - <span data-ttu-id="6c06f-263">1 käyttäjä</span><span class="sxs-lookup"><span data-stu-id="6c06f-263">1 user</span></span>

    - <span data-ttu-id="6c06f-264">71 asiakasta</span><span class="sxs-lookup"><span data-stu-id="6c06f-264">71 accounts</span></span>

    - <span data-ttu-id="6c06f-265">137 yhteyshenkilöä</span><span class="sxs-lookup"><span data-stu-id="6c06f-265">137 contacts</span></span>

    - <span data-ttu-id="6c06f-266">Erilaisia tapahtumatyyppejä ja -luokkia</span><span class="sxs-lookup"><span data-stu-id="6c06f-266">Various transaction types and categories</span></span>

    - <span data-ttu-id="6c06f-267">50 tuotetta ja 1 tuotehinnasto</span><span class="sxs-lookup"><span data-stu-id="6c06f-267">50 products with 1 product price list</span></span>

    - <span data-ttu-id="6c06f-268">14 hintaa/kustannushinnastot</span><span class="sxs-lookup"><span data-stu-id="6c06f-268">14 price/cost lists</span></span>

    - <span data-ttu-id="6c06f-269">31 ominaisuutta (resurssin osaamisaluetta) 2 luokitusmallissa ja 3 tasolla (luokitusarvot)</span><span class="sxs-lookup"><span data-stu-id="6c06f-269">31 characteristics (resource skills) in 2 rating models with 3 levels (rating values)</span></span>

- <span data-ttu-id="6c06f-270">Project Service</span><span class="sxs-lookup"><span data-stu-id="6c06f-270">Project Service</span></span>

    - <span data-ttu-id="6c06f-271">8 organisaatioyksikköä</span><span class="sxs-lookup"><span data-stu-id="6c06f-271">8 organizational units</span></span>

    - <span data-ttu-id="6c06f-272">6 roolikohtaisia käyttötasoa</span><span class="sxs-lookup"><span data-stu-id="6c06f-272">6 role-specific utilization levels</span></span>

    - <span data-ttu-id="6c06f-273">2,8 k + roolihinnan määritykset</span><span class="sxs-lookup"><span data-stu-id="6c06f-273">2.8k+ role-price specifications</span></span>

- <span data-ttu-id="6c06f-274">Field Service</span><span class="sxs-lookup"><span data-stu-id="6c06f-274">Field Service</span></span>

    - <span data-ttu-id="6c06f-275">4 aluetta</span><span class="sxs-lookup"><span data-stu-id="6c06f-275">4 territories</span></span>

    - <span data-ttu-id="6c06f-276">5 työtilaustyyppiä</span><span class="sxs-lookup"><span data-stu-id="6c06f-276">5 work order types</span></span>

    - <span data-ttu-id="6c06f-277">22 asiakasresurssia</span><span class="sxs-lookup"><span data-stu-id="6c06f-277">22 customer assets</span></span>

    - <span data-ttu-id="6c06f-278">9 tapauksen tyyppiä ja liittyviä resurssin ominaisuuksia (9), palveluita (13) ja palvelutehtäviä (13)</span><span class="sxs-lookup"><span data-stu-id="6c06f-278">9 incident types with a range of associated resource characteristics (9), services (13) and service tasks (13)</span></span>
   
<span data-ttu-id="6c06f-279">**Esittelytietopaketti** asentaa noin 179 työtilausta, 12 projektia ja liitetyt liiketapahtumatiedot.</span><span class="sxs-lookup"><span data-stu-id="6c06f-279">The **Demo Data** package installs approximately 179 work orders, 12 projects, and associated transactional data.</span></span> 

### <a name="change-the-work-hours-for-sample-resources"></a><span data-ttu-id="6c06f-280">Näyteresurssien työtuntien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="6c06f-280">Change the work hours for sample resources</span></span>

<span data-ttu-id="6c06f-281">Kaikilla varattavissa olevilla resursseilla on 24 työtunnin oletuskalenteri.</span><span class="sxs-lookup"><span data-stu-id="6c06f-281">By default, all bookable resources have a 24 work hours calendar.</span></span>

<span data-ttu-id="6c06f-282">Jos haluat muuttaa varattavissa olevien näyteresurssien työtunteja, siirry kohtaan **Universal Resource Scheduling** > **Aikataulutus** > **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-282">If you need to change the work hours for sample bookable resources, go to **Universal Resource Scheduling** > **Scheduling** > **Resources**.</span></span>

<span data-ttu-id="6c06f-283">Valitse käyttäjä (esimerkiksi Spencer Low) ja muuta käyttäjän työtunnit. Tätä asetusta käytetään useilla käyttäjillä.</span><span class="sxs-lookup"><span data-stu-id="6c06f-283">Select a user (for example, Spencer Low) and change Spencer's work hours to the hours you want to apply to multiple users.</span></span> <span data-ttu-id="6c06f-284">Siirry kohtaan **Universal Resource Scheduling** > **Asetukset** > **Työtuntimallit** ja muokkaa **Oletustyömalli**-tietuetta.</span><span class="sxs-lookup"><span data-stu-id="6c06f-284">Go to **Universal Resource Scheduling** > **Settings** > **Work Hour Templates** and edit the **Default Work Template** record.</span></span> <span data-ttu-id="6c06f-285">Valitse **Malliresurssi**-kentässä käyttäjä, jonka työtunnit haluat ottaa käyttöön muissa resursseissa.</span><span class="sxs-lookup"><span data-stu-id="6c06f-285">In the **Template Resource** field, select a user with work hours that you want to apply to other resources.</span></span> <span data-ttu-id="6c06f-286">Siirry kohtaan **Universal Resource Scheduling** > **Aikataulutus** > **Resurssit** > **Aktiiviset varattavissa olevat resurssit**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-286">Go to **Universal Resource Scheduling** > **Scheduling** > **Resources** > **Active Bookable Resources**.</span></span> <span data-ttu-id="6c06f-287">Valitse muutettavat resurssit ja valitse sitten **Määritä kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="6c06f-287">Select the resources you want to change, and then select **Set Calendar**.</span></span> <span data-ttu-id="6c06f-288">Valitse avattavasta **Työmalli**-luettelosta **Oletustyötunti**-malli tai toinen malli, jossa on oikea malliresurssi.</span><span class="sxs-lookup"><span data-stu-id="6c06f-288">On the **Work Template** drop-down list, select the **Default Work Hour** template or another template with the correct templating resource.</span></span> <span data-ttu-id="6c06f-289">Nyt aikataulutaulukossa pitäisi näkyä resurssien päivitetyt työtunnit.</span><span class="sxs-lookup"><span data-stu-id="6c06f-289">When you go to the schedule board, you should see that the resources now have updated work hours.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="6c06f-290">![Aktiivisten varattavissa olevien resurssien näyttökuva](media/sample-data-6.png)</span><span class="sxs-lookup"><span data-stu-id="6c06f-290">![Screenshot of active bookable resources](media/sample-data-6.png)</span></span>
