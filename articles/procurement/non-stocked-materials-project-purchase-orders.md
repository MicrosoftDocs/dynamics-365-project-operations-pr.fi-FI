---
title: Ei-varastoitujen materiaalien tilaaminen projektille käyttämällä projektien ostotilauksia
description: Tässä aiheessa selitetään, miten voit tilata ei-varastoituja materiaaleja projektille käyttämällä projektien ostotilauksia.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563018"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Ei-varastoitujen materiaalien tilaaminen projektille käyttämällä projektien ostotilauksia

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Organisaatiosi hankintaosasto saattaa käyttää [ostotilauksia](/dynamics365/supply-chain/procurement/purchase-order-overview) tuote- ja palvelutilausten seuraamiseen. Ei-varastoitujen materiaalien ostotilaukset voidaan määrittää projektille. Näiden ostotilausten laskutus kirjaa kulun projektille.

## <a name="prerequisites"></a>edellytykset
Ota projektin ostotilausten toiminto käyttöön seuraavien vaiheiden mukaisesti.

1. Siirry Dynamics 365 Financessa **Tietojen hallinta** -työtilaan.
2. Hae ja valitse ominaisuusluettelosta ominaisuus **Ota projektin ostotilaukset käyttöön Project Operations resurssiin/ei-varastoitaviin perustuvissa skenaarioissa -palvelussa**.
3. Valitse **Ota käyttöön**.
4. Määritä ei-varastoidut materiaalit ja odottavat toimittajan laskut niin kuin on kuvattu kohdassa [Ei-varastoitujen materiaalien ja odottavien toimittajan laskujen määrittäminen](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Projektin ostotilauksen luominen projektin ostotilausluettelosta

1. Siirry Financessa kohtaan **Projektinhallinta ja kirjanpito** > **Projektit** > **Kaikki projektit** ja valitse projekti.
2. Valitse toimintoruudun **Hallinta**-välilehden **Uusi**-ryhmässä **Nimiketehtävä** > **Ostotilaus**.
3. Valitse **Luo ostotilaus** -sivulla toimittaja, jonka kanssa haluat tehdä ostotilauksen, syötä muut tarvittavat tiedot ja valitse **OK**.
4. Valitse **Ostotilaus**-sivulla **Ostotilauksen rivit** -ruudukossa **Lisää rivi**.
5. Syötä nimikkeen numero, määrä, yksikkö, yksikköhinta ja muut tiedot tarpeen mukaan.

    > [!NOTE]
    > Projektin ostotilauksissa voi käyttää vain ei-varastoituja nimikkeitä ja palveluita. Varastoituja nimikkeitä ja hankintaluokkia ei tueta.

6. Jatka kohteiden lisäämista tarpeen mukaan ja vahvista ostotilaus.

    Tuotteiden ja palveluiden kuitit voidaan kirjata luomalla ja kirjaamalla tuotteen kuitti.

    > [!NOTE]
    > Tuotteiden kuitteja ei kirjata projektin toteutuneisiin Microsoft Dataversessa eivätkä ne vaikuta projektin alareskontraan.

    Kun toimittaja lähettää laskun ostotilauksen nimikkeistä ja palveluista, hankintaosasto voi muodostaa ostotilaukselle laskun siirtymällä toimintoruudussa kohtaan **Lasku** > **Muodosta** > **Lasku**. Lisätietoja odottavista toimittajan laskuista löytyy kohdasta [Ei-varastoitujen materiaalien ostaminen käyttämällä odottavaa toimittajan laskua](pending-vendor-invoices.md).
