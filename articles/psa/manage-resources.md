---
title: Resurssien hallinta
description: Tässä aiheessa on tietoja resurssien hallinnasta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 5788a457c888bd2ab945fa52df82157a7c17d56b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589836"
---
# <a name="manage-resources"></a>Resurssien hallinta

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation sisältää resurssipäällikön koontinäytön, joka tarjoaa visuaalisen yleiskuvan resurssien kysynnöistä ja käytöstä koko organisaatiossa. Tämän koontinäytön kaavioita voidaan käyttää seuraavien tietojen visualisointiin:

- **Resurssin kysyntä** – Kaaviossa **Aktiivinen resurssipyyntö** näkyvät resurssit, jotka on lähetetty. Resurssit koostetaan joko roolin tai projektin perusteella.
- **Lähettämätön resurssin kysyntä** – Kaaviossa **Kohdentamaton resurssin kysyntä** näkyvät kaikki resurssitarpeet, joita ei ole lähetetty. Se auttaa resurssipäällikköitä tarkastelemaan kysyntää, joka ei ole vakaa ja joka voidaan lähettää resurssipyynnön kautta.
- **Kuluneen viikon laskutettava käyttö** – Kaaviossa **Roolikohtainen käyttö** näkyy organisaation todellisen roolikohtaisen laskutettavan käytön prosenttiosuus tavoitteena olevasta roolikohtaisesta laskutettavasta käytöstä.

    > [!NOTE]
    > Kaavio **Roolikohtainen käyttö** saadaan käyttöön luomalla työ, jossa suoritetaan UpdateRoleUtilization-työnkulku. Tämä toistuva työ suoritetaan seitsemän päivän välein seitsemän edellisen päivän laskutettavan käytön laskemista varten. Tulokset koostetaan roolikohtaisesti.

## <a name="manage-project-team-members"></a>Projektiryhmän jäsenten hallinta

Projektipäälliköt voivat käyttää resurssipäällikön koontinäyttöä projektien resurssien hallintaan. He voivat esimerkiksi lisätä ryhmän jäsenen suoraan projektiin ja varata ryhmän jäsenen täyttämään resurssitarpeet, jotka yleinen resurssi on tallentanut.

### <a name="add-a-team-member-directly-to-a-project"></a>Ryhmän jäsenen lisääminen suoraan projektiin

Ryhmän jäsen lisätään suoraan projektiin valitsemalla **Projektit**-sivun **Ryhmä**-välilehdessä **Uusi**. Näkyviin tulee **Pikaluonti: projektiryhmän jäsen** -valintaikkuna. Tässä valintaikkunassa voidaan suorittaa seuraavat tehtävät:

- **Varaa nimetty resurssi** – Valitse resurssin nimi kentässä **Varattavissa oleva resurssi**. Valitse sitten rooli, määritä ajanjakso ja valitse kohdennustapa. Valittu nimetty resurssi lisätään projektiin valittua kohdennustapaa ja resurssikalenteria käyttäen.
- **Lisää yleinen resurssi** – Jätä **Varattavissa oleva resurssi** -kenttä tyhjäksi ja valitse rooli, määritä ajanjakso ja valitse ensisijainen kohdennustapa. Ryhmään lisätään yleinen resurssi paikkamerkiksi säilyttämään kysyntämalli, jota käytetään nimettyjen resurssien varaamiseen ryhmässä. Tarve luodaan projektikalenterin mukaisesti.
- **Lisää ryhmään nimetty resurssi ilman resurssikapasiteetin käyttöä** – Valitse resurssi kentässä **Varattavissa oleva resurssi**. Määritä sitten ajanjakso ja valitse kohdennustavaksi **Ei mitään**. Resurssi lisätään ryhmään, mutta resurssin kapasiteettia ei käytetä varauksella.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Ryhmän jäsenen varaaminen yleisen resurssin resurssitarpeen täyttämiseen

PSA:ssa voit varata projektiryhmän yleisen resurssin ja määrittää roolin, tarvitun kapasiteetin ja kapasiteetin jaon. Resurssin kysynnässä voit määrittää määritteitä, jotka yhdistetään yleiseen resurssiin. Näitä määritteitä ovat tarvittavat osaamisalueet, ensisijainen organisaatioyksikkö ja ensisijaiset resurssit.

