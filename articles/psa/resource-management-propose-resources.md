---
title: Projektiresurssien ehdottaminen
description: Tässä aiheessa on tietoja projektiresurssien ehdottamisesta.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 1fcb8d1d40286cf5cbb23338f93b072ae5bed70d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120179"
---
# <a name="propose-project-resources"></a>Projektiresurssien ehdottaminen

Resurssipäälliköt voivat ehdottaa resurssia projektipäällikölle resurssipyynnön avulla.

1. Valitse pyyntöruudukosta tai itse pyynnöstä **Etsi resursseja**.
2. Valitse resurssi **Aikatauluavustaja**-sivulta, ja valitse sen jälkeen **Luo resurssivaraus** -ruudusta **Varaustila**-kentästä **Varaa**.

    ![Ehdotettu resurssi valittu](media/Resource-Management-image62.png)

Seuraavat tilapäivitykset toteutuvat:

- **Aikatauluavustaja** -sivulla tilailmaisimet päivittyvät ilmaisemaan, että varaus on ehdotettu eikä sitova.

    ![Ehdotetun varauksen tilailmaisimet Aikatauluavustaja -sivulla](media/Resource-Management-image63.png)

- Resurssipyynnössä tilaksi vaihtuu **Tarvitsee tarkistusta**.

    ![Resurssipyynnön tilaksi vaihtuu Tarvitsee tarkistusta.](media/Resource-Management-image64.png)

- Projektin **Ryhmä**-välilehdellä yleisen ryhmän jäsenen **Pyyntötilan** arvoksi vaihtuu **Tarvitsee tarkistusta**.

    ![Yleisen ryhmän jäsenen pyyntötila vaihtuu tilaksi Tarvitsee tarkistusta Ryhmä-välilehdellä.](media/Resource-Management-image48.png)

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

**Resurssien käyttöaste** -näkymä on **Resurssit**-ruudussa.

![Resurssien käyttöaste -näkymä](media/Resource-Management-image65.png)

Kukin ruudukon solu kuvaa resurssin laskutettavaa käyttöprosenttia kauden, esimerkiksi päivän, viikon tai kuukauden, aikana. Solujen värittämiseen käytetään seuraavia kaavoja:

- **Vihreä:** Laskutettava käyttö \>= Resurssin tavoitekäyttö
- **Keltainen:** Tavoitekäyttö – 20 \<= Laskutettava käyttö \< Tavoitekäyttö
- **Punainen:** Laskutettava käyttö \< Tavoitekäyttö – 20

Koska **Resurssien käyttöaste** -näkymä perustuu aikataulutaulutaulukkoon, voit suodattaa tuloksia käyttämällä aikataulutaulukon suodatustoimintoja.

Ruudukko edellyttää, että määrität kohteen käytön joko roolille tai yksittäiselle resurssille. Tämä määritetään kohteessa **Resurssit** \> **Resurssiroolit**.

Lisäksi jokaiselle varattavissa olevalle resurssille on määritettävä oletusrooli. Siirry kohtaan **Resurssit** \> **Resurssit**. Varmista **Project Service**-välilehdellä, että resurssin rooli on määritetty, ja että **Onko oletus** -kentän arvo on **Kyllä**. Voit llisätä muita rooleja, joiden **Onko oletus = Ei**. Roolia, jossa **Onko oletus = Kyllä** käytetään määrittämään resurssin käyttöaste tavoitteen mukaisesti.

![Oletusrooli asetettu](media/Resource-Management-image67.png)

**Project Service** -välilehdellä voit myös määrittää yksittäisen tavoitekäytön resurssille. Käytön laskenta käyttää sen jälkeen tätä tavoitekäyttöastetta määrittääkseen resurssin tavoitteen resurssin oletusroolin tavoitteen asemesta.

Resurssin käyttöaste näytetään ainoastaan, jos resurssilla on hyväksyttyä laskutettavaa aikaa sen jakson aikana, joka näkyy ruudukossa.

## <a name="resource-availability"></a>Resurssin käytettävyys

On tärkeää, että resurssipäälliköt voivat tarkastella resurssien saatavuutta ja päivittää varauksia. Joissakin tapauksissa ei ole virallista kysyntää (resurssipyyntöä), mutta resurssipäällikön on vastattava suunnittelemattomaan kysyntään, joka tulee esimerkiksi sähköpostitse, puhelimitse tai pikaviestin kautta. Resurssipäälliköt käyttävät aikataulutaulukkoa resurssien ja varausten päivittämiseen.

Resurssin työaikaa käytetään perusteena resurssin saatavuuden laskennassa. Resurssivaraukset kuluttavat resurssien kapasiteettia.

![Aikataulutaulukko](media/Resource-Management-image68.png)

Aikataulutaulukko käyttää värejä ja varjostusta, kun se näyttää varauksia, saatavuutta ja ylivarauksia sekä varausten tilan. Aikataulutaulukon asetusten avulla voit näyttää selitteen.

Jos yksittäisen varattavan resurssin vieressä näkyy oikealle osoittava nuoli aikataulutaulukossa, resurssi voidaan laajentaa niin, että siinä näkyvät sen työn tiedot, johon resurssi on varattu.

![Varattava resurssi laajennettuna aikataulutaulukossa](media/Resource-Management-image69.png)

Koska Dynamics 365 Project Service Automation käyttää Universal Resource Scheduling -moottoria, jos sinulla on myös Dynamics 365 Field Service asennettuna,voit katsella resurssivarausten tietoja projekteille, työtilauksille ja mille tahansa muille kohteille, joihin olet laajentanut aikatauluttamisen.

![Projektien ja työtilausten resurssivarausten tiedot](media/Resource-Management-image70.png)

Jos haluat tarkastella lisätietoja yksittäisestä resurssista, avaa resurssikortti napsauttamalla sitä hiiren kakkospainikkeella.

![Resurssikortti](media/Resource-Management-image71.png)
