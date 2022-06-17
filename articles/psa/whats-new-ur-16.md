---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 16, V3
description: Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista Project Service Automationin päivitysjulkaisussa 16, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e4429ace3d8206369b91917cf87f6968fbb12277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926496"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation -päivitysjulkaisu 16, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.  Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja on aiheessa [Ensisijaisen ratkaisun asentaminen tai päivittäminen](/dynamics365/project-service/upgrade-psa-home-page).
Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita PSA V3:n päivitysjulkaisussa 16. Tällä versiolla on koontinumero V3.10.6.34 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä tammikuusta 2020 lähtien.


## <a name="update-release-16"></a>Päivitysjulkaisu 16

### <a name="bug-fixes"></a>Ohjelmistovirheiden korjaukset

-   Aika ja kulu

    -   Korjattu: Käyttäjät, jotka yrittävät lähettää poistettuja aika- ja kulumerkintöjä hyväksyttäväksi, näkevät nyt asiaankuuluvat virhesanomat.

-   Projektinhallinta

    -   Korjattu: Malleissa ryhmän jäsenille määritettyjä resursointiyksiköitä noudatetaan ja malleja sovelletaan uuteen projektiin.

    -   Korjattu: Parannettu tietueiden omistajuuden uudelleenkohdistuksen käsittelyä.

    -   Korjattu: Projekteja, joita kopioidaan parhaillaan, ei voi kopioida ennen kuin kaikki kopiointitoiminnot on suoritettu loppuun.

-   Resurssienhallinta

    -   Korjattu: Laajennetut varaukset käsittelevät nyt lyhyet kestot oikein eivätkä luo nollatunteja laajennetuille varauksille.

    -   Korjattu: Täsmäytysnäkymä muodostetaan nyt, kun projektin aikavyöhyke on +5:30 GMT ja käyttäjän aikavyöhyke on jokin muu.

-   Sales

    -   Korjattu: Kun sopimusriviin yhdistetty projekti poistetaan ja uusi projekti yhdistetään, uuden projektin todellisten tietueita ei arvioitu uudelleen sopimusrivillä määritettyjen laskutus- ja hinnoittelusääntöjen perusteella. Tämä on korjattu tässä julkaisussa. Uuden yhdistetyn projektin hinnoittelu ja todelliset tietueet palautetaan ja luodaan uudelleen oikein sopimusrivin hinnoittelu- ja laskutussääntöjen perusteella. Myös yhdistämättömän projektin todelliset tietueet arvioidaan ja luodaan uudelleen tämän seurauksena.

    -   Korjattu: Arviorivin **Summa**-kenttään lisätty lisätarkistus, joka varmistaa, että null-arvot eivät säily.

    -   Korjattu: Kun projektin todelliset arvot on päivitetty, projektin päälomakkeeseen on lisätty päivityspainike, jotta käyttäjät voivat synkronoida todelliset arvot uudelleen.

    -   Korjattu: Kun käyttäjät päivittävät versiosta 2.X versioon 3.X, projektit, joiden nimi on NULL, ovat sallittuja.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
