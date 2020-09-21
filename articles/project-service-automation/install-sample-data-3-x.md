---
title: Näytetietojen asennus.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: kfend
ms.suite: ''
ms.technology: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.assetid: 8580fc8b-868a-42a3-aa04-2afab28d6de4
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 1c1300116fe42091620267fb128ca6c63184970e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751100"
---
# <a name="sample-data-installation-for-the-project-service-application"></a><span data-ttu-id="c7ece-102">Näytetietojen asennus Project Service -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="c7ece-102">Sample data installation for the Project Service application</span></span>

<span data-ttu-id="c7ece-103">Jos haluat luoda omia esittely-ympäristöjä, voit käyttää Microsoftin ladattavissa olevia näytetietopaketteja, joissa esitellään sovellustesi ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="c7ece-103">To help you build your own demo environments, Microsoft provides downloadable sample data packages that showcase the capabilities of your apps.</span></span> <span data-ttu-id="c7ece-104">Näytetietopaketteja on kahta tyyppiä:</span><span class="sxs-lookup"><span data-stu-id="c7ece-104">There are two types of sample data packages:</span></span>
- <span data-ttu-id="c7ece-105">viite- ja asetustiedot</span><span class="sxs-lookup"><span data-stu-id="c7ece-105">reference/setup data</span></span>
- <span data-ttu-id="c7ece-106">esittelytiedot (viite- ja asetustiedot ja liiketapahtumatiedot, kuten työtilaukset ja projektit)</span><span class="sxs-lookup"><span data-stu-id="c7ece-106">demo data (reference/setup and transactional data such as work orders and projects)</span></span>

<span data-ttu-id="c7ece-107">**Viitteiden** näytetietopaketit ovat ladattavissa kolmessa erillisessä paketissa. Voit siis asentaa vain Project Service- tai vain Field Service -sovelluksen näytetiedot tai molempien sovellusten näytetiedot kerralla.</span><span class="sxs-lookup"><span data-stu-id="c7ece-107">The sample **reference** data packages are downloadable in three different packages, so you can install data only for Project Service, or only for Field Service, or you can install sample data for both applications at once.</span></span>

<span data-ttu-id="c7ece-108">Asetus- ja viitetietojen näytetietopaketit:</span><span class="sxs-lookup"><span data-stu-id="c7ece-108">The sample setup/reference data packages are:</span></span>

