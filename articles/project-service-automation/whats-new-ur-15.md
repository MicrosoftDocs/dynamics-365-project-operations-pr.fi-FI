---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 15, V3
description: Tässä aiheessa on tietoja Project Service Automation -päivitysversion 15, V3:n uusista ominaisuuksista.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751172"
---
# <a name="project-service-automation-v3-update-release-15"></a>Project Service Automation V3, päivitysjulkaisu 15

Olemme iloisia voidessamme julkistaa uusimman Dynamics 365 Project Service Automation (PSA) -sovelluksen päivityksen. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, käy Dynamics 365 online -hallintakeskuksessa ja asenna päivitys siirtymällä Ratkaisut-sivulle. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita PSA V3 -päivitysjulkaisussa 15. Tällä versiolla on koontinumero V3.10.5.28 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä tammikuusta 2020 lähtien.

## <a name="update-release-15"></a>Päivitysjulkaisu 15 

### <a name="enhancements"></a>Parannukset

- Projektinhallinta

### <a name="bug-fixes"></a>Ohjelmistovirheiden korjaukset

- Aika ja kulu

  - Korjattu: Lisää latausvirheen käsittely täsmäytysnäkymään.
  - Korjattu: Projektiresurssikeskus: Nimeä **Summa** uudelleen epäselvyyden vähentämiseksi.
  - Korjattu: Säädä **Kopioi aikamerkinnän sarakkeet** -näkymä sisältämään tyypin.
  - Korjattu: aikamerkinnän keston muokkaaminen ruudukkonäkymässä desimaalinumeroita käyttäen aiheuttaa joillekin numeroille tuntemattoman virheen.

- Projektinhallinta

  - Korjattu: **Käytä seurantanäkymässä** -kohteen avattavaa valikkoa laajennetaan nyt vaihtoehtojen leveyden mukaan.
  - Korjattu: kun projekteja hallitaan yli 13 aikavyöhykkeellä, tehtävien laskennassa voi näkyä virheellisiä tuloksia.
  - Korjattu: **Ryhmän jäsenen päättymisaika** on korjattu käytettäessä 24 tunnin kalenteria.
  - Korjattu: **BPF** on aktivoitu uudelleen **msdyn_project**-päälomakkeessa.
  - Korjattu: varausten laskennassa ei enää ohiteta yhtä päivää.
  - Korjattu: projektilomakkeeseen on lisätty uusi ilmoituspalkki, kun aikavyöhyke eroaa käyttäjän ja projektin välillä.

- Sales

  - Korjattu: kuluarvioluokan valintaa voidaan käyttää kaksoiskappaleiden suodattamiseen.
  - Korjattu: Koodi kohdassa **PluginDomain.ExecuteInTryCatchBlock(..)** ei enää piilota poikkeuksen alkuperää.
  - Korjattu: Ei enää virheviestiä **Projektin valinta** -kohdassa **Tarjousrivi**-lomakkeessa, kun projekteja on yli 1 000.
  - Korjattu: **Arviot**-ruudukko työmääräarvioille ja kuluarvioille näyttää nyt oikean valuuttasymbolin.
  - Korjattu: kun organisaatio on päivittänyt PSA:n päivitysversiosta 14 päivitysversioon 15, **Aikataulu** -välilehti ei enää näy tyhjänä **Projekti**-lomakkeessa.
