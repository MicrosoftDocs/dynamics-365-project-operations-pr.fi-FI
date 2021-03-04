---
title: Myyntituottoarvioiden hallinta
description: Tässä aiheessa on tietoja myyntituottoarvioiden määrittämisestä projekteille.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531411"
---
# <a name="manage-revenue-estimates"></a>Myyntituottoarvioiden hallinta

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Voit luoda, laskea, kirjata, peruuttaa tai eliminoida tuottoarvioita. Voit tehdä tämän joko manuaalisesti tai kausittaisen prosessin avulla. Tässä aiheessa on tietoja myyntituottoarvioiden määrittämisestä projekteille.

### <a name="manage-revenue-estimates-manually"></a>Myyntituottoarvioiden manuaalinen hallinta

Valitse kiinteähintaisen tuoton arviointiprojektissa tai **Arviokysely** -sivulla (**Projektinhallinta ja kirjanpito** > **Raportit ja kyselyt** > **Arviokyselyt ja raportit**) **Arviot**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Tuottoarvioiden hallinta kausittaisen prosessin avulla

Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kausittainen** > **Arviot** ja valitse vastaava prosessi.

## <a name="create-a-revenue-estimate"></a>Tuottoarvion luominen

Suorita seuraavat vaiheet tuottoarvion luomiseksi. 

1. Siirry kohtaan **Projektinhallintaan ja kirjanpito** > **Kausittainen** > **Arviot**.
2. Valitse **Uusi**. Valitse seuraavat parametrit sivulla **Arvioiden luonti**:

   - **Kausikoodi** : Tämä koodi määrittää, kuinka usein arvioita kirjataan.
   - **Arvion päivämäärä**: Päivämäärä, jolloin arvio käsitellään.
   - **Jatkuva**: Valitse tämä valintaruutu, jos haluat luoda arvioita vain, jos edellisellä kaudella on kirjattu arvioita tai jos arvio on ensimmäinen luotu arvio. Jos tätä ei ole valittu, arviot luodaan, vaikka arvioita ei olisi kirjattu edelliselle kaudelle.
   - **Valmistumiskustannukset** -menetelmä: Määritä, miten jäljellä oleva projektityö arvioidaan. Lisätietoja on kohdassa [Valmistumiskustannusten menetelmät](cost-complete-methods.md).
   - **Valmistumismenetelmä**: Valitse valmistumismenetelmä seuraavista vaihtoehdoista:
     - **Automaattinen**: Valmistumisprosentti lasketaan automaattisesti ja laskentaan sisältyvien kustannusrivien perusteella. Kustannusmalli määrittää sisällytetyt kustannusrivit.
     - **Manuaalinen**: Valmistumisprosentti on yhtä suuri kuin viimeisen arvion valmistumisprosentti. Kun arvio on luotu, voit muuttaa arvoa **Manuaalinen laskenta** **Arviot**-sivulla.
     - **Kustannusmallista**: Automaattisen ja manuaalisen menetelmän yhdistelmä. Tämä asetus määritetään automaattisesti tai manuaalisesti kustannusmallin oletusarvon mukaan.
   - **Ennustemalli**: Valitse arviolle ennustemalli.
   - **Tulosta arvioluettelo**: Luo ja näytä arvioluettelo. Luettelo sisältää nykyisen funktion tilan. Voit tulostaa arviosta annetut varoitukset raporttiin. Seuraavat ehdot aiheuttavat varoitusten näkymisen arviointiluettelossa:
     - Valmistumisprosentti on yli 100.
     - Valmistumisprosentti on alle nolla.
     - Negatiivinen määrä **Valmistuu myöhemmin**-sarakkeessa.
     - Arvio, jolla ei ole vastaavaa sopimussummaa.
     - Arvio, jolla ei ole liitettyä kustannusarviota.
   - **Näytä infoloki**: Valitse tämä vaihtoehto, jos haluat saada sanoman, joka sisältää tietoja arviointiprojekteista, jotka on käsitelty työn suorituksen aikana.


## <a name="post-wip-or-accruals"></a>Kirjaa Käynnissä oleva tai kertymät

Kun arviot on arvioitu, ne säilyvät, pienenevät tai kasvavat. Voit sitten kirjata käynnissä olevan työn, kun käytössä on **Valmistunut sopimus** -arviointiperiaate, tai kirjata kertymän, kun käynnissä on **Valmistumisprosentti**-arviointiperiaate.
  
Arviointikauden tila muuttuu **Luodusta** **Kirjatuksi**.

## <a name="reverse-wip-or-accruals"></a>Peruuta käynnissä oleva työ tai kertymä

Käytä peruutustoimintoa palauttamaan jo kirjattu käynnissä oleva työ tai kertymä ja luo sen jälkeen arviot kaudelle.

> [!NOTE]
> Jos haluat peruuttaa kauden, joka on muiden kausien välissä, peruuta tarvittavat arviointikaudet ja kirjaa ne sitten uudelleen. Koska kaikki seuraavat kaudet määräytyvät edellisen kauden arvioiden mukaan, älä ohita kausia.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Arviointiprojektin poistaminen ja projektin lopettaminen

Arviointiprosessin viimeisessä vaiheessa poistetaan arviointiprojekti ja lopetetaan kiinteähintainen projekti, kun valmistumisprosentti on 100 prosenttia.

Seuraava tapahtuu, kun suoritat poiston:

- Jos kyseessä on kiinteähintainen projekti, jonka sopimus on täytetty, käynnissä olevan työn arvot tyhjenevät saldotileiltä ja kirjautuvat tuotto- ja tappiotileille.
- Jos kyseessä on kiinteähintainen projekti, jolla on valmistumisprosentti, kertymät poistetaan tuotto- ja tappiotileiltä.

Arvion tilaksi vaihtuu **Eliminoitu**.

> [!NOTE]
> Erityistapauksissa prosenttiosuus voi ulottua yli 100 prosenttiin. Kun näin tapahtuu, vähennä valmistumis prosenttia käyttämällä **Määritä valmistumiskustannuksiksi nolla -menetelmää**, jotta saavutetaan 100 prosenttia.

## <a name="reverse-elimination"></a>Poiston peruuttaminen

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kausittainen** > **Arviot** > **Peruuta poisto**. 
2. Valitse toimintoruudun **Prosessi**-välilehden **Ylläpito**-ryhmässä **Arvio**. 
3. Valitse **Peruuta poisto**.

Tämän sivun avulla voit peruuttaa kaikki poistot, joilla on tietty arviopäivä ja joiden arvio tila on **Eliminoitu**. Tapahtuman tila muuttuu sen jälkeen, kun olet valinnut tarvittavat kentät.

Tämä myös muuttaa automaattisesti projektin tilaksi **Työn alla**, jos projektin vaiheeksi on määritetty valmis. Projektikauden arvion tila vaihtuu takaisin arvoksi **Kirjattu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]