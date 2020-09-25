---
title: Päivitykseen liittyviä huomioita - Microsoft Dynamics 365 Project Service Automation -versiosta 2.x tai 1.x versioon 3
description: Tässä aiheessa on tietoja asioista, jotka on otettava huomioon päivitettäessä Project Service Automation -versiosta 2.x tai 1.x versioon 3.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: e4fae2ea-9013-488e-a666-f7192dd42c0b
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: ba710eb8c07df7dac97e8b911184c00b87b14548
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751209"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Päivitykseen liittyviä huomioita - PSA:n versio 2.x tai 1.x versioon 3
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation ja Field Service
Sekä Dynamics 365 Project Service Automation että Dynamics 365 Field Service käyttävät Universal Resourcing Scheduling (URS) -ratkaisua resurssien aikatauluttamiseen. Jos ilmentymässäsi on sekä Project Service Automation että Field Service, sinun kannattaa suunnitella molempien ratkaisujen päivittämistä uusimpiin versioihin (Project Service Automation -versioon 3.x ja Field Service -versioon 8.x). Project Service Automationin tai Field Servicen päivittäminen asentaa uusimman URS-version, mikä tarkoittaa, että epäyhtenäinen toiminta on mahdollista, jos saman esiintymän Project Service Automation- ja Field Service -ratkaisuja ei päivitetä uusimpaan versioon.

## <a name="resource-assignments"></a>Resurssien kohdennukset
Project Service Automation -versiossa 2 ja versiossa 1 tehtävien kohdennukset tallennettiin alitehtävinä (kutsutaan myös rivitehtäviksi) **Tehtäväentiteetissä**, ja ne liittyivät epäsuorasti **Resurssien kohdentaminen** -entiteettiin. Rivitehtävä näkyi työrakenteen (WBS) kohdennuksen ponnahdusikkunassa.

![Työrakenteen rivitehtävät Project Service Automation -versiossa 2 ja 1](media/upgrade-line-task-01.png)

Project Service Automation -versiossa 3 sen pohjana oleva rakenne varattavien resurssien kohdentamiseksi tehtäviin on muuttunut. Rivitehtävä on vanhentunut, ja **Tehtäväentiteetin** tehtävän ja **Resurssin kohdennuksen** entiteetin ryhmän jäsenen välillä on suora 1:1 suhde. Projektiryhmän jäsenelle kohdennetut tehtävät tallennetaan nyt suoraan Resurssin kohdennus -entiteettiin.  

Nämä muutokset vaikuttavat sellaisten aiemmin luotujen projektien päivittämiseen, joilla on resurssien kohdennuksia projektiryhmän nimetyille varattaville resursseille ja yleisille resursseille. Tämä aihe sisältää seikkoja, jotka sinun on otettava huomioon projekteissasi, kun päivität versioon 3. 

### <a name="tasks-assigned-to-named-resources"></a>Tehtävät kohdennettuina nimetyille resursseille
Käyttämällä pohjana olevaa tehtäväentiteettiä, tehtävät versiossa 2 ja versiossa 1 sallivat ryhmän jäsenten ottaa muun kuin oletuksena määritetyn roolinsa. Esimerkiksi Karita Repo, joka on oletusarvoisesti kohdennettu ohjelmapäällikön rooliin, voitiin kohdentaa tehtävään, jonka rooli oli Kehittäjä. Versiossa 3 nimetyn ryhmän jäsenen rooli on aina oletus, joten mikä tahansa tehtävä, johon Karita Repo on delegoitu, käyttää hänen ohjelmapäällikön oletusrooliaan.

