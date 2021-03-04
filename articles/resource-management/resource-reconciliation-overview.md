---
title: Resurssin täsmäytyksen yleiskatsaus
description: Tässä aiheessa on tietoja, joiden avulla voit varmistaa, että projektien resurssivaraukset ja kohdennukset ovat linjassa.
author: ruhercul
manager: AnnBe
ms.date: 01/08/2021
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
ms.openlocfilehash: 8723cfad1e7cd07774e37023c5427b0a5833a554
ms.sourcegitcommit: cffc84187007b34211c90babef8af5152d4d92ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/12/2021
ms.locfileid: "4849620"
---
# <a name="resource-reconciliation-overview"></a>Resurssin täsmäytyksen yleiskatsaus

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Ryhmän jäsenillä varaukset ja kohdennukset ovat löyhästi sidoksissa. Toisin sanoen resursseilla voi olla kohdennuksia ilman varauksia ja varauksia ilman kohdennuksia. Ihannetapauksessa varaukset ja kohdennukset ovat samoja, jotta resurssit ovat sitoutuneet suorittamaan kohdennettuja tehtäviään. Varaukset saattavat kuitenkin perustua käytettävyyteen ja tehtävien ajoitukset saattavat muuttua projektin edetessä. Siten varausten ja kohdennusten löyhä sidoksisuus luo joustavuutta.

**Projektit**-sivulla on **Täsmäytys**-välilehti, jonka avulla projektipäälliköt voivat täsmäyttää ryhmänsä jäsenten varaukset ja kohdennukset projektiryhmille.

**Täsmäytys**-välilehti näyttää kunkin ryhmän jäsenen varaukset ja kohdennukset yksittäisten tehtävien kohdennusten tasolle asti. Tunnit näkyvät soluissa, jotka voivat edustaa aikajaksoja kuukausista päiviin. Välilehdissä näkyy myös projektin kokonaissumma yhdessä **summasarakkeen** kanssa.

**Täsmäytys**-välilehti laskee kunkin resurssin osalta koosteen erosta ryhmän jäsenen varausten ja ryhmän jäsenen kohdennettujen tehtävien välillä. Ihannetapauksessa eron pitäisi olla 0 (nolla). Varausten ja kohdennusten välillä ei siis pitäisi olla eroa. Erot on korostettu väreillä ja varjostuksilla, jotta huomio kiinnittyy kahteen tilanteeseen:

- **Varauspuute** – Varauspuutteessa on kyse siitä, että resurssilla on enemmän kohdennuksia kuin varauksia. Koska tätä kapasiteettia ei ole varattu, projektipäällikkö voi halutessaan korjata tämän tilanteen laajentamalla resurssin varauksia kattamaan puutteen.
- **Ylimääräiset varaukset** – ylimääräisiä varauksia tapahtuu, kun resurssi on kirjattu projektiin, mutta sitä ei ole kohdennettu tehtäviin. Tämä tilanne voi olla hyväksyttävä, jos resurssi on varattu projektille ennen tehtävien kohdentamista. Muissa tapauksissa, joissa resurssia ei ole suunnitelmissa delegoida tehtäviin, projektipäällikön on kuitenkin syytä harkita resurssin varausten peruuttamista. Tällä tavalla kapasiteettia voidaan käyttää toisessa projektissa.

Kun aikaa tarkastellaan päivätasoa korkeammalla tasolla (kuten kuukausitasolla), resurssin nettoero voi olla nolla (tällöin varaukset vastaavat kohdennuksia). Aikaa viikkotasolla tarkasteltaessa voi olla, että kohdennuksia on nolla tuntia, ja varauksia 40 tuntia ensimmäisellä viikolla, mutta 40 tuntia kohdennuksia ja nolla tuntia varauksia toisella viikolla. Yleisellä tasolla varaukset ja kohdennukset täsmäävät, mutta niiden välillä voi olla viikkokohtaisia eroja.

Aikaa korkeilla tasoilla tarkasteltaessa **Täsmäytys**-välilehden soluissa on ilmaisin, joka ilmoittaa, että alemmilla aikatasoilla on eroja. Kaksoisnapauttamalla tai kaksoisnapsauttamalla solua voit lähentää näkymää nähdäksesi eron. Voit sitten loitontaa näkymää valitsemalla ja pitämällä( tai napsauttamalla hiiren kakkospainiketta). Valitsemalla resurssin ja käyttämällä sitten **Seuraava ero** -ohjausobjektia voit siirtyä seuraavaan eroon resurssin varausten ja kohdennusten välillä. Voit myös palata takaisin käyttämällä **Edellinen ero** -ohjausobjektia. Voit myös poistaa eronilmaisimen ja siirtymistoiminnon käytöstä **Asetukset**-kohdassa.

Tilanteissa, joissa resurssille on kohdennuksia mutta ei varauksia, valitse varauspuute **Projektit**-sivun **Täsmäytys**-välilehdessä ja valita sitten **Laajenna varausta**. Näkyviin tulee **Laajenna varausta** -valintaikkuna, jota tarvitaan resurssin puutteen käsittelemiseen. Valintaikkunassa näkyvät myös resurssin olemassa olevat varaukset kaikissa projekteissa tai muissa ajoitettavissa entiteeteissä. Jos valitset **OK** luodaksesi varauksen resurssille sen käytettävyydestä riippumatta, voit aiheuttaa ylivarauksen.

**Laajenna varausta** -toiminnolla luodut varaukset liitetään ensisijaiseen projektivaatimukseen. Kun laajennus aloitetaan, sen tarkkaa laajennusvaatimusta ei voida määrittää, koska resurssiin voi liittyä useita projektia koskevia vaatimuksia.

Projektipäällikkö tai resurssipäällikkö voi sitten käyttää aikataulutustaulua hallitakseen tilanteita, joissa resurssin varaukset ylittävät kapasiteetin.
