---
title: Päivittäminen Project Service Automationista Project Operationsiin
description: Tässä artikkelissa on yleiskatsaus Microsoft Dynamics 365 Project Service Automationin päivittämisestä Dynamics 365 Project Operationsiin.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.openlocfilehash: 30eb02240de6617d4c550ce59db2a454eee36f5b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912972"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Päivittäminen Project Service Automationista Project Operationsiin

Olemme iloisia voidessamme julkaista kolme ensimmäistä vaihetta päivittämisessä Microsoft Dynamics 365 Project Service Automationista Dynamics 365 Project Operationsiin. Tässä artikkelissa on yleiskatsaus asiakkaille, jotka ovat lähdössä tälle jännittävälle matkalle. Tulevissa artikkelissa käsitellään kehittäjiä koskevia seikkoja ja ominaisuuksien parannuksia. Niissä tulee olemaan ohjeita, joiden avulla voit valmistautua päivittämiseen Project Operationsiin. Lisäksi selitetään, mitä voit odottaa päivityksen valmistuttua.

Päivityksen toimitus jakautuu kolmeen vaiheeseen.

| Päivityksen toimitus | Vaihe 1 (tammikuu 2022) | Vaihe 2 (huhtikuun aalto 2022) | Vaihe 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Ei riippuvuutta projektien työrakenteesta (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS Project Operationsin tällä hetkellä tuetuissa rajoissa | | :heavy_check_mark: | :heavy_check_mark: |
| WBS Project Operationsin tällä hetkellä tuettujen rajojen ulkopuolella, mukaan lukien Project Desktop Client -tuki | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Päivitysprosessin ominaisuudet 

Osana päivitysprosessia olemme lisänneet sivustokarttaan päivityslokit, jotta järjestelmänvalvojat voivat diagnosoida virheet helpommin. Uuden käyttöliittymän lisäksi lisätään uudet kelpoisuussäännöt, jotta varmistetaan tietojen eheys päivityksen jälkeen. Päivitysprosessiin lisätään seuraavat vahvistukset.

| Vahvistukset | Vaihe 1 (tammikuu 2022) | Vaihe 2 (huhtikuun aalto 2022) | Vaihe 3  |
|-------------|------------------------|---------------------------|---------------------------|
| Työrakenne vahvistetaan yleisten tietojen eheysrikkomusten varalta (esimerkiksi resurssivaraukset, jotka on liitetty samaan päätehtävään, mutta joilla on eri pääprojektit). | | :heavy_check_mark: | :heavy_check_mark: |
| Työrakenne vahvistetaan [Project for the Webin tunnettuja rajoja](/project-for-the-web/project-for-the-web-limits-and-boundaries) vastaan. | | :heavy_check_mark: | :heavy_check_mark: |
| Työrakenne vahvistetaan Project Desktop Clientin tunnettuja rajoja vastaan. | |  | :heavy_check_mark: |
| Varattavat resurssit ja projektikalenterit arvioidaan yleisten yhteensopimattomien kalenterisääntöjen poikkeusten varalta. | | :heavy_check_mark: | :heavy_check_mark: |

Vaiheessa 2 asiakkaiden, jotka päivittävät Project Operationsiin, aiemmin luodut projektit päivitetään vain luku -muotoon projektisuunnittelua varten. Tässä vain luku -käyttökokemuksessa koko WBS näkyy seurantaruudukossa. Halutessaan muokata WBS:ää projektipäälliköt voivat valita **Muunna** **Projektit**-pääsivulla. Sitten taustaprosessi päivittää projektin niin, että se tukee Project for The Webin uutta projektin aikataulutuskokemusta. Tämä vaihe soveltuu asiakkaille, joilla on projekteja, jotka sopivat [Project for the Webin tunnettuihin rajoihin](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Vaiheessa 3 lisätään Project Desktop Client -tuki. Se hyödyttää asiakkaita, jotka haluavat jatkaa projektiensa muokkaamista kyseisestä sovelluksesta. Jos aiemmin luodut projektit muunnetaan uuteen Project for the Web -kokemukseen, pääsy apuohjelmaan otetaan pois käytöstä jokaisen muunnetun projektin osalta.

## <a name="prerequisites"></a>edellytykset

Jotta asiakas on oikeutettu vaiheen 1 päivitykseen, asiakkaan on täytettävä seuraavat ehdot:

- Kohdeympäristöllä ei saa olla yhtään tietuetta **msdyn_projecttask**-entiteetissä.
- Asiakkaan kaikille aktiivisille käyttäjille on määritettävä kelvolliset Project Operations -käyttöoikeudet. 
- Asiakkaan on vahvistettava päivitysprosessi vähintään yhdessä ei-tuotantoympäristössä, joka sisältää edustavan tietojoukon, joka on tasattu tuotantotietojen kanssa.
- Kohdeympäristö on päivitettävä Project Service Automation Update Release 41 (3.10.62.162) -versioon tai uudempaan versioon.

Vaiheen 2 ja vaiheen 3 edellytykset päivitetään, kun yleinen saatavuus tulee ajankohtaiseksi.

## <a name="licensing"></a>Käyttöoikeudet

Jos sinulla on voimassa olevat Project Service Automation -käyttöoikeudet, voit asentaa Project Operationsin ja käyttää sitä. Project Operations sisältää Project Service Automationin kaikki ominaisuudet ja enemmänkin. Näin ollen voit testata Project Operationsin ominaisuuksia samalla, kun jatkat Project Service Automationin käyttämistä tuotannossa. Kun Project Service Automation -käyttöoikeudet vanhenevat, sinun täytyy siirtyä Project Operationsiin. Kun suunnittelet tätä siirtymistä, ota huomioon, että Project Operations -käyttöoikeuteen ei sisälly Project Service Automation -käyttöoikeutta.

## <a name="testing-and-refactoring-customizations"></a>Mukautusten testaaminen ja optimointi

Tuo aluksi kaikki mukautukset puhtaaseen Project Operations (lite) -ympäristöön, jotta varmistetaan, että tuonti onnistui ja että yritystoiminnot toimivat odotetusti.

Seuraavassa on joitakin asioita, joihin on syytä varautua:

- Tuonti voi epäonnistua puuttuvien riippuvuuksien vuoksi. Toisin sanoen mukautukset liittyvät kenttiin tai muihin komponetteihin, jotka on poistettu Project Operationsista. Poista tällöin nämä riippuvuudet kehitysympäristöstä.
- Jos ei-hallittuihin ja hallittuihin ratkaisuihin sisältyy komponentteja, joita ei ole mukautettu, poista kyseiset komponentit ratkaisusta. Jos esimerkiksi mukautat **Projekti**-entiteettiä, lisää ratkaisuun vain entiteetin otsikko. Älä lisää kaikkia kenttiä. Jos olet aiemmin lisännyt kaikki alikomponentit, sinun täytyy ehkä luoda uusi ratkaisu manuaalisesti ja lisätä siihen asiaankuuluvia osia.
- Lomakkeet ja näkymät eivät ehkä näy odotetusti. Joissakin tilanteissa, jos olet mukauttanut valmiita lomakkeita tai näkymiä, mukautukset voivat estää Project Operationsin uusien päivitysten tulemisen voimaan. Näiden ongelmien tunnistamiseksi on suositeltavaa tehdä vierekkäinen tarkistus Project Operationsin puhtaan asennuksen ja mukautukset sisältävän Project Operations -asennuksen välillä. Vertaa yrityksen eniten käyttämiä lomakkeita ja varmista, että lomakkeen versio on edelleen järkevä eikä lomakkeesta puutu mitään lomakkeen puhtaaseen versioon nähden. Tee vastaava vierekkäinen tarkistus kaikkien mukauttamiesi näkymien osalta.
- Liiketoimintalogiikka voi epäonnistua suorituksen aikana. Koska viittauksia laajennuksien kenttiin ei ole vahvistettu tuonnin aikana, liiketoimintalogiikka saattaa epäonnistua, koska viittauksia kenttiin ei enää ole, ja voit saada seuraavaa esimerkkiä muistuttavan virhesanoman: ”’Projekti’-entiteetti ei sisällä määritettä, jossa Name = 'msdyn_plannedhours' ja NameMapping = 'Logical'." Muuta tällaisessa tapauksessa mukautukset käyttämään uusia kenttiä. Jos käytät laajennuksen logiikassa automaattisesti luotuja välityspalvelimen luokkia ja vahvan tyypin viittauksia, välityspalvelimet kannattaa ehkä muodostaa uudelleen puhtaasta asennuksesta. Näin voit helposti tunnistaa kaikki paikat, joissa laajennukset ovat riippuvaisia vanhentuneista kentistä.

Kun olet päivittänyt mukautukset Project Operationsin puhdasta tuontia varten, siirry seuraavaan vaiheisiin.

## <a name="end-to-end-testing-in-development-environments"></a>Päästä päähän -testaus kehitysympäristöissä

### <a name="initiate-upgrade"></a>Päivityksen aloittaminen 

1. Hae ja valitse ympäristö Power Platform -hallintakeskuksessa. Hae ja valitse sitten sovelluksista **Dynamics 365 Project Operations**.
2. Aloita päivitys valitsemalla **Asenna**. Power Platform -hallintakeskus esittää tämän asennuksen uutena asennuksena. Project Service Automationin aiempi versio kuitenkin tunnistetaan ja aiemmin luotu asennus päivitetään.

    Kun päivitys on valmis, ympäristön on osoitettava, että Project Operations on asennettu ja että Project Service Automationia ei ole asennettu.

    > [!NOTE]
    > Päivitys voi kestää useita tunteja sen mukaan, miten paljon tietoja ympäristössä on. Päivitystä hallinnoivan ydinryhmän on suunniteltava päivitys asiaankuuluvasti ja suoritettava päivitys työajan ulkopuolella. Jos tietomäärä on suuri, päivitys tulee joissakin tapauksissa suorittaa viikonloppuna. Aikataulutusta koskevan päätöksen tulisi perustua alempien ympäristöjen testaustuloksiin.

3. Päivitä mukautetut ratkaisut tarpeen mukaan. Ota tässä vaiheessa käyttöön muutokset, jotka teit mukautuksiin tämän artikkelin kohdassa [Mukautusten testaaminen ja optimointi](#testing-and-refactoring-customizations).
4. Siirry kohtaan **Asetukset** \> **Ratkaisut** ja valitse **Project Operationsin vanhentuneet komponentit** -ratkaisun asennuksen poistaminen.

    Tämä ratkaisu on tilapäinen ratkaisu, joka sisältää päivityksen aikana olemassa olevat komponentit ja tietomallin. Kun poistat tämän ratkaisun, poistat kaikki kentät ja komponentit, joita ei enää käytetä. Näin voit yksinkertaistaa käyttöliittymää sekä helpottaa integrointia ja laajennuksia.
    
### <a name="validate-common-scenarios"></a>Tarkista yleiset tilanteet

Kun tarkistat mukautukset, on suositeltavaa tarkistaa myös sovellusten välillä tuetut liiketoimintaprosessit. Nämä liiketoimintaprosessit sisältävät muun muassa myyntientiteettien, kuten tarjousten ja palvelusopimusten, luomisen sekä projektien luomisen, jotka sisältävät työrakenteet ja toteutuneiden arvojen hyväksynnän.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Tärkeät muutokset Project Service Automationin ja Project Operationsin välillä

Tässä osassa on yhteenveto Project Service Automationin ja Project Operationsin välisistä tärkeistä muutoksista.

### <a name="project-planning"></a>Projektin suunnittelu

Project Operationsin projektin suunnitteluominaisuudet eivät enää perustu asiakaspään logiikkaan ja palvelinpään logiikkaan. Project Operations käyttää sen sijaan Project for the Webiä aikataulutusmoduulina. Tämä aikataulutusmuutos mahdollistaa useita uusia ominaisuuksia kuten Board- ja Gantt-näkymät, resurssipohjaisen suunnittelun, [tehtävien tarkistusluettelon kohteet](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) ja projektin aikataulutustilat. Uusia aikataulutusominaisuuksia tukee myös monipuolinen joukko uusia [ohjelmointirajapintoja (API)](../project-management/schedule-api-preview.md). Näiden ohjelmointirajapintojen tarkoituksena on varmistaa, ettei mikään WBS-entiteetin luontia, päivittämistä tai poistamista varten ohjelmoitu toiminto vioita aikataulun laskennallisia kenttiä.

## <a name="billing-and-pricing"></a>Laskutus ja hinnoittelu

Project Operationsin jatkuvan kehittämisen ansiosta laskutukseen ja hinnoitteluun on käytettävissä useita uusia ominaisuuksia. Seuraavassa on joitakin esimerkkejä.

- [Materiaalikäytön kirjaaminen projekteihin ja projektitehtäviin](../material/material-usage-log.md)
- [Alihankinnan hallinta](../pro/subcontracting/managing-subcontracts-overview.md)
- [Ennakkomaksut ja ennakkomaksuun perustuvat palvelusopimukset](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Sopimuksen ei-ylitettävä tila ja vahvistus](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Tehtäväpohjainen laskutus

## <a name="frequently-asked-questions"></a>Usein kysyttyjä kysymyksiä

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Mitä käyttöönottotyyppejä tuetaan tällä hetkellä päivittämistä varten?

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operationsin käyttöönotto – lite                        | Tuettu               |
| Dynamics 365 Financen projektinhallinta ja kirjanpito | Project Operationsin käyttöönotto – lite                        | Ei tueta tällä hetkellä |
| Projektinhallinta ja kirjanpito Financessa              | Project Operations resurssien ja ei-varastoitavien skenaarioissa     | Ei tueta tällä hetkellä |
| Project Service Automation 3.x                         | Project Operations resurssien ja ei-varastoitavien skenaarioissa     | Ei tueta tällä hetkellä |
| Project for the Web (erillinen ympäristö)            | Project Operationsin käyttöönotto – lite                        | Ei tueta tällä hetkellä |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Miten Project Operations voidaan asentaa ennen kuin päivitystyökalut ovat saatavilla?

Project Operationsin asentamiseen ennen päivitystyökalujen saatavilla oloa on kaksi vaihtoehtoa:

- Valmistele uusi ympäristö.
- Ota Project Operations erillisesti käyttöön myyntiorganisaatioissa, joissa ei ole Project Service Automationia.

> [!NOTE]
> Jos Project Service Automation on asennettu organisaatioon, mutta sitä ei ole käytetty, sen voi poistaa. Kun olet poistanut Project Service Automationin kokonaan, Project Operations voidaan asentaa samaan organisaatioon.
