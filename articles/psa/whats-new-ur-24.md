---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 24, V3
description: Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista Project Service Automationin päivitysjulkaisussa 24, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
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
ms.reviewer: johnmichalak
ms.openlocfilehash: d2cd8c18a2ea10ae090d8258d835453b279d717f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926404"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation -päivitysjulkaisu 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3:n päivitysjulkaisussa 24. Tällä versiolla on koontinumero V3.10.42.43 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä lokakuusta 2020 lähtien.

## <a name="update-release-24"></a>Päivitysjulkaisu 24

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

**Sales**

Seuraavat ongelmat on korjattu:

- Ongelma määritettäessä oletushinnastoa tuotteille.
- Tarjouksen voiton suorituskyky on hidas, koska upotettu hinnasto ja roolien hintatietueet kopioidaan.
- **Projektisopimus/myyntikeskus** > **Tuoterivinimike/Tilausrivimäärä** pyöristetään automaattisesti lähimpään kokonaislukuun.
- Korota järjestelmäoikeuksiin, kun luetaan hinnastoja.
- Kopioi asiakkaan osoitekentät **address1_freighttermscode** ja **address1_shippingmethodcode** tarjoukseen/tilaukseen. 


**Aika ja kulu**

Seuraavat ongelmat on korjattu:

- **Aikamerkintä-ruudukko** ei tue **Vain päivämäärä** -aikatoiminnallisuutta.
- **Aikamerkintä** ei päivity automaattisesti. Manuaalinen päivitys vaaditaan.
- Aikatietoja ei voi tuoda tehtävästä silloin, kun resurssin tehtävissä on tauko (0 tuntia).
- Kun luodaan aikamerkintää, määritä aloitukseksi sama kuin **msdyn_date**.
- Ota aikamerkinnän joukkomuokkaus uudelleen käyttöön.

**Resurssienhallinta**

Seuraavat ongelmat on korjattu:

- Jos yritetään päivittää päivän sisäisen varauksen tilaa ilman tarvetta, toiminto heittää null-ref -poikkeuksen.
- Virhe **täsmäytysnäkymän** lataamisessa.


**Projektinhallinta**

Seuraavat ongelmat on korjattu:

- Kun siirrytään **projektiaikataulussa** **manuaalisesta** **automaattiseen**, automaattinen tallennus ei valmistu.
- Kulukustannuksia ei pitäisi laskea **Projektin seuranta -ruudukon** varianssia kohti.
- **Arvioiden tunniste** -sarakkeiden epäjohdonmukainen toiminta latauksen aikana verrattuna **aikavaihe**-tyypin vaihtamiseen.
- Projektin todelliset kustannukset eivät ehkä vastaa **toteutuneiden arvojen** summaa.
- **Yhteenveto**-välilehden **Arvioitu päättymispäivä** ei vastaa **Työrakenne-aikataulua**.
- **Päivitä todelliset tunnit** ei toimi oikein, kun ulonnetaan.
- Projektipäällikkö, joka ei ole **pääliiketoimintayksikössä**, ei voi luoda projektia.
- **Kuluarvioiden** tehtävän tai luokan muutokset eivät säily.
- **Sopimuksen kopio** kopioi laskutusaikataulut ja suoritustilan.
- **Päivitä toteutuneet** -painike laskee yhteenvetotehtävät virheellisesti.
- Microsoft Project -apuohjelma: Korjaa null-viittausvirhe, jos jollain ryhmän jäsenellä on tyhjä resursointiyksikkö.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
