---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 14, V3
description: Tässä artikkelissa on tietoja Project Service Automationin V3:n päivitysversion 14 uusista ominaisuuksista.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: e8e5132f970e3ec5742842175c118faf98a7b079
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926542"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation -päivitysjulkaisu 14, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Olemme iloisia voidessamme julkistaa uusimman Dynamics 365 Project Service Automation (PSA) -sovelluksen päivityksen. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, käy Dynamics 365 online -hallintakeskuksessa ja asenna päivitys siirtymällä Ratkaisut-sivulle. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita PSA V3:n päivitysjulkaisussa 14. Tällä versiolla on koontinumero V3.10.4.21 ja se on saatavilla seuraavan aikataulun mukaan:

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