Jos olet määrittänyt resurssin tehtävän oletusroolin ulkopuolelle versiossa 2 ja versiossa 1, ohjelman päivityksen yhteydessä, nimetylle resurssille kohdennetaan oletusrooli kaikille tehtäväkohdennuksille, riippumatta roolin kohdennuksesta versiossa2. Tämän tuloksena lasketuissa arvioissa on eroja version 2 tai version 1 ja version 3 välillä, koska arviot lasketaan resurssin roolin eikä rivitehtävän kohdennuksen perusteella. Esimerkiksi versiossa 2 kaksi tehtävää on kohdennettu Aurora Harilalle. Rooli rivitehtävälle tehtävässä 1 on Kehittäjä ja tehtävässä 2 ohjelmapäällikkö. Aurora Harilan oletusrooli on ohjelmapäällikkö.

![Useita rooleja yhdellä resurssilla](media/upgrade-multiple-roles-02.png)

Koska kehittäjien ja ohjelmapäällikön roolit eroavat toisistaan, kustannusten ja myynnin arviot ovat seuraavat:

![Resurssiroolien kustannusarviot](media/upggrade-cost-estimates-03.png)

![Resurssiroolien myyntiarviot](media/upgrade-sales-estimates-04.png)

Kun päivität versioon 3, rivitehtävät korvautuvat resurssikohdennuksilla varattavissa olevan resurssiryhmän jäsenen tehtävässä. Kohdennus käyttää varattavissa olevan resurssin oletusroolia. Seuraavassa kuvassa Aurora Harila, jolla on ohjelmapäällikön rooli, on resurssi.

![Resurssien kohdennukset](media/resource-assignment-v2-05.png)

Koska arviot perustuvat resurssin oletusrooliin, myynti- ja kustannusarviot voivat muuttua. Huomaa, että seuraavassa grafiikassa ei enää näy **Kehittäjän** roolia, koska rooliksi on nyt otettu varattavan resurssin oletusrooli.

![Oletusroolien kustannusarviot](media/resource-assignment-cost-estimate-06.png)
![Oletusroolien myyntiarviot](media/resource-assignment-sales-estimate-07.png)

Kun päivitys on valmis, voit muokata ryhmän jäsenen roolin joksikin muuksi kuin oletusarvoksi. Jos kuitenkin muutat ryhmän jäsenen roolia, se muuttuu kaikissa hänelle kohdennetuissa tehtävissä, koska ryhmän jäsenille ei enää sallita useita rooleja versiossa 3.

![Resurssiroolin päivittäminen](media/resource-role-assignment-08.png)

Tämä pätee myös nimetyille resursseille kohdennettuihin rivitehtäviin silloin, kun resurssin organisaatio yksikköä muutetaan oletusarvosta toiseksi organisaatioyksiköksi. Kun version 3 päivitys on valmis, kohdennus käyttää resurssin oletusorganisaatioyksikköä sen sijaan, että se olisi määritetty rivitehtävässä.

### <a name="tasks-assigned-to-generic-resources"></a>Tehtävät kohdennettuina yleisille resursseille
Versiossa 2 ja versiossa 1 voit määrittää roolille ja organisaatioyksikölle tehtävän ja luoda sitten **Luo ryhmä** -ominaisuuden avulla yleisiä resursseja tehtävään määritettyjen määritteiden perusteella. Versiossa 3 luodaan yleisiä ryhmän jäseniä, joilla on rooli ja organisaatioyksikkö, ja ryhmän jäsenet kohdennetaan sen jälkeen tehtäviin.

Versiossa 2 ja versiossa 1 projektit, joilla on yleisiä resursseja, voivat olla kahdessa tilassa tai niiden yhdistelmä tehtävätasolla. Esimerkiksi seuraavat skenaariot ovat mahdollisia:

- Tehtäviä, joiden roolit ja organisaatio yksiköt on määritetty, mutta joille ei ole luotu resurssien kohdennusta.
- Tehtäviä, joilla on yleisten ryhmän jäsenten resurssikohdennuksia, jotka on kohdennettu luomalla yleinen resurssi **Luo ryhmä** -ominaisuuden avulla.

Ennen kuin aloitat päivityksen, suosittelemme, että luot ryhmän uudelleen kullekin projektille, jolla on yleisille resursseihin kohdennettuja tehtäviä, tai joille ei ole vielä suoritettu ryhmänluontiprosessia.

