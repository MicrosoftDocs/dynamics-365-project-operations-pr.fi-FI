---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 12, V3
description: Tässä aiheessa on tietoja Project Service Automation -päivitysversion 12, V3:n uusista ominaisuuksista.
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
ms.openlocfilehash: daf0e6c7a4b1b953cb808cfefab74475c47d3996
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143824"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation -päivitysjulkaisu 12, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Olemme iloisia voidessamme julkistaa uusimman Dynamics 365 Project Service Automation (PSA) -sovelluksen päivityksen. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, käy Dynamics 365 online -hallintakeskuksessa ja asenna päivitys siirtymällä Ratkaisut-sivulle. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 12. Tällä versiolla on koontinumero V3.10.2.34 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä lokakuusta 2019 lähtien.

## <a name="update-release-12"></a>Päivitysjulkaisu 12

### <a name="bug-fixes"></a>Ohjelmistovirheiden korjaukset

- Aika ja kulu

    - Korjattu: aikamerkinnän virheviesteihin on päivitetty merkityksellisempiä tietoja.
    - Korjattu: Aikamerkintöjen ruudukko ja aikataulu näyttävät pystysuuntaisen vierityspalkin tarpeen mukaan.
    - Korjattu: Lähetettyjä kulu- ja aikamerkintöjä voidaan hyväksyä.
    - Korjattu: Hyväksynnän peruuttamisen vahvistusvalintaikkunan sanoma on korjattu, jotta se vastaisi hyväksynnän tilaa, kun se muutetaan tilasta **Hyväksytty** tilaan **Lähetetty**.
    - Korjattu: **Hinta**- **Yksikkö**- ja **Määrä**-kentät on nyt lukittu kulutietueessa sen jälkeen, kun se on hyväksytty.

- Projektinhallinta

    - Korjattu: **Uusi**-toiminto **Ryhmän jäsen** -päälomakkeessa on poistettu.
    - Korjattu: Resurssivaraukset on päivitetty epätarkkojen pyöristysten virheiden vuoksi, jotka johtivat tehtävän päättymispäivän muutokseen.
    - Korjattu: Käyttäjä näkee tehtäväruudukossa oleelliset palvelinpuolen virheet.
    - Korjattu: ryhmän jäsenen nimi muodostetaan nyt tehtävän Henkilöt-valitsimella toimen nimen sijaan.

- Resurssienhallinta

    - Korjattu: Mallista luotujen projektien resurssitarvetiedot käyttävät nyt projektikalenteria.
    - Korjattu: Taidot ja kompetenssit siirtyvät nyt oletusarvon mukaan roolien päätiedoista kyseiselle roolille luodulle resurssitarpeelle.

- Sales

    - Korjattu: **Sopimus**-päälomakkeesta löytyi päällekkäisiä objektitunnuksia.
    - Korjattu: logiikka on päivitetty, jotta **Tarjousanalyysi** -välilehti näkyy siten, että se näyttää välilehden metatietomääritykset.
    - Korjattu: Todellisten arvojen tietueen kirjanpitopäivä on nyt peräisin ajan/kulun merkintäpäivämäärästä eikä hyväksynnän päivämäärästä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]