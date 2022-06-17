---
title: Toimittajan laskujen otsikkotiedot
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Project Operationsin toimittajan laskun otsikossa olevia toimintoja.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929854"
---
# <a name="header-details-for-vendor-invoices"></a>Toimittajan laskujen otsikkotiedot

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Project Operationsin toimittajan laskun otsikossa olevia toimintoja.

Projektipäälliköt voivat suunnitella ja toteuttaa projekteja, ja he voivat käyttää alihankkijoita ja ostaa tuotteita ja palveluita toimittajilta. Projektin toteuttamisen aikana kustannukset aiheutuvat palveluista, materiaaleista ja kululuokista, jotka hankitaan alihankintasopimuksista toimittajien kanssa. Toimittaja laskuttaa nämä kustannukset projekteilta luomalla toimittajan laskuja.

Seuraavassa taulukossa on tietoja toimittajan laskujen otsikoiden kentistä Project Operationsissa.

| Field | Description | Toiminnallinen vaikutus |
| --- | --- | --- |
| Name | Toimittajan laskun nimi. | Kaikissa avattavissa toimittajan laskujen luetteloissa toimittajan laskun nimi näkyy ensimmäisessä sarakkeessa, mikä auttaa tunnistamaan toimittajan laskun. Kun toimittajan lasku luodaan oletusarvoisesti alihankintasopimuksesta, toimittajan laskun **Nimi**-kenttään määritetään arvo, joka koostuu alihankkijan nimestä ja kuluvasta päivämäärästä. |
| Description | Lyhyt kuvaus palveluista ja tuotteista, joita laskutetaan toimittajan laskulla. | Ei mikään |
| Toimittaja | Tuotteita ja palveluita laskuttavan yrityksen nimi. Tämän yrityksen tulisi olla asiakastietue, jonka suhdetyyppi on **Toimittaja** tai **Alihankkija**. | <p>Oletusarvot syötetään automaattisesti seuraaviin kenttiin valitun toimittajan mukaan:</p><ul><li>Valuutta</li><li>hinnastot</li><li>Maksuehdot</li><li>Maksuosoite</li></ul> |
| Alihankinta | Viittaus toimittajan laskun alihankkijaan. | <p>Oletusarvot syötetään automaattisesti seuraaviin kenttiin valitun alihankkijan mukaan:</p><ul><li>Valuutta</li><li>hinnastot</li><li>Maksuehdot</li><li>Maksuosoite</li></ul><p>Toimittajan laskun otsikossa valittu alihankkija syötetään oletusarvoisesti toimittajan laskuriveille, eikä sitä voi muuttaa siellä.</p> |
| Laskun pvm | Toteutuneiden kustannusten päivämäärä, joka luodaan, kun toimittajan lasku vahvistetaan. | Laskun päivämäärää käytetään myös oikean ostohinnaston valitsemiseen joko liittyvään toimittajaan liitetyistä hinnastoista tai projektin parametreista. |
| Tilan syy | Toimittajan laskun tila. | <p>Tila määrittää, missä liiketoimintaprosessissa toimittajan lasku on ja voiko sitä muokata. Tässä on muutamia käytettävissä olevia arvoja:</p><ul><li>**Luonnos** – toimittajan laskua voi muokata.</li><li>**Vahvistettu** – Toimittajan lasku on tarkistettu ja vahvistettu. Tässä tilassa olevaa toimittajan laskua ei voi muokata tai poistaa.</li><li>**Käsittelyssä** – Toimittajan laskua tarkistetaan. Tässä tilassa olevaa toimittajan laskua voi muokata, mutta ei poistaa.</li><li>**Peruutettu** – Toimittajan lasku on peruutettu. Tässä tilassa olevaa toimittajan laskua ei voi muokata tai poistaa.</li></ul> |
| Valuutta | Valuutta, jossa toimittaja laskuttaa tuotteista ja palveluista toimittajan laskulla. | Alihankintasopimukseen viittaavasta toimittajan laskusta alihankintasopimuksen valuutta syötetään oletusarvoisesti toimittajan laskun valuutaksi. Jos toimittajan laskussa ei viitata alihankintasopimukseen, oletusarvo syötetään toimittajan tilitietueesta, ja sitä voidaan muuttaa. Kun toimittajan lasku on tallennettu, valuuttaa ei voi enää muokata. |
| Sopimusyksikkö | Sen yrityksen divisioona, joka vastaa palvelujen ja/tai tuotteiden vastaanottamisesta toimittajalta. | Ei mikään |
| Maksuehdot | Luotujen toimittajan laskujen maksuehdot. Oletusarvo syötetään automaattisesti toimittajatilin tietueesta. | Alihankinnan maksuehdot kopioidaan kaikkiin toimittajan laskuihin, jotka liittyvät alihankintasopimukseen. Maksuehtoja voidaan päivittää, jos toimittajan laskun tilana on **Luonnos**. |
| Maksuosoite | Osoite sille toimittajalle, jolle maksut on lähetettävä. Oletusarvo syötetään automaattisesti toimittajatilin tietueesta. | Alihankinnan maksuosoite kopioidaan maksuosoitteeksi kaikkiin kyseiselle alihankintasopimukselle luotuihin toimittajan laskuihin. Maksuosoite voidaan päivittää, jos toimittajan laskun tilana on **Luonnos**. |
| Välisumma | Jos toimittajan laskulla ei ole rivejä, syötä laskun välisumma ennen veroja. Jos toimittajan laskussa on rivejä, tämä kenttä on vain luku -tyyppinen. Tässä tapauksessa näytetyssä summassa on toimittajan laskun kaikkien rivien välisumma. | Ei mikään |
| Vero yhteensä | Jos toimittajan laskulla ei ole rivejä, syötä alihankintasopimuksen kokonaisverot. Jos toimittajan laskussa on rivejä, tämä kenttä on vain luku -tyyppinen. Tässä tapauksessa näytetyssä summassa on toimittajan laskun kaikkien rivien verosummien summa. | Ei mikään |
| Loppusumma | Tässä lasketussa kentässä näkyy toimittajan laskun kokonaissumma verojen lisäämisen jälkeen. | Ei mikään |

> [!NOTE]
> Seuraavia toimittajan laskun kenttiä ei voi muuttaa, kun toimittajan lasku on tallennettu: **Toimittaja**, **Alihankintasopimus**, **Valuutta**, **Sopimusyksikkö** ja **Maksuehdot**. Jos näihin toimittajan laskun kenttiin on tehtävä muutoksia, poista toimittajan lasku ja luo uusi toimittajan lasku.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