Noudata näitä vaiheita määrittääksesi kehittäjän yleisen resurssin tarvittavat osaamisalueet.

1. Varaa yleinen resurssi valitsemalla **Projektit**-sivun **Ryhmä**-välilehdessä **Uusi**.

    ![Ryhmässä varattu yleinen resurssi.](media/Resource-Management-image9.png)

2. Valitse **Kaikki ryhmän jäsenet** -näkymän **Resurssitarve**-sarakkeessa linkki lisätäksesi yleisen resurssin tarvittavat osaamisalueet.

    ![Tarvelinkki.](media/Resource-Management-image10.png)

3. Valitse näkyviin tulevan **Resurssitarve**-sivun **Osaamisalueet**-ruudukossa kolme pistettä (**...**) ja sitten **Lisää uusi tarveominaisuus** lisätäksesi kehittäjän tarvittavat osaamisalueet.

    ![Lisää uusi tarveominaisuus -komento.](media/Resource-Management-image11.png)

4. Valitse tarvittava osaamisalue näkyviin tulevan **Pikaluonti: tarveominaisuus** -valintaikkunan **Ominaisuus**-kentässä. Valitse sitten **Luokitusarvo** -kentässä kyseisen osaamisalueen pätevyystaso. Määritä lopuksi **Resurssitarve**-kentässä tarve hakemaan resursseja organisaatioyksiköistä tai jopa nimetyistä resursseista. Kun olet valmis, valitse **Tallenna**.

    ![Pikaluonti: Tarveominaisuus-valintaikkuna.](media/Resource-Management-image12.png)

5. Täytä resurssitarve valitsemalla **Resurssitarve**-sivulla **Varaa**.

    ![Resurssitarve-sivun varauspainike.](media/Resource-Management-image13.png)

    Voit myös valita yleisen resurssin **Kaikki ryhmän jäsenet** -ruudukossa ja valita sitten **Varaa**.

    ![Varauspainike Kaikki ryhmän jäsenet -ruudukon yläpuolella.](media/Resource-Management-image14.png)

    > [!NOTE]
    > Tässä esimerkissä on 40 tarvittua tuntia, mutta ei yhtään varattuja tunteja, koska yleisillä resursseilla ei ole varauksia. Lisäksi siinä ei ole kohdennettuja tunteja, koska yleinen resurssi on lisätty suoraan ryhmään. Sitä ei siis lisätty tehtävien kohdennuksella.

    **Ajoitusavustaja**-sivulla voit suodattaa käytettävissä olevia resursseja resurssitarpeessa määritettyjen tarpeiden mukaan. Resurssit lajitellaan aikataulutaulukossa määritettyjen lajitteluparametrien perusteella.

    ![Ajoitusavustaja-sivu.](media/Resource-Management-image15.png)

    Seuraavassa esitellään usein käytettyjä suodattimia:

    - **Ominaisuudet ja luokitus** – Suodata osaamisalueiden, sertifiointien ja muiden resurssien ominaisuuksien sekä pätevyysluokitusten mukaan.
    - **Roolit** – Suodata varattavissa oleville resursseille määritettyjen oletusroolien perusteella.
    - **Organisaatioyksiköt** – Suodata varattavissa olevia resursseja niille määritettyjen organisaatioyksiköiden perusteella.

6. Jos et ole tyytyväinen ensimmäisen tarvehaun tuloksiin, voit muuttaa suodatusperusteita. Laajenna **Suodatinnäkymä**-ruutu ja valitse **Haku** löytääksesi lisää resursseja.

    ![Suodatinnäkymä-ruutu.](media/Resource-Management-image16.png)

7. Voit muuttaa tulosten lajittelutapaa valitsemalla **Lajittele.**

    ![Lajittelukomento.](media/Resource-Management-image17.png)

8. Valitse resursseja tarpeessa määritetyn ja ruudukon yläosassa näkyvän kysynnän mukaisesti. Voit tyhjentää ruudukon solujen valinnan ja jättää kyseisen resurssikapasiteetin avoimeksi. Varatuksi voidaan valita vain yksi resurssi kerrallaan.

