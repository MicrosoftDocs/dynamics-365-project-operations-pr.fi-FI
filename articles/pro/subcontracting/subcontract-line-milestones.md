---
title: Alihankintarivin välitavoitteet
description: Tässä artikkelissa käsitellään välitavoitteeseen perustuvan laskuaikataulun luontia ja ylläpitoa toimittajan kanssa tehdyssä alihankinnassa.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 431a57adf82c79f72d44886636183d48e0931f53
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522415"
---
# <a name="subcontract-line-milestones"></a>Alihankintarivin välitavoitteet

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operationsissa alihankintarivi, jossa on kiinteähintainen laskutusmenetelmä, voi määrittää välitavoitteeseen perustuvan laskuaikataulun toimittajan kanssa.

Toimittajan laskutuksen välitavoitteet voidaan luoda automaattisesti käyttämällä määritettyä toistumisväliä tai ne voidaan luoda manuaalisesti.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Välitavoitteeseen perustuvan laskuaikataulun luominen automaattisesti alihankintariville

Seuraavien vaiheiden mukaisesti voit luoda automaattisesti välitavoitteeseen perustuvan laskuaikataulun tasaisesti jaoteltujen välitavoitteiden kiinteälle joukolle.

1. Siirry kohtaan **Asetukset** > **Laskutustiheydet** ja määritä alihankintariveille laskutustiheys.
2. Avaa **Alihankinnat** -sivu, avaa alihankinta, jota haluat käsitellä ja avaa sitten kiinteähintainen alihankintarivi, jolle haluat luoda välitavoiteaikataulun.
3. Valitse **Alihankintarivien välitavoitteet** -välilehdestä **Luo jaksoittaiset välitavoitteet**.
4. Kirjoita tai valitse valintaikkunassa päivämääräväli, välitavoitteiden määrä ja laskutuksen tiheys. Voit valita aloituspäivän tai valita välitavoitteiden määrän ja laskutuksen tiheyden tai alkamispäivän tai valita päättymispäivän ja laskutuksen tiheyden. Päättymispäivää ja välitavoitteiden määrää ei voi valita.
Tämän tiedon avulla järjestelmä luo välitavoitteita ja tietueita, jotka näkyvät **Välitavoitteet**-ruudukossa.

   - **Välitavoitteen nimi** – Välitavoitteen nimeksi määritetään välitavoitteen päivämäärä laskun tiheyden perusteella.
   - **Välitavoitteen päivämäärä** – Laskutuksen tiheyteen perustuva päivämäärä.
   - **Välitavoitteen summa** – Laskettu jakamalla alihankintarivin välisumma välitavoitteiden määrällä.

Jos alihankintarivillä on arvo **Arvioitu verosumma** -kentässä, tämä arvo lisätään kuhunkin välitavoitteeseen tasaisesti jaksoittaisia välitavoitteita luotaessa.

Alihankintarivin välitavoitteiden kokonaissumman on oltava yhtä kuin alihankintarivin arvo. Jos ne eivät ole yhtä suuri, tapahtuu virhe. Voit korjata virheen ja tarkistaa, että välitavoitteen kokonaissumma on sama kuin alihankintarivin arvo luomalla, muokkaamalla tai poistamalla välitavoite- ja verosummia. Kun muutokset on tehty, voit varmistaa, että virheitä ei enää ole tallentamalla ja päivittämällä sivun.

## <a name="manually-create-subcontract-line-milestones"></a>Alihankintarivin välitavoitteiden manuaalinen luominen

Alihankintarivin kiinteähintaiset välitavoitteet voi luoda manuaalisesti, jos niitä ei jaeta kausittain. Luodaksesi alihankintarivin välitavoitteen manuaalisesti toimi seuraavasti.

1. Valitse siirtymisruudussa **Alihankinnat** ja avaa sitten alihankinta, jota haluat käsitellä.
2. Avaa kiinteähintainen alihankintarivi, jolle haluat luoda välitavoitteen.
3. Valitse **Alihankintarivin välitavoitteet** -välilehden aliruudukosta **+ Uusi alihankintarivin välitavoite**.
4. Syötä **Uusi alihankintarivin välitavoite** -sivulla tarvittavat tiedot seuraavan taulukon mukaisesti.

    | Kenttä | Kuvaus |Toiminnallinen vaikutus|
    | --- | --- |----------------------|
    | Välitavoitteen nimi | Välitavoitteen nimi. |Tämä näkyy kaikkien hakujen ensimmäisenä sarakkeena alihankintarivin välitavoitteiden perusteella. Tähän välitavoitteeseen perustuva toimittajan laskurivi käyttää myös alihankintarivin välitavoitteen nimeä toimittajan laskurivin oletusnimenä.|
    | Kuvaus | Välitavoitteen kuvaus. |Tähän välitavoitteeseen perustuva toimittajan laskurivi käyttää myös alihankintarivin välitavoitteen kuvausta toimittajan laskurivin oletuskuvauksena.|
    | Välitavoitteen päivämäärä | Päivämäärä, jolloin automaattisen laskun luontiprosessin tulisi etsiä tämän välitavoitteen tila, jotta se voidaan ottaa huomioon laskutuksessa.| Tätä arvoa käytetään toimittajan laskurivin oletuspäivämääränä, kun tätä alihankintariviä laskutetaan. |
    | Summa | Asiakkaalta laskutettavan välitavoitteen summa tai arvo. |Tätä arvoa käytetään toimittajan laskurivin oletusmääränä, kun tätä alihankintariviä laskutetaan. |
    | Vero | Välitavoitteessa käytetty verosumma.| Tätä arvoa käytetään toimittajan laskurivin oletusveromääränä, kun tätä alihankintariviä laskutetaan. |
    | Verollinen summa | Tämä vain luku -kenttä lasketaan muodossa summa + vero.|Tätä arvoa käytetään toimittajan laskurivin oletusarvona, kun tätä alihankintariviä laskutetaan. |
    | Laskun tila | Kun välitavoite on luotu, tämä tila määritetään aina arvoon **Ei valmis laskutukseen**.|  Kun tila on **Valmis laskutukseen**, toimittajan laskun luonti sisällyttää tämä välitavoitteen toimittajan laskuun. |

5. Valitse **Tallenna ja sulje**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
