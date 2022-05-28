---
title: Sisäisten projektien kirjanpidon määrittäminen
description: Tässä ohjeaiheessa on tietoja siitä, miten projektitoimintojen sisäisten projektien kirjanpitokäytäntöjä määritetään.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9da72d8dbf720e380a49a1010caca472ee024783
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597840"
---
# <a name="configure-accounting-for-internal-projects"></a>Sisäisten projektien kirjanpidon määrittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Sisäiset projektit mahdollistavat sen, että yritykset voivat seurata aktiviteetteihin liittyviä kustannuksia, joita ei laskuteta asiakkaalta. Sisäisiä projekteja ovat esimerkiksi seuraavat:

- Tuotteen, kuten mobiilisovelluksen, kehittäminen ja kehitykseen liittyvien kustannusten seuraaminen.
- Ennakkomyyntiajan ja -kulujen hallinta. Tämä ennakkomyynnin sisäinen projekti voidaan muuntaa myöhemmin laskutettavaksi projektiksi, jos tarjous on voitettu.

Projekteja, jotka eivät liity sopimukseen Dynamics 365 Project Operationsissa, käsitellään sisäisinä. Projektin kustannus- ja tuottoprofiileita ei käytetä määrittämään projektin kirjanpitosääntöjä. Sisäiset projektikustannukset kirjataan aina käyttämällä voiton ja tappion periaatteita. Tapahtumarekisterin kirjanpitotilit määritetään **Tapahtumarekisterin kirjauksen asetukset** -sivulla.

- Aikatapahtumat kirjataan veloittamalla **Kustannus**-tiliä ja hyvittämällä **Palkanlaskennan kohdistus** -tiliä.
- Kulutapahtumat kirjataan veloittamalla **Kustannus**-tiliä ja hyvittämällä **Kulujen vastatili** -tiliä.
- Nimiketapahtumat kirjataan veloittamalla **Kustannus** -tiliä ja hyvittämällä **Kustannus - nimike** -tilille.

Kun tapahtumat on kirjattu projektiin ja projekti on liitetty projektisopimukseen, järjestelmä peruuttaa kaikki kertyneet tapahtumat ja luo uudet laskutettavat tapahtumat. Laskutettavat tapahtumat noudattavat kunkin projektin kustannus- ja tuottoprofiilissa määritettyjä kirjanpitosääntöjä.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
