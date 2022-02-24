---
title: Töiden suunnittelu Microsoft Projectissa Project Service -apuohjelmalla | MicrosoftDocs
description: Tässä aiheessa on tietoja Microsoft Project Servicen Microsoft Project -apuohjelman lisäämisestä, määrityksestä ja käytöstä.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 9556feac5481e20bde1c9624c0eccc05385eaa94
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145984"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Töiden suunnittelu Microsoft Projectissa Project Service Automation -apuohjelmalla

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] helpottaa projektinsuunnittelua, kuten arvioita. Voit määrittää työn niin, että kustannukset, tavoite ja myynnin arvot ovat selvillä, kun lopullinen ehdotus lähetetään.  

 Asentamalla [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)]in voit suunnitella työt tutussa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] -ympäristössä. Käytä [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]in tehokkaita suunnittelu- ja hallintatoimintoja ja päivitä projektisuunnitelma sitten Project Service Automationiin.  

> [!IMPORTANT]
> - Jotta SharePointin tiedostojen hallintatoimintoa voi käyttää [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] -tiedostojesi tallentamiseksi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -projekteja varten, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]in järjestelmänvalvojan on otettava tiedostojen hallinta käyttöön. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] on yhteensopiva vain [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Editionin kanssa.  

## <a name="download-and-install-the-add-in"></a>Apuohjelman lataaminen ja asentaminen  
 Varmista, että [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -kirjautumistiedot ovat valmiina. Tarvitset näitä tietoja [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]in ja [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]in välisen yhteyden muodostamiseen.  

1.  Voit ladata tuetun Project Service -versiosi lisäosan [joko V2.X](https://go.microsoft.com/fwlink/?linkid=828268) tai [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956) latauskeskuksesta.  

2.  Napsauta lataamislinkkiä.  

3.  Kun lataus on valmis, asenna apuohjelma valitsemalla **Kyllä**.  

## <a name="configure-the-add-in"></a>Apuohjelman määrittäminen  

1. Avaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ja valitse **Project Service** -välilehti.  

2. Valitse **Yhdistä**.  

3. Anna kirjautumistiedot ja valitse **Kirjaudu**.  

   Voit nyt aloittaa apuohjelman käytön.  

## <a name="read-from-a-template"></a>Mallin lukeminen  
 Lue [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa luodusta ja [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]in kopioidusta mallista ja aloita projektin suunnittelu. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Projektimallin luominen (Project Service Automation)](../psa/create-project-template.md)  

1.  Valitse **Project Service** -välilehdessä **Lue** > **Project Service Automation -projektimalli**.  

2.  Valitse ensin projektimalli luettelosta ja sitten **Avaa**.  

    > [!NOTE]
    >  Mallista Projectiin kopioidut tehtävät määritetään oletusarvoisesti manuaalisesti aikataulutetuksi.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]in roolien delegointi projektin resursseille  

1.  Avaa projekti ja napsauta **Tehtävä**-valintanauhaa.  

2.  Valitse ensin **Gantt-kaavio**-valikko ja valitse sitten **Resurssitaulukko**.  

3.  Napsauta Resurssitaulukko-kohdassa avattavaa **Project Service -resurssirooli** -valikkoa ja valitse Project Service Automation -rooli.  

## <a name="staff-your-project-with-resources"></a>Resurssien valinta projektiin  

1.  Valitse Project Service -välilehdessä ensin rivi ja sitten **Etsi resursseja**.  

2.  Valitse **Varaa resurssi** -näytössä projektissa käytettävä resurssi.  

3.  Valitse ensin **Varaa** ja sitten **OK**.  

## <a name="publish-your-project"></a>Projektin julkaiseminen  
Kun projektisuunnittelu on valmis, seuraavana vaiheena on projekti tuonti ja julkaisu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa.  

Projekti tuodaan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]iin. Hinnoittelu- ja ryhmänmuodostusprosessia käytetään. Avaa projekti [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa ja tarkista, että ryhmä, projektiarviot ja työrakenne on luotu. Seuraavassa taulukossa näkyy, mistä löydät tulokset:


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gantt-kaaviot**   | Tuo tiedot [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]:n **Työrakenne**-näytölle. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Resurssisivu** |   Tuo tiedot [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]:n **Projektiryhmän jäsenet** -näytölle.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Käytön käyttö**    |    Tuo tiedot [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]:n **Projektin arviot** -näyttöön.     |

**Projektin tuominen ja julkaisu**  
1. Valitse **Project Service** -välilehdessä **Julkaise** > **Uusi Project Service Automation -projekti**.  

2. Anna **Julkaise uuteen Project Service -projektiin** -valintaikkunassa **Projektin nimi** ja valitse **Asiakas**.  

3. Voit vaihtoehtoisesti valita **Linkitä projektisuunnitelma Project Service Automationiin** -vaihtoehdon, jolloin suunnitelman Project-tiedosto linkitetään Project Service Automationiin.  

4. Valitse **Julkaise**.  

   Kun Project-tiedosto linkitetään [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]iin, Project-tiedostosta tulee päätiedosto ja [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]in työrakenne on vain luku -muotoinen.  Jos haluat tehdä muutoksia projektisuunnitelmaan, ne on tehtävä [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa ja julkaistava päivityksinä [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa.  

## <a name="edit-a-project-thats-been-imported"></a>Tuodun projektin muokkaaminen  
 Voit tehdä [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]iin tuotuun projektisuunnitelmaan muutoksia kahdella tavalla:  

- Voit avata päätiedoston ja muokata sitä [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa.  

- Voit poistaa tiedoston linkin ja muokata sitä suoraan Project Servicessä. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]ista ladattu tiedosto lukitaan oletusarvoisesti, ja sitä voi muokata vain Projectissa. Jos haluat muokata tiedostoa [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa, tiedoston linkitys on poistettava.  

### <a name="edit-in-pn_microsoft_project"></a>Muokkaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa  

1. Valitse päävalikosta **Project Service** > **Projektit**.  

2. Avaa projektiluettelosta [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa luotu projekti.  

3. Valitse valintanauhassa **Avaa MS Projectissa**. Linkitetty päätiedosto avataan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa.  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Tiedoston linkin poistaminen ja sen muokkaaminen [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Servicessä  

1. Valitse päävalikosta **Project Service** > **Projektit**.  

2. Avaa projektiluettelosta [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa luotu projekti.  

3. Valitse valintanauhassa **Poista projektin linkitys MS Projectista**.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Project-tiedoston lataaminen SharePointiin tai Office-ryhmiin  
 Voit ladata Project-tiedoston SharePointiin, jossa se sijaitsee [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projektin liitetyissä tiedostoissa.  SharePoint-tiedostojen hallinnan määrittäjän on oltava järjestelmänvalvoja, joka voi myös ottaa toiminnon käyttöön Project-entiteetissä. 

 Voit myös ladata Project-tiedoston [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)]iin, jos Office-ryhmät on määritetty.

### <a name="upload-a-file-for-sharepoint"></a>Lataa tiedosto SharePointia varten  

1. Valitse päävalikosta **Project Service** > **Siirrä**.  

2. Valitse **Project Service Automation -projektin asiakirjat**.  

3. Valitse **Ota Avaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa käyttöön** -valintaikkunassa **Kyllä** tai **Ei**.  

   - Jos valitset **Kyllä**, voit valita **Avaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa** -painiketta Project Service Automationissa sekä käynnistää [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]in ja ladata Project-tiedoston SharePoint-tiedostokirjastosta.  

   - Jos valitset **Ei**, **Avaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa** -painikkeen linkki ei toimi.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] -tiedosto sijaitsee [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa tietyn [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -projektin **Tiedostot**-kohdassa.  

### <a name="upload-a-file-for-office-groups"></a>Tiedoston siirtäminen Office-ryhmiin  

1. Valitse päävalikosta **Project Service** > **Siirrä**.  

2. Valitse **Project Service Automation -projektin asiakirjat**.  

3. Valitse **Ota Avaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa käyttöön** -valintaikkunassa **Kyllä** tai **Ei**.  

   - Jos valitset **Kyllä**, voit valita **Avaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa** -painiketta Project Service Automationissa sekä käynnistää [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]in ja ladata Project-tiedoston SharePoint-tiedostokirjastosta.  

   - Jos valitset **Ei**, **Avaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa** -painikkeen linkki ei toimi.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] -tiedosto sijaitsee [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa tietyn [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -projektin **Tiedostot**-kohdassa.  

## <a name="publish--your-project-as-a-template"></a>Projektin julkaiseminen mallina  
 Voit tallentaa projektin ja käyttää sitä uudelleen tallentamalla sen projektimallina [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa.  Projektimalleja ovat [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa uudelleenkäytettäviä projektisuunnitelmia. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Projektimallin luominen (Project Service Automation)](../psa/create-project-template.md)  

1. Valitse **Project Service** -välilehdessä **Julkaise** > **Uusi Project Service Automation -projektimalli**.  

2. Anna **Julkaise uuteen Project Service -malliin** -valintaikkunassa **Projektimallin nimi**.  

3. Voit vaihtoehtoisesti valita **Linkitä projektisuunnitelma Project Service Automationiin** -vaihtoehdon, jolloin Project-tiedosto linkitetään [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]iin.  

4. Valitse **Julkaise**.  

Kun Project-tiedosto linkitetään [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]iin, Project-tiedostosta tulee päätiedosto ja [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -mallin työrakenne on vain luku -muotoinen.  Jos haluat tehdä muutoksia projektisuunnitelmaan, ne on tehtävä [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa ja julkaistava päivityksinä [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa.

## <a name="read-a-resource-loaded-schedule"></a>Resurssin ladatun aikataulun lukeminen

Kun projektia luetaan Project Service Automationista, resurssin kalenteria ei synkronoida työasemaohjelmaan. Jos tehtävien kestoissa, työmäärissä tai lopuissa on eroja, syynä on luultavasti se, että resursseilla ja työpöytäohjelmailla ei ole samaa työtuntimallikalenteria, jota käytetään projektissa.


## <a name="data-synchronization"></a>Tietojen synkronoiminen

Seuraavassa taulukossa kuvataan, miten tiedot synkronoidaan Project Service Automationin ja Microsoft Project -työpöytäapuohjelman välillä.

| **Entiteetti** | **Kenttä** | **Microsoft Project Project Service Automationiin** | **Project Service Automation Microsoft Projectiin** |
| --- | --- | --- | --- |
| Projektin tehtävä | Eräpäivä | ● | - |
| Projektin tehtävä | Arvioitu työmäärä | ● | - |
| Projektin tehtävä | MS Project -asiakastunnus | ● | - |
| Projektin tehtävä | Ylätason tehtävä | ● | - |
| Projektin tehtävä | Project | ● | - |
| Projektin tehtävä | Projektitehtävä | ● | - |
| Projektin tehtävä | Projektitehtävän nimi | ● | - |
| Projektin tehtävä | Resursointiyksikkö (vanhentunut versiossa 3.0) | ● | - |
| Projektin tehtävä | Suunniteltu kesto | ● | - |
| Projektin tehtävä | Aloituspäivämäärä | ● | - |
| Projektin tehtävä | WBS-tunnus | ● | - |

| **Entiteetti** | **Kenttä** | **Microsoft Project Project Service Automationiin** | **Project Service Automation Microsoft Projectiin** |
| --- | --- | --- | --- |
| Ryhmän jäsen | MS Project -asiakastunnus | ● | - |
| Ryhmän jäsen | Toimen nimi | ● | - |
| Ryhmän jäsen | projekti | ● | ● |
| Ryhmän jäsen | Projektiryhmä | ● | ● |
| Ryhmän jäsen | Resursointiyksikkö | - | ● |
| Ryhmän jäsen | Rooli | - | ● |
| Ryhmän jäsen | Työtunnit | Ei synkronoitu | Ei synkronoitu |

| **Entiteetti** | **Kenttä** | **Microsoft Project Project Service Automationiin** | **Project Service Automation Microsoft Projectiin** |
| --- | --- | --- | --- |
| Resurssien delegointi | Päivämäärästä | ● | - |
| Resurssien delegointi | tuntia | ● | - |
| Resurssien delegointi | MS Project -asiakastunnus | ● | - |
| Resurssien delegointi | Suunniteltu työ | ● | - |
| Resurssien delegointi | Project | ● | - |
| Resurssien delegointi | Projektiryhmä | ● | - |
| Resurssien delegointi | Resurssien delegointi | ● | - |
| Resurssien delegointi | Tehtävä | ● | - |
| Resurssien delegointi | Päivämäärään | ● | - |

| **Entiteetti** | **Kenttä** | **Microsoft Project Project Service Automationiin** | **Project Service Automation Microsoft Projectiin** |
| --- | --- | --- | --- |
| Projektitehtävän riippuvuudet | Projektitehtävän riippuvuus | ● | - |
| Projektitehtävän riippuvuudet | Linkkityyppi | ● | - |
| Projektitehtävän riippuvuudet | Edeltäjän tehtävä | ● | - |
| Projektitehtävän riippuvuudet | Project | ● | - |
| Projektitehtävän riippuvuudet | Seuraajan tehtävä | ● | - |

### <a name="see-also"></a>Katso myös  
 [Projektipäällikön opas](../psa/project-manager-guide.md)
