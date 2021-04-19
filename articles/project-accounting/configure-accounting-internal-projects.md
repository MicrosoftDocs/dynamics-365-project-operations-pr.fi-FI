---
title: Sisäisten projektien kirjanpidon määrittäminen
description: Tässä ohjeaiheessa on tietoja siitä, miten projektitoimintojen sisäisten projektien kirjanpitokäytäntöjä määritetään.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857974"
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
