---
title: Toimittajalaskujen luominen
description: Tässä artikkelissa käsitellään toimittajan laskun käsitettä ja toimittajan laskujen luontia Microsoft Dynamics 365 Project Operationsissa.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475416"
---
# <a name="create-vendor-invoices"></a>Toimittajalaskujen luominen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Jos haluat käyttää tässä artikkelissa kuvattua toimintoa, ota käyttöön **Ota käyttöön alihankinnan todellisten arvojen käsittely Project Operationsissa resurssipohjaisia skenaarioita varten** -ominaisuus **Ominaisuushallinta**-työtilassa.

Microsoft Dynamics 365 Project Operationsin toimittajalaskutuksen avulla voidaan kirjata projektiin toimittajien suorittamien palvelujen ja/tai materiaalien toimitusten kustannukset.

Kun palvelut ja/tai materiaalit alihankitaan toimittajalta, alihankintasopimus edustaa tämän toimittajan kanssa tehtyä sopimusta. Kun toimittaja toimittaa palvelut tai materiaalit vastaanotetaan ja käytetään projektitehtävissä, kustannukset kirjataan projektiin. Tämän jälkeen toimittaja lähettää säännöllisesti laskuja. Nämä laskut tarkistetaan ja täsmäytetään projektiin tallennettuihin kustannuksiin. Kun tarkistusprosessi on valmis, toimittajan lasku vahvistetaan ja se vapautetaan maksua varten.

## <a name="scenarios-for-use"></a>Käyttöskenaarioita

Project Operationsin toimittajien laskujen avulla voidaan tukea kahta erillistä skenaariota:

- Asiakkaat käyttävät täysiä alihankkimiskokemuksia.
- Asiakkaat eivät käytä täysiä alihankkimiskokemuksia, mutta he haluavat yhtenäisen näkymän projektien kustannuksista Project Operationsissa.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Asiakkaat käyttävät täysiä alihankkimiskokemuksia

Toimittajan laskujen käyttökokemusten avulla voidaan tarkistaa aikakirjaukset, materiaalin käyttö ja kulumerkinnät, jotka liittyvät alihankintakomponentteihin, ja täsmäyttää ne toimittajan laskuriveihin. Tämän prosessin avulla voidaan tarkistaa toimittajan laskurivien tarkkuus. Kun tarkistusprosessi on valmis ja toimittajan lasku vahvistetaan, järjestelmä kumoaa toteutuneet tiedot, jotka on tallennettu hyväksytyissä aika-, kulu- ja materiaalikäyttölokeissa, ja luo uudet kustannusten toteutuneet arvot käyttämällä toimittajan laskurivejä.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Asiakkaat eivät käytä täysiä alihankkimiskokemuksia, mutta he haluavat yhtenäisen näkymän projektien kustannuksista Project Operationsissa

Jos seuraat alihankkijaprosessia kolmannen osapuolen järjestelmässä, voit kirjata kustannukset ulkopuolisesta järjestelmästä Project Operationsiin luomalla toimittajan laskuja, jotka eivät viittaa alihankintasopimuksiin. Näin projektipäälliköilläsi voi olla yksi yhtenäinen näkymä projektin kaikista kustannuksista.

## <a name="create-vendor-invoices-in-project-operations"></a>Toimittajan laskujen luominen Project Operationsissa

Toimittajan laskut luodaan Dynamics 365 Financessa **Ostoreskontra**-moduulin avulla. Toimittajan laskuja ei voi luoda suoraan Dataversessa.

### <a name="set-up-vendor-invoice-verification"></a>Määritä toimittajan laskun tarkistus

Jos toimittajan lasku on tarkoitettu alihankintasopimukselle Dataversessa, ota käyttöön **Projektipäällikön manuaalinen tarkistus on pakollinen** -parametri. Vaihtoehdon asetus määrittää, vahvistetaanko toimittajan lasku automaattisesti Dataversessa vai edellyttääkö se manuaalista vahvistusta. Jokaisen projektin toimittajan laskun otsikko sisältää samannimisen vaihtoehdon. Oletusarvon mukaan kaikkien projektin toimittajan laskujen otsikon vaihtoehdoksi määritetään tässä määritetty arvo. Voit kuitenkin päivittää arvon tarpeen mukaan yksittäisten toimittajan laskujen otsikossa.

Jos asetuksena on **Kyllä**, Financessa luotavalla ja Dataverseen synkronoidulla toimittajan laskulla on **Luonnos**-tila. Projektipäällikön on tarkistettava ja vahvistettava lasku, ennen kuin se käsitellään ja kirjataan tietyille Financen projekti- ja kirjanpitotileille.

Jos vaihtoehdoksi on määritetty **Ei**, toimittajan lasku vahvistetaan automaattisesti. Sinun ei tarvitse tehdä mitään.

Toimittajan laskun tarkistus määritetään seuraavasti.

