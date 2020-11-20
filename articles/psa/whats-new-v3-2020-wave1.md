---
title: Uutuudet ja muutokset Project Service Automation -versiossa 3.x vuoden 2020 1. julkaisuaallossa
description: Tässä aiheessa on tietoja Project Service Automation -version 3 uusista ja muuttuneista ominaisuuksista vuoden 2020 1. julkaisuaallossa.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2308f83e09c25059b6a36599b04b5b00f66c704f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126479"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Uutuudet ja muutokset Project Service Automation -versiossa 3 vuoden 2020 1. julkaisuaallossa
Aihe korostaa tärkeitä päivitysnäkökohtia, kun siirrytään uusimpaan Project Service Automation (PSA) -versioon 3.x vuoden 2020 1. julkaisuaallossa.

## <a name="time-entry"></a>Aikamerkintä
Ajan syöttökokemusta on laajennettu siten, että se antaa mahdollisuuden pidentää aikamerkintöjä asiakasskenaarioille. Tähän sisältyy mahdollisuus lisätä merkintätyyppejä, jotka nyt toimivat eri tavoilla perustuen **Aikamerkinnän asetukset** -malliin, joka näytetään **ajan lähteenä**. Tähän toimintoon on lisätty uusi ratkaisu, jonka nimi on aika, kulut, tilat ja hyväksynnät (TESA).

### <a name="upgrade-consideration"></a>Päivityksessä huomioon otettavia seikkoja
Tämän toiminnon tueksi PSA-järjestelmän roolit on päivitetty siten, että ne sisältävät uusia oikeuksia. Nämä oikeudet myöntävät lukuoikeuden uuteen entiteettiin nimeltä **Aikamerkinnän asetukset**.

Käyttäjille, jotka tarvitsevat mahdollisuuden kirjata aikoja, on annettava käyttäjärooli **Aikamerkinnän käyttäjä** aiemmin annettujen roolien lisäksi. Tämä rooli sisältää uudet toiminnot ja varmistaa, että ajan syöttö toimii edelleen.

Jos sinulla on myös mukautettuja sovellusmoduuleja, jotka sisältävät kaikki aikamerkintäkohteen lomakkeet, sinun on poistettava **TESA-aikamerkinnän pikaluontilomake** moduulista.

### <a name="currently-extended-time-entry-changes"></a>Tällä hetkellä pidennetyt aikamerkinnän muutokset
Jotta aikamerkinnän nykyiseen käyttöön vaikutettaisiin mahdollisimman vähän, tämä roolien muutos on ainoa perusvaatimus, jota tarvitaan, jotta aikamerkintöjä voidaan jatkaa. Jos olet luonut mukautettuja näkymiä tai erillisiä ajansyöttökokemuksia, määritä **Aikamerkinnän asetukset** -kentille oikeat PSA-arvot.
