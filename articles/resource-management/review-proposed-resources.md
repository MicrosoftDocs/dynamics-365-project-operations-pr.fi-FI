---
title: Ehdotettujen resurssien tarkasteleminen
description: Tässä aiheessa on tietoja projektiresurssien ehdottamisesta.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075315"
---
# <a name="review-proposed-resources"></a>Ehdotettujen resurssien tarkasteleminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Resurssipäälliköt voivat ehdottaa resurssia projektipäällikölle resurssipyynnön avulla.

1. Valitse pyyntöruudukosta tai itse pyynnöstä **Etsi resursseja**.
2. Valitse resurssi **Aikatauluavustaja** -sivulta, ja valitse sen jälkeen **Luo resurssivaraus** -ruudusta **Varaustila** -kentästä **Varaa**.

Seuraavat tilapäivitykset toteutuvat:

- **Aikatauluavustaja** -sivulla tilailmaisimet päivittyvät ilmaisemaan, että varaus on ehdotettu eikä sitova.
- Resurssipyynnössä tilaksi vaihtuu **Tarvitsee tarkistusta**.
- Projektin **Ryhmä** -välilehdellä yleisen ryhmän jäsenen **Pyyntötilan** arvoksi vaihtuu **Tarvitsee tarkistusta**.

Projektipäällikkö voi joko hyväksyä tai hylätä ehdotuksen.

Kun resurssipäälliköt käsittelevät resurssipyyntöjä, he voivat käyttää mitä tahansa seuraavista tavoista:

- Ehdota useita resursseja kysynnän tyydyttämiseksi, jos yhtään resurssia ei ole käytettävissä tarvittavien tuntien suorittamiseen. Ehdotetut tunnit jaetaan sitten useiden resurssien kesken, jotka voivat täyttää vaaditut tunnit. Tässä skenaariossa tunnit eivät voi olla päällekkäisiä.
- Ehdota vähemmän resursseja kuin on tarpeen. Tässä skenaariossa ehdotettu resurssikapasiteetti on pienempi kuin vaadittu pyytäjän määrittämä aika. Tämän vuoksi, kun pyytäjän on hyväksynyt ehdotetut resurssit, järjestelmä luo täyttämättömän resurssivaatimuksen, joka tallentaa jäljelle jäävän kysynnän.
- Varaa useita resursseja kysynnän tyydyttämiseksi, jos yhtään resurssia ei ole käytettävissä tarvittavien tuntien suorittamiseen.
- Varaa vähemmän resursseja kuin on tarpeen. Tässä skenaariossa varatut tunnit ovat vähemmän kuin tarvittavat tunnit. Järjestelmä opastaa varaamaan resursseja varauksen sijaan, jotta pyytäjä voi tarkistaa ja seurata jäljellä olevaa kysyntää.

## <a name="billable-utilization"></a>Laskutettava käyttöaste

Resursseilla voi olla tavoite laskutettavalle käytölle. Tämä tavoitekäyttö määritetään joko resurssinoletusroolin ominaisuudeksi tai se määritellään yksittäisen varattavan resurssin tietueessa. Käytön laskennat perustuvat todellisiin tunteihin, jotka resurssit ovat raportoineet hyväksyttyjen aikakirjausten kautta.

Käytön laskennassa käytetään seuraavia kaavoja:

- Lakutettava käyttö = Laskutettavat todelliset tunnit ÷ Resurssin kapasiteetti
- Ei-laskutettava käyttö = Todellinen aika, jonka laskutustyyppi ID = Ei-laskutettava, Täydentävä tai Ei käytettävissä ÷ Resurssin kapasiteetti
- Sisäinen = Todellinen aika ilman myyntisopimusta ÷ Resurssin kapasiteetti
- Resurssin kapasiteetti = Resurssin työtunnit – Poissa toimistosta – Muut kuin työpäivät

**Resurssien käyttöaste** -näkymä on **Resurssit** -ruudussa.

Kukin ruudukon solu kuvaa resurssin laskutettavaa käyttöprosenttia kauden, esimerkiksi päivän, viikon tai kuukauden, aikana. Solujen värittämiseen käytetään seuraavia kaavoja:

- **Vihreä:** Laskutettava käyttö \>= Resurssin tavoitekäyttö
- **Keltainen:** Tavoitekäyttö – 20 \<= Laskutettava käyttö \< Tavoitekäyttö
- **Punainen:** Laskutettava käyttö \< Tavoitekäyttö – 20

Koska **Resurssien käyttöaste** -näkymä perustuu aikataulutaulutaulukkoon, voit suodattaa tuloksia käyttämällä aikataulutaulukon suodatustoimintoja.

Ruudukko edellyttää, että määrität kohteen käytön joko roolille tai yksittäiselle resurssille. Tämä määritetään kohteessa **Resurssit** \> **Resurssiroolit**.

Lisäksi jokaiselle varattavissa olevalle resurssille on määritettävä oletusrooli. Siirry kohtaan **Resurssit** \> **Resurssit**. Varmista **Project Service** -välilehdellä, että resurssin rooli on määritetty, ja että **Onko oletus** -kentän arvo on **Kyllä**. Voit llisätä muita rooleja, joiden **Onko oletus = Ei**. Roolia, jossa **Onko oletus = Kyllä** käytetään määrittämään resurssin käyttöaste tavoitteen mukaisesti.

**Project Service** -välilehdellä voit myös määrittää yksittäisen tavoitekäytön resurssille. Käytön laskenta käyttää sen jälkeen tätä tavoitekäyttöastetta määrittääkseen resurssin tavoitteen resurssin oletusroolin tavoitteen asemesta.

Resurssin käyttöaste näytetään ainoastaan, jos resurssilla on hyväksyttyä laskutettavaa aikaa sen jakson aikana, joka näkyy ruudukossa.

## <a name="resource-availability"></a>Resurssin käytettävyys

On tärkeää, että resurssipäälliköt voivat tarkastella resurssien saatavuutta ja päivittää varauksia. Joissakin tapauksissa ei ole virallista kysyntää (resurssipyyntöä), mutta resurssipäällikön on vastattava suunnittelemattomaan kysyntään, joka tulee esimerkiksi sähköpostitse, puhelimitse tai pikaviestin kautta. Resurssipäälliköt käyttävät aikataulutaulukkoa resurssien ja varausten päivittämiseen.

Resurssin työaikaa käytetään perusteena resurssin saatavuuden laskennassa. Resurssivaraukset kuluttavat resurssien kapasiteettia.

Aikataulutaulukko käyttää värejä ja varjostusta, kun se näyttää varauksia, saatavuutta ja ylivarauksia sekä varausten tilan. Aikataulutaulukon asetusten avulla voit näyttää selitteen.

Jos yksittäisen varattavan resurssin vieressä näkyy oikealle osoittava nuoli aikataulutaulukossa, resurssi voidaan laajentaa niin, että siinä näkyvät sen työn tiedot, johon resurssi on varattu.

Koska Dynamics 365 Project Operations käyttää Universal Resource Scheduling -ohjelmaa, jos myös Dynamics 365 Field Service on asennettu,voit katsella resurssivarausten tietoja projekteille, työtilauksille ja mille tahansa muille kohteille, joihin olet laajentanut aikatauluttamisen.

Jos haluat tarkastella lisätietoja yksittäisestä resurssista, avaa resurssikortti napsauttamalla sitä hiiren kakkospainikkeella.

