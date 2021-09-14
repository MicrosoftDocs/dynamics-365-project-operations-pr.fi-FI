---
title: Alihankintarivin välitavoitteet
description: Tässä aiheessa selitetään, miten luodaan ja ylläpidetaan välitavoitteeseen perustuvaa laskuaikataulua toimittajan kanssa tehdyssä alihankinnassa.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3301e5a627e4842009fcd5e352f1b76fd3053ee3
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323772"
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

    | Kenttä | Kuvaus |
    | --- | --- |
    | Välitavoitteen nimi | Välitavoitteen nimi. |
    | Kuvaus | Välitavoitteen kuvaus.  |
    | Välitavoitteen päivämäärä | Päivämäärä, jolloin automaattisen laskun luontiprosessin tulisi etsiä tämän välitavoitteen tila, jotta se voidaan ottaa huomioon laskutuksessa. Tämä arvo sisältyy toimittajan laskuriviin, kun tästä alihankinnasta laskutetaan. |
    | Summa | Asiakkaalta laskutettavan välitavoitteen summa tai arvo. Tämä arvo sisältyy toimittajan laskuriviin, kun tästä alihankinnasta laskutetaan. |
    | Vero | Välitavoitteessa käytetty verosumma. Tämä arvo sisältyy toimittajan laskuriviin, kun tästä alihankinnasta laskutetaan. |
    | Verollinen summa | Tämä vain luku -kenttä lasketaan muodossa summa + vero. Tämä arvo sisältyy toimittajan laskuriviin, kun tästä alihankinnasta laskutetaan. |
    | Laskun tila | Kun välitavoite on luotu, tämä tila määritetään aina arvoon **Ei valmis laskutukseen**.  Kun tila on **Valmis laskutukseen**, toimittajan laskun luonti sisällyttää tämä välitavoitteen toimittajan laskuun. |

5. Valitse **Tallenna ja sulje**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
