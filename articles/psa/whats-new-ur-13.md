---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 13, V3
description: Tässä aiheessa on tietoja Project Service Automation -päivitysversion 13, V3:n uusista ominaisuuksista.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: dbdcb811bfeacf17e841d679f097c591c16cd4c0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281024"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation -päivitysjulkaisu 13, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Olemme iloisia voidessamme julkistaa uusimman Dynamics 365 Project Service Automation (PSA) -sovelluksen päivityksen. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, käy Dynamics 365 online -hallintakeskuksessa ja asenna päivitys siirtymällä Ratkaisut-sivulle. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 13. Tällä versiolla on koontinumero V3.10.3.18 ja se on saatavilla seuraavan aikataulun mukaan:

- **Yleinen saatavuus (itsepäivitys):** marraskuu 2019
- **Automaattinen päivitys:** joulukuu 2019


## <a name="update-release-13"></a>Päivitysjulkaisu 13 

### <a name="bug-fixes"></a>Ohjelmistovirheiden korjaukset

- Aika ja kulu

     - Korjattu: **Kulun hyväksyntä** -sivun hakutoiminto ei toimi, kun haetaan kulun tarkoituksen mukaan.

- Resurssienhallinta

     - Korjattu: Täsmäytyksessä numerot on päivitetty oikealle tasatuiksi.
     - Korjattu: Nimettyjä resursseja ei voi delegoida tehtäviin **Ajoitus**-välilehden kautta.

- Projektinhallinta

     - Korjattu: Poikkeus null-viittauksesta, kun määritetään ryhmän jäsentä, kun **TransactionType** puuttuu **Unit**- ja **DefaultGroup**-tiedoista.

- Sales

     - Korjattu: päällekkäiset tapahtumatyyppitietueet palauttavat virheen, kun roolien hintatietueita luodaan.
     - Korjattu: **Uusi mahdollisuus**-, **Tarjous**-, **Tilausrivi**- ja **Lisää tuotteet** -lisäpainikkeet näkyvät mahdollisuuksien, tarjousten, tilaustuotteiden ja projektipohjaisten rivien aliruudukon komennoissa.




[!INCLUDE[footer-include](../includes/footer-banner.md)]