- [<span data-ttu-id="c7ece-109">**V902PSMasterData** - vain Project Service -sovelluksen versio 3.x</span><span class="sxs-lookup"><span data-stu-id="c7ece-109">**V902PSMasterData** - Project Service version 3.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [<span data-ttu-id="c7ece-110">**V902FSMasterData** - vain Field Service -sovelluksen versio 8.x</span><span class="sxs-lookup"><span data-stu-id="c7ece-110">**V902FSMasterData** - Field Service version 8.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [<span data-ttu-id="c7ece-111">**V902FPSMasterData** - Field Service -sovelluksen versio 8.x ja Project Service -sovelluksen versio 3.x</span><span class="sxs-lookup"><span data-stu-id="c7ece-111">**V902FPSMasterData** - Field Service 8.x and Project Service 3.x</span></span>](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

<span data-ttu-id="c7ece-112">Uusin **esittelytietojen**tietopaketti:</span><span class="sxs-lookup"><span data-stu-id="c7ece-112">The latest **demo** data package is:</span></span>

 - [<span data-ttu-id="c7ece-113">**FPSDemoData** - Field Service 8.x ja Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="c7ece-113">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span></span>](https://aka.ms/fpsdemodatapackage)

   <span data-ttu-id="c7ece-114">Asennusohjeet poikkeavat hieman sen mukaan, luoko vai määrittääkö käyttäjä osan, mutta muuten ohjeet ovat samat kuin edellisessä [**blogikirjoituksessa**](https://aka.ms/fpsdemodatablog).</span><span class="sxs-lookup"><span data-stu-id="c7ece-114">Installation instructions differ slightly in the users to create and configure section but the rest is the same as in the previous [**blog post**](https://aka.ms/fpsdemodatablog).</span></span> <span data-ttu-id="c7ece-115">Tässä paketissa on rajoitettu esittelytietojoukko, ja sen asentaminen kestää noin 3 tuntia.</span><span class="sxs-lookup"><span data-stu-id="c7ece-115">This package features a reduced demo data set and takes approximately 3 hours to install.</span></span>

<span data-ttu-id="c7ece-116">Nämä näytetietopaketit ovat saatavana vain englanninkielisinä.</span><span class="sxs-lookup"><span data-stu-id="c7ece-116">These sample data packages are available in English only.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c7ece-117">**Näytetietojen asennusta ei voi peruuttaa.**</span><span class="sxs-lookup"><span data-stu-id="c7ece-117">**There is no way to uninstall the sample data.**</span></span> <span data-ttu-id="c7ece-118">Nämä paketit tulee asentaa vain esittely-, arviointi-, koulutus- tai testijärjestelmiin.</span><span class="sxs-lookup"><span data-stu-id="c7ece-118">You should only install these packages on demonstration, evaluation, training, or test systems.</span></span> <span data-ttu-id="c7ece-119">Huomaa myös, että yksittäisen paketin asennuksen jälkeen toisen yksittäisen paketin asennusta ei tueta.</span><span class="sxs-lookup"><span data-stu-id="c7ece-119">Also note that installing an individual package, and then installing the other individual package, is not supported.</span></span> <span data-ttu-id="c7ece-120">(Toisin sanoen et voi asentaa **FSMasterData**-pakettia ja sen jälkeen **PSMasterData**-pakettia tai päin vastoin) Jos tarvitset jossakin vaiheessa molempien sovellusten näytetietoja, asennettavan paketin tulee olla **v902FPSMasterData**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-120">(In other words, you can't install **FSMasterData** followed by **PSMasterData**, or vice versa.) If you see yourself needing sample data for both applications at any point in the future, you should install the **v902FPSMasterData** package.</span></span>

<span data-ttu-id="c7ece-121">Kun asennat jonkin näytetietopaketin, asennusprosessi suorittaa seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="c7ece-121">When you install any of the sample data packages, the installation process performs the following actions:</span></span>

- <span data-ttu-id="c7ece-122">Luo tai määrittää oletusparametrit, joiden avulla käytetään Project Service- tai Field Service -sovellusta tai molempia sovelluksia (jos käytettävissä).</span><span class="sxs-lookup"><span data-stu-id="c7ece-122">Creates or sets default parameters for using Project Service, Field Service, or both applications (if applicable).</span></span>

- <span data-ttu-id="c7ece-123">Tuo sovellusten näytetiedot, kuten varattavat resurssit, sovelluskohtaiset roolit, myynti- ja kustannushinnastot, organisaatioyksiköt, myyntiprosessitietueet ja muut entiteetit, joiden avulla esitellään tärkeimpiä ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="c7ece-123">Imports sample data for the applications, such as bookable resources, application-specific roles, sales and cost price lists, organizational units, sales process records, and other entities to demonstrate key capabilities.</span></span>  

<span data-ttu-id="c7ece-124">**Esittelytietopaketti** sisältää edellä olevat ja lisää liiketapahtumatietoja, kuten työtilauksia ja projekteja.</span><span class="sxs-lookup"><span data-stu-id="c7ece-124">With the **demo data** package, you get the above and additional transactional data such as work orders and projects.</span></span>

<span data-ttu-id="c7ece-125">Haluatko tietää, millaisia ominaisuuksia voit esitellä näytetietojen kanssa?</span><span class="sxs-lookup"><span data-stu-id="c7ece-125">Wondering what capabilities you can demo with the sample data?</span></span> <span data-ttu-id="c7ece-126">Katso kuvitteellinen Fabrikam Robotics -skenaario [teknisissä huomautuksissa](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="c7ece-126">See the Fabrikam Robotics fictitious scenario in [Technical notes](#technical-notes).</span></span>

<span data-ttu-id="c7ece-127">Jos sinulla on näiden näytetietopakettien asentamiseen liittyviä kysymyksiä, [lähetä sähköpostiviesti osoitteeseen fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c7ece-127">If you have questions about installing these sample data packages, [send us an email at fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7ece-128">Vaatimukset</span><span class="sxs-lookup"><span data-stu-id="c7ece-128">Requirements</span></span>

<span data-ttu-id="c7ece-129">Asennustoiminnoissa edellytetään, että kohdeilmentymä (organisaatio) täyttää seuraavat vaatimukset:</span><span class="sxs-lookup"><span data-stu-id="c7ece-129">The installation protocol assumes the following about your target instance (org):</span></span>

- <span data-ttu-id="c7ece-130">Peruskieli on englanti ja perusvaluutta Yhdysvaltain dollari (USD,$).</span><span class="sxs-lookup"><span data-stu-id="c7ece-130">Base language is English and base currency is US dollar (USD,$).</span></span>

- <span data-ttu-id="c7ece-131">Organisaatiolla ei ole Project Service- tai Field Service -tietoja tai sillä on vain oletustiedot, jotka tulevat minkä tahansa uuden organisaation mukana.</span><span class="sxs-lookup"><span data-stu-id="c7ece-131">The org has no Project Service or Field Service data already, or only has barebones default data that comes with any new org.</span></span>

- <span data-ttu-id="c7ece-132">Yrityssovelluksen oikea versio on jo asennettu:</span><span class="sxs-lookup"><span data-stu-id="c7ece-132">The correct version of the business application is already installed:</span></span>
       
    - <span data-ttu-id="c7ece-133">**FPSDemoData tai v902FPSMasterData:** Organisaatioon on asennettu Field Service -sovelluksen versio 8.x ja Project Service -sovelluksen versio 3.x.</span><span class="sxs-lookup"><span data-stu-id="c7ece-133">**For FPSDemoData or v902FPSMasterData:** The org has Field Service version 8.x and Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="c7ece-134">**v902PSMasterData:** Organisaatioon on asennettu Project Service -sovelluksen versio 3.x.</span><span class="sxs-lookup"><span data-stu-id="c7ece-134">**For v902PSMasterData:** The org has Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="c7ece-135">**v902FSMasterData:** Organisaatioon on asennettu Field Service -sovelluksen versio 8.x.</span><span class="sxs-lookup"><span data-stu-id="c7ece-135">**For v902FSMasterData:** The org has Field Service version 8.x installed.</span></span>

> [!NOTE]
> <span data-ttu-id="c7ece-136">Jos näytetiedot on asennettava olemassa olevan Project Service- tai Field Service -kokeilu- tai esittely-ympäristöön, jossa on jo tietoja (ei suositella), asennusohjelman suorittamat turvallisuuteen liittyvät esitarkistukset on poistettava käytöstä tilapäisesti.</span><span class="sxs-lookup"><span data-stu-id="c7ece-136">If you need to install the sample data on top of an existing Project Service and Field Service trial or demo environment that already has data (not recommended), you'll need to suspend the safety prechecks performed by the installer.</span></span> <span data-ttu-id="c7ece-137">Lisätietoja on alla olevissa teknisissä huomautuksissa.</span><span class="sxs-lookup"><span data-stu-id="c7ece-137">For more information, see the technical notes below.</span></span>

## <a name="prepare-for-installation"></a><span data-ttu-id="c7ece-138">Asennuksen valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="c7ece-138">Prepare for installation</span></span>

<span data-ttu-id="c7ece-139">Asennusohjelma on suoritettava tietokoneella, jossa on käytössä Windowsin uusin versio (Windows 10 on suositeltu versio).</span><span class="sxs-lookup"><span data-stu-id="c7ece-139">You need to run the installer on a computer with a recent version of Windows (Windows 10 preferred).</span></span>

<span data-ttu-id="c7ece-140">Tietokoneessa on oltava verkkoyhteys. **Asennus- tai viitetietojen** asentaminen voi kestää **tunnin**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-140">You should plan for the computer to remain connected to a network, and for the installation to run for up to **1 hour** for **setup/reference data**.</span></span> <span data-ttu-id="c7ece-141">(Yleensä **FPSMasterData**-paketin asennus kestää noin 30 minuuttia. Paketti sisältää kummankin sovelluksen mallitiedot.) **FPSDemoData**-paketin asennus kestää noin **3 tuntia**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-141">(Normally the installation takes around 30 minutes for **FPSMasterData**, which includes sample data for both applications.) For the **FPSDemoData**, the installation will take around **3 hours**.</span></span>

<span data-ttu-id="c7ece-142">Tietokoneen näytönsäästäjätoiminto tulee poistaa käytöstä.</span><span class="sxs-lookup"><span data-stu-id="c7ece-142">The computer should have the screen saver function turned off.</span></span> <span data-ttu-id="c7ece-143">Muussa tapauksessa asennuksen istunnon tunnistetiedot menetetään, kun näytönsäästäjä menee päälle (ellet pidä istuntoa aktiivisena koko ajan).</span><span class="sxs-lookup"><span data-stu-id="c7ece-143">Otherwise, session credentials for the installation may be lost when the screen saver engages (unless you keep your session active throughout).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="c7ece-144">![Näytönsäästäjän asetusten näyttökuva, jossa näytönsäästäjä on poistettu käytöstä](media/sample-data-1.png)</span><span class="sxs-lookup"><span data-stu-id="c7ece-144">![Screenshot of screen saver settings, with screen saver turned off](media/sample-data-1.png)</span></span>

## <a name="download-and-unpack"></a><span data-ttu-id="c7ece-145">Lataaminen ja paketin purkaminen</span><span class="sxs-lookup"><span data-stu-id="c7ece-145">Download and unpack</span></span>

<span data-ttu-id="c7ece-146">Project Service- ja Field Service -näytetietojen asennusohjelma jaetaan automaattisesti purkautuvana suoritettavana tiedostona.</span><span class="sxs-lookup"><span data-stu-id="c7ece-146">The Project Service and Field Service sample data installer is distributed as a self-extracting executable.</span></span> <span data-ttu-id="c7ece-147">Tiedostojen nimet voivat vaihdella näytetietopaketin mukaan. Vaiheet ovat kuitenkin samat asennettavasta paketista riippumatta.</span><span class="sxs-lookup"><span data-stu-id="c7ece-147">The file names may vary depending on the sample data package, but otherwise the steps are the same no matter which package you install.</span></span>

<span data-ttu-id="c7ece-148">Kun paketti on ladattu, suorita .exe-tiedosto ja hyväksy pakatun zip-tiedoston purkamisen ehdot.</span><span class="sxs-lookup"><span data-stu-id="c7ece-148">After downloading a package, run the .exe file, and then accept terms and conditions to unpack the compressed zip file.</span></span> <span data-ttu-id="c7ece-149">Tämän jälkeen tiedoston sisältö puretaan tietokoneen kansioon.</span><span class="sxs-lookup"><span data-stu-id="c7ece-149">You then need to extract contents of that file to a folder on the computer.</span></span>

<span data-ttu-id="c7ece-150">Käyttöjärjestelmästä ja suojausasetuksista riippuen zip-tiedoston purkamisen jälkeen on suoritettava seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="c7ece-150">Depending on the operating system and security settings, you may need to perform the following steps after unpacking the zip file:</span></span>

1. <span data-ttu-id="c7ece-151">Etsi **FPSDemoData.dll**-tiedosto **v902FPSMasterData** / **PackageDeployer_FPSDemoData**-kansiossa ja kaksoisnapsauta sitä.</span><span class="sxs-lookup"><span data-stu-id="c7ece-151">Find and right-click the **FPSDemoData.dll** file in the **v902FPSMasterData** / **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="c7ece-152">Valitse **Poista esto**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-152">Choose **Unblock**.</span></span>

3. <span data-ttu-id="c7ece-153">Valitse **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-153">Select **Apply**.</span></span>

4. <span data-ttu-id="c7ece-154">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-154">Select **OK**.</span></span>


## <a name="create-or-configure-users"></a><span data-ttu-id="c7ece-155">Käyttäjien luominen tai määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c7ece-155">Create or configure users</span></span>

<span data-ttu-id="c7ece-156">**FPSDemoData**-paketti edellyttää kuutta käyttäjää, kun taas **FPSMasterData**-paketit edellyttävät yhtä käyttäjää.</span><span class="sxs-lookup"><span data-stu-id="c7ece-156">The **FPSDemoData** package requires six users while **FPSMasterData** packages require one user.</span></span> <span data-ttu-id="c7ece-157">Viittaa oikeaan, näytetietopaketille tarkoitettuun versioon.</span><span class="sxs-lookup"><span data-stu-id="c7ece-157">Refer to the correct one for your sample data package.</span></span>

## <a name="create-or-configure-users---setupreference-data-packages"></a><span data-ttu-id="c7ece-158">Käyttäjien luominen tai määrittäminen – asetus- ja viitetietopaketit</span><span class="sxs-lookup"><span data-stu-id="c7ece-158">Create or configure users - setup/reference data packages</span></span>

<span data-ttu-id="c7ece-159">**FPSMasterData**-paketti on suunniteltu niin, että se asentaa yhden käyttäjän, jonka nimi on Spencer Low, sekä tässä kuvatut asetukset.</span><span class="sxs-lookup"><span data-stu-id="c7ece-159">The **FPSMasterData** package is designed to install with one user named Spencer Low with the settings described here.</span></span> <span data-ttu-id="c7ece-160">Jotta paketti asentuu oikein, ympäristöösi on luotava käyttäjät (tai käyttäjät on nimettävä uudelleen tilapäisesti), jotta ne vastaavat näytetietojen määritystä.</span><span class="sxs-lookup"><span data-stu-id="c7ece-160">To install the package correctly, you need to create (or temporarily rename) users in your environment to match the incoming sample data configuration.</span></span>

<span data-ttu-id="c7ece-161">Voit luoda tai määrittää käyttäjiä siirtymällä kohtaan **Asetukset** > **Suojaus** > **Käyttäjät** ja tekemällä seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="c7ece-161">To create or configure users, go to **Settings** > **Security** > **Users**, and do the following:</span></span>

1. <span data-ttu-id="c7ece-162">Määritä UserFullname="Spencer Low" ja käyttäjätunnukseksi "spencerl" (**pienet kirjaimet**) projektipäällikön ja käytäntöpäällikön rooleihin.</span><span class="sxs-lookup"><span data-stu-id="c7ece-162">Set UserFullname="Spencer Low" with username "spencerl" (**lowercase**) to the Project Manager and Practice Manager roles.</span></span>

2. <span data-ttu-id="c7ece-163">Valitse käyttäjäksi **Spencer Low** ja valitse sitten **Hallitse rooleja**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-163">Select the **Spencer Low** user, and then select **Manage Roles**.</span></span> <span data-ttu-id="c7ece-164">Etsi **järjestelmänvalvojan** rooli ja valitse se. Myönnä Spencer Low'lle täydet järjestelmänvalvojan oikeudet valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-164">Find and select the **System Administrator** role, and then select **OK** to grant full admin rights to Spencer Low.</span></span> <span data-ttu-id="c7ece-165">Tämän vaihe on välttämätön, koska siinä varmistetaan, että näytetiedot luodaan oikean käyttäjän omistuksen kanssa. Näin näkymien täyttäminen tapahtuu oikein.</span><span class="sxs-lookup"><span data-stu-id="c7ece-165">This step is necessary to ensure that sample records are created with the correct user ownership and therefore populate views correctly.</span></span>

3. <span data-ttu-id="c7ece-166">Päivitä ladatun paketin tietojen yhdistämisen tiedostoon oletuskäyttäjän sähköpostiosoitteet.</span><span class="sxs-lookup"><span data-stu-id="c7ece-166">From the downloaded package, you need to update a data mapping file with email addresses of the default user context.</span></span> <span data-ttu-id="c7ece-167">Avaa **PkgFolder**, etsi **ImportUserMapFile.xml** -tiedosto ja avaa se Muistiossa (tai Visual Studiossa tai toisessa XML-editorissa).</span><span class="sxs-lookup"><span data-stu-id="c7ece-167">To do this, open **PkgFolder**, and then find and open the **ImportUserMapFile.xml** file in Notepad (or Visual Studio or another XML editor).</span></span> <span data-ttu-id="c7ece-168">Määritä **DefaultUserToMapTo=**-kenttään käyttäjän Spencer Low sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="c7ece-168">Set the **DefaultUserToMapTo=** field to the email address of the Spencer Low user.</span></span>

4. <span data-ttu-id="c7ece-169">Jos et käytä Spencer Low'n käyttäjätunnusta **spencerl**, sinun on päivitettävä toinen tiedosto.</span><span class="sxs-lookup"><span data-stu-id="c7ece-169">If you aren't using Spencer Low with username **spencerl**, you need to update an additional file.</span></span> <span data-ttu-id="c7ece-170">Avaa **DemoDataPreImportConfig.xml**-tiedosto ja etsi **userstocreateandconfigure**-tunniste.</span><span class="sxs-lookup"><span data-stu-id="c7ece-170">Open the **DemoDataPreImportConfig.xml** file, and then find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="c7ece-171">Päivitä **\<sisäänkirjauksen\>** tunnisteeksi käyttäjän Spencer Low käyttäjätunnus.</span><span class="sxs-lookup"><span data-stu-id="c7ece-171">Update the **\<login\>** tag with the username of your Spencer Low user.</span></span> <span data-ttu-id="c7ece-172">Lisätietoja on [teknisissä huomautuksissa](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="c7ece-172">For additional details, see [Technical notes](#technical-notes).</span></span>

## <a name="create-or-configure-users---demo-data-package"></a><span data-ttu-id="c7ece-173">Käyttäjien luominen tai muokkaaminen – esittelytietopaketti</span><span class="sxs-lookup"><span data-stu-id="c7ece-173">Create or configure users - demo data package</span></span>

<span data-ttu-id="c7ece-174">Esittelytietopakettia varten tarvitaan kuusi käyttäjää.</span><span class="sxs-lookup"><span data-stu-id="c7ece-174">The demo data package requires six users.</span></span> <span data-ttu-id="c7ece-175">Paketti asennetaan oikein seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="c7ece-175">For the package to install correctly, do the following:</span></span>

 1. <span data-ttu-id="c7ece-176">Luo käyttäjiä tai vaihda väliaikaisesti käyttäjien nimet vastaamaan saapuvaa mallitietomääritystä valitsemalla **Asetukset** > **Suojaus** > **Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-176">Create or temporarily rename existing users to match incoming sample data configuration by going to **Settings** > **Security** > **Users**.</span></span>
 
    <span data-ttu-id="c7ece-177">Näitä rooleja tarvitaan vain henkilöpohjaisissa esittelyissä.</span><span class="sxs-lookup"><span data-stu-id="c7ece-177">These roles are only needed for persona-based demos.</span></span>  
    - <span data-ttu-id="c7ece-178">Käytä kenttätyöntekijänä käyttäjää Fullname="David So"</span><span class="sxs-lookup"><span data-stu-id="c7ece-178">User Fullname="David So" as Field Service Technician</span></span>   
    - <span data-ttu-id="c7ece-179">Käytä asiakaspalvelijana ja kenttäpalvelun aikatauluttajana käyttäjää Fullname="Jamie Reding"</span><span class="sxs-lookup"><span data-stu-id="c7ece-179">User Fullname="Jamie Reding" as Customer Service & Field Service Dispatcher</span></span>   
    - <span data-ttu-id="c7ece-180">Käytä asiakaspäällikkönä käyttäjää Fullname="Molly Clark"</span><span class="sxs-lookup"><span data-stu-id="c7ece-180">User Fullname="Molly Clark" as Account Manager</span></span>   
    - <span data-ttu-id="c7ece-181">Käytä käytäntö- ja projektipäällikkönä käyttäjää Fullname="Spencer Low"</span><span class="sxs-lookup"><span data-stu-id="c7ece-181">User Fullname="Spencer Low" as Practice and Project Manager</span></span>  
    - <span data-ttu-id="c7ece-182">Käytä tiimin jäsenenä käyttäjää Fullname="Veronica Quek"</span><span class="sxs-lookup"><span data-stu-id="c7ece-182">User Fullname="Veronica Quek" as Team Member</span></span>   
    - <span data-ttu-id="c7ece-183">Käyttäjä Fullname="William Contoso"</span><span class="sxs-lookup"><span data-stu-id="c7ece-183">User Fullname="William Contoso"</span></span>
  
2. <span data-ttu-id="c7ece-184">Määritä edellä mainituille kuudelle käyttäjälle järjestelmänvalvojan rooli esittelytietojen tuontia varten, jotta näytetiedot tuodaan oikein.</span><span class="sxs-lookup"><span data-stu-id="c7ece-184">For the purposes of demo data import, assign the six users above the Administrator role so sample records import correctly.</span></span> 

3. <span data-ttu-id="c7ece-185">Avaa **PkgFolder** ja etsi ja avaa sitten **ImportUserMapFile.xml**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-185">Open **PkgFolder** and then find and open **ImportUserMapFile.xml**.</span></span> <span data-ttu-id="c7ece-186">Päivitä **New=**-kentät järjestelmän käyttäjiä vastaaviksi sähköpostiosoitteiksi.</span><span class="sxs-lookup"><span data-stu-id="c7ece-186">Update the **New=** fields to the email addresses of corresponding Users in your system.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="c7ece-187">![Näyttökuva UserMapFile-tiedostosta](media/sample-data-7.png)</span><span class="sxs-lookup"><span data-stu-id="c7ece-187">![Screen shot of UserMapFile](media/sample-data-7.png)</span></span>

4. <span data-ttu-id="c7ece-188">Jos "Spencer Low" -nimisen käyttäjän koko nimellä on eri käyttäjätunnus kuin **"spencerl"**, myös lisätiedosto on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="c7ece-188">If your "Spencer Low" full name user has a different user ID than **"spencerl"**, then you need to update an additional file.</span></span> <span data-ttu-id="c7ece-189">Avaa **DemoDataPreImportConfig.xml** ja etsi **userstocreateandconfigure**-tunniste.</span><span class="sxs-lookup"><span data-stu-id="c7ece-189">Open **DemoDataPreImportConfig.xml** and find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="c7ece-190">Päivitä loginId (kirjainkoolla on merkitystä) **\<login\>**-tunnisteeseen.</span><span class="sxs-lookup"><span data-stu-id="c7ece-190">Update the **\<login\>** tag with the loginId (case-sensitive).</span></span> 

5. <span data-ttu-id="c7ece-191">Ensimmäisen käyttäjän kalenterin (joka on **userstocreateandconfigure**-tunnisteessa) avulla lisätään kaikkien varattavien resurssien työtunnit esittelytietoja tuotaessa.</span><span class="sxs-lookup"><span data-stu-id="c7ece-191">The first user's calendar (in the **userstocreateandconfigure** tag) is used to populate the work hours for all bookable resources on import of demo data.</span></span> <span data-ttu-id="c7ece-192">Valitse **Asetukset** > **Suojaus** > **Käyttäjät**, etsi käyttäjä Spencer Low ja avaa Työtunnit-asetus.</span><span class="sxs-lookup"><span data-stu-id="c7ece-192">Navigate to **Settings** > **Security** > **Users**, find your "Spencer Low" user, and open the "Work Hours" option.</span></span> <span data-ttu-id="c7ece-193">Muokkaa nykyisiä työtunteja valitsemalla **Koko viikoittain toistuva aikataulu alusta loppuun** -asetus.</span><span class="sxs-lookup"><span data-stu-id="c7ece-193">Edit the existing work hours, selecting the **Entire recurring weekly schedule from start to end** option.</span></span> <span data-ttu-id="c7ece-194">Varmista, että **työtunneiksi on määritetty 8.00–17.00 (9 tuntia) maanantaista perjantaihin ja aikavyöhykkeeksi on määritetty Tyynenmeren normaaliaika (USA ja Kanada)**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-194">Ensure the **Work hours are set to 8 AM - 5 PM (9 Hours), Monday to Friday and with the Timezone set to Pacific Time (US & Canada)**.</span></span> <span data-ttu-id="c7ece-195">Tällä tavoin varmistaa, että projekti- ja aikataulutaulukko näkyvät odotetusti.</span><span class="sxs-lookup"><span data-stu-id="c7ece-195">This is needed to ensure that the Project and Schedule board show as expected.</span></span>

<span data-ttu-id="c7ece-196">**Suositus:** Organisaatiolle kannattaa luoda varmuuskopio nyt siltä varalta, että asennuksessa on palattava aloituskohtaan. Näin saattaa käydä, jos näytetietojen asennuksen aikana tapahtuu virhe.</span><span class="sxs-lookup"><span data-stu-id="c7ece-196">**Recommendation:** Consider creating a backup of your org now, in case you need to revert to your starting point if something goes wrong during the sample data installation.</span></span> <span data-ttu-id="c7ece-197">Lisätietoja on kohdassa [Ilmentymien varmuuskopiointi ja palautus](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span><span class="sxs-lookup"><span data-stu-id="c7ece-197">For more information, see [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span></span>

## <a name="run-the-package-deployer"></a><span data-ttu-id="c7ece-198">Suorita Package Deployer</span><span class="sxs-lookup"><span data-stu-id="c7ece-198">Run the Package Deployer</span></span>

1. <span data-ttu-id="c7ece-199">Etsi ja suorita **PackageDeployer.exe**. Se on **v902FPSMasterData**- TAI **PackageDeployer_FPSDemoData**-kansiossa.</span><span class="sxs-lookup"><span data-stu-id="c7ece-199">Find and run **PackageDeployer.exe** in the **v902FPSMasterData** OR **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="c7ece-200">Hyväksy ehdot.</span><span class="sxs-lookup"><span data-stu-id="c7ece-200">Accept the terms and conditions.</span></span>

3. <span data-ttu-id="c7ece-201">Seuraava ikkuna:</span><span class="sxs-lookup"><span data-stu-id="c7ece-201">On the next window:</span></span>

   <span data-ttu-id="c7ece-202">a.</span><span class="sxs-lookup"><span data-stu-id="c7ece-202">a.</span></span> <span data-ttu-id="c7ece-203">Valitse **Office 365**:n käyttöönottotyyppi.</span><span class="sxs-lookup"><span data-stu-id="c7ece-203">Select deployment type **Office 365**.</span></span>

   <span data-ttu-id="c7ece-204">b.</span><span class="sxs-lookup"><span data-stu-id="c7ece-204">b.</span></span> <span data-ttu-id="c7ece-205">Käytä järjestelmänvalvojalle Käyttäjien luominen tai määrittäminen -kohdassa luotua käyttäjää ja salasanaa (Spencer Low ja käyttäjätunnus spencerl).</span><span class="sxs-lookup"><span data-stu-id="c7ece-205">Use the user and password of the system administrator user configured in "Create or configure users" ("Spencer Low" with "spencerl" username).</span></span>

   <span data-ttu-id="c7ece-206">c.</span><span class="sxs-lookup"><span data-stu-id="c7ece-206">c.</span></span> <span data-ttu-id="c7ece-207">Varmista, että **Näytä käytettävissä olevien organisaatioiden luettelo** on valittu.</span><span class="sxs-lookup"><span data-stu-id="c7ece-207">Make sure **Display list of available organizations** is selected.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="c7ece-208">![Näyttökuva Package Deployer -ikkunasta, jossa on valittu Näytä käytettävissä olevien organisaatioiden luettelo](media/sample-data-2.png)</span><span class="sxs-lookup"><span data-stu-id="c7ece-208">![Screenshot of Package Deployer window with "Display list of available organizations" selected](media/sample-data-2.png)</span></span>

4. <span data-ttu-id="c7ece-209">Valitse organisaatio, johon haluat asentaa näytetiedot.</span><span class="sxs-lookup"><span data-stu-id="c7ece-209">Select the organization where you want to install the sample data.</span></span>

5. <span data-ttu-id="c7ece-210">Valitse **Seuraava** niin kauan, kunnes näkyviin tulee **Esittelytietojen asetukset** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="c7ece-210">Select **Next** until you see the **Demo Data Setup** dialog.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="c7ece-211">![Esittelytietojen asennusohjelman tilaikkunan näyttökuva](media/sample-data-3.png)</span><span class="sxs-lookup"><span data-stu-id="c7ece-211">![Screenshot of the demo data installer status window](media/sample-data-3.png)</span></span>

6. <span data-ttu-id="c7ece-212">Ennen kuin jatkat, ota huomioon, että näytetietojen asentaminen voi kestää jopa tunnin (yleensä se kestään noin 10 minuuttia).</span><span class="sxs-lookup"><span data-stu-id="c7ece-212">Before proceeding, note that installing sample data could take up to one hour (normally ~10 minutes).</span></span> <span data-ttu-id="c7ece-213">Varmista, että tietokone on päällä, verkkoyhteys säilyy asennusprosessin ajan ja että istunto pysyy aktiivisena.</span><span class="sxs-lookup"><span data-stu-id="c7ece-213">You'll need to make sure the computer remains on and connected to a network throughout the installation process, and that your session remains active.</span></span>   

7. <span data-ttu-id="c7ece-214">Kun olet valmis, valitse **Seuraava** ja aloita näytetietojen asennusprosessi.</span><span class="sxs-lookup"><span data-stu-id="c7ece-214">When you're ready, click **Next** to start the sample data installation process.</span></span> <span data-ttu-id="c7ece-215">Kun näytetiedot on ladattu, valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-215">After the sample data is loaded, click **Finish**.</span></span>

## <a name="verify-the-sample-data-installation"></a><span data-ttu-id="c7ece-216">Näytetietojen asennuksen tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="c7ece-216">Verify the sample data installation</span></span>

<span data-ttu-id="c7ece-217">Tarkista, että Fabrikam Robotics -yrityksen kuvitteellisen skenaarion tietueet ja entiteettityypit näkyvät halutulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="c7ece-217">For a sanity check, verify that the number of records and types of entities listed in Fabrikam Robotics fictitious scenario appear as expected.</span></span>

<span data-ttu-id="c7ece-218">Kun näytetiedot on ladattu kokonaan, kirjaudu sisään käyttäjänä Spencer Low ja vahvista seuraavat kohdat:</span><span class="sxs-lookup"><span data-stu-id="c7ece-218">After the sample data completely loads, sign in as the Spencer Low user and confirm the following:</span></span>

- <span data-ttu-id="c7ece-219">Jos Project Service -sovellus on asennettu, siirry kohtaan **Project Service** > **Asetukset** > **Hinnastot**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-219">If the Project Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="c7ece-220">Vahvista, että tietojoukon jokaiselle maalle/alueelle on määritetty laskutus- ja kustannushinnat soveltuvassa valuutassa.</span><span class="sxs-lookup"><span data-stu-id="c7ece-220">Confirm that bill rates and costs rates exist with the appropriate currency for each country/region in the data set.</span></span>

- <span data-ttu-id="c7ece-221">Jos Project Service -sovellus on asennettu, siirry kohtaan **Universal Resource Scheduling** > **Asetukset** > **Organisaatioyksiköt**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-221">If the Project Service application is installed, go to **Universal Resource Scheduling** > **Settings** > **Organizational Units**.</span></span> <span data-ttu-id="c7ece-222">Vahvista, että jokaiseen organisaatioyksikköön (lukuun ottamatta kaupunkikirjauksia) on liitetty soveltuvassa valuutassa oleva kustannushinnasto.</span><span class="sxs-lookup"><span data-stu-id="c7ece-222">Confirm that a cost price list with the appropriate currency has been associated with each org unit (excluding city entries).</span></span> <span data-ttu-id="c7ece-223">Jos joku puuttuu, etsi oikea kustannushinnasto ja liitä se.</span><span class="sxs-lookup"><span data-stu-id="c7ece-223">If any are missing, find and associate the correct cost price list.</span></span>

- <span data-ttu-id="c7ece-224">Jos Field Service -sovellus on asennettu, siirry kohtaan **Project Service** > **Asetukset** > **Hinnastot**</span><span class="sxs-lookup"><span data-stu-id="c7ece-224">If the Field Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="c7ece-225">Varmista, että laskutus- ja kustannushinnat on määritetty.</span><span class="sxs-lookup"><span data-stu-id="c7ece-225">Confirm that bill rates and costs rates exist.</span></span> <span data-ttu-id="c7ece-226">Siirry kohtaan **Field Service** > **Asetukset** > **Hinnastot** ja tarkista, että tietojoukon jokaiselle maalle/alueelle on määritetty laskutus- ja kustannushinnat soveltuvassa valuutassa.</span><span class="sxs-lookup"><span data-stu-id="c7ece-226">Go to **Field Service** > **Settings** > **Price Lists** and check that bill rates and costs rates exist, with the appropriate currency, for each country/region in the data set.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="c7ece-227">![Aktiivisten hinnastojen näyttökuva](media/sample-data-4.png)</span><span class="sxs-lookup"><span data-stu-id="c7ece-227">![Screenshot of active price lists](media/sample-data-4.png)</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="c7ece-228">![Aktiivisten organisaatioyksiköiden näyttökuva](media/sample-data-5.png)</span><span class="sxs-lookup"><span data-stu-id="c7ece-228">![Screenshot of active organizational units](media/sample-data-5.png)</span></span>

## <a name="technical-notes"></a><span data-ttu-id="c7ece-229">Tekniset huomautukset</span><span class="sxs-lookup"><span data-stu-id="c7ece-229">Technical notes</span></span>

<span data-ttu-id="c7ece-230">Alla on lisää näiden tietojen asennukseen liittyviä teknisiä tietoja.</span><span class="sxs-lookup"><span data-stu-id="c7ece-230">See below for more technical details on the installation of this data.</span></span>

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a><span data-ttu-id="c7ece-231">Näytetietojen asentaminen aiemmin luotujen tietojen päälle (ei suositella)</span><span class="sxs-lookup"><span data-stu-id="c7ece-231">Installing sample data on top of existing data (not recommended)</span></span>

<span data-ttu-id="c7ece-232">Jos näytetiedot on asennettava olemassa olevan Field Service- tai Project Service -kokeilu- tai esittely-ympäristöön, jossa on jo tietoja, asennusohjelman suorittamat turvallisuuteen liittyvät esitarkistukset on poistettava käytöstä tilapäisesti.</span><span class="sxs-lookup"><span data-stu-id="c7ece-232">If you need to install sample data on top of an existing Field Service or Project Service trial or demo environment that already has data, you'll need to suspend the safety prechecks performed by the installer.</span></span>

<span data-ttu-id="c7ece-233">Jos haluat tehdä niin, siirry **PkgFolder**-kansioon, etsi **DemoDataPreImportConfig.xml**-tiedosto ja avaa se Muistiolla (tai toisella XML-editorilla).</span><span class="sxs-lookup"><span data-stu-id="c7ece-233">To do this, go to the **PkgFolder** folder to find and open the **DemoDataPreImportConfig.xml** file with Notepad (or another XML editor).</span></span>

<span data-ttu-id="c7ece-234">Etsi seuraava arvo ja muuta Tosi-arvo Epätosi-arvoksi:</span><span class="sxs-lookup"><span data-stu-id="c7ece-234">Find the following value, and then change the setting from true to false:</span></span>

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

<span data-ttu-id="c7ece-235">Tämän muutoksen vuoksi asennusohjelma ohittaa joitakin tärkeitä turvallisuustarkistuksia, esimerkiksi seuraavat:</span><span class="sxs-lookup"><span data-stu-id="c7ece-235">This change causes the installer to bypass some important safety checks, including:</span></span>

- <span data-ttu-id="c7ece-236">Vahvistetaan, että aktiivisia **organisaatioyksikkötietueita** on vain yksi, ja annetaan sen nimeksi **Fabrikam US**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-236">Confirming that there is no more than one active **Organizational Unit** record, and then renaming it to **Fabrikam US**.</span></span>

- <span data-ttu-id="c7ece-237">Vahvistetaan, että aktiivisia **työmallitietueita** on vain yksi.</span><span class="sxs-lookup"><span data-stu-id="c7ece-237">Confirming that there is no more than one active **Work Template** record.</span></span>

- <span data-ttu-id="c7ece-238">Vahvistetaan, että aktiivisia **projektiparametritietueita** on vain yksi, ja annetaan sen nimeksi **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-238">Confirming that there is no more than one active **Project Parameter** record, and then renaming that entry to **Parameters**.</span></span>

### <a name="configuration-components"></a><span data-ttu-id="c7ece-239">Määrityksen komponentit</span><span class="sxs-lookup"><span data-stu-id="c7ece-239">Configuration components</span></span>

<span data-ttu-id="c7ece-240">Tässä tuontia edeltävässä määritystiedostossa on useita muita määrityksen komponentteja.</span><span class="sxs-lookup"><span data-stu-id="c7ece-240">There are a number of other configuration components in this pre-import configuration file.</span></span> <span data-ttu-id="c7ece-241">Teknisille käyttäjille tiedoksi, että niitä ovat esimerkiksi seuraavat:</span><span class="sxs-lookup"><span data-stu-id="c7ece-241">For technical users, some of these include:</span></span>

- <span data-ttu-id="c7ece-242">**\<RequiredSolutions\>** määrittää ratkaisun edellyttämät asennukset ja niiden versionumerot.</span><span class="sxs-lookup"><span data-stu-id="c7ece-242">**\<RequiredSolutions\>** specifies prerequisite solution installations and their version numbers.</span></span>

- <span data-ttu-id="c7ece-243">**\<InstallSampleData\>** määrittää, onko sovellusten valmiit näytetiedot asennettu.</span><span class="sxs-lookup"><span data-stu-id="c7ece-243">**\<InstallSampleData\>** controls whether out-of-the-box sample data for the apps is installed.</span></span>

    - <span data-ttu-id="c7ece-244">epätosi - ohittaa näiden oletustietojen asennuksen (poistettavissa)</span><span class="sxs-lookup"><span data-stu-id="c7ece-244">false - skips installation of this built-in data (which is removable)</span></span>

    - <span data-ttu-id="c7ece-245">tosi - asentaa oletustiedot yhdessä FS- ja PSA-näytetietojen asennuksen kanssa</span><span class="sxs-lookup"><span data-stu-id="c7ece-245">true - installs the built-in data concurrent with installation of the FS and PSA sample data</span></span>

- <span data-ttu-id="c7ece-246">**\<PreImportDataCollection\>** määrittää vakiotiedoston tietokartat ja liittyvät tietueet, jotka tuodaan ennen päänäytetietojen asennusta.</span><span class="sxs-lookup"><span data-stu-id="c7ece-246">**\<PreImportDataCollection\>** specifies flat-file Data Maps and associated Records to be imported ahead of the main sample data installation.</span></span>

- <span data-ttu-id="c7ece-247">**\<EntitiesToEnableScheduling\>** määrittää, mitkä Microsoft Dynamics -entiteetit otetaan käyttöön aikataulutuksessa (aka Universal Resource Scheduling).</span><span class="sxs-lookup"><span data-stu-id="c7ece-247">**\<EntitiesToEnableScheduling\>** specifies which entities should be enabled for Booking in Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span></span>

- <span data-ttu-id="c7ece-248">**\<UsersToCreateAndConfigure\>** määrittää varattavissa olevat resurssit, jotka luodaan (jos niitä ei jo ole) ennen näytetietojen tuontia.</span><span class="sxs-lookup"><span data-stu-id="c7ece-248">**\<UsersToCreateAndConfigure\>** specifies Bookable Resources that will be created (if they don't exist already) before the sample data import executes.</span></span> <span data-ttu-id="c7ece-249">Ota huomioon, että lähdejärjestelmän näytetietojen varattavissa oleva resurssi vastaa kohdejärjestelmän varattavissa olevan resurssin tietueita FullName-kohdassa ja kunkin resurssin sisäänkirjauksessa.</span><span class="sxs-lookup"><span data-stu-id="c7ece-249">Note that the source system sample data Bookable Resource match with the target system Bookable Resource records on the FullName and login of each resource.</span></span> <span data-ttu-id="c7ece-250">Tämän vuoksi esimääritystiedoston nimiä EI voi muuttaa, ennen kuin näytetiedot on tuotu kohdejärjestelmään käyttämällä näitä nimiä, varattavissa olevat resurssit ja aktivoitujen käyttäjien tietueet on nimetty uudelleen ja tiedot viety uudelleen tuontia varten lopulliseen kohdejärjestelmään (samalla päivitetään vastaavasti **ImportUserMapFile.xml**-tiedoston vanhat ja uudet merkinnät).</span><span class="sxs-lookup"><span data-stu-id="c7ece-250">Therefore, it is NOT possible to change the names in this preconfiguration file unless you first import sample data into a target system using these names, then rename the Bookable Resources to your desired name set along with the Enabled User records, and then export the data again for import into your final destination system (updating the **ImportUserMapFile.xml** Old and New entries accordingly).</span></span>

- <span data-ttu-id="c7ece-251">**\<PluginsToDisable\>** määrittää nimikkeen laajennukset, jotka on poistettava käytöstä näytetietojen tuonnin aikana. Tämän jälkeen ne otetaan uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="c7ece-251">**\<PluginsToDisable\>** specifies very discrete line-item plug-ins that must be disabled during the sample data import and then reenabled afterwards.</span></span>

### <a name="fabrikam-robotics-fictitious-scenario"></a><span data-ttu-id="c7ece-252">Fabrikam Robotics -yrityksen kuvitteellinen skenaario</span><span class="sxs-lookup"><span data-stu-id="c7ece-252">Fabrikam Robotics fictitious scenario</span></span>

<span data-ttu-id="c7ece-253">Field Service- ja Project Service -viitetietojen näytetietopaketit asentavat **Fabrikamin valmistuksen perustiedot (v3.0.0.0) -ratkaisun** sekä noin 4 000 tietuetta ja 40 eri entiteettiä.</span><span class="sxs-lookup"><span data-stu-id="c7ece-253">The Field Service and Project Service sample reference data packages install the **Fabrikam Manufacturing Master Data (v3.0.0.0) solution**, along with approximately 4,000 records and approximately 40 different entities.</span></span> <span data-ttu-id="c7ece-254">Field Service- ja Project Service -sovelluksen erilliset näytetietopaketit sisältävät kyseisen sovelluksen **v902FPSMasterData**-näytetietojen alijoukon.</span><span class="sxs-lookup"><span data-stu-id="c7ece-254">The separate sample data packages for Field Service or Project Service contain a subset of the **v902FPSMasterData** sample data for that application.</span></span> <span data-ttu-id="c7ece-255">**Esittelytietopaketti** asentaa **Fabrikamin valmistuksen perustiedot (v3.0.0.7) -ratkaisun**, jossa on noin 22 000 tietuetta 148 entiteetissä.</span><span class="sxs-lookup"><span data-stu-id="c7ece-255">The **Demo Data** package installs the **Fabrikam Manufacturing Demo Data (v3.0.0.7) solution** with approximately 22,000 records across 148 entities.</span></span>

<span data-ttu-id="c7ece-256">Kuvitteellinen Fabrikam Robotics -yritys valmistaa elektronisten laitteiden kokoonpanolinjan robotteja. Yritys on tunnettu tuotteiden laadusta, innovoinnista ja hyvästä asiakaspalvelusta. Siihen kuuluvat esimerkiksi asennuksen suunnittelu, käyttöönotto ja jatkuva ylläpito.</span><span class="sxs-lookup"><span data-stu-id="c7ece-256">The fictional company, Fabrikam Robotics, is a manufacturer of electronic device assembly line robots and is known for their product quality, innovation, and solid customer service, including installation planning, implementation, and ongoing maintenance services.</span></span> <span data-ttu-id="c7ece-257">Fabrikamin pääkonttori on Yhdysvalloissa (Fabrikam US). Sillä on projektikohtaisia palvelutoimintoja Ranskassa, Intiassa, Isossa-Britanniassa ja Sveitsissä.</span><span class="sxs-lookup"><span data-stu-id="c7ece-257">Fabrikam is headquartered in the United States (Fabrikam US), and has project-based service operations in France, India, the United Kingdom, and Switzerland.</span></span>

<span data-ttu-id="c7ece-258">Kenttäpalvelutoiminnot on keskitetty Yhdysvaltoihin ja siellä enimmäkseen Seattlen alueelle.</span><span class="sxs-lookup"><span data-stu-id="c7ece-258">Field service operations are centered in the United States, mostly in the greater Seattle area.</span></span> <span data-ttu-id="c7ece-259">Yritys hyödyntää esineiden internetiä (IoT), jonka avulla on mahdollista seurata asiakasresurssien suorituskykyä ja tarjota entistäkin proaktiivisempaa asiakaspalvelua asiakkaan tiloissa.</span><span class="sxs-lookup"><span data-stu-id="c7ece-259">The company is focused on leveraging Internet of Things (IoT) connectivity to monitor customer asset performance and deliver increasingly proactive onsite services.</span></span>

<span data-ttu-id="c7ece-260">Näytetietojen korkean tason yleiskatsaus on seuraava:</span><span class="sxs-lookup"><span data-stu-id="c7ece-260">A high-level overview of the sample data is as follows:</span></span>

- <span data-ttu-id="c7ece-261">Yleiset näytetietoelementit (kuuluvat kumpaankin sovellukseen)</span><span class="sxs-lookup"><span data-stu-id="c7ece-261">Common sample data elements (included for both applications)</span></span>

    - <span data-ttu-id="c7ece-262">1 käyttäjä</span><span class="sxs-lookup"><span data-stu-id="c7ece-262">1 user</span></span>

    - <span data-ttu-id="c7ece-263">71 asiakasta</span><span class="sxs-lookup"><span data-stu-id="c7ece-263">71 accounts</span></span>

    - <span data-ttu-id="c7ece-264">137 yhteyshenkilöä</span><span class="sxs-lookup"><span data-stu-id="c7ece-264">137 contacts</span></span>

    - <span data-ttu-id="c7ece-265">Erilaisia tapahtumatyyppejä ja -luokkia</span><span class="sxs-lookup"><span data-stu-id="c7ece-265">Various transaction types and categories</span></span>

    - <span data-ttu-id="c7ece-266">50 tuotetta ja 1 tuotehinnasto</span><span class="sxs-lookup"><span data-stu-id="c7ece-266">50 products with 1 product price list</span></span>

    - <span data-ttu-id="c7ece-267">14 hintaa/kustannushinnastot</span><span class="sxs-lookup"><span data-stu-id="c7ece-267">14 price/cost lists</span></span>

    - <span data-ttu-id="c7ece-268">31 ominaisuutta (resurssin osaamisaluetta) 2 luokitusmallissa ja 3 tasolla (luokitusarvot)</span><span class="sxs-lookup"><span data-stu-id="c7ece-268">31 characteristics (resource skills) in 2 rating models with 3 levels (rating values)</span></span>

- <span data-ttu-id="c7ece-269">Project Service</span><span class="sxs-lookup"><span data-stu-id="c7ece-269">Project Service</span></span>

    - <span data-ttu-id="c7ece-270">8 organisaatioyksikköä</span><span class="sxs-lookup"><span data-stu-id="c7ece-270">8 organizational units</span></span>

    - <span data-ttu-id="c7ece-271">6 roolikohtaisia käyttötasoa</span><span class="sxs-lookup"><span data-stu-id="c7ece-271">6 role-specific utilization levels</span></span>

    - <span data-ttu-id="c7ece-272">2,8 k + roolihinnan määritykset</span><span class="sxs-lookup"><span data-stu-id="c7ece-272">2.8k+ role-price specifications</span></span>

- <span data-ttu-id="c7ece-273">Field Service</span><span class="sxs-lookup"><span data-stu-id="c7ece-273">Field Service</span></span>

    - <span data-ttu-id="c7ece-274">4 aluetta</span><span class="sxs-lookup"><span data-stu-id="c7ece-274">4 territories</span></span>

    - <span data-ttu-id="c7ece-275">5 työtilaustyyppiä</span><span class="sxs-lookup"><span data-stu-id="c7ece-275">5 work order types</span></span>

    - <span data-ttu-id="c7ece-276">22 asiakasresurssia</span><span class="sxs-lookup"><span data-stu-id="c7ece-276">22 customer assets</span></span>

    - <span data-ttu-id="c7ece-277">9 tapauksen tyyppiä ja liittyviä resurssin ominaisuuksia (9), palveluita (13) ja palvelutehtäviä (13)</span><span class="sxs-lookup"><span data-stu-id="c7ece-277">9 incident types with a range of associated resource characteristics (9), services (13) and service tasks (13)</span></span>
   
<span data-ttu-id="c7ece-278">**Esittelytietopaketti** asentaa noin 179 työtilausta, 12 projektia ja liitetyt liiketapahtumatiedot.</span><span class="sxs-lookup"><span data-stu-id="c7ece-278">The **Demo Data** package installs approximately 179 work orders, 12 projects, and associated transactional data.</span></span> 

### <a name="change-the-work-hours-for-sample-resources"></a><span data-ttu-id="c7ece-279">Näyteresurssien työtuntien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="c7ece-279">Change the work hours for sample resources</span></span>

<span data-ttu-id="c7ece-280">Kaikilla varattavissa olevilla resursseilla on 24 työtunnin oletuskalenteri.</span><span class="sxs-lookup"><span data-stu-id="c7ece-280">By default, all bookable resources have a 24 work hours calendar.</span></span>

<span data-ttu-id="c7ece-281">Jos haluat muuttaa varattavissa olevien näyteresurssien työtunteja, siirry kohtaan **Universal Resource Scheduling** > **Aikataulutus** > **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-281">If you need to change the work hours for sample bookable resources, go to **Universal Resource Scheduling** > **Scheduling** > **Resources**.</span></span>

<span data-ttu-id="c7ece-282">Valitse käyttäjä (esimerkiksi Spencer Low) ja muuta käyttäjän työtunnit. Tätä asetusta käytetään useilla käyttäjillä.</span><span class="sxs-lookup"><span data-stu-id="c7ece-282">Select a user (for example, Spencer Low) and change Spencer's work hours to the hours you want to apply to multiple users.</span></span> <span data-ttu-id="c7ece-283">Siirry kohtaan **Universal Resource Scheduling** > **Asetukset** > **Työtuntimallit** ja muokkaa **Oletustyömalli**-tietuetta.</span><span class="sxs-lookup"><span data-stu-id="c7ece-283">Go to **Universal Resource Scheduling** > **Settings** > **Work Hour Templates** and edit the **Default Work Template** record.</span></span> <span data-ttu-id="c7ece-284">Valitse **Malliresurssi**-kentässä käyttäjä, jonka työtunnit haluat ottaa käyttöön muissa resursseissa.</span><span class="sxs-lookup"><span data-stu-id="c7ece-284">In the **Template Resource** field, select a user with work hours that you want to apply to other resources.</span></span> <span data-ttu-id="c7ece-285">Siirry kohtaan **Universal Resource Scheduling** > **Aikataulutus** > **Resurssit** > **Aktiiviset varattavissa olevat resurssit**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-285">Go to **Universal Resource Scheduling** > **Scheduling** > **Resources** > **Active Bookable Resources**.</span></span> <span data-ttu-id="c7ece-286">Valitse muutettavat resurssit ja valitse sitten **Määritä kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="c7ece-286">Select the resources you want to change, and then select **Set Calendar**.</span></span> <span data-ttu-id="c7ece-287">Valitse avattavasta **Työmalli**-luettelosta **Oletustyötunti**-malli tai toinen malli, jossa on oikea malliresurssi.</span><span class="sxs-lookup"><span data-stu-id="c7ece-287">On the **Work Template** drop-down list, select the **Default Work Hour** template or another template with the correct templating resource.</span></span> <span data-ttu-id="c7ece-288">Nyt aikataulutaulukossa pitäisi näkyä resurssien päivitetyt työtunnit.</span><span class="sxs-lookup"><span data-stu-id="c7ece-288">When you go to the schedule board, you should see that the resources now have updated work hours.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="c7ece-289">![Aktiivisten varattavissa olevien resurssien näyttökuva](media/sample-data-6.png)</span><span class="sxs-lookup"><span data-stu-id="c7ece-289">![Screenshot of active bookable resources](media/sample-data-6.png)</span></span>
