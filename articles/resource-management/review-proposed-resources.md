---
title: Ehdotettujen resurssien tarkasteleminen
description: Tässä aiheessa on tietoja projektiresurssien ehdottamisesta.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401169"
---
# <a name="review-proposed-resources"></a>Ehdotettujen resurssien tarkasteleminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Resurssipäälliköt voivat ehdottaa resurssia projektipäällikölle resurssipyynnön avulla.

1. Valitse pyyntöruudukosta tai itse pyynnöstä **Etsi resursseja**.
2. Valitse resurssi **Aikatauluavustaja**-sivulta, ja valitse sen jälkeen **Luo resurssivaraus** -ruudusta **Varaustila**-kentästä **Varaa**.

Seuraavat tilapäivitykset toteutuvat:

- **Aikatauluavustaja** -sivulla tilailmaisimet päivittyvät ilmaisemaan, että varaus on ehdotettu eikä sitova.
- Resurssipyynnössä tilaksi vaihtuu **Tarvitsee tarkistusta**.
- Projektin **Ryhmä**-välilehdellä yleisen ryhmän jäsenen **Pyyntötilan** arvoksi vaihtuu **Tarvitsee tarkistusta**.

Projektipäällikkö voi joko hyväksyä tai hylätä ehdotuksen.

Kun resurssipäälliköt käsittelevät resurssipyyntöjä, he voivat käyttää mitä tahansa seuraavista tavoista:

- Ehdota useita resursseja kysynnän tyydyttämiseksi, jos yhtään resurssia ei ole käytettävissä tarvittavien tuntien suorittamiseen. Ehdotetut tunnit jaetaan sitten useiden resurssien kesken, jotka voivat täyttää vaaditut tunnit. Tässä skenaariossa tunnit eivät voi olla päällekkäisiä.
- Ehdota vähemmän resursseja kuin on tarpeen. Tässä skenaariossa ehdotettu resurssikapasiteetti on pienempi kuin vaadittu pyytäjän määrittämä aika. Tämän vuoksi, kun pyytäjän on hyväksynyt ehdotetut resurssit, järjestelmä luo täyttämättömän resurssivaatimuksen, joka tallentaa jäljelle jäävän kysynnän.
- Varaa useita resursseja kysynnän tyydyttämiseksi, jos yhtään resurssia ei ole käytettävissä tarvittavien tuntien suorittamiseen.
- Varaa vähemmän resursseja kuin on tarpeen. Tässä skenaariossa varatut tunnit ovat vähemmän kuin tarvittavat tunnit. Järjestelmä opastaa varaamaan resursseja varauksen sijaan, jotta pyytäjä voi tarkistaa ja seurata jäljellä olevaa kysyntää.

## <a name="resource-availability"></a>Resurssin käytettävyys

On tärkeää, että resurssipäälliköt voivat tarkastella resurssien saatavuutta ja päivittää varauksia. Joissakin tapauksissa ei ole virallista kysyntää (resurssipyyntöä), mutta resurssipäällikön on vastattava suunnittelemattomaan kysyntään, joka tulee esimerkiksi sähköpostitse, puhelimitse tai pikaviestin kautta. Resurssipäälliköt käyttävät aikataulutaulukkoa resurssien ja varausten päivittämiseen.

Resurssin työaikaa käytetään perusteena resurssin saatavuuden laskennassa. Resurssivaraukset kuluttavat resurssien kapasiteettia.

Aikataulutaulukko käyttää värejä ja varjostusta, kun se näyttää varauksia, saatavuutta ja ylivarauksia sekä varausten tilan. Aikataulutaulukon asetusten avulla voit näyttää selitteen.

Jos yksittäisen varattavan resurssin vieressä näkyy oikealle osoittava nuoli aikataulutaulukossa, resurssi voidaan laajentaa niin, että siinä näkyvät sen työn tiedot, johon resurssi on varattu.

Koska Dynamics 365 Project Operations käyttää Universal Resource Scheduling -ohjelmaa, jos myös Dynamics 365 Field Service on asennettu,voit katsella resurssivarausten tietoja projekteille, työtilauksille ja mille tahansa muille kohteille, joihin olet laajentanut aikatauluttamisen.

Jos haluat tarkastella lisätietoja yksittäisestä resurssista, avaa resurssikortti napsauttamalla sitä hiiren kakkospainikkeella.



[!INCLUDE[footer-include](../includes/footer-banner.md)]