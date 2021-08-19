---
title: Heinäkuun 2021 uudet ominaisuudet – Project Operations resurri/ei-varastoitavien skenaarioissa
description: Tässä aiheessa on tietoja laatupäivityksistä, jotka ovat käytettävissä Project Operationsin heinäkuussa 2021 julkaistussa versiossa resurssi- tai ei-varastopohjaisiin skenaarioihin.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 69507427521466335df9cbbaba79db1cfc7be91386b8b2ded5b1c384555946ee
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008042"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Heinäkuun 2021 uudet ominaisuudet – Project Operations resurri/ei-varastoitavien skenaarioissa

*Käytetään: Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa*

Tämä aihe koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

   - Project Operations Microsoft Dataverse -ympäristön versiossa 4.12.0.148 tai 4.12.0.152.
   - Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.20.

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

Tähän julkaisuun sisältyvät seuraavat ominaisuudet:

- Järjestelmänvalvojat voivat tarkastella PSS-lokeja ja toimintajoukon lokeja asetusvalikosta. Lokit tallennetaan 90 päivän ajaksi.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Tässä versiossa ei ole päivityksiä Project Operationsin kaksoiskirjoituskartoille.

Project Operationsin kaksoiskirjoituskarttojen luettelo ja versiot ovat kohdassa [Project Operationsin kaksi kaksoiskirjoituskarttojen versiot](../environment/resource-dual-write-maps.md).

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja rahoitusratkaisun versiota. Tietyt ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Kartan aktiivinen versio näkyy **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Aktivoi kartan uusi versio valitsemalla **Taulukkokarttaversiot**, valitsemalla uusin versio ja tallentamalla valittu versio. Jos olet mukauttanut valmiin taulukkokartan, kohdista muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisessä on ongelma, noudata kohdan [Puutuvat sarakkeet -ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) ohjeita kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| **Ominaisuusalue**              | **Viitenumero** | **Laatupäivitys**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Laskutus ja hinnoittelu           | 2224046              | **Tapahtuman luokka** -kenttää voi muokata **Tarjousrivin tiedot** -välilehdessä, mutta se on lukittu, jos työskentelet **Tarjousrivin tiedot** -sivulla.                                                                     |
| Laskutus ja hinnoittelu           | 2224400              | **Sulje tarjous voitettuna** -toiminto epäonnistuu, kun tarjouksella ei ole päivämäärän välitavoitteita.                                                                                                                                    |
| Laskutus ja hinnoittelu           | 2234089              | Kun kirjoitat tuotteen kuvauksen manuaalisesti, se tyhjenee, kun materiaaliarviolle on syötetty määrä.                                                                                                                         |
| Laskutus ja hinnoittelu           | 2234100              | **Tehtävän laskutuksen määritys** -ruudukko ei sisällä **Materiaali**-saraketta, ja se on arvo projektin **Tehtävälaskutus**-välilehdessä.                                                                                                       |
| Laskutus ja hinnoittelu           | 2277409              | Tuotetunnusta ei voi käyttää sopimusrivin tiedoissa materiaalityypin rivillä.                                                                                                                                        |
| Laskutus ja hinnoittelu           | 2281728              | Sopimusrivin luominen turhaan laskee toteutuneet arvot uudelleen ja aiheuttaa merkittävän lisäyksen tietojen määrään, mikä vaikuttaa suorituskykyyn.                                                                                |
| Laskutus ja hinnoittelu           | 2298668              | Takaisinvetoon ja poistettuun kuluun liittyviä kirjauskansion rivejä ei poisteta.                                                                                                                                     |
| Laskutus ja hinnoittelu           | 2300192              | Kun useat käyttäjät muokkaavat laskua, uusi laskun rivi voidaan luoda vahvistetulle laskulle.                                                                                   |
| Laskutus ja hinnoittelu           | 2301569              | Laskuja ei voi korjata, jos \$0 summan ennakkomaksu on otettu käyttöön.                                                                                                                                        |
| Laskutus ja hinnoittelu           | 2307965              | Virhe tapahtuu luotaessa luokkahintaa, jonka arvot puuttuvat.                                                                                                                           |
| Laskutus ja hinnoittelu           | 2326870              | Virhe tapahtuu kohteessa **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** joa **producttypecode** on tyhjäarvoinen.                                                                            |
| Laskutus ja hinnoittelu           | 2332732              | Virhe tapahtuu luotaessa sopimusrivin välitavoitetta ilman tilausriviä.                                                                                                                |
| Projektin suunnittelu ja seuranta | 2181094              | Projektin aikataulutuksen ohjelmointirajapinta tukee nyt PSS-lokeja ja toimintojoukon lokeja, jotka on tallennettu 90 päivän ajaksi.                                                                                                                  |
| Projektin suunnittelu ja seuranta | 2254201              | **Aikataulutustila**-selitteeseen päivitetään tietoja, jotka kuvaavat oletuslogiikkaa.                                                                                                                                      |
| Projektin suunnittelu ja seuranta | 2300252              | **openProject**-vastausvälimuisti päivitetään, ja se sisältää välimuistiavaimen tunnuksen omistajan ja arvot **base Url** ja **Segment Url**, jotta **Request Url** voidaan aina luoda uudelleen, jos **base Url** muuttuu. |
| Projektin suunnittelu ja seuranta | 2301312              | **msdyn_membershipstatus** on poistettu **projektiryhmän jäsen** -näkymästä.                                                                                                                                        |
| Projektin suunnittelu ja seuranta | 2302759              | Tuotteet haetaan turhaan **Resurssimääritykset**-, **Arviot**- ja **Kuluarviot**-välilehdissä.                                                                                                        |
| Projektin suunnittelu ja seuranta | 2308050              | **CopyProject** epäonnistuu virheilmoituksella "Tunnusta etäpalvelun kanssa keskustelua varten ei saatu".                                                                                                                           |
| Projektin suunnittelu ja seuranta | 2322650              | **Projektitehtäväluettelo**-näkymä on päivitetty näyttämään tehtävän päivämäärä oletusarvoisesti.                                                                                                            |
| Projektin suunnittelu ja seuranta | 2327266              | **CopyProject** luo virheen "Avainta ei löydy sanakirjasta" arvioita luotaessa.                                                                                                      |
| Projektin suunnittelu ja seuranta | 2328123              | **CopyProject** luo virheen "Tunnusta etäpalvelun kanssa keskustelua varten ei saatu".                                                                                                                          |
| Projektin suunnittelu ja seuranta | 2336258              | **CopyProject** kopioi resurssien paikkojen nimet virheellisesti.                                                                                                                                                 |
| Laskutus ja hinnoittelu           | 2224476              | **Varattavissa oleva resurssi** -kenttä ei saa oikeaa oletusarvoa kirjautunut käyttäjä **Materiaalin käyttö** -sivulla.                                                                                                            |
| Resurssienhallinta           | 2277249              | Virhe päivitessä muita kuin projektipohjaisia resurssivaatimuksia.                                                                                                            |
| Resurssienhallinta           | 2323869              | Resurssin käyttö ei tunnista suodatettuja resursseja oikein.                                                                                                                                             |
| Aika ja kulu              | 2176538              | **Aikamerkinnän** ohjausobjektissa käytetään virheellisiä suodatinoperaattoreita.                                                                                                                                                   |
| Aika ja kulu              | 2177462              | Aikamerkinnän poistaminen ruudukosta ei päivitä **Lähetä**-, **Peruuta**-, **Poista**- ja **Muokkaa merkintää** -painikkeen tilaa odotetulla tavalla.                                                                                        |
| Aika ja kulu              | 2299985              | **TimeEntriesImportFromResourceAssignment** ei ylläpidä määrityksen alkamis-/lopetusaikaa.                                                                                                  |
| Aika ja kulu              | 2318426              | Kun aikamerkintä on lähetetty, lukittuja kenttiä voi edelleen muokata.                                                                                                                                   |
| Aika ja kulu              | 2323749              | Virhe luotaessa kulu varattavan resurssin **Liittyvä**-välilehdestä.                                                                                                      |
| Aika ja kulu              | 2327678              | Kun luot aikamerkinnän varattavissa olevan resurssin **Liittyvä**-välilehdessä, pääresurssia ei välitetä aikamerkinnän ohjausobjektiin.                                                                            |
| Yhteiset                       | 2296857              | Pitkään suoritettavien töiden edistymisen seuranta.                                                                                                                                                                        |
| Yhteiset                       | 2253682              | Project Operationsin kaksoiskirjoitusratkaisua ei pitäisi asentaa, kun kaksoiskirjoitusydin asennetaan ympäristöön, jossa ei ole kaksoiskirjoituksen hallintaratkaisua.                                                |
| Yhteiset                       | 2316420              | Project Servicen ytimen valmistelu epäonnistuu, jos sovelluksen käyttäjän liiketoimintayksikköä muutetaan.                                                                                                                     |
| Yhteiset                       | 2376405              | Julkaisijan korjaama päivitysongelma (laatupäivitys on saatavana versiossa 4.12.0.152)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Financen projektinhallinta ja kirjanpito

