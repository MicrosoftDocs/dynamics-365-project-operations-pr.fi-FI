---
title: Joulukuun 2021 uudet toiminnot – Project Operationsin lite-käyttöönotto
description: Tässä artikkelissa on tietoja Project Operationsin lite-käyttöönoton joulukuussa 2021 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914076"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Joulukuun 2021 uudet toiminnot – Project Operationsin lite-käyttöönotto

_Käytetään: Lite-käyttöönotto – kauppa proformalaskutukseen_

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

### <a name="subcontract-management"></a>Alihankinnan hallinta 

- [Projektiryhmän jäsenten alihankinta](../subcontracting/subcontracting-project-team-members.md): Projektipäällikkö voi luoda nimettyjä tai yleisiä ryhmän jäseniä sekä alihankintoja ja alihankintarivejä henkilöstön määrittämistä ja arviointia varten.
- [Projektiryhmän jäsenten alihankintavaihtoehdot](../subcontracting/subcon-options.md): Kun projektipäällikkö tekee henkilöstön määrityspäätöksiä nimetyille ja yleisille projektiryhmän jäsenille, hän voi tarkistaa aiemmin luotuja alihankintoja tai luoda uusia alihankintoja yhdelle tai useammalle projektiryhmän jäsenelle. 
- [Alihankittujen resurssimääritysten kustannusarvio](../subcontracting/costing-subcon-ra.md): Projektin kustannusarvio ottaa huomioon alihankitut resurssimääritykset ja laskee ne käyttäen alihankintoihin liitettyjä ostohinnastoja. 
- [Aikataulutaulukon määrittäminen niin, että se näyttää sopimustyöntekijät ja alihankitun kapasiteetin](../subcontracting/configure-sb-subcon.md): Project Operationsin aikataulutaulukko on nyt määritetty niin, että sen avulla voi hakea ja ehdottaa varattavien resurssien sopimustyöntekijätyyppiä, alihankittua kapasiteettia ja työntekijöitä. Tätä määritystä voi käyttää, kun haetaan resursseja tietyn projektitarpeen henkilöstömäärityksen kontekstissa tai kun haetaan projektitarpeen kontekstin ulkopuolella.
- [Projektin henkilöstömääritykset sopimustyöntekijöillä ja alihankitulla kapasiteetilla](../subcontracting/staffing-cw.md): Sopimustyöntekijöitä voi nyt varata projekteissa, jotka käyttävät aikataulutaulukon kokemusta.
- [Alihankittujen komponenttien ajan, kulujen ja materiaalikäytön kirjaaminen projekteissa](../subcontracting/recording-subcon-actuals.md): Sopimustyöntekijät voivat kirjata aikaa ja kuluja, ja projektiryhmän jäsenet voivat myös kirjata ostettujen materiaalien käyttöä käyttäen projektin alihankintaa. Näin voit tallentaa tarkat kustannukset projekteissa, joissa käytetään ostettua kapasiteettia tai materiaaleja.
- [Alihankinnan tilasiirtymät](../subcontracting/subcon-states.md): Alihankinta voi olla vahvistettu (neuvottelut käyty toimittajan kanssa), suljettu (toimitus on tehty) tai peruutettu (sopimuksen purkaminen toimittajan kanssa ennen kuin toimitus on tehty).

### <a name="task-planning"></a>Tehtävien suunnittelu
- Parannettu vianmääritys järjestelmänvalvojia varten. Kun käyttäjä ei voi avata projektia, järjestelmänvalvoja voi tarkastaa virheet, jotka eivät liity käyttöoikeuksiin ja jotka on muodostettu Project for the webistä [projektin aikataulutuslokeissa](../../project-management/schedule-api-logs.md).
- [Käytä tarkistusluetteloita Microsoft Project for the webissä](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Microsoft Project for the Webissä voit lisätä tehtävään tarkistusluettelon, joka seuraa tiettyjä kohteita.

## <a name="quality-updates"></a>Laatupäivitykset

| **Ominaisuusalue** | **Viitenumero** | **Laatupäivitys** |
| --- | --- | --- |
| Suunnittelu ja seuranta | 2392596 | Aikataulun ohjelmointirajapinnat sallivat nyt päivitykset kentiin **Jäljellä oleva työmäärä**, **Työmäärä valmis** ja **% valmis**. |
| Suunnittelu ja seuranta | 2478497 | Aikataulun ohjelmointirajapintojen **Tehtävän numero**- ja **Tehtävän tunnus** -kentät voivat olla tyhjät, koska järjestelmä täyttää ne käyttämällä automaattista numerointia.|
| Aika ja kulu | 2468135 | Hyväksynnän uudelleenyritysten määrä pienenee viidestä kolmeen. |
| Aika ja kulu | 2468188 | Korjattu ongelma, joka syntyy, kun lokiteksti ylittää enimmäismäärän **notetext**-määritteessä **Huomautus**-entiteetissä. |
