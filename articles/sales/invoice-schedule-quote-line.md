---
title: Projektipohjaisten tarjousrivien laskutusaikataulu
description: Tässä artikkelissa on tietoja laskutusaikataulun ja välitavoitteiden luomisesta tarjousriveille.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b1e431bc3586f9fef7a01348555e4ee4e06cc66c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918308"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Projektipohjaisten tarjousrivien laskutusaikataulu

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Projektipohjainella tarjousrivillä voi ilmaista laskutusaikataulun. Tämä on valinnaista tarjousvaiheen aikana, koska sovellus ei tue projektin laskuttamista, kun se on sidottu tarjousriviin. Laskutus on sallittu vain, kun tarjous on voitettu. Laskutusaikataulun tarjosuvaiheessa luomisen vaikutus loppupäähän on se, että tämä laskutusaikataulu kopioidaan projektipohjaiseen sopimusriviin. Jos et luo laskutusaikataulua tarjousvaiheen aikana, voit tehdä sen projektipohjaisella sopimusrivillä.

Laskutusaikataulun tarkoitus on kaiken kaikkiaan sallia projektipohjaisen sopimusrivin laskuluonnosten automaattinen luonti. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Aika- ja materiaalilaskutusaikataulun luominen projektipohjaiselle tarjousriville

Kun projektipohjaisen tarjousrivin laskutusmenetelmä on Aika ja materiaali, järjestelmä luo päivämäärään perustuvan laskutusaikataulun. Jos haluat luoda päivämäärään perustuvan laskutusaika taulun automaattisesti, tee seuraavat toimet.

1. Siirry kohtaan **Asetukset** > **Laskujen tiheys** ja määritä laskujen tiheys.
2. Avaa **Tarjoukset**-sivulla projektitarjous ja aseta pyydetty toimituspäivä **Yhteenveto**-välilehdessä.
3. Avaa aika-ja materiaalitarjousrivi, jolle haluat luoda päivämäärään perustuvan laskutusaikataulun. 
4. Valitse **Laskutusaikataulu**-välilehdellä **laskutuksen aloitus**- ja **Laskujen tiheys** -kenttien arvot. 
5. Valitse aliruudukossa **Luo laskutusaikataulu**.
6. Sovellus luo laskutusaikataulun, jossa on **Laskun suorituspäivä**-, **Tapahtuman katkaisupäivä**- ja **Suorituksen tila** -kentät määritetty seuraavasti:

    - **Laskun suorituspäivä** määritetään päivämääräksi, joka määräytyy laskujen tiheyden perusteella.
    - **Tapahtuman katkaisupäivä** -arvoksi on määritetty päivä ennen arvoa **Laskun suorituspäivä**.
    - **Suorituksen tila** -arvoksi määritetään automaattisesti **Ei suoritettu**. Kun automaattisen laskun luonnin työ suoritetaan tietylle laskun suorituspäivälle, se päivittää tämän kentän arvoksi joko **Suoritus onnistui** tai **Suoritus epäonnistui**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Kiinteähintaisen laskutusaikataulun luominen projektipohjaiselle tarjousriville

Kun projektipohjaisellatarjous rivillä on **Kiinteä hinta** laskutusmenetelmä, järjestelmä luo välitavoittepohjaisen laskutusaikataulun. Suorita seuraavat vaiheet, kun haluat luoda tämän aikataulun automaattisesti tietylle kalenterikaudelle tasaisesti jaetulle kiinteiden välitavoitteiden joukolle.

1. Siirry kohtaan **Asetukset** > **Laskujen tiheys** ja määritä laskujen tiheys.
2. Avaa **Tarjoukset**-sivulla projektitarjous ja aseta pyydetty toimituspäivä **Yhteenveto**-välilehdessä.
3. Avaa kiinteähintainen tarjousrivi, jolle on luotava välitavoiteaikataulu. 
4. Valitse **Laskutusaikataulu**-välilehdellä **laskutuksen aloitus**- ja **Laskujen tiheys** -kenttien arvot. 
5. Valitse aliruudukossa **Luo jaksoittaiset välitavoitteet**.
6. Sovellus luo laskutusaikataulun, jossa on välitavoitteen nimi, päivämäärä ja summa.

    - Välitavoitteen nimeksi määritetään päivämäärä, joka määräytyy laskujen tiheyden perusteella.
    - Välitavoitteen päivämääräksi määritetään päivämäärä, joka määräytyy laskujen tiheyden perusteella.
    - Välitavoitteen summa lasketaan jakamalla tarjouksen summa projektipohjaisella tarjousrivillä välitavoitteiden määrällä, joka määräytyy laskujen tiheyden sekä laskutuksen alkamispäivän ja pyydettyjen toimituspäivien mukaan.
    - Jos tarjousrivillä on myös arvioitu verosumma, tämä arvo jaetaan tasan kunkin välitavoitteen kesken samalla, kun luodaan jaksoittaisia välitavoitteita.

### <a name="manually-create-milestones"></a>Luo välitavoitteet manuaalisesti

Kiinteähintaisia välitavoitteita voidaan luoda myös manuaalisesti, jos niitä ei jaeta jaksoittain. Luo välitavoitteet manuaalisesti seuraavasti:

Avaa kiinteähintainen tarjousrivi, jolle on luotava välitavoite. Valitse **Laskutusaikataulu**-välilehden aliruudukossa **+ Luo uusi tarjousrivin välitavoite** ja anna tarvittavat tiedot seuraavan taulukon perusteella.

| **Kenttä** | **Sijainti** | **Kuvaus** | **Loppupään vaikutus** |
| --- | --- | --- | --- |
| Välitavoitteen nimi | Pikaluonti | Välitavoitteen nimi. | Tämä välitetään projektisopimusrivin välitavoitteeseen ja laskuun |
| Projektin tehtävä | Pikaluonti | Jos välitavoite on sidottu projektitehtävään, voit lisätä tämän viitteen avulla mukautetun logiikan, joka määrittää välitavoitteen tilan tehtävän tilan perusteella. | Sovelluksella ei ole tämän tehtävän viitteen suhteen vaikutusta loppupäähän. |
| Välitavoitteen päivämäärä | Pikaluonti | Määritä päivämäärä, jolloin automaattisen laskunluontiprosessin on etsittävä tämän välitavoitteen tila, jotta se voidaan ottaa huomioon laskutusta varten. | Tämä välitetään projektisopimusrivin välitavoitteeseen ja laskuun. |
| Laskun tila | Pikaluonti | Kun välitavoite luodaan, tämän tilan arvoksi on aina määritetty **Ei valmis laskutettavaksi**. | Tämä välitetään projektisopimusrivin välitavoitteeseen ja laskuun. |
| Rivisumma | Pikaluonti | Välitavoitteen summa tai arvo, joka laskutetaan asiakkaalta. | Tämä välitetään projektisopimusrivin välitavoitteeseen ja laskuun. |
| Vero | Pikaluonti | Välitavoitteeseen sovellettava verosumma. | Tämä välitetään projektisopimusrivin välitavoitteeseen ja laskuun. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]