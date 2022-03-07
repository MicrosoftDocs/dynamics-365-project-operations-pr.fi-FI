---
title: Projektin henkilöstön määrittäminen sopimustyöntekijöillä ja alihankitulla kapasiteetilla
description: Tässä aiheeesa selitetään, miten projektin henkilöstö määritetään sopimustyöntekijöillä ja alihankitulla kapasiteetilla Microsoft Dynamics 365 Project Operationsissa.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902854"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Projektin henkilöstön määrittäminen sopimustyöntekijöillä ja alihankitulla kapasiteetilla

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Yleiset projektiryhmän jäsenet voi määrittää työntekijöillä tai sopimustyöntekijöillä. Kun määrität projektin henkilöstöä sopimustyöntekijöillä, voit rajoittaa määritysvaihtoehtoja tiettyihin sopimustyöntekijöihin, jotka on määritetty alihankintariville. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Hae henkilöstöresurssivaatimuksia sopimustyöntekijöillä, jotka kuuluvat tietylle alihankintariville

Voit hakea henkilöstöresurssivaatimuksia sopimustyöntekijöillä, jotka kuuluvat tietylle alihankintariville, seuraavasti:

1. Luo yleinen projektiryhmän jäsen, joka viittaa alihankintaan ja alihankintariviin.
2. Luo resurssitarve kyseistä yleistä projektiryhmän jäsentä varten käyttämällä **Luo tarve** -painiketta projektiryhmän jäsenten aliruudukossa.
3. Valitse ryhmän jäsenen rivi ja valitse **Varaa**-painike aliruudukossa. 
4. Tämä avaa Aikataulutaulukon ja tarvekontekstin. Muiden määritteiden kuten päivämäärä-, rooli- ja organisaatioyksikkökenttien lisäksi Aikataulutaulukon suodattimet täytetään automaattisesti resurssitarpeen toimittaja-, alihankinta- ja alihankintarivikentillä.
5. Järjestelmä etsii resursseja, jotka vastaavat suodatusehtoja, ja näyttää ne luettelossa. 
6. Valitse jokin suodatetuista resursseista ja varaa resurssi tarvetta varten. 
7. Projektiryhmän jäsen luodaan ja se päivitetään alihankinta- ja alihankintariviviitteillä. Siirry kohtaan **Projektiarviot** ja valitse **Päivitä hinnat** nähdäksesi resurssimäärityksen päivitetyn kustannuksen. 

> [!NOTE]
> Projektiryhmän jäsenen päivittäminen alihankinta- ja alihankintariviviitteillä ei ole välttämättä aina mahdollista varauksen aikana, jos resurssi on määritetty useampiin alihankintariveihin. Jos järjestelmä ei pysty päivittämään projektiryhmän jäsentä alihankinnalla ja alihankintarivillä, avaa projektiryhmän jäsentietue ja päivitä kyseiset kentät manuaalisesti niin, että kustannusarvio vastaa tarkasti alihankkijan kustannusta.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Hae ja määritä henkilöstön resurssitarve millä tahansa sopimustyöntekijällä

Voit hakea ja määrittää henkilöstön resurssitarpeen millä tahansa sopimustyöntekijällä seuraavasti:

1. Luo yleinen projektiryhmän jäsen.
2. Luo resurssitarve kyseistä yleistä projektiryhmän jäsentä varten käyttämällä **Luo tarve** -painiketta projektiryhmän jäsenten aliruudukossa.
3. Valitse ryhmän jäsenen rivi ja valitse **Varaa**-painike aliruudukossa. 
4. Tämä avaa Aikataulutaulukon ja tarvekontekstin. Muiden määritteiden kuten päivämäärä-, rooli- ja organisaatioyksikkökenttien lisäksi Aikataulutaulukon suodattimet täytetään automaattisesti resurssitarpeen toimittaja-, alihankinta- ja alihankintarivikentillä. Koska tarpeeseen ei ollut täytetty alihankinta- tai alihankintariviarvoja, kyseiset määritteet näkyvät tyhjinä suodatinruudussa.
5. Järjestelmä etsii resursseja, jotka vastaavat suodatusehtoja, ja näyttää ne luettelossa.
6. Päivitä suodatinruudun **Työntekijätyyppi**-kenttä muotoon **Sopimustyöntekijä** rajataksesi haun sopimustyöntekijöihin. Päivitä suodatinruudun kohta **Toimittaja** valitaksesi toimittajan ja rajataksesi haun näyttämään vain sopimustyöntekijät, jotka kuuluvat tietylle toimittajayritykselle.
7. Valitse sopimustyöntekijä luettelosta ja varaa resurssi tarvetta varten.
8. Projektiryhmän jäsen luodaan. Projektiryhmän jäsentä ei kuitenkaan päivitetä alihankinnalla tai alihankintarivillä, ja siksi resurssin määritystä ei lasketa käyttäen alihankinnan hinnoittelua. Päivitä projektiryhmän jäsen manuaalisesti alihankintarivillä, siirry kohtaan **Projektiarviot** ja valitse **Päivitä hinnat** nähdäksesi resurssimäärityksen päivitetyn kustannuksen.

> [!NOTE]
> Projektiryhmän jäsenet, joiden **Työntekijätyyppi** on **Sopimustyöntekijä**, mutta joilla ei ole alihankintaviitettä, merkitään muotoon **Pätemätön** **Projektiryhmän jäsenet** -ruudukossa. Jos on projektiryhmän jäseniä, joilla on tämä tila, avaa projektiryhmän jäsentietue ja päivitä alihankinta- ja alihankintarivikentät manuaalisesti niin, että kustannusarvio vastaa tarkasti alihankkijan kustannusta **Arviot**-välilehdessä. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
