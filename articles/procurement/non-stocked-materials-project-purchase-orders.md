---
title: Ei-varastoitujen materiaalien tilaaminen projektille käyttämällä projektien ostotilauksia
description: Tässä artikkelissa käsillään ei-varastoitujen materiaalien tilaamista projektiin käyttämällä projektien ostotilauksia.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929808"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Hankintaluokkien tai ei-varastoitujen materiaalien tilaaminen projektille käyttämällä projektien ostotilauksia

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Organisaatiosi hankintaosasto saattaa käyttää [ostotilauksia](/dynamics365/supply-chain/procurement/purchase-order-overview) tuote- ja palvelutilausten seuraamiseen. Hankintaluokkien tai ei-varastoitujen materiaalien ostotilaukset voidaan määrittää projektille. Näiden ostotilausten laskutus kirjaa kulun projektille.

## <a name="prerequisites"></a>edellytykset
Ota projektin ostotilausten toiminto käyttöön seuraavien vaiheiden mukaisesti.

1. Avaa Dynamics 365 Financessa **Ominaisuuksien hallinta** -työtila.
2. Hae ja valitse ominaisuusluettelosta ominaisuus **Ota projektin ostotilaukset käyttöön Project Operations resurssiin/ei-varastoitaviin perustuvissa skenaarioissa -palvelussa**.
3. Valitse **Ota käyttöön**.
4. Määritä ei-varastoidut materiaalit ja odottavat toimittajan laskut niin kuin on kuvattu kohdassa [Ei-varastoitujen materiaalien ja odottavien toimittajan laskujen määrittäminen](configure-materials-nonstocked.md).
5. Määritä hankintaluokkia, kuten on kuvattu ohjeaiheessa [Hankintaluokkien käyttö projektin ostotilauksissa ja odottavissa toimittajan laskuissa](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Projektin ostotilauksen luominen projektin ostotilausluettelosta

1. Siirry Financessa kohtaan **Projektinhallinta ja kirjanpito** > **Projektit** > **Kaikki projektit** ja valitse projekti.
2. Valitse toimintoruudun **Hallinta**-välilehden **Uusi**-ryhmässä **Nimiketehtävä** > **Ostotilaus**.
3. Valitse **Luo ostotilaus** -sivulla toimittaja, jonka kanssa haluat tehdä ostotilauksen, syötä muut tarvittavat tiedot ja valitse **OK**.
4. Valitse **Ostotilaus**-sivulla **Ostotilauksen rivit** -ruudukossa **Lisää rivi**.
5. Syötä nimikkeen numero tai hankintaluokka, määrä, yksikkö, yksikköhinta ja muut tiedot tarpeen mukaan.

    > [!NOTE]
    > Projektin ostotilauksissa voi käyttää vain hankintaluokkia, ei-varastoituja nimikkeitä ja palveluita. Varastoituja nimikkeitä ei tueta.

6. Jatka nimikkeiden tai hankintaluokkien lisäämistä tarpeen mukaan ja vahvista ostotilaus.

    Tuotteiden ja palveluiden kuitit voidaan kirjata luomalla ja kirjaamalla tuotteen kuitti.

    > [!NOTE]
    > Tuotteiden kuitteja ei kirjata projektin toteutuneisiin Microsoft Dataversessa eivätkä ne vaikuta projektin alareskontraan.

    Kun toimittaja lähettää laskun ostotilauksen nimikkeistä ja palveluista, hankintaosasto voi muodostaa ostotilaukselle laskun siirtymällä toimintoruudussa kohtaan **Lasku** > **Muodosta** > **Lasku**. Lisätietoja odottavista toimittajan laskuista löytyy kohdasta [Ei-varastoitujen materiaalien ostaminen käyttämällä odottavaa toimittajan laskua](pending-vendor-invoices.md).