Tehtäville, jotka on kohdennettu yleisille ryhmän jäsenille, jotka luotiin **Luo ryhmä** -toiminnolla, päivitys jättää yleiset resurssit ryhmään ja jättää kohdennuksen kyseiselle ryhmän jäsenelle. Suosittelemme, että luot yleiselle ryhmän jäsenelle resurssivaatimuksen päivityksen jälkeen, mutta ennen kuin varaat tai lähetät resurssipyynnön. Tämä säilyttää kaikki sellaiset organisaation yleisten ryhmän jäsenten organisaatioyksikön määritykset, jotka eroavat projektinsopimusorganisaation organisaatioyksiköstä.

Esimerkiksi Projekti Z -projektissa sopimusorganisaatioyksikkö on Contoso US. Projektisuunnitelmassa toteutusvaiheeseen kuuluvat testaustehtävät on kohdennettu roolille tekninen konsultti, ja kohdennettu organisaatioyksikkö on Contoso India.

![Toteutusvaiheen organisaatiomääritys](media/org-unit-assignment-09.png)

Toteutusvaiheen jälkeen integrointitestaustehtävä kohdennetaan roolille tekninen konsultti, mutta organisaatioksi määritellään Contoso US.  

![Integrointitestaustehtävän organisaatiomääritys](media/org-unit-generate-team-10.png)

Kun luot projektille ryhmän, kaksi yleistä ryhmän jäsentä luodaan tehtävien eri organisaatioyksiköiden takia. Tekniseen konsulttiin 1 liitetään Contoso India -tehtävät ja tekninen konsultti 2 saa Contoso US -tehtävät.  

![Yleiset ryhmän jäsenet luotu](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> Project Service Automation -versiossa 2 ja versiossa 1 ryhmän jäsenellä ei ole organisaatioyksikköä, jota ylläpidettäisiin rivitehtävässä.

![Rivitehtävät Project Service Automation -versiossa 2 ja 1](media/line-tasks-12.png)

Voit tarkastella organisaatioyksikköä arviot-näkymässä. 

![Organisaatioyksikön arviot](media/org-unit-estimates-view-13.png)
 
Kun päivitys on valmis, se rivitehtävän organisaatioyksikkö, joka vastaa yleistä ryhmän jäsentä, lisätään yleiseen ryhmän jäseneen, ja rivitehtävä poistetaan. Tämän vuoksi on suositeltavaa, että ennen päivittämistä luot tai luot ryhmän uudelleen jokaiselle projektille, joka sisältää yleisiä resursseja.

Jos tehtävä on kohdennettu roolille, jonka organisaatioyksikkö on eri kuin sopimusprojektin organisaatioyksikkö, eikä ryhmää ole luotu, päivitys luo roolille yleisen ryhmän jäsenen, mutta käyttää projektin sopimusyksikköä ryhmän jäsenen organisaatioyksikkönä. Viitaten esimerkkiin Project Z, tämä tarkoittaa sitä, että sopimusorganisaatioyksikkö Contoso US ja toteutusvaiheen projektisuunnitelman testitehtävät on kohdennettu roolille tekninen konsultti organisaatioyksiköllä Contoso India. Integrointitestaustehtävä, joka suoritetaan toteutusvaiheen jälkeen, on kohdennettu roolille tekninen konsultti. Organisaatioyksikkö on Contoso US, eikä ryhmää ole luotu. Päivitys luo yhden yleisen ryhmän jäsenen, teknisen konsultin, jolle on määritetty tunnit kaikista kolmesta tehtävästä, sekä Contoso US -organisaatioyksikön, projektin sopimusorganisaatioyksikön.   
 
Oletusarvon muuttaminen eri resurssoiville organisaatioyksiköille luomattomille ryhmän jäsenille on se syy, miksi suosittelemme, että luot tai luot uudelleen ryhmän jokaiselle projektille, joka sisältää yleisiä resursseja ennen kuin päivität, jotta organisaatioyksikköjen kohdennuksia ei menetetä.