1. Siirry Financessa kohtaan **Projektinhallinta ja kirjanpito** \> **Määritys** \> **Projektinhallinnan ja kirjanpidon parametrit**.
1. Määritä **Taloustiedot**-välilehdessä **Projektipäällikön manuaalinen tarkistus on pakollinen** -asetuksen arvoksi **Kyllä**, jos yrityskäytäntö edellyttää alihankkijatoimittajan laskujen tarkistamista. Jos projektipäällikön tarkistus ei ole pakollinen Dataversessa, jätä asetuksen arvoksi **Ei**. Asetusta käytetään oletusarvoisesti **Odottava toimittajan lasku** -sivulla.

> [!NOTE]
> Alihankintasopimuksille luotuja toimittajan laskuja Dataversessa voi käsitellä oikein vain , jos **Projektipäällikön manuaalinen tarkistus on pakollinen** -asetuksena on **Kyllä**. Projektipäällikkö voi manuaalisesti täsmäyttää alihankkijoiden luomat ajan, materiaalin ja kulujen toteutuneet arvot toimittajan laskuriveille vain, jos asetuksena on **Kyllä**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Hankintojen integrointitilin luominen toimittajan laskuille

Kun toimittajan lasku on kirjattu Finance for Project Operations – Integrated Environment (non-stock) -ympäristössä, taloustiedot kirjataan hankinnan integrointitilille. Järjestelmä luo kirjatulle laskulle toteutuneet summat Dataversessa. Nämä toteutuneet summat kirjataan Financessa käyttämällä Projektin integrointikirjauskansiota. Projektin integrointikirjauskansion kirjaaminen kirjaa todellisen kustannuksen ja kumoaa Hankinnan integrointitilin.

Voit määrittää Hankintojen integrointitilin toimittajan laskuille seuraavasti.

1. Siirry Financessa kohtaan **Projektinhallinta ja kirjanpito** \> **Määritys** \> **Projektinhallinnan ja kirjanpidon parametrit**.
1. Valitse **Project Operations – Dynamics 365 Customer Engagement**-välilehdessä **Materiaalit** \> **Hankintojen integrointitili**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Alihankintasopimuksen toimittajalaskujen luominen ja kirjaaminen

Kun ostoreskontran käsittelijä saa alihankkijalta laskun, Financessa luodaan uusi lasku.

1. Siirry Financessa kohtaan **Ostoreskontra** \> **Laskut** \> **Odottavat toimittajan laskut**.
1. Luo toimittajan lasku valitsemalla **toimintoruudussa** **Uusi**.
1. Valitse laskun otsikon **Laskutili**-kentässä **Alihankkija**.
1. Valitse laskun päivämäärä.
1. Määritä **Otsikko**-välilehdessä **Projektipäällikön manuaalinen tarkistus on pakollinen** -asetuksen arvoksi **Kyllä**. Tämän vaihtoehdon oletusasetus tulee **Projektinhallinnan ja kirjanpidon parametrit** -sivulta. Sitä voidaan kuitenkin muuttaa toimittajan laskun tasolla.
1. Valitse **Laskurivi**-pikavälilehdessä **Lisää rivi**, jos haluat luoda toimittajan laskurivin.
1. Valitse alihankintariveille luotu kustannusluokka ja kirjoita yksikköhinta, mittayksikkö ja määrä.
1. Valitse Toimittajan laskurivit -osan **Projekti**-välilehdestä projekti, jonka kanssa alihankkija jakaa alihankkijalaskun.
1. Valitse projektiluokka. Se voi olla jokin seuraavista tyypeistä: **Nimike**, **Kulu**, **Materiaalit** tai **Tunnit**.
1. Valitse rooli vain, jos valittu projektiluokka on **Tunti**-tyyppinen.
1. Kirjaa toimittajan lasku valitsemalla **Kirjaa**.

Voit vaihtoehtoisesti luoda toimittajan laskun valitsemalla **Ostoreskontra** \> **laskut** \> **Avaa toimittajan laskut** ja valitsemalla **Uusi**.

Kun toimittajan lasku on kirjattu, se on käytettävissä Dataversessa projektipäällikön tarkistamista ja käsittelyä varten.

## <a name="vendor-invoice-processing-in-dataverse"></a>Toimittajan laskujen käsittely Dataversessa

Dataversessa luodussa toimittajan laskussa jotkin kenttien arvot tulevat Financessa tallennetusta toimittajan laskusta. Muut arvot ovat oletusarvoja alihankintasopimuksesta.

Seuraavat kentät ja liittyvät tietueet kopioidaan alihankintasopimuksesta toimittajan laskun otsikkoon:

- Valuutta
- Sopimusyksikkö
- Maksuehdot

Project Operations lisää alihankintasopimuksen ja alihankintarivin oletusviittauksen toimittajan laskuriveille seuraavien kenttien arvojen perusteella:

- Tapahtumaluokka
- Rooli
- Tapahtumaluokka
- Tuotekentät
- Project
- Tehtävä

> [!NOTE]
> Kiinteähintaisia alihankkijarivejä ei tueta Project Operationsissa.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
