---
title: Päivärahat
description: Tässä artikkelissa on tietoja kulujen hallinnassa käytettävistä päivärahasäännöistä.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 8fa634c23391c47c0c583647165dce2b396535e5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930176"
---
# <a name="per-diems"></a>Päivärahat

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_


Päiväraha on palkka, joka maksetaan työhön matkustavalle työntekijälle. Kulujen hallinnassa voit luoda päivärahasääntöjä eri matkatilanteisiin. Päivärahahinnat voivat perustua vuodenaikaan, matkustuspaikkaan tai molempiin. Kun luot päivärahasäännön, voit määrittää, että prosenttiosuus päivärahahinnasta pidätetään, jos työntekijä saa ilmaisia aterioita tai palveluita. Voit myös määrittää tuntien vähimmäis- ja enimmäismäärät, joiden puitteissa päiväraha koskee työntekijän matkustamista.

## <a name="configuration"></a>Määritys 

1. Voit lisätä päivärahasijainteja valitsemalla **Määritä** > **Laskutoimitukset ja koodit** > **Päivärahasijainnit**.
2. Valitse kunkin yllä lisätyn sijainnin kohdalla päivärahahinta ja valuutta, joka on voimassa hotellin, aterioiden ja muiden kulujen alkamis- ja päättymispäivän välillä. Päivärahahinnat ja valuutat määritetään kohdassa **Määritä** > **Laskutoimitukset ja koodit** > **Päivärahat**.
3. **Päivärahasijainnit**-sivulla määritetään päivärahahintojen tasot. Päivärahahintojen tasojen avulla voit määrittää, kuinka monta prosenttia päivittäisestä korvauksesta jaetaan hotelli-, ateria- ja muiden kulujen mukaan. 
4. Voit määrittää aamiaisen, lounaan tai päivällisen aterianvähennysprosentin päivittämällä kentät **Kulujen hallinnan parametrit** -sivun **Päiväraha**-välilehdessä. 
    
## <a name="submit-expenses-using-per-diem"></a>Kulujen lähettäminen päivärahan avulla
Jos haluat lähettää kuluja käyttäen päivärahoja, käytä **Päiväraha**-kululuokkaa, kun luot kuluraporttia. Anna **Päivärahan alkupäivämäärä**-, **Päivärahan loppupäivämäärä** ja **Päivärahan sijainti**. Summa lasketaan valitun sijainnin päivärahahintojen perusteella, ja ateriavähennys lasketaan päivärahatasojen perusteella.


[!INCLUDE[footer-include](../includes/footer-banner.md)]