9. Varaa valittu resurssi valitsemalla **Varaa** ja jätä aikataulutaulukko avoimeksi, jotta voit valita lisää resursseja. Voit myös valita **Varaa ja poistu** varataksesi valitun resurssin ja sulkeaksesi aikataulutaulukon.

    ![Varattava resurssi.](media/Resource-Management-image19.png)

    Saat ilmoituksen varatuista tunneista. Kysynnän ilmaisimet näyttävät, kuinka suuri osa tarpeesta on täytetty ja kuinka paljon sitä on jäljellä. Voit myös katsoa, kuinka paljon valitun resurssin kapasiteetista on käytetty. Lisätietoja resurssin varauksista saat valitsemalla **Laajenna**.

9. Palaa **Kaikki ryhmän jäsenet** -näkymään. Huomaa, että yleinen resurssi on ruudukossa korvattu nimetyllä resurssilla ja että kyseiselle resurssille on merkitty 40 tuntia varatuksi.

    ![Päivitetty Kaikki ryhmän jäsenet -ruudukko.](media/Resource-Management-image20.png)

    > [!NOTE]
    > Kohdennettuja tunteja ei näytetä, koska ne varattiin suoraan ryhmässä. Niitä ei varattu tehtävien kohdennuksella.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Yleisten resurssien kohdennus tehtäville ja resurssitarpeiden luominen

PSA:ssa voit luoda tehtäviä ja sitten kohdentaa niille yleisiä resursseja. Tällöin paikkamerkit voivat edustaa resurssin kysyntää, kun arvioit aikatauluasi ja talouslukujasi. Tämän jälkeen voit luoda resurssitarpeita yleisille resursseille ja täyttää ne.

1. Luo tehtävä valitsemalla **Projektit**-sivun **Aikataulut**-välilehdeltä **Lisää**.

    ![Uusi tehtävä on luotu.](media/Resource-Management-image21.png)

2. Valitse **Resurssit**-kentässä **Resurssivalitsin**-symboli. Resurssivalitsin tulee näkyviin ja näyttää projektin olemassa olevat ryhmän jäsenet.

    ![Resurssivalitsin.](media/Resource-Management-image22.png)

3. Kirjoita uuden yleisen resurssin nimi ja valitse **Luo**.

    ![Uuden yleisen resurssin nimi on annettu.](media/Resource-Management-image23.png)

4. Valitse yleisen resurssin rooli näkyviin tulevan **Pikaluonti: projektiryhmän jäsen** -valintaikkunan **Rooli**-kentässä. Valitse yleiselle resurssille organisaatioyksikkö **Resursointiyksikkö**-kentässä. Valitse sitten **Tallenna**.

    ![Pikaluonti: projektiryhmän jäsen -valintaikkuna.](media/Resource-Management-image24.png)

    Yleinen ryhmän jäsen on nyt kohdennettu tehtävälle.

    ![Yleinen ryhmän jäsen on kohdennettu tehtävälle.](media/Resource-Management-image25.png)

    Uusi yleinen ryhmän jäsen näkyy **Ryhmä**-välilehdessä. Huomaa, että jäsenellä on vain kohdennettuja tunteja. Nämä tunnit ovat yhteismäärä kaikista yleiselle ryhmän jäsenelle kohdennetuista tehtävistä. Yleisellä ryhmän jäsenellä ei vielä ole tarvittuja tunteja tai resurssitarvetta.

    ![Yleinen ryhmän jäsen Ryhmä-välilehdessä.](media/Resource-Management-image26.png)

5. Voit nyt kohdentaa yleisen ryhmän jäsenen muihin tehtäviin resurssivalitsimen avulla.

    ![Yleinen ryhmän jäsen resurssivalitsimessa.](media/Resource-Management-image27.png)

    Kun olet kohdentanut yleisen resurssin haluamiisi tehtäviin, voit luoda resurssitarpeen yleiselle resurssille.

