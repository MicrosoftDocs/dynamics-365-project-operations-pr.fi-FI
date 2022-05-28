---
title: Maaliskuun 2022 Project Operations Lite -käyttöönoton uudet ominaisuudet
description: Tässä aiheessa on tietoja Project Operationsin Lite-käyttöönoton maaliskuussa 2022 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583746"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Maaliskuun 2022 Project Operations Lite -käyttöönoton uudet ominaisuudet

_Käytetään: Lite-käyttöönotto – kauppa proformalaskutukseen_

Tämä aihe koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.30.0.99

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

- Alihankinta: Toimittajan laskujen luonti ja täsmäytyskokemukset

## <a name="quality-updates"></a>Laatupäivitykset

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Aika ja kulut | 2388011 | Näytä hylkäyskommentit aikamerkinnän lähettäjille joukkohyväksynnän aikana. |
| Projektin suunnittelu ja seuranta | 2495294 | Projektin tietoja ei voi muokata **Tehtävän tiedot** -sivulla. |
| Laskutus ja hinnoittelu | 2499605 | Tarjouksen välitavoitteista luodut palvelusopimuksen välitavoitteet on merkitty virheellisesti vain luku -tilaan. |
| Projektin suunnittelu ja seuranta | 2506050 | Toimintojoukko pysyy odottavana tunnin, jos tallennettavia muutoksia ei ole. Tämän jälkeen joukko merkitään virheellisesti **Epäonnistunut**-merkinnäksi, mutta se pitäisi suorittaa heti. |
| Laskutus ja hinnoittelu | 2507401 | Oletussopimusyksiköt on syötetty väärin projekteihin virheellisen välimuistin vuoksi. |
| Laskutus ja hinnoittelu | 2541660 | **Myyntitilauksen luonnin vahvistus** kaksoiskirjoituksessa tulisi olla vain projektipohjaisia tilauksia varten. |
| Laskutus ja hinnoittelu | 2552745 | Veroa ei jaeta asiakkaiden kesken, jotka ovat määrittäneet jaetut laskutussäännöt. |
| Laskutus ja hinnoittelu | 2558859 | Parannetut virhesanomat, kun hinnoitteludimensiot on määritetty. |
| Laskutus ja hinnoittelu | 2558933 | **Tuonti projektiarvioista** epäonnistuu, kun **msdyn\_project** lisätään hinnoitteludimensioksi. |
| Laskutus ja hinnoittelu | 2559101 | Projektiparametrien poisto ei ole estetty, ja se aiheuttaa ongelmia. |
|   Mahdollisuuksien hallinta | 2570390 | Kaksoiskirjoituslaajennuksen pakottaa tilityypiksi tarjouksissa, tilauksissa ja mahdollisuuksissa **Asiakas**, vaikka tilityyppi ei olisikaan oikea. |
| Laskutus ja hinnoittelu | 2586097 | Jaettuja laskutettuja kustannuksia ei peruuteta, kun projekti poistetaan projektisopimusriviltä. |
| Laskutus ja hinnoittelu | 2589619 | Lisättyjen materiaalien vero välitetään laskuttamattoman myynnin toteutuneiksi ja laskuun. |
|   Mahdollisuuksien hallinta | 2594015 | Tarjousta ei voi sulkea voitettuna asiakkaille, joilla on **Net60**-maksuehdot. |
| Projektin suunnittelu ja seuranta | 2595841 | Project for the Webissä käyttäjät saavat virhesanoman puuttuvasta kohteesta **msdyn\_actualstart** kun he luovat uuden resurssipyynnön. |
| Aika ja kulu | 2602511 | Aikamerkintöjen **Hylännyt**-kentässä näkyy **Järjestelmä** eikä nimetty käyttäjä hylkääjänä. |
| Aika ja kulu | 2602528 | Projektin hyväksyjä voi hyväksyä niiden projektien ajan, joihin häntä ei ole merkitty hyväksyjäksi. |
| Laskutus ja hinnoittelu | 2608550 | Korjauslaskun voi vahvistaa, vaikka alkuperäiseen versioon ei olisi tehty muutoksia. |

## <a name="removed-and-deprecated-features"></a>Poistetut ja vanhentuneet ominaisuudet

[Project Operationsin poistetut tai vanhentuneet ominaisuudet](../../whats-new/removed-depreciated-features-project.md) -aiheessa on kuvattu ominaisuuksia, jotka on poistettu tai vanhentuneet Dynamics 365 Project Operationsissa.

- Poistettu toiminto ei ole enää käytettävissä tuotteessa.
- Vanhentunutta ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Vanhentumisilmoitus näkyy [Project Operationsin poistetut tai vanhentuneet toiminnot](../../whats-new/removed-depreciated-features-project.md) -ohjeaiheessa 12 kuukautta ennen ominaisuuden poistoa tuotteesta.
