---
title: Alihankintarivin välitavoitteet
description: Tässä aiheessa selitetään, miten luodaan ja ylläpidetaan välitavoitteeseen perustuvaa laskuaikataulua toimittajan kanssa tehdyssä alihankinnassa.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7f99853f5f649f96225b7d72580db97bb92de7c5
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558498"
---
# <a name="subcontract-line-milestones"></a>Alihankintarivin välitavoitteet

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

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