5. Valitse yleinen resurssi **Ryhmä**-välilehdessä ja valitse sitten **Luo tarve**.

    ![Luo tarve -komento.](media/Resource-Management-image28.png)

    Kun tarve on luotu, yleisellä ryhmän jäsenellä on tarvitut tunnit sekä linkki resurssitarpeeseen.

    ![Resurssitarpeen linkki.](media/Resource-Management-image29.png)

    Kun olet varannut nimetyn resurssin, yleinen resurssi poistetaan ryhmästä ja korvataan nimetyllä resurssilla.

    ![Nimetyllä resurssilla korvattu yleinen resurssi.](media/Resource-Management-image30.png)

    **Aikataulut**-välilehdellä yleisen resurssin kohdennukset poistetaan ja korvataan nimetyllä resurssilla.

    ![Yleisen resurssin kohdennukset korvataan nimetyllä resurssilla Aikataulut-välilehdessä.](media/Resource-Management-image31.png)

    > [!NOTE]
    > Tämä tapahtuu vain, kun nimetty resurssi on täysin varattu yleiselle resurssitarpeelle. Kun nimetty resurssi korvaa yleisen resurssitarpeen osittain tai useat nimetyt resurssit korvaavat resurssitarpeen, yleinen resurssi pysyy kohdennettuna tehtävälle.

    Seuraavassa kuvassa 80-tuntinen tehtävä on suunniteltu viiden päivän kestolle (16 tuntia päivässä viiden päivän ajan) ja kohdennettu yleiselle resurssille nimeltään **Toiminnallinen** (Functional).

    ![80-tuntinen ja viisipäiväinen tehtävä kohdennettuna yleiselle resurssille Toiminnallinen.](media/Resource-Management-image32.png)

    Kun luot tarpeen, se käsittää 80 tuntia viiden päivän aikana.

    ![Tarve luotu 80 tunnille viiden päivän aikana.](media/Resource-Management-image33.png)

    Koska käytettävissä olevat resurssit työskentelevät vain kahdeksan tuntia päivässä, tarpeen täyttämiseen tarvitaan kaksi resurssia.

    ![Toinen resurssi.](media/Resource-Management-image35.png)

    **Ryhmä**-välilehdessä näkyy nyt, että yleisellä resurssilla ei ole tarvittuja tunteja, mutta kohdennetut tunnit näkyvät yhä niiden kahden nimetyn resurssin kanssa, jotka täyttävät tarpeen.

    ![Kaksi nimettyä resurssia Ryhmä-välilehdessä.](media/Resource-Management-image36.png)

    **Aikataulut**-välilehdessä yleinen resurssi on edelleen kohdennettuna tehtävälle.

    ![Yleisiä resursseja Aikataulut-välilehdessä.](media/Resource-Management-image37.png)

PSA ei kohdenna molempia resursseja tehtävälle, koska silloin aikataulu olisi huonommin ennustettavissa. Tässä yksinkertaisessa esimerkissä tunnit on helppo jakaa tasan kahden resurssin kesken. Monimutkaisemmissa skenaarioissa, joihin liittyy useita tehtäviä ja useita resursseja, PSA:n on tehtävä oletuksia siitä, miten useille resursseille useissa tehtävissä tehdyt varaukset kohdennetaan.

Siksi projektipäällikkö on näissä skenaarioissa vastuussa useiden varausten jäsentelystä ja tarpeenmukaisesta kohdennuksesta. Varausten kohdistamiseksi projektipäällikkö siirtää tehtävät yleisiltä resursseilta nimetyille resursseille ja varmistaa **Täsmäytys**-näkymän avulla, että kohdistus toimii varausten kanssa.

### <a name="edit-a-resource-requirement"></a>Resurssitarpeen muokkaaminen

Kun resurssitarve on luotu, projektipäällikkö tai resurssipäällikkö voi haluta muokata tietoja tarkentaakseen hakuehtoja, kun käytetään aikataulutaulukkoa. Resurssitarvetta muokataan seuraavasti.

1. Valitse **Projektit**-sivun **Ryhmä**-välilehdestä linkki mihin tahansa yleisen resurssin tarpeeseen.
2. Näkyviin tulevalla **Resurssitarve**-sivulla voit päivittää useita määritteitä. Seuraavassa on joitakin esimerkkejä.

    - Nimi
    - Päivämäärästä
    - Päivämäärään
    - Kesto
    - Resurssityyppi

**Resurssitarve**-sivulla projektipäällikkö tai resurssipäällikkö voi määrittää myös seuraavat tiedot:

- Osaamisalueet
- Roolit
- Resurssin asetukset
- Ensisijainen organisaatioyksikkö

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Resurssivarausten päivittäminen, kun ne on varattu projektille

Kun olet lisännyt projektiryhmään yleisen tai nimetyn resurssin, voit muuttaa resurssin varauksia.

