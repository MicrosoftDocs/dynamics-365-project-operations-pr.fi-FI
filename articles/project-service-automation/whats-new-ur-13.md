---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 13, V3
description: Tässä aiheessa on tietoja Project Service Automation -päivitysversion 13, V3:n uusista ominaisuuksista.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751174"
---
# <a name="project-service-automation-v3-update-release-13"></a>Project Service Automation V3, päivitysjulkaisu 13
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
     - Korjattu: Yilmääräiset **Uusi mahdollisuus**-, **Tarjous**-, **Tilausrivi**- ja **Lisää tuote** -painikkeet näkyvät Mahdollisuudet-, Tarjoukset- ja Tilaa tuotteita -kohtien komennoissa sekä projektipohjaisten rivien aliruudukossa.


