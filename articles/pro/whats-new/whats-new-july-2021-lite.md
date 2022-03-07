---
title: Heinäkuun 2021 Project Operations lite-käyttöönoton uudet ominaisuudet
description: Tässä aiheessa on tietoja laatupäivityksistä, jotka ovat käytettävissä Project Operationsin lite-käytöönoton heinäkuussa 2021 julkaistussa versiossa .
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6992498df5beb97d4e7197e301f093320dc28a23
ms.sourcegitcommit: 3abf1e67938d91bd826b025ae3187cd313f556b9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433649"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Heinäkuun 2021 Project Operations lite-käyttöönoton uudet ominaisuudet

_Käytetään: Lite-käyttöönotto – kauppa proformalaskutukseen_

Tämä aihe koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

  - Project Operations Dataverse-ympäristön versiossa 4.12.0.148.

## <a name="quality-updates"></a>Laatupäivitykset
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