1. Valitse ryhmän jäsen **Projektit**-sivun **Ryhmä**-välilehdessä ja valitse sitten **Ylläpidä varauksia**.

    ![Valitun ryhmän jäsenen aikataulutaulukko avattuna.](media/Resource-Management-image40.png)

    Aikataulutaulukko tulee näkyviin, ja siinä näkyvät projektiryhmän jäsenen varaukset. Laajentamalla ryhmän jäsenen tietueen näet tunnit, jotka on varattu tälle projektille ja muille projekteille, joissa käytetään ryhmän jäsenen kapasiteettia.

2. Voit pidentää tai lyhentää varausta valitsemalla sen ja vetämällä sitä. Näkyviin tulee **Luo resurssivaraus**-valintaikkuna, jossa voit muokata varausta.

    ![Luo resurssivaraus -valintaikkuna.](media/Resource-Management-image41.png)

3. Napsauta varausta hiiren kakkospainikkeella. Voit käyttää tätä pikavalikkoa seuraaviin toimiin:

    - Varauksen tilan muuttaminen.
    - Varauksen muokkaaminen.
    - Projektiryhmän resurssin korvaaminen.

### <a name="change-the-booking-status"></a>Varauksen tilan muuttaminen

Voit muuttaa mitä tahansa oletusarvoista tai muokattua varauksen tilaa.

![Muuta tilaa -komento.](media/Resource-Management-image42.png)

PSA:ssa voidaan käyttää seuraavia tiloja:

- **Peruttu** – Tämä tila peruu resurssin varauksen ja vapauttaa resurssin kapasiteetin.
- **Sitova varaus** – Tämä tila käyttää resurssin kapasiteetin. Varauksella on yleensä tämä tila, kun **Ylläpidä varauksia** avataan **Kaikki ryhmän jäsenet** -ruudukossa **Projektit**-sivulla.
- **Alustava varaus** – Tämä tila lisää resurssin ryhmälle, mutta ei käytä resurssin kapasiteettia. Se ilmaisee, että resurssi on varattu mahdollista työtä varten ja että sillä on tästä huolimatta tarvittaessa kapasiteettia muita töitä varten. Resurssien kokonaiskäytettävyyden näkymässä alustavilla varauksilla on eri tila kuin sitovilla varauksilla.
- **Ehdotettu** – Tämä tila ilmaisee resurssipäällikön tai projektipäällikön resurssiehdotusta. Ehdotukset eivät käytä resurssin kapasiteettia, eikä resurssia lisätä projektiryhmään. Resurssin sitovaksi varaamiseksi ryhmälle projektipäällikön on hyväksyttävä ehdotus.

### <a name="submit-resource-requests"></a>Lähetä resurssipyyntöjä

Resurssipyyntöjä käytetään siirtämään kysyntöjä (resurssitarpeita), jotka resurssipäällikön on täytettävä. Jos kyse on ryhmällä jo olevasta yleisestä resurssista, resurssipyyntö voidaan lähettää suoraan. Resurssipyyntö voidaan täyttää kahdella tavalla:

- Resurssipäällikkö täyttää pyynnön suoraan. Tällöin yleinen resurssi korvataan sitovalla varauksella, jolla on nimetty resurssi.
- Resurssipäällikkö ehdottaa projektipäällikölle resurssia, ja projektipäällikkö hyväksyy tai hylkää ehdotetun resurssin.

#### <a name="direct-fulfillment-of-resource-requests"></a>Resurssipyyntöjen suora täyttäminen

Kun resurssitarve luodaan, projektipäällikkö voi lähettää yleistä resurssia koskevan resurssipyynnön valitsemalla resurssin ja sitten **Lähetä pyyntö**.

![Lähetä pyyntö -painike.](media/Resource-Management-image45.png)

Resursseja koskevia kommentteja voi antaa pyynnön täyttävälle resurssipäällikölle. Kun pyyntö on lähetetty, ryhmän jäsenen **Tila** -kentän arvoksi vaihtuu **Lähetetty**.

![Valinnaisten kommenttien antaminen.](media/Resource-Management-image46.png)

Kun resurssipäällikkö täyttää pyynnön, yleinen ryhmän jäsen korvataan nimetyllä resurssilla **Kaikki ryhmän jäsenet** -ruudukossa.

