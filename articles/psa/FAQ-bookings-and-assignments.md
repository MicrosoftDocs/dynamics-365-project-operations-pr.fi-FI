---
title: Miten resurssivaraukset ja tehtävien delegoinnit liittyvät toisiinsa
description: Tässä aiheessa on tietoja siitä, miten hallita nimettyjä resursseja, resurssien varauksia ja resurssien delegointeja ja siitä, miten ne liittyvät toisiinsa.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 83b1bf39c71275f2e8e4ec20082f711154696586
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286199"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Miten resurssivaraukset ja tehtävien delegoinnit liittyvät toisiinsa

[!include [banner](../includes/psa-now-project-operations.md)]

Nimettyjä resursseja voidaan varata projektiryhmälle ja delegoiduille projektitehtäville kahdella tavalla:

- Resurssi voidaan varata suoraan projektiin ja sitten delegoida projektitehtäville.
- Tehtävät voidaan delegoida yleiselle resurssille, jota käytetään, kun yleinen etsitään ja korvataan nimetyllä resurssilla. 

Molemmissa tapauksissa resurssin varaamisen yhteydessä varataan resurssin kapasiteetti.

Projektipäällikkö, joka suunnittelee projektin, omistaa projektisuunnitelman ja -aikataulun. Kun projektipäällikkö käyttää delegoinnissa yleistä resurssia ja luo resurssipyynnön siitä, hän voi varata resursseja projektiin ilman projektisuunnitelmassa määritettyjä jaksottumisia. Projektipäälliköt voivat varata resursseja projektiin ja delegoida niitä sitten tehtäville. He eivät kuitenkaan voi kohdistaa varausten jaksottumisia tehtävien jaksottumisiin. Varaukset eivät vaikuta projektiaikatauluun.

Järjestelmässä voi olla esimerkiksi monimutkainen projekti, jonka useiden päällekkäisten tehtävien samantyyppisiä resursseja on käsiteltävä samanaikaisesti. Jos resurssille on annettu jaksottuminen, joka on erilainen kuin niiden delegointien koonti, tehtäviä on vaikea muokata niin, että ne sopivat varausten jaksottumiseen niiden erillisissä tehtävissä ja niiden alkuperäisissä jaksottumisissa.

ALla olevassa esimerkissä neljän tehtävän joukon saman resurssin edellyttämä kokonaistyö on 62 tuntia kahden viikon jakson aikana. Sille on määritetty tietty jaksottuminen. Jos resurssille Bob on varattu 62 tuntia saman kahden viikon aikana, mutta jaksottuminen on eri, tarpeen ja varausten tasaus on tehty.

| **Tehtävien jaksottumiset**    | **Tunnit yhteensä** | Ma 4.6. | Ti 5.6. | Ke 6.6. | To 7.6. | Pe 8.6. | La 9.6. | Su 10.6. | Ma 11.6. | Ti 12.6. | Ke 13.6. | To 14.6. | Pe 15.6. |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Tehtävä 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Tehtävä 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Tehtävä 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Tehtävä 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Summat**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Bobin käytettävyys
| **Resurssin varaus** | **Tunnit yhteensä** | Ma 4.6. | Ti 5.6. | Ke 6.6. | To 7.6. | Pe 8.6. | La 9.6. | Su 10.6. | Ma 11.6. | Ti 12.6. | Ke 13.6. | To 14.6. | Pe 15.6. |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Varattujen resurssien jaksottumisen tehtäviin delegointia varten päiväkohtaisesti ei kuitenkaan ole systemaattista tapaa. Jos projektipäällikkö haluaa muuttaa projektiaikataulua niin, että se vastaa resurssin käytettävyyttä, delegointi on poistettava ja kaikkia tehtäviä muutettava niin, että ne vastaavat varauksen jaksottumisia.

Jos organisaatio on antanut projektin suunnittelutehtävän sekä projektipäällikölle että resurssipäällikölle palvelupyynnössä, projektipäällikkö määrittää aikataulun. Aikataulu sisältää vaaditun työn jakso jaksottumisen. Projektipäällikön tulee tietää, jos resurssipäällikkö muuttaa työn jaksottumisia todellisten resurssien varaamisen yhteydessä ja vaikuttaa näin aikatauluun. Jos resurssipäällikkö toteuttaa jotain, mitä projektipäällikkö ei ole pyytänyt, resurssipäällikön ja projektipäällikön on sovittava projektiaikatauluun tehtävistä muutoksista yhdessä.

Koska varauksia ja delegointeja ei ole yhdistetty tiiviisti, on mahdollista varata tehtävien jaksottumisista poikkeavia jaksottumisia tai muuttaa delegointeja, jolloin varaukset ja delegoinnit eivät vastaa toisiaan.

**Täsmäytys**-näkymän avulla projektipäällikkö voi tarkastella kunkin projektiryhmän jäsenen varauksia ja delegointeja. Ryhmän jäsenten varausten ja delegointien väliset ristiriidat esitetään näkymässä värien ja varjostusten avulla. Näiden tietojen perusteella projektipäällikkö voi laajentaa resurssin varauksia niissä palvelupyynnöissä, joissa on delegointeja mutta ei varauksia, tai peruuttaa varauksia, jos resursseja on varattu ilman delegointeja.

> [!NOTE]
> Jos siirrät tehtävän, jolle olet määrittänyt jaksottumisen itse, jaksottumisia ei ylläpidetä. Jaksotukset luodaan projektikalenterin mukaan. Niiden avulla otetaan huomioon työajan ja lomien muutokset. Tämä on tarkoituksellista, koska järjestelmä ei tunnista alkuperäisen jaksottumisen tarkoitusta eikä pysty määrittämään sitä, kannattaako jaksottuminen säilyttää uudella ajanjaksolla. Koska varauksia ja delegointeja ei ole yhdistetty, varaukset säilytetään alkuperäisten varausten jaksottumisissa. Tällöin varaus on peruutettava ja tehtävä varaus uudelleen uuden delegoinnin jaksottumiseen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]