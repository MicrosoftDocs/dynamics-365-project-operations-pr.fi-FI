---
title: Toimittajan laskun välitavoitteiden rivit
description: Tässä artikkelissa käsitellään toimittajan laskurivien luontia alihankintasopimuksen välitavoitteita varten.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 212d68c32e712ac2349d1670f9e799bcc5144148
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931326"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Toimittajan laskun välitavoitteiden rivit

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Microsoft Dynamics 365 Project Operationsin toimittajan laskussa voi olla toimittajan laskurivejä välitavoitteita varten, jotka on määritetty alihankintasopimuksen rivillä. Projektipäälliköt voivat kirjata välitavoitteiden toimittajan laskurivien avulla niiden palvelujen kustannukset, jotka hankitaan välitavoitepohjaisina kustannuksina, jotka aiheutuvat projektiin hankituista palveluista tai tuotteista.

Välitavoitteiden toimittajan laskuriveillä on aina viitattava alihankintasopimuksen riviin, jolla on kiinteähintainen laskutustapa. Kun toimittajan välitavoitelaskurivi viittaa alihankintasopimuksen riviin, projektipäälliköt voivat yhdistää ja tarkistaa perustana olevat ajan, kulujen ja materiaalien kustannukset, jotka viittaavat kyseiseen alihankintasopimuksen riviin välitavoitteen suhteen ja jonka toimittaja laskuttaa.

Seuraavassa taulukossa on tietoja toimittajan välitavoitelaskurivien kentistä.

| Field | Description | Toiminnallinen vaikutus |
| --- | --- | --- |
| Name | Toimittajan laskurivin nimi tunnistamisen helpottamiseksi. | Tämä nimi näkyy kaikkien toimittajan laskuriveihin perustuvien valintojen ensimmäisenä sarakkeena. |
| Description | Lyhyt kuvaus palveluista, joita toimittaja laskuttaa toimittajan laskurivillä. | Ei mikään |
| Alihankinta | Alihankinta, jossa palvelut tilattiin alun perin. | Kun toimittajan laskulle valitaan alihankinta, kaikki toimittajan laskurivit perivät tämän valinnan. Toimittajan laskussa ei voi olla toimittajan laskurivejä, jotka viittaavat eri alihankintoihin. |
| Alihankintarivi | Alihankintarivi, jossa palvelut tilattiin alun perin. Valittavissa olevien alihankintarivien luettelo rajoittuu valitun alihankkijan riveihin. | Kun toimittajan laskurivillä valitaan alihankintarivi välitavoitteille, **Rooli**- ja **Tapahtumaluokka**-kentät sekä tuotteeseen liittyvät kentät eivät ole oleellisia, eikä niitä voi käyttää. **Määrä**-, **Yksikkö**- ja **Yksikköryhmä**-kentillä ei myöskään ole merkitystä välitavoitepohjaisiin toimittajan laskuriveihin. |
| Tapahtuman päivä | Päivämäärä, jona toimittajan laskurivin todellinen kustannus kirjataan projektiin. | Ei mikään |
| Tapahtumaluokka | Valitse **Välitavoite**, jos haluat kirjata toimittajan laskun valmistunutta välitavoitetta varten, joka on määritetty alihankintasopimuksen rivillä. | Ei mikään |
| Välitavoite | Valitse liittyvällä alihankintarivillä määritetty välitavoite, joka on merkitty **Valmis laskutettavaksi**. | Alihankintasopimuksen rivin välitavoitteelle, jonka tila on **Valmis laskutettavaksi** voidaan valita toimittajan laskurivillä. |
| Project | Sen projektin nimi, jossa laskutettavat palvelut on käytetty. | Tämä kenttä on pakollinen, eikä sitä voi jättää tyhjäksi. |
| Tehtävä | Sen projektitehtävän nimi, jossa laskutettavat palvelut on käytetty. Tämä kenttä on käytettävissä vain, jos projekti on valittu. Projektitehtävän valinta on valinnainen. | Jos tämä kenttä jätetään tyhjäksi, projektipäällikkö voi yhdistää toimittajan laskurivin liittyvän alihankintasopimuksen tapahtumaluokkaan, joka on kirjattu mihin tahansa projektin tehtävään. Jos toimittajan laskurivillä ei ole viittausta alihankkijariviin ja tämä kenttä jätetään tyhjäksi, toimittajan laskurivin luomaa kustannusta ei linkitetä laskuttamattoman myynnin toteutuneisiin arvoihin. Tässä tapauksessa jos tehtäväpohjainen laskutus on määritetty, kustannuksia ei ehkä voi laskuttaa loppuasiakkaalta. |
| Välitavoitteen summa | Anna liittyvällä alihankintarivillä määritetyn välitavoitteen arvo, joka on valmis laskutettavaksi. | Ei mikään |
| Arvonlisävero | Anna arvonlisäveron summa. | Ei mikään |
| Loppusumma | Toimittajan laskurivin kokonaissumma verot mukaan lukien. Tämä kenttä lasketaan muodossa *Välitavoitteen summa* +  *arvonlisävero*. | Ei mikään |

> [!NOTE]
> Kun luodaan toimittajan laskurivi, joka viittaa alihankintasopimuksen rivin välitavoitteen, alihankintasopimuksen välitavoitteen tilaksi päivittyy **Toimittajan lasku luotu**. Kun toimittajan lasku vahvistetaan, alihankintasopimuksen rivin välitavoitteen tilaksi päivittyy **Toimittajan lasku vahvistettu**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
