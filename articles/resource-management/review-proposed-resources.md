---
title: Ehdotettujen resurssien tarkasteleminen
description: Tässä aiheessa on tietoja projektiresurssien ehdottamisesta.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b3077f98052fcac9989a81b2fab12fa30d65d970
ms.sourcegitcommit: ebcaec7806ee8aee1323ef532d5b7735d27edd04
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403791"
---
# <a name="review-proposed-resources"></a>Ehdotettujen resurssien tarkasteleminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Resurssipäälliköt voivat ehdottaa resurssia projektipäällikölle resurssipyynnön avulla.

Voit tarkastella ehdotettuja resursseja seuraavasti:

1. Valitse **Pyyntö**-ruudukosta tai itse pyynnöstä **Etsi resursseja**.
2. Valitse **Ajoitusavustaja**-sivulla resurssi ja vahvista sitten, että kaikki ehdotetut tunnit sisältyvät ehdotettuun varaukseen.
3. Määritä **Luo resurssivaraus** -ruudussa **Varauksen tila** -kenttä arvoon **Ehdotettu** ja valitse sitten **Varaa**.

    > [!NOTE]
    > Kun **Varauksen tila** määritetään arvoon **Ehdotettu**, resurssia ei varata kiinteästi eikä yleistä resurssia korvata nimetyllä ryhmän jäsenellä.

    Seuraavat tilapäivitykset toteutuvat:

    - **Ajoitusavustaja**-sivulla tilailmaisimet päivittyvät ilmaisemaan, että varaus on ehdotettu eikä kiinteä.
    - Resurssipyynnössä tilaksi vaihtuu **Tarvitsee tarkistusta**.
    - Projektin **Ryhmä**-välilehdellä yleisen ryhmän jäsenen **Pyyntötilan** arvoksi vaihtuu **Tarvitsee tarkistusta**.

Projektipäällikkö voi hyväksyä tai hylätä ehdotuksen.

Kun resurssipäälliköt käsittelevät resurssipyyntöjä, he voivat käyttää mitä tahansa seuraavista tavoista:

- Ehdota useita resursseja kysynnän tyydyttämiseksi, jos yhtään resurssia ei ole käytettävissä tarvittavien tuntien suorittamiseen. Ehdotetut tunnit jaetaan sitten useiden resurssien kesken, jotka voivat täyttää vaaditut tunnit. Tässä skenaariossa tunnit eivät voi olla päällekkäisiä.
- Ehdota vähemmän resursseja kuin on tarpeen. Tässä skenaariossa ehdotettu resurssikapasiteetti on pienempi kuin vaadittu pyytäjän määrittämä aika. Kun pyytäjä on hyväksynyt ehdotetut resurssit, järjestelmä luo täyttämättömän resurssivaatimuksen, joka tallentaa jäljelle jäävän kysynnän.
- Varaa useita resursseja kysynnän tyydyttämiseksi, jos yhtään resurssia ei ole käytettävissä tarvittavien tuntien suorittamiseen.
- Varaa vähemmän resursseja kuin on tarpeen. Tässä skenaariossa varatut tunnit ovat vähemmän kuin tarvittavat tunnit. Järjestelmä opastaa varaamaan resursseja varauksen sijaan, jotta pyytäjä voi tarkistaa ja seurata jäljellä olevaa kysyntää.

## <a name="resource-availability"></a>Resurssin käytettävyys

Resurssipäälliköiden on voitava tarkastella resurssien saatavuutta ja päivittää varauksia. Joissakin tapauksissa ei ole muodollista kysyntää (resurssipyyntöä). Resurssipäällikön on kuitenkin vastattava suunnittelemattomaan kysyntään, joka tulee muiden kanavien, kuten sähköpostiviestien, puheluiden tai pikaviestien, kautta. Resurssipäälliköt käyttävät **Aikataulutaulukkoa** resurssien ja varausten päivittämiseen.

Resurssin työaikaa käytetään perusteena resurssin saatavuuden laskennassa. Resurssivaraukset kuluttavat resurssien kapasiteettia.

**Aikataulutaulukko**  käyttää värejä ja varjostusta, kun se näyttää varauksia, saatavuutta ja ylivarauksia sekä varausten tilan. **Aikataulutaulukossa** olevan asetuksen avulla voit näyttää selitteen.

Jos yksittäisen varattavan resurssin vieressä näkyy oikealle osoittava nuoli **aikataulutaulukossa**, resurssi voidaan laajentaa niin, että siinä näkyvät sen työn tiedot, johon resurssi on varattu.

Koska Dynamics 365 Project Operations käyttää Universal Resource Scheduling -moottoria, jos sinulla on myös Dynamics 365 Field Service asennettuna,voit katsella resurssivarausten tietoja projekteille, työtilauksille ja mille tahansa muille kohteille, joihin olet laajentanut aikatauluttamisen.

Jos haluat tarkastella lisätietoja yksittäisestä resurssista, avaa resurssikortti napsauttamalla sitä hiiren kakkospainikkeella.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
