---
title: Ryhmän jäsenien lisääminen Ryhmän jäsen -ruudukosta
description: Tässä aiheessa on tietoja Ryhmän jäsen -resurssien hallinnasta.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 0f975d295b4c0ccef9827767beabd32ffd761faa
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897717"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Ryhmän jäsenien lisääminen Ryhmän jäsen -ruudukosta

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations sisältää resurssipäällikön koontinäytön, joka tarjoaa visuaalisen yleiskuvan resurssien kysynnöistä ja käytöstä koko organisaatiossa. Tämän koontinäytön kaavioita voidaan käyttää seuraavien tietojen visualisointiin:

- **Resurssin kysyntä**: Kaaviossa **Aktiivinen resurssipyyntö** näkyvät resurssit, jotka on lähetetty. Resurssit koostetaan joko roolin tai projektin perusteella.
- **Lähettämätön resurssin kysyntä**: Kaaviossa **Kohdentamaton resurssin kysyntä** näkyvät kaikki resurssitarpeet, joita ei ole lähetetty. Tämä kaavio auttaa resurssipäällikköitä tarkastelemaan kysyntää, joka ei ole vakaa ja joka voidaan lähettää resurssipyynnön kautta.
- **Kuluneen viikon laskutettava käyttö**: Kaaviossa **Roolikohtainen käyttö** näkyy organisaation todellisen roolikohtaisen laskutettavan käytön prosenttiosuus tavoitteena olevasta roolikohtaisesta laskutettavasta käytöstä.

    > [!NOTE]
    > Kaavio **Roolikohtainen käyttö** saadaan käyttöön luomalla työ, jossa suoritetaan **UpdateRoleUtilization**-työnkulku. Tämä toistuva työ suoritetaan seitsemän päivän välein seitsemän edellisen päivän laskutettavan käytön laskemista varten. Tulokset koostetaan roolikohtaisesti.

## <a name="manage-project-team-members"></a>Projektiryhmän jäsenten hallinta

Projektipäälliköt voivat käyttää resurssipäällikön koontinäyttöä projektien resurssien hallintaan. He voivat esimerkiksi lisätä ryhmän jäsenen suoraan projektiin ja varata ryhmän jäsenen täyttämään resurssitarpeet, jotka yleinen resurssi on tallentanut.

### <a name="add-a-team-member-directly-to-a-project"></a>Ryhmän jäsenen lisääminen suoraan projektiin

Ryhmän jäsen lisätään suoraan projektiin valitsemalla **Projektit**-lomakkeen **Ryhmä**-välilehdessä **Uusi**. Näkyviin tulee **Pikaluonti: projektiryhmän jäsen** -valintaikkuna. Tässä valintaikkunassa voidaan suorittaa seuraavat tehtävät:

- **Varaa nimetty resurssi**: Valitse resurssin nimi kentässä **Varattavissa oleva resurssi**. Valitse sitten rooli, määritä ajanjakso ja valitse kohdennustapa. Valittu nimetty resurssi lisätään projektiin valittua kohdennustapaa ja resurssikalenteria käyttäen.
- **Lisää yleinen resurssi**: Jätä **Varattavissa oleva resurssi** -kenttä tyhjäksi ja valitse rooli, määritä ajanjakso ja valitse ensisijainen kohdennustapa. Yleinen resurssi lisätään ryhmään paikkamerkkinä. Paikkamerkki sisältää kysyntäkuvion, jota käytetään nimettyjen resurssien varaamiseen ryhmässä. Tarve luodaan projektikalenterin mukaisesti.
- **Lisää ryhmään nimetty resurssi ilman resurssikapasiteetin käyttöä**: Valitse resurssi kentässä **Varattavissa oleva resurssi**. Valitse ajanjakso ja valitse kohdennustavaksi **Ei mitään**. Resurssi lisätään ryhmään, mutta resurssin kapasiteettia ei käytetä varauksella.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Ryhmän jäsenen varaaminen yleisen resurssin resurssitarpeen täyttämiseen

