---
title: Alihankittujen komponenttien ajan, kulujen ja materiaalin käytön kirjaaminen
description: Tässä artikkelissa käsitellään sitä, miten Microsoft Dynamics 365 Project Operations seuraa alihankittujen komponenttien ajan, kulujen ja materiaalin käytön kirjaamista projekteissa.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 89fbbfcd1535660e92d0cc80beb91029331e990f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261132"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Alihankittujen komponenttien ajan, kulujen ja materiaalin käytön kirjaaminen projekteissa

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Tässä artikkelissa käsitellään sitä, miten Microsoft Dynamics 365 Project Operations seuraa alihankittujen komponenttien ajan, kulujen ja materiaalin käytön kirjaamista projekteissa.

## <a name="costing-for-subcontractor-time-on-projects"></a>Alihankkijan ajan kustannuslaskenta projekteissa
Project Operationsissa sopimustyöntekijät voivat kirjata aikaa projekteissa samaan tapaan kuin työntekijät. Kun sopimustyöntekijä syöttää aikaa projekteihin ja/tai projektitehtäviin, hän voi valita tietyn alihankinnan ja alihankintarivin.

Kun sopimustyöntekijöiden syöttämä aika on hyväksytty, projektin kustannus kirjataan käyttämällä yksikkökustannushintaa, joka on määritetty kyseiselle sopimustyöntekijäresurssille kyseisen alihankinnan ostohinnaston **Roolin hinnat** -osassa.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Alihankittujen kulujen kustannuslaskenta projekteissa
Kun lisäät kuluja projekteihin, voit valita kulumerkinnälle alihankinnan ja alihankintarivin. 

Kun kulumerkintä on syötetty ja hyväksytty, kulu kirjataan projektiin käyttämällä projektipohjaista yksikköhintaa, joka on määritetty kyseiselle tapahtumaluokalle kyseisen alihankinnan ostohinnaston **Luokan hinnat** -osassa.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Alihankittujen materiaalien kustannuslaskenta projekteissa
Kun syötät materiaalien käyttöä projekteihin, voit valita materiaalin käyttölokille alihankinnan ja alihankintarivin. Kun materiaalin käyttöloki on syötetty ja hyväksytty, materiaalikulu kirjataan projektiin käyttämällä projektipohjaista yksikköhintaa, joka on määritetty kyseiselle tuotteelle alihankinnan ostohinnaston **Hinnaston nimikkeet** -osassa.

Materiaalin käyttö voidaan kirjata projekteissa myös käsin lisätyille tuotteille. Tämäntyyppinen materiaalin käyttö voidaan linkittää myös alihankintaan ja alihankintariviin. Kun kirjaat käsin lisättyjen tuotteiden materiaalikäyttöä, on syötettävä kyseisen käsin lisätyn tuotteen yksikkökustannus. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
