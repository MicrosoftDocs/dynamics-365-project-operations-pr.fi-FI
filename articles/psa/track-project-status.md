---
title: Projektin tilan seuraaminen
description: Projektin tilan seuraaminen Project Servicessä
author: ruhercul
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
ms.openlocfilehash: 32e5867a773206aaed532645302b7f7cc789d5074f9acdb3bbb95acf8492d25e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996702"
---
# <a name="track-a-projects-status-project-service"></a>Seuraa projektin tilaa (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] -palvelussa voit seurata asiakkaan projektin edistymistä.  

Valmistelun edetessä projektin vaiheet päivitetään automaattisesti vastaamaan valmistelun vaihetta:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Uusi**    | Kun luot projektin, vaiheeksi on määritetty **uusi**. Jos projekti on luotu mallista, tässä vaiheessa projektilla voi olla aikataulu, arviot ja ryhmän tiedot. Muussa tapauksessa se on projektin jäsennys, ja sinun on syötettävä manuaalisesti muut projektin osat. |
|  **Tarjous**   |      Kun liität projektin tarjoukseen tai luot sen tarjouksesta, projektivaiheeksi on määritetty **tarjous**, ja arvioitu aloitus- ja päättymispäivät päivitetään myös. Kun projekti on on tarjousvaiheessa, tarjouksen yksityiskohdat näkyvät **Myynti**-välilehdellä **Projekti**-sivulla.      |
|   **Suunnitelma**   |                                     Kun projektiin liittyvä tarjous voittaa ja valmistelu etenee sopimusvaiheeseen, projektivaihe päivittää **suunnitelman**. Sopimuksen tiedot näkyvät **Myynti**-välilehdellä **Projektin**-sivulla.                                      |
| **Valmis** |                    Kun projektin työ on valmis, voit vaihtaa vaiheeksi **Valmis**. Kun projektivaiheeksi on muutettu valmis, on selvää, että työ on suoritettu 100-prosenttisesti, mutta projekti pidetään avoinna, jotta odottavat aika- tai kulumerkinnät kirjataan.                     |
|  **Sulje**   |           Kun kaikki tapahtumat on tallennettu projektiin ja et odota uusia kirjattavaksi, voit manuaalisesti määrittää vaiheeksi **Sulje**. Kun projektin tilaksi on määritetty **Sulje**, et voi kirjautua enää projektin tapahtumiin ja projektin voi vain lukea.           |

## <a name="to-track-a-projects-status"></a>Projektin tilan seuraaminen  

1.  Siirry kohtaan **Project Service > Projektit**.  

2.  Napsauta käsiteltävää projektia.  

3.  Valitse näytön yläosassa olevassa palkissa, projektin nimen vieressä oleva alanuoli ja valitse sitten **Projektin seuranta**.  

4.  Valitse **Työmäärän seuranta** tai **Kustannusten seuranta** tehtäväluettelon yläpuolella olevasta avattavasta luettelosta.  

5.  Voit muokata tehtävää kaksoisnapsauttamalla sitä. Voit muuttaa aikaa ja tehtävän edistymistä myös siirtämällä palkkeja tai muuttamalla niiden kokoa Gantt-kaaviossa.  

### <a name="see-also"></a>Katso myös  
 [Projektipäällikön opas](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]