Project Operationsissa voit varata yleisen resurssin projektiryhmässä. Voit myös määrittää tehtävän, tarvittavan kapasiteetin ja kapasiteetin jakamisen. Resurssitarpeessa voit määrittää määritteitä, jotka yhdistetään yleiseen resurssiin. Näitä määritteitä ovat tarvittavat osaamisalueet, ensisijainen organisaatioyksikkö ja ensisijaiset resurssit.

Suorita seuraavat vaiheet määrittääksesi kehittäjän yleisen resurssin tarvittavat osaamisalueet.

1. Varaa yleinen resurssi valitsemalla **Projektit**-lomakkeen **Ryhmä**-välilehdessä **Uusi**.
2. Valitse **Kaikki ryhmän jäsenet** -näkymän **Resurssitarve**-sarakkeessa linkki lisätäksesi yleisen resurssin tarvittavat osaamisalueet.
3. Valitse **Resurssitarve**-lomakkeen **Osaamisalueet**-ruudukossa kolme pistettä (**...**) ja sitten **Lisää uusi tarveominaisuus** lisätäksesi kehittäjän tarvittavat osaamisalueet.
4. Valitse tarvittava osaamisalue **Pikaluonti: tarveominaisuus** -valintalomakkeen **Ominaisuus**-kentässä.
5. Valitse **Luokitusarvo** -kentässä kyseisen osaamisalueen pätevyystaso. 
6. Määritä **Resurssitarve**-kentässä tarve hakemaan resursseja organisaatioyksiköistä tai jopa nimetyistä resursseista. Kun olet valmis, valitse **Tallenna**.
7. Täytä resurssitarve valitsemalla **Resurssitarve**-lomakkeessa **Varaa**. Voit myös valita yleisen resurssin **Kaikki ryhmän jäsenet** -ruudukossa ja valita sitten **Varaa**.

    > [!NOTE]
    > Tässä esimerkissä on 40 tarvittua tuntia, mutta ei yhtään varattuja tunteja, koska yleisillä resursseilla ei ole varauksia. Lisäksi siinä ei ole kohdennettuja tunteja, koska yleinen resurssi on lisätty suoraan ryhmään sen sijaan, että se lisättäsiin tehtävän delegoinnin kautta.

    **Ajoitusavustaja**-lomakkeessa voit suodattaa käytettävissä olevia resursseja resurssitarpeessa määritettyjen tarpeiden mukaan. Resurssit lajitellaan aikataulutaulukossa määritettyjen lajitteluparametrien perusteella.

   Joitain eniten käytettyjä suodattimia:

    - **Ominaisuudet ja luokitus**: Suodata osaamisalueiden, sertifiointien ja muiden resurssien ominaisuuksien sekä pätevyysluokitusten mukaan.
    - **Roolit**: Suodata varattavissa oleville resursseille määritettyjen oletusroolien perusteella.
    - **Organisaatioyksiköt**: Suodata varattavissa olevia resursseja niille määritettyjen organisaatioyksiköiden perusteella.

8. Jos et ole tyytyväinen ensimmäisen tarvehaun tuloksiin, voit muuttaa suodatusperusteita. Laajenna **Suodatinnäkymä**-ruutu ja valitse **Haku** löytääksesi lisää resursseja. Voit muuttaa tulosten lajittelutapaa valitsemalla **Lajittele.**
9. Valitse resursseja tarpeessa määritetyn ja ruudukon yläosassa näkyvän kysynnän mukaisesti. Voit tyhjentää ruudukon solujen valinnan ja jättää kyseisen resurssikapasiteetin avoimeksi. Varatuksi voidaan valita vain yksi resurssi kerrallaan.
10. Varaa valittu resurssi valitsemalla **Varaa** ja jätä aikataulutaulukko avoimeksi, jotta voit valita lisää resursseja. Voit myös valita **Varaa ja poistu** varataksesi valitun resurssin ja sulkeaksesi aikataulutaulukon.
11. Palaa **Kaikki ryhmän jäsenet** -näkymään. Huomaa, että yleinen resurssi on ruudukossa korvattu nimetyllä resurssilla ja että kyseiselle resurssille on merkitty 40 tuntia varatuksi.

    > [!NOTE]
    > Kohdennettuja tunteja ei näytetä, koska ne varattiin suoraan ryhmässä. Niitä ei varattu tehtävien kohdennuksella.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Yleisten resurssien kohdennus tehtäville ja resurssitarpeiden luominen

Project Operationsissa voit luoda tehtäviä ja sitten kohdentaa niille yleisiä resursseja. Paikkamerkit voivat näin edustaa resurssin kysyntää, kun arvioit aikatauluasi ja talouslukujasi. Tämän jälkeen voit luoda resurssitarpeita yleisille resursseille ja täyttää ne.

1. Luo tehtävä valitsemalla **Projektit**-lomakkeen **Aikataulut**-välilehdeltä **Lisää**.
2. Valitse **Resurssit**-kentässä **Resurssivalitsin**-symboli. Resurssivalitsin tulee näkyviin ja näyttää projektin olemassa olevat ryhmän jäsenet.
3. Kirjoita uuden yleisen resurssin nimi ja valitse **Luo**.
4. Valitse yleisen resurssin rooli näkyviin tulevan **Pikaluonti: projektiryhmän jäsen** -valintaikkunan **Rooli**-kentässä. 
5. Valitse yleiselle resurssille organisaatioyksikkö **Resursointiyksikkö**-kentässä. Valitse sitten **Tallenna**. Yleinen ryhmän jäsen on nyt kohdennettu tehtävälle.

   Uusi yleinen ryhmän jäsen näkyy **Ryhmä**-välilehdessä. Huomaa, että jäsenellä on vain kohdennettuja tunteja. Nämä tunnit ovat yhteismäärä kaikista yleiselle ryhmän jäsenelle kohdennetuista tehtävistä. Yleisellä ryhmän jäsenellä ei ole tarvittuja tunteja tai resurssitarvetta.

6. Voit nyt kohdentaa yleisen ryhmän jäsenen muihin tehtäviin resurssivalitsimen avulla.

   Kun olet kohdentanut yleisen resurssin haluamiisi tehtäviin, voit luoda resurssitarpeen yleiselle resurssille.

7. Valitse yleinen resurssi **Ryhmä**-välilehdessä ja valitse sitten **Luo tarve**. Kun tarve on luotu, yleisellä ryhmän jäsenellä on tarvitut tunnit sekä linkki resurssitarpeeseen.

  Kun olet varannut nimetyn resurssin, yleinen resurssi poistetaan ryhmästä ja korvataan nimetyllä resurssilla. **Aikataulut**-välilehdellä yleisen resurssin kohdennukset poistetaan ja korvataan nimetyllä resurssilla.

  > [!NOTE]
  > Tämä tapahtuu vain, kun nimetty resurssi on täysin varattu yleiselle resurssitarpeelle. Kun nimetty resurssi korvaa yleisen resurssitarpeen osittain tai useat nimetyt resurssit korvaavat resurssitarpeen, yleinen resurssi pysyy kohdennettuna tehtävälle.

Project Operations ei kohdenna molempia resursseja tehtävälle, koska silloin aikataulu olisi huonommin ennustettavissa. Tässä yksinkertaisessa esimerkissä tunnit on helppo jakaa tasan kahden resurssin kesken. Monimutkaisemmissa skenaarioissa, joihin liittyy useita tehtäviä ja useita resursseja, PSA:n on tehtävä oletuksia siitä, miten useille resursseille useissa tehtävissä tehdyt varaukset kohdennetaan.

Siksi projektipäällikkö on näissä skenaarioissa vastuussa useiden varausten jäsentelystä ja tarpeenmukaisesta kohdennuksesta. Varausten kohdistamiseksi projektipäällikkö siirtää tehtävät yleisiltä resursseilta nimetyille resursseille ja varmistaa **Täsmäytys**-näkymän avulla, että kohdistus toimii varausten kanssa.

### <a name="edit-a-resource-requirement"></a>Resurssitarpeen muokkaaminen

Kun resurssitarve on luotu, projektipäällikkö tai resurssipäällikkö voi haluta muokata tietoja tarkentaakseen hakuehtoja, kun käytetään aikataulutaulukkoa. Resurssitarvetta muokataan seuraavasti.

1. Valitse **Projektit**-lomakkeen **Ryhmä**-välilehdestä linkki mihin tahansa yleisen resurssin tarpeeseen.
2. Kirjoita näkyviin tulevaan **Resurssitarve**-lomakkeeseen tarvittavat kenttätiedot.

   **Resurssitarve**-lomakkeessa projektipäällikkö tai resurssipäällikkö voi myös määrittää osaamisalueet, roolit, resurssiasetukset ja ensisijaisen organisaatioyksikön.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Resurssivarausten päivittäminen, kun ne on varattu projektille

Kun olet lisännyt projektiryhmään yleisen tai nimetyn resurssin, voit muuttaa resurssin varauksia.

1. Valitse ryhmän jäsen **Projektit**-lomakkeen **Ryhmä**-välilehdessä ja valitse sitten **Ylläpidä varauksia**.
 
   Aikataulutaulukko tulee näkyviin, ja siinä näkyvät projektiryhmän jäsenen varaukset. Laajentamalla ryhmän jäsenen tietueen näet tunnit, jotka on varattu tälle projektille ja muille projekteille, joissa käytetään ryhmän jäsenen kapasiteettia.

2. Voit pidentää tai lyhentää varausta valitsemalla sen ja vetämällä sitä. Näkyviin tulee **Luo resurssivaraus**-valintaikkuna, jossa voit muokata varausta.
3. Napsauta varausta hiiren kakkospainikkeella. Voit käyttää tätä pikavalikkoa seuraaviin toimiin:

    - Varauksen tilan muuttaminen
    - Varauksen muokkaaminen
    - Projektiryhmän resurssin korvaaminen

### <a name="change-the-booking-status"></a>Varauksen tilan muuttaminen

Voit muuttaa mitä tahansa oletusarvoista tai muokattua varauksen tilaa.

Project Operationsissa voidaan käyttää seuraavia tiloja:

- **Peruttu**: Peruu resurssin varauksen ja vapauttaa resurssin kapasiteetin.
- **Sitova varaus**: kuluttaaa resurssin kapasiteettia. Varauksella on yleensä tämä tila, kun **Ylläpidä varauksia** avataan **Kaikki ryhmän jäsenet** -ruudukossa **Projektit**-lomakkeessa.
- **Alustava varaus** – Lisää resurssin ryhmälle, mutta ei käytä resurssin kapasiteettia. Tämä tila ilmaisee, että resurssi on varattu mahdollista työtä varten ja että sillä on tästä huolimatta tarvittaessa kapasiteettia muita töitä varten. Resurssien kokonaiskäytettävyyden näkymässä alustavilla varauksilla on eri tila kuin sitovilla varauksilla.
- **Ehdotettu** – Ilmaisee resurssipäällikön tai projektipäällikön resurssiehdotusta. Ehdotukset eivät käytä resurssin kapasiteettia, eikä resurssia lisätä projektiryhmään. Resurssin sitovaksi varaamiseksi ryhmälle projektipäällikön on hyväksyttävä ehdotus.

### <a name="submit-resource-requests"></a>Resurssipyyntöjen lähettäminen

Resurssipyyntöjä käytetään siirtämään kysyntöjä tai resurssitarpeita, jotka resurssipäällikön on täytettävä. Jos kyse on ryhmällä jo olevasta yleisestä resurssista, resurssipyyntö voidaan lähettää suoraan. Resurssipyyntö voidaan täyttää kahdella tavalla:

- Resurssipäällikkö täyttää pyynnön suoraan. Tällöin yleinen resurssi korvataan sitovalla varauksella, jolla on nimetty resurssi.
- Resurssipäällikkö ehdottaa projektipäällikölle resurssia, ja projektipäällikkö hyväksyy tai hylkää ehdotetun resurssin.

