---
title: Sisäisten projektien kirjanpidon määrittäminen
description: Tässä artikkelissa on tietoja siitä, miten Project Operationsin sisäisten projektien kirjanpitokäytäntöjä määritetään.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7fc2b7247da699a194688b18aa0a695b06cc44c6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919458"
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