![Yleinen ryhmän jäsen korvattu nimetyllä resurssilla Kaikki ryhmän jäsenet -ruudukossa.](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Resurssiehdotusten käyttäminen resurssipyynnöissä

Resurssin suoran resurssipyyntöä varten varaamisen sijaan resurssipäällikkö voi ehdottaa projektipäällikölle resurssia. Resurssipäällikkö voi käyttää tätä vaihtoehtoa esimerkiksi, kun tarpeille ei ole tarkkaa vastaavuutta. Kun resurssipäällikkö ehdottaa resurssia, projektipäällikkö näkee, että yleisen ryhmän jäsenen **Tila**-kentän arvoksi vaihtuu **Tarkistettava**.

![Yleisen ryhmän jäsenen tilaksi vaihtunut Tarkistettava.](media/Resource-Management-image48.png)

Voit tarkastella ehdotettua resurssia yhdessä ehdotuksen varauksen vaikutuksen visualisoinnin kanssa kaksoisnapsauttamalla ryhmän jäsentä, jolla on tila **Tarkistettava**. Valitse sitten **Ehdotetut resurssit**-välilehti.

![Ehdotetut resurssit -välilehti.](media/Resource-Management-image49.png)

Voit hyväksyä kaikki ehdotukset valitsemalla **Hyväksy kaikki ehdotukset** ja hylätä ne valitsemalla **Hylkää kaikki ehdotukset**. Jos hyväksyt ehdotetut resurssit, ne varataan projektille sitovasti ryhmän jäseniksi ja korvaavat yleiset resurssit.

> [!NOTE]
> Kaikki ehdotukset on joko hyväksyttävä tai hylättävä. Niitä ei voi hyväksyä tai hylätä osittain.

### <a name="substitute-a-resource-on-the-project-team"></a>Projektiryhmän resurssin korvaaminen

Joskus projektipäällikön on korvattava projektille varattu ryhmän jäsen.

1. Valitse korvattava resurssi **Projektit**-sivun **Ryhmä**-välilehdessä ja valitse sitten **Ylläpidä varauksia**.
2. Näet projektit, joille resurssi on kohdennettu, laajentamalla resurssia.

    ![Laajennettu resurssi, jossa näkyvät sen projektit.](media/Resource-Management-image50.png)

3. Napsauta projektia hiiren kakkospainikkeella ja valitse **Korvaa resurssi**.
4. Jos tiedät, millä resurssilla haluat korvata nykyisen resurssin, valitse tai kirjoita resurssin nimi ja valitse **Delegoi uudelleen**.

    ![Korvaavan resurssin määrittäminen.](media/Resource-Management-image51.png)

    Vaihtoehtoisesti voit etsiä resurssia seuraavasti:

    1. Valitse **Etsi korvaava**.

        ![Korvaavan resurssin hakeminen.](media/Resource-Management-image52.png)

        Ajoitusavustaja palauttaa luettelon käytettävissä olevista korvaavista resursseista. Voit lisäksi suodattaa käytettävissä olevia resursseja ajoitusavustajassa löytääksesi sopivan korvaavan resurssin.

        ![Käytettävissä olevien korvaavien resurssien luettelo.](media/Resource-Management-image53.png)

    2. Korvaa resurssi valitsemalla haluamasi resurssi ja sitten **Korvaava**.

        ![Korvaava resurssi valittuna.](media/Resource-Management-image54.png)

    Varaukset ja kohdennukset siirretään uudelle resurssille.

    ![Varaukset ja kohdennukset siirretty uudelle resurssille.](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Ryhmän jäsenen varausten ja kohdennusten täsmäyttäminen

Ryhmän jäsenillä varaukset ja kohdennukset ovat löyhästi sidoksissa. Toisin sanoen resursseilla voi olla kohdennuksia ilman varauksia ja varauksia ilman kohdennuksia. Ihannetapauksessa varaukset ja kohdennukset ovat samoja, jotta resurssit ovat sitoutuneet suorittamaan kohdennettuja tehtäviään. Varaukset saattavat kuitenkin perustua käytettävyyteen ja tehtävien ajoitukset saattavat muuttua projektin edetessä. Siten varausten ja kohdennusten löyhä sidoksisuus luo joustavuutta.

PSA:ssa on **Täsmäytys**-välilehti, jonka avulla projektipäälliköt voivat täsmäyttää ryhmänsä jäsenten varaukset ja kohdennukset projektiryhmille.

![Täsmäytys-välilehti.](media/Resource-Management-image56.png)

**Täsmäytys**-välilehti näyttää kunkin ryhmän jäsenen varaukset ja kohdennukset yksittäisten tehtävien kohdennusten tasolle asti. Se näyttää tunnit soluissa, jotka edustavat aikajaksoja kuukausista päiviin asti.

Välilehdissä näkyy myös projektin kokonaissumma yhdessä summasarakkeen kanssa.

Välilehti laskee kunkin resurssin osalta koosteen erosta ryhmän jäsenen varausten ja ryhmän jäsenen kohdennettujen tehtävien välillä. Ihannetapauksessa eron pitäisi olla 0 (nolla). Varausten ja kohdennusten välillä ei siis pitäisi olla eroa. Erot on korostettu väreillä ja varjostuksilla, jotta huomio kiinnittyy kahteen tilanteeseen:

- **Varauspuute** – Varauspuutteessa on kyse siitä, että resurssilla on enemmän kohdennuksia kuin varauksia. Koska tätä kapasiteettia ei ole varattu, projektipäällikkö voi halutessaan korjata tämän tilanteen laajentamalla resurssin varauksia kattamaan puutteen.
- **Ylimääräiset varaukset** – ylimääräisiä varauksia tapahtuu, kun resurssi on kirjattu projektiin, mutta sitä ei ole kohdennettu tehtäviin. Tämä tilanne voi olla hyväksyttävä, jos resurssi on varattu projektille ennen tehtävien kohdentamista. Muissa tapauksissa resurssia ei kuitenkaan ole tarkoitus kohdentaa tehtäville. Näissä tapauksissa projektipäällikön tulisi harkita resurssin varausten peruuttamista, jotta kapasiteettia voidaan käyttää toisessa projektissa.

Kun aikaa tarkastellaan päivätasoa korkeammalla tasolla (kuten kuukausitasolla), resurssin nettoero voi olla nolla (tällöin varaukset = kohdennukset). Aikaa viikkotasolla tarkasteltaessa voi olla, että kohdennuksia on nolla tuntia, ja varauksia 40 tuntia ensimmäisellä viikolla, mutta 40 tuntia kohdennuksia ja nolla tuntia varauksia toisella viikolla. Yleisellä tasolla varaukset ja kohdennukset täsmäävät, mutta niiden välillä voi olla viikkokohtaisia eroja.

Aikaa korkeilla tasoilla tarkasteltaessa **Täsmäytys**-välilehden soluissa on ilmaisin, joka ilmoittaa, että alemmilla aikatasoilla on eroja. Kaksoisnapsauttamalla solua voit lähentää näkymää nähdäksesi eron. Voit sitten loitontaa näkymää napsauttamalla hiiren kakkospainiketta. Valitsemalla resurssin ja käyttämällä sitten **Seuraava ero** -ohjausobjektia voit siirtyä seuraavaan eroon resurssin varausten ja kohdennusten välillä. Voit myös palata takaisin käyttämällä **Edellinen ero** -ohjausobjektia. Voit myös poistaa eronilmaisimen ja siirtymistoiminnon käytöstä **Asetukset**-kohdassa.

![Eronilmaisin.](media/Resource-Management-image57.png)

Tilanteissa, joissa resurssille on kohdennuksia mutta ei varauksia, voit valita varauspuutteen **Projektit**-sivun **Täsmäytys**-välilehdessä ja valita sitten **Laajenna varausta**. Näkyviin tulee **Laajenna varausta** -valintaikkuna, jota tarvitaan resurssin puutteen käsittelemiseen. Ikkunassa näkyvät myös resurssin olemassa olevat varaukset kaikissa projekteissa tai muissa ajoitettavissa entiteeteissä. Jos valitset **OK** luodaksesi varauksen resurssille sen käytettävyydestä riippumatta, voit aiheuttaa ylivarauksen.

![Varaus-valintaikkunan laajentaminen.](media/Resource-Management-image58.png)

Projektipäällikkö tai resurssipäällikkö voi sitten käyttää aikataulutustaulua hallitakseen tilanteita, joissa resurssin varaukset ylittävät kapasiteetin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