#### <a name="direct-fulfillment-of-resource-requests"></a>Resurssipyyntöjen suora täyttäminen

Kun resurssitarve luodaan, projektipäällikkö voi lähettää yleistä resurssia koskevan resurssipyynnön valitsemalla resurssin ja sitten **Lähetä pyyntö**. Resursseja koskevia kommentteja voi antaa pyynnön täyttävälle resurssipäällikölle. Kun pyyntö on lähetetty, ryhmän jäsenen **Tila** -kentän arvoksi vaihtuu **Lähetetty**. Kun resurssipäällikkö täyttää pyynnön, yleinen ryhmän jäsen korvataan nimetyllä resurssilla **Kaikki ryhmän jäsenet** -ruudukossa.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Resurssiehdotusten käyttäminen resurssipyynnöissä

Resurssin suoran resurssipyyntöä varten varaamisen sijaan resurssipäällikkö voi ehdottaa projektipäällikölle resurssia. Resurssipäällikkö voi käyttää tätä vaihtoehtoa esimerkiksi, kun tarpeille ei ole tarkkaa vastaavuutta. Kun resurssipäällikkö ehdottaa resurssia, projektipäällikkö näkee, että yleisen ryhmän jäsenen **Tila**-kentän arvoksi vaihtuu **Tarkistettava**.

Voit tarkastella ehdotettua resurssia sekä visualisointia ehdotuksen varauksen vaikutuksesta. 

1. Kaksoisnapsauta ryhmän jäsentä, jonka tila on **Tarkistettava**. 
2. Valitse **Ehdotetut resurssit**-välilehti.
3. Voit hyväksyä kaikki ehdotukset valitsemalla **Hyväksy kaikki ehdotukset** ja hylätä ne valitsemalla **Hylkää kaikki ehdotukset**. Jos hyväksyt ehdotetut resurssit, ne varataan projektille sitovasti ryhmän jäseniksi ja korvaavat yleiset resurssit.

> [!NOTE]
> Kaikki ehdotukset on joko hyväksyttävä tai hylättävä. Niitä ei voi hyväksyä tai hylätä osittain.

### <a name="substitute-a-resource-on-the-project-team"></a>Projektiryhmän resurssin korvaaminen

Joskus projektipäällikön on korvattava projektille varattu ryhmän jäsen.

1. Valitse korvattava resurssi **Projektit**-lomakkeen **Ryhmä**-välilehdessä ja valitse sitten **Ylläpidä varauksia**.
2. Näet projektit, joille resurssi on kohdennettu, laajentamalla resurssia.
3. Napsauta projektia hiiren kakkospainikkeella ja valitse **Korvaa resurssi**.
4. Jos tiedät, millä resurssilla haluat korvata nykyisen resurssin, valitse tai kirjoita resurssin nimi ja valitse **Delegoi uudelleen**.

Tai. Jos sinun on etsittävä resurssia, suorita seuraavat vaiheet.

1. Valitse **Etsi korvaava**.

   Ajoitusavustaja palauttaa luettelon käytettävissä olevista korvaavista resursseista. Voit lisäksi suodattaa käytettävissä olevia resursseja ajoitusavustajassa löytääksesi sopivan korvaavan resurssin.

2. Korvaa resurssi valitsemalla haluamasi resurssi ja sitten **Korvaava**.   

   Varaukset ja kohdennukset siirretään uudelle resurssille.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Ryhmän jäsenen varausten ja kohdennusten täsmäyttäminen

Ryhmän jäsenillä varaukset ja kohdennukset ovat löyhästi sidoksissa. Toisin sanoen resursseilla voi olla kohdennuksia ilman varauksia ja varauksia ilman kohdennuksia. Ihannetapauksessa varaukset ja kohdennukset ovat samoja, jotta resurssit ovat sitoutuneet suorittamaan kohdennettuja tehtäviään. Varaukset saattavat kuitenkin perustua käytettävyyteen ja tehtävien ajoitukset saattavat muuttua projektin edetessä. Siten varausten ja kohdennusten löyhä sidoksisuus luo joustavuutta.

Project Operationsissa on **Täsmäytys**-välilehti, jonka avulla projektipäälliköt voivat täsmäyttää ryhmänsä jäsenten varaukset ja kohdennukset projektiryhmille.

**Täsmäytys**-välilehti näyttää kunkin ryhmän jäsenen varaukset ja kohdennukset yksittäisten tehtävien kohdennusten tasolle asti. Se näyttää tunnit soluissa, jotka edustavat aikajaksoja kuukausista päiviin asti.

Välilehdissä näkyy myös projektin kokonaissumma yhdessä summasarakkeen kanssa.

Välilehti laskee kunkin resurssin osalta koosteen erosta ryhmän jäsenen varausten ja ryhmän jäsenen kohdennettujen tehtävien välillä. Ihannetapauksessa eron pitäisi olla 0 (nolla). Varausten ja kohdennusten välillä ei siis pitäisi olla eroa. Erot on korostettu väreillä ja varjostuksilla, jotta huomio kiinnittyy kahteen tilanteeseen:

- **Varauspuute** – Tässä on kyse siitä, että resurssilla on enemmän kohdennuksia kuin varauksia. Koska tätä kapasiteettia ei ole varattu, projektipäällikkö voi halutessaan korjata tämän tilanteen laajentamalla resurssin varauksia kattamaan puutteen.
- **Ylimääräiset varaukset** – Tämä tapahtuu, kun resurssi on kirjattu projektiin, mutta sitä ei ole kohdennettu tehtäviin. Tämä tilanne voi olla hyväksyttävä, jos resurssi on varattu projektille ennen tehtävien kohdentamista. Muissa tapauksissa resurssia ei kuitenkaan ole tarkoitus kohdentaa tehtäville. Näissä tapauksissa projektipäällikön tulisi harkita resurssin varausten peruuttamista, jotta kapasiteettia voidaan käyttää toisessa projektissa.

Kun aikaa tarkastellaan päivätasoa korkeammalla tasolla, kuten kuukausitasolla, resurssin nettoero voi olla nolla. Toisin sanoen varaukset = kohdennukset. Aikaa viikkotasolla tarkasteltaessa voi olla, että kohdennuksia on nolla tuntia, ja varauksia 40 tuntia ensimmäisellä viikolla, mutta 40 tuntia kohdennuksia ja nolla tuntia varauksia toisella viikolla. Yleisellä tasolla varaukset ja kohdennukset täsmäävät, mutta niiden välillä voi olla viikkokohtaisia eroja.

Aikaa korkeilla tasoilla tarkasteltaessa **Täsmäytys**-välilehden soluissa on ilmaisin, joka ilmoittaa, että alemmilla aikatasoilla on eroja. Kaksoisnapsauttamalla solua voit lähentää näkymää nähdäksesi eron. Voit sitten loitontaa näkymää napsauttamalla hiiren kakkospainiketta. Valitsemalla resurssin ja sitten **Seuraava ero** -kohtaa voit siirtyä seuraavaan eroon resurssin varausten ja kohdennusten välillä. Siirry takaisin valitsemalla **Edellinen ero**. Voit myös poistaa eronilmaisimen ja siirtymistoiminnon käytöstä **Asetukset**-kohdassa.

Tilanteissa, joissa resurssille on kohdennuksia mutta ei varauksia, voit valita varauspuutteen **Projektit**-lomakkeen **Täsmäytys**-välilehdessä ja valita sitten **Laajenna varausta**. Näkyviin tulee **Laajenna varausta** -valintaikkuna, jota tarvitaan resurssin puutteen käsittelemiseen. Valintaikkunassa näkyvät myös resurssin olemassa olevat varaukset kaikissa projekteissa tai muissa ajoitettavissa entiteeteissä. Jos valitset **OK** luodaksesi varauksen resurssille sen käytettävyydestä riippumatta, voit aiheuttaa ylivarauksen.

Projektipäällikkö tai resurssipäällikkö voi sitten käyttää aikataulutustaulua hallitakseen tilanteita, joissa resurssin varaukset ylittävät kapasiteetin.