| Ominaisuusalue                      | Viitenumero | Laatupäivitys                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektinhallinta ja kirjanpito | 4620267          | Lomakkeita ei voi mukauttaa lisäämään **Tarkoitus**-kenttää **Projektin kirjattu tapahtuma**-, **Laskuehdotuksen luonti**- ja **Laskuehdotus**- sivuille.                                                                                                                                                                                         |
| Projektinhallinta ja kirjanpito | 4613449          | Kun valitset Financessa projektisopimustunnuksen, integroitu Project Operations -ympäristö avaa sivun ja luo uuden tietueen aiemmin luotujen projektisopimusten sivun sijaan.                                                                                                                                           |
| Projektinhallinta ja kirjanpito | 4614445          | Project Operationsin integroidun skenaarion käyttöönotossa ei voi muokata kenttää **nimikeen arvonlisäveroryhmä** laskuehdotuksessa, joka tuotiin väliympäristöstä. Nimikkeen arvonlisäveroryhmän on oltava muokattavissa kaikille tapahtumatyypeille, mukaan lukien tilit, tunnit, kulut, maksut ja nimikkeet. |
| Projektinhallinta ja kirjanpito |                  | Negatiivisesta aikatapahtuman korjauksesta johtuvaa laskuehdotusta ei voi kirjata.                                                                                                                                                                                                                                              |
| Projektinhallinta ja kirjanpito |                  | Laskuehdotusrivitovat päällekkäisiä, koska samanaikaisesti käynnissä on useita **tuo väliympäristöstä** -vaiheittaisia jaksottaisia prosesseja.                                                                                                                                                                                                                |

