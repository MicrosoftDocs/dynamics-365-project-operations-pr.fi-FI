---
title: Kesäkuun 2022 Project Operations lite-käyttöönoton uudet ominaisuudet
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Project Operations Lite -käyttöönoton kesäkuussa 2022 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031189"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Kesäkuun 2022 Project Operations lite-käyttöönoton uudet ominaisuudet

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.43.0.77 tai 4.43.0.119

## <a name="quality-updates"></a>Laatupäivitykset

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Alihankinta | 2708885 | Korjattiin virhesanoma, joka annetaan, kun käyttäjä luo varattavissa olevan resurssin varauksen otsikon, johon ei ole täytetty varattavissa olevaa resurssia. |
| Projektin suunnittelu ja seuranta | 2629441 | Korjattiin työkulun käynnistyslogiikkaa siten, että päättymättömän silmukan syntyminen estetään projektitehtäviä päivitettäessä. |
| Aika ja kulut | 2641209 | Määrityksistä tai varauksista tuotavissa aikamerkinnöissä on säilytettävä varattavissa olevan resurssin viite. |
| Projektin suunnittelu ja seuranta | 2651148 | Projektiasiakirjan otsikon on oltava suojattu.|
| Projektin suunnittelu ja seuranta | 2653145 | Lisättiin tarkistuksia varmistamaan, ettei sellaisen projektitietueen luonti ole mahdollista, jonka nimessä on ei-kelvollisia merkkejä. |
| Aika ja kulut | 2654710 | Korjattiin **Hyväksynnät**-sivun suodatus. |
| Laskutus ja hinnoittelu | 2667805 | Lisättiin tarkistuksia estämään laskutetun toteutuneen myynnin luonti, jos taustalla ei ole laskuttamatonta toteutunutta myyntiä. |
| Laskutus ja hinnoittelu | 2668378 | Lisättiin tarkistukset estämään mukautetun hinnoitteludimension lisääminen, jos loogista nimeä ja kentän nimeä ei ole täytetty. |
| Aika ja kulut | 2700428 | Parannettiin hyväksyntälogiikka varmistamaan, että projektin muut hyväksyntäjoukot voivat käsitellä, vaikka yksi hyväksyntäjoukko jumiutuisi järjestelmätöihin. |
