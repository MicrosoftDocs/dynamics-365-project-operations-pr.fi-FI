---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 14, V3
description: Tässä aiheessa on tietoja Project Service Automation -päivitysversion 14, V3:n uusista ominaisuuksista.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751173"
---
# <a name="project-service-automation-v3-update-release-14"></a>Project Service Automation V3, päivitysjulkaisu 14
Olemme iloisia voidessamme julkistaa uusimman Dynamics 365 Project Service Automation (PSA) -sovelluksen päivityksen. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, käy Dynamics 365 online -hallintakeskuksessa ja asenna päivitys siirtymällä Ratkaisut-sivulle. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita PSA V3 -päivitysjulkaisussa 14. Tällä versiolla on koontinumero V3.10.4.21 ja se on saatavilla seuraavan aikataulun mukaan:

- **Yleinen saatavuus (itsepäivitys):** tammikuu 2020
- **Automaattinen päivitys:** 2020 helmikuu

## <a name="update-release-14"></a>Päivitysjulkaisu 14

### <a name="enhancements"></a>Parannukset

- Sales

     - Mukautettujen kenttien arvot kopioidaan **Tarjousrivin tiedot** -kohdasta **Projektisopimusrivin tiedot** -kohtaan, kun tarjouksen tilaksi päivitetään **Suljettu voitettuna**.
     - Vahvistetut projektit voidaan muuttaa tilaan **Suljettu hävittynä**.

- Resurssienhallinta

     - Kun varauksia laajennetaan, käyttäjille näytetään vahvistusvalintaikkuna, jossa on varauksen tulosten yhteenveto ja linkki varausten ylläpitämiseen.


### <a name="bug-fixes"></a>Ohjelmistovirheiden korjaukset

- Aika ja kulu

     - Korjattu: käyttäjien kokemusta parannettu, kun käyttäjä ei ole valinnut korjattavia merkintöjä.

- Resurssienhallinta

     - Korjattu: Resurssin varaus useaan kertaan ylittää varattavissa olevan resurssin nimen.

- Sales

     - Korjattu: kokonaismyyntihintaa ei lasketa, ennen kuin käyttäjä syöttää myös kustannushinnan projektin kuluarvioihin.
     - Korjattu: Tarjouksen sulkeminen tilassa **Voitettu** epäonnistuu, jos liittyvä projektisopimus ei ole tilassa **Luonnos**.

