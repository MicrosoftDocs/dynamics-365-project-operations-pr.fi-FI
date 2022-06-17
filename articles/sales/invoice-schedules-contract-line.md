---
title: Laskutusaikataulun luominen projektipohjaisella sopimusrivillä
description: Tässä artikkelissa on tietoja laskutusaikataulun ja välitavoitteiden luomisesta sopimusriveille.
author: rumant
ms.date: 10/17/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 490a61b67f54bdad95ecfce905191c381dddc85b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914996"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Laskutusaikataulun luominen projektipohjaisella sopimusrivillä 

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Voit luoda laskutusaikataulun projektipohjaiselle sopimusriville. Laskutus on sallittu vain, kun palvelusopimus on voitettu ja olet luomassa projektisopimusta. Laskun aikataulussa voi automaattisesti luoda projektipohjaisen sopimusrivin luonnoslaskuja. Jos kuitenkin luot laskuja manuaalisesti, voit ohittaa laskuaikataulun luomisen sopimusriveille.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Aika- ja materiaalilaskutusaikataulun luominen sopimusriville

Kun projektipohjaisella sopimusrivillä on aika- ja materiaalilaskutapa, voit luoda päivämäärään perustuvan laskuaikataulun. Jos haluat luoda päivämäärään perustuvan laskutusaika taulun automaattisesti, tee seuraavat toimet.

1. Siirry kohtaan **Asetukset** > **Laskujen tiheys** ja määritä laskujen tiheys.
2. Siirry projektisopimustietueeseen ja valitse haluamasi päivämäärä **Yhteenveto**-välilehden **pyydetty toimituspvm** -kentässä.
3. Avaa **aika- ja materiaali** -sopimusrivi, jolle haluat luoda päivämäärään perustuvan laskutusaikataulun. 
4. Valitse **Laskutusaikataulu**-välilehdellä laskutuksen aloitus- ja laskujen tiheys -kenttien arvot.
5. Valitse aliruudukossa **Luo laskutusaikataulu**. Luodaan laskutusaikataulu, jossa on **Laskun suorituspäivä**-, **Tapahtuman katkaisupäivä**- ja **Suorituksen tila** -kentät määritetty seuraavasti:

    - **Laskun suorituspäivä**: Tämän päivämäärän määrää laskutiheys.
    - **Tapahtuman katkaisupäivä**: Päivä ennen laskun suorituspäivää.
    - **Suorituksen tila**: Määritetään automaattisesti **Ei suoritettu**. Kun automaattisen laskun luonnin työ suoritetaan tietylle laskun suorituspäivälle, kentän arvoksi päivitetään joko **Suoritus onnistui** tai **Suoritus epäonnistui**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Kiinteähintaisen laskutusaikataulun luominen sopimusriville

Kun sopimusrivillä on kiinteähintainen laskutusmenetelmä, voit luoda välitavoitepohjaisen laskutusaikataulun. 

> [!NOTE]
> Sopimusriville ei voi luoda välitavoitteita, jos sopimusriviin ei ole liitetty yhtään projektia.

Suorita seuraavat vaiheet, jotta voit luoda välitavoitepohjaisen laskuaikataulun kiinteälle joukolle tasaisesti jaettuja välitavoitteita kalenterijaksolle.

1. Siirry kohtaan **Asetukset** > **Laskujen tiheys** ja määritä laskujen tiheys.
2. Siirry projektisopimustietueeseen ja valitse haluamasi päivämäärä **Yhteenveto**-välilehden **pyydetty toimituspvm** -kentässä.
3. Avaa **kiinteähintainen** sopimusrivi, jolle luot välitavoiteaikataulun. Valitse **Laskutusvälitavoitteet**-välilehdellä laskutuksen aloitus- ja laskujen tiheys -kenttien arvot. 
4. Valitse aliruudukossa **Luo jaksoittaiset välitavoitteet**. Laskun aikataulu luodaan siten, että **välitavoitteen nimi**, **välitavoitteen päivä** ja **välitavoitteen summa** -kentät ovat seuraavat:

    - **Välitavoitteen nimi**: Tämä nimi määräytyy laskun lähettämistiheyden mukaan.
    - **Välitavoitteen päivämäärä**: Tämän päivämäärän määrää laskutiheys.
    - **Välitavoitteen summa**: Tämä määrä lasketaan jakamalla sopimuksen summa sopimusrivillä välitavoitteiden määrällä, joka määräytyy laskujen tiheyden, laskutuksen alkamispäivän ja pyydettyjen toimituspäivien mukaan.

    Jos sopimusrivillä on arvo **arvioitu verosumma** -kentässä, tämä kenttä on myös suhteutettu kuhunkin välitavoitteeseen samalla tavalla, kun luodaan kausittaisia välitavoitteita.

Laskutuksen välitavoitteiden on vastattava sopimusrivin sovittua arvoa. Jos näin ei ole, saat virheilmoituksen **sopimusrivi**-sivulla. Voit korjata virheen tarkistamalla, että laskun välitavoitteet ovat rivin sopimuksen arvon mukaisia luomalla, muokkaamalla tai poistamalla välitavoitteita. Kun muutokset on tehty, voit poistaa virheen päivittämällä sivun.

### <a name="manually-create-milestones"></a>Luo välitavoitteet manuaalisesti

Voit luoda kiinteähintaisia välitavoitteita myös manuaalisesti, jos niitä ei jaeta jaksoittain. Luo välitavoite manuaalisesti suorittamalla seuraavat vaiheet.

1. Avaa kiinteän hinnan sopimusrivi, jolle olet luomassa välitavoitetta, ja **Valitse laskun ajoitus** -välilehden aliruudukossa **+ Luo uusi sopimusrivivälitavoite**. 
2. Kirjoita **välitavoitteen luonti** -sivulla seuraavan taulukon edellyttämät tiedot.

| Field | Sijainti | Kuvaus | Loppupään vaikutus |
| --- | --- | --- | --- |
| Välitavoitteen nimi | Pikaluonti | Välitavoitteen nimen tekstikenttä. | Tämä siirretään projektin sopimusrivin välitavoitteeseen ja laskuun. |
| Projektin tehtävä | Pikaluonti | Jos välitavoite on sidottu projektitehtävään, lisää tähän viitteeseen mukautettu logiikka asettaaksesi välitavoitteen tilan tehtävän tilan perusteella. | Sovelluksella ei ole tämän tehtävän viitteen suhteen vaikutusta loppupäähän. |
| Välitavoitteen päivämäärä | Pikaluonti | Määritä päivämäärä, jolloin automaattisen laskunluontiprosessin on etsittävä tämän välitavoitteen tila, jotta se voidaan ottaa huomioon laskutusta varten. | Tämä siirretään projektin sopimusrivin välitavoitteeseen ja laskuun. |
| Laskun tila | Pikaluonti | Kun välitavoite luodaan, tämän tilan arvoksi on aina määritetty **Ei valmis laskutettavaksi** tai **Ei aloitettu**. | Tämä siirretään projektin sopimusrivin välitavoitteeseen ja laskuun. |
| Rivisumma | Pikaluonti | Välitavoitteen summa tai arvo, joka laskutetaan asiakkaalta. | Tämä siirretään projektin sopimusrivin välitavoitteeseen ja laskuun. |
| Vero | Pikaluonti | Välitavoitteessa käytetty verosumma. | Tämä siirretään projektin sopimusrivin välitavoitteeseen ja laskuun. |

3. Valitse **Tallenna ja sulje**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]