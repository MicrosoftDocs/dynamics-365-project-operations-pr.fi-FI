---
title: Kulujen hallinnan työnkulkujen määrittäminen
description: Voit määrittää työnkulkuprosessin, jota käytetään matka- ja kuluasiakirjojen tarkistukseen ja hyväksyntään.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896547"
---
# <a name="set-up-workflows-for-expense-management"></a>Kulujen hallinnan työnkulkujen määrittäminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Voit määrittää matka- ja kuluasiakirjojen tarkistuksen ja hyväksynnän työnkulkuprosessin. Voit määrittää kuluraporttien, matkustusehdotusten ja käteisennakkopyyntöjen työnkulut.

Työn kulku edustaa liiketoimintaprosessia ja määrittää, miten asiakirja siirtyy järjestelmässä. Työnkulku tarkoittaa myös sitä, kenen on suoritettava tehtävä tai hyväksyttävä asiakirja. Työnkulkujärjestelmän käyttäminen tuo seuraavat hyödyt organisaatiolle:

- **Yhtenäiset prosessit**: Voit määrittää kuluraportin tietyille asiakirjoille, kuten ostoehdotuksille ja kuluraporteille. Työnkulkujärjestelmän avulla varmistat, että asiakirjat käsitellään ja hyväksytään yhdenmukaisesti ja tehokkaasti.
- **Prosessin näkyvyys**: Voit seurata tietyn työnkulun esiintymän tila-, historia- ja suorituskykymittareita. Tämän avulla voit määrittää, onko työnkulkuun tehtävä muutoksia tehokkuuden parantamiseksi.
- **Keskitetty työluettelo**: Käyttäjät voivat tarkastella keskitettyä työluetteloa ja tarkastella heille määritettyjä työnkulun tehtäviä ja hyväksyntöjä. 

## <a name="workflow-types"></a>Työnkulkutyypit

Seuraavassa taulukossa on esitetty työnkulkutyypit, jotka **kulun hallinnan** avulla voi luoda.


|              <strong>Tyyppi</strong>              |                   <strong>Tämän tyypin avulla voit</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Kuluraportin automaattinen hyväksyntä</strong> |            Luo kuluraporttien hyväksyntätyönkulkuja.             |
|  <strong>Kuluraportin automaattinen kirjaaminen</strong>   |        Luo työnkulkujen automaattinen kirjaaminen kuluraportteihin.        |
|       <strong>Kulurivin nimike</strong>        |     Luo kuluraporttien rivinimikkeiden hyväksyntätyönkulkuja.      |
| <strong>Kulun rivinimikkeen automaattinen kirjaaminen</strong> | Luo kuluraporttien rivinimikkeiden työnkulkujen automaattinen kirjaaminen. |
|       <strong>Matkustusehdotus</strong>       |          Luo matkaehdotusten hyväksyntätyönkulkuja.           |
|      <strong>Käteisennakkopyyntö</strong>      |         Luo hyväksyntätyönkulut käteisennakkopyynnöille.          |
|        <strong>ALV:n palautus</strong>        | Voit luoda hyväksyntätyönkulkuja arvonlisäveron palautusta varten.  |
