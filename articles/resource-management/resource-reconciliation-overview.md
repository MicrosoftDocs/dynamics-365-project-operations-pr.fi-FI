---
title: Resurssin täsmäytyksen yleiskatsaus
description: Tässä aiheessa on tietoja siitä, että projektin resurssien varaukset ja toimeksiannot on kohdistettu.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.openlocfilehash: 574afac3bf5d1f6e5e13d8c61aa1ace6188f4008
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125714"
---
# <a name="resource-reconciliation-overview"></a>Resurssin täsmäytyksen yleiskatsaus

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Ryhmän jäsenillä varaukset ja kohdennukset ovat löyhästi sidoksissa. Toisin sanoen resursseilla voi olla kohdennuksia ilman varauksia ja varauksia ilman kohdennuksia. Ihannetapauksessa varaukset ja kohdennukset ovat samoja, jotta resurssit ovat sitoutuneet suorittamaan kohdennettuja tehtäviään. Varaukset saattavat kuitenkin perustua käytettävyyteen ja tehtävien ajoitukset saattavat muuttua projektin edetessä. Siten varausten ja kohdennusten löyhä sidoksisuus luo joustavuutta.

**Täsmäytys**-välilehti **Projekti**-lomakkeella antaa projektipäälliköille mahdollisuuden täsmäyttää ryhmänsä jäsenten varaukset ja kohdennukset projektiryhmille.

**Täsmäytys**-välilehti näyttää myös kunkin ryhmän jäsenen varaukset ja kohdennukset yksittäisten tehtävien kohdennusten tasolle asti. Tunnit näytetään soluissa, jotka edustavat aikajaksoja kuukausista päiviin asti.

Välilehdissä näkyy myös projektin kokonaissumma yhdessä **summasarakkeen** kanssa.

Välilehti laskee kunkin resurssin osalta koosteen erosta ryhmän jäsenen varausten ja ryhmän jäsenen kohdennettujen tehtävien välillä. Ihannetapauksessa eron pitäisi olla 0 (nolla). Varausten ja kohdennusten välillä ei siis pitäisi olla eroa. Erot on korostettu väreillä ja varjostuksilla, jotta huomio kiinnittyy kahteen tilanteeseen:

- **Varauspuute** – Varauspuutteessa on kyse siitä, että resurssilla on enemmän kohdennuksia kuin varauksia. Koska tätä kapasiteettia ei ole varattu, projektipäällikkö voi halutessaan korjata tämän tilanteen laajentamalla resurssin varauksia kattamaan puutteen.
- **Ylimääräiset varaukset** – ylimääräisiä varauksia tapahtuu, kun resurssi on kirjattu projektiin, mutta sitä ei ole kohdennettu tehtäviin. Tämä tilanne voi olla hyväksyttävä, jos resurssi on varattu projektille ennen tehtävien kohdentamista. Muissa tapauksissa resurssia ei kuitenkaan ole tarkoitus kohdentaa tehtäville. Näissä tapauksissa projektipäällikön tulisi harkita resurssin varausten peruuttamista, jotta kapasiteettia voidaan käyttää toisessa projektissa.

Kun aikaa tarkastellaan päivätasoa korkeammalla tasolla (kuten kuukausitasolla), resurssin nettoero voi olla nolla (tällöin varaukset = kohdennukset). Aikaa viikkotasolla tarkasteltaessa voi olla, että kohdennuksia on nolla tuntia, ja varauksia 40 tuntia ensimmäisellä viikolla, mutta 40 tuntia kohdennuksia ja nolla tuntia varauksia toisella viikolla. Yleisellä tasolla varaukset ja kohdennukset täsmäävät, mutta niiden välillä voi olla viikkokohtaisia eroja.

Aikaa korkeilla tasoilla tarkasteltaessa **Täsmäytys**-välilehden soluissa on ilmaisin, joka ilmoittaa, että alemmilla aikatasoilla on eroja. Kaksoisnapsauttamalla solua voit lähentää näkymää nähdäksesi eron. Voit sitten loitontaa näkymää napsauttamalla hiiren kakkospainiketta. Valitsemalla resurssin ja käyttämällä sitten **Seuraava ero** -ohjausobjektia voit siirtyä seuraavaan eroon resurssin varausten ja kohdennusten välillä. Voit myös palata takaisin käyttämällä **Edellinen ero** -ohjausobjektia. Voit myös poistaa eronilmaisimen ja siirtymistoiminnon käytöstä **Asetukset**-kohdassa.


Tilanteissa, joissa resurssille on kohdennuksia mutta ei varauksia, voit valita varauspuutteen **Projektit**-sivun **Täsmäytys**-välilehdessä ja valita sitten **Laajenna varausta**. Näkyviin tulee **Laajenna varausta** -valintaikkuna, jota tarvitaan resurssin puutteen käsittelemiseen. Ikkunassa näkyvät myös resurssin olemassa olevat varaukset kaikissa projekteissa tai muissa ajoitettavissa entiteeteissä. Jos valitset **OK** luodaksesi varauksen resurssille sen käytettävyydestä riippumatta, voit aiheuttaa ylivarauksen.

Projektipäällikkö tai resurssipäällikkö voi sitten käyttää aikataulutustaulua hallitakseen tilanteita, joissa resurssin varaukset ylittävät kapasiteetin.

