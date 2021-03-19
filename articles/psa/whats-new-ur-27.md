---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 27, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 27, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 8879229b50ef113d6d6cb8622b707f0c12182a57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280304"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 27, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 27. Tällä versiolla on koontinumero V3.10.45.98 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä tammikuusta 2021 lähtien.

## <a name="update-release-27"></a>Päivitysjulkaisu 27

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

**Yleiset**

Seuraavat ongelmat on korjattu:

- Project Service Automationin laajennusten luomia lokeja ei ole määritetty automaattisesti poistettaviksi.
- Automaattinen päivitys epäonnistui, koska Project Service Automation -ratkaisu sisältää vanhan NavBarArea-tyhjäarvon ja otsikkoelementin.

**Aika ja kulu**

Seuraavat ongelmat on korjattu:

- **Aikamerkinnän** ruudukossa näkyy virheellisiä tietoja **Aikavyöhykkeestä riippumaton** -päivämäärän toimintatavalle.
- **Aikamerkinnän** ruudukko luo virheellisen ajan **Aikavyöhykkeestä riippumaton** -päivämäärän toimintatavalle.
- Tehtävän valinta ei rajoitu vain valittuun projektiin **Aikamerkinnän muokkaus** -sivulla.
- Ajan hyväksyminen projektiin liittymättömille aikamerkinnöille on estetty, koska järjestelmä etsii projektin hyväksyjää.
- Toteutuneiden tietojen oikeat merkinnät tuovat näkyviin väärän virhesanoman.
- Kun tehtävä sisältää tyhjäarvon toteutuneita kustannuksia varten ja projektin kokonaissummat päivitetään, tapahtuu seuraava virhe: "Annettu avain ei ole hakemistossa".
- Tietyissä esiintymissä **Projektiarvio**-välilehden **Ryhmittele**-suodattimissa ei näy kuluarvioita.
- **Kesäaika**-jakson esiintymisväli ei ole oikea aikamerkintöjä varten.

**Projektinhallinta**

Seuraavat ongelmat on korjattu:

- Välimuistiin tehdyt parannukset, jotka parantavat **Projekti**-sivun lataamiseen liittyvää suorituskykyä.
- Vanhentunut liiketoimintasääntö, joka estää projektitehtävien valmistumisen.
- Microsoft Project -apuohjelman jaksottuminen ei ole apuohjelman kalenterin mukainen, mikä johtaa virheellisiin resurssivaatimuksiin.
- Projektien luominen malleista määrittää virheellisesti määrityspäivämäärät ja estää resurssitarpeiden luomisen.
- Käyttäjä ei voi käyttää **Luokka**-, **Kuvaus**- tai **Tila**-asetuksia näppäimistön avulla.
- Projektin todelliset myyntiarvot eivät lisää maksu- ja materiaalimyyntiarvoja.
- Toteutuneiden myyntien ja toteutuneiden kustannusten koostaminen toimii virheellisesti, kun käytössä on eri valuuttakurssit.
- **Työtuntien oletusmallin** kuvaus on harhaanjohtava.
- Tehtävän sisentäminen ei poista **luokkaa** käyttöliittymästä, ennen kuin se on päivitetty.
- Puuttuva tarkistus sen varmistamiseksi, että projektin siirtäminen päättymispäivää pitemmälle ei ole sallittu.

**Sales**

Seuraavat ongelmat on korjattu:

- Projektitarjousrivillä luodaan tyhjäarvolla viittauspoikkeus, koska **Tuo projektin arviosta** ei ole näkyvissä, kun projektia ei ole valittu.
- Seuraava virhe: "Objektin viitettä ei ole määritetty objektin esiintymään" tapahtuu, kun tarjous suljetaan **voitettuna**.
- Muokkauksen tilaa ei ole määritetty todellisen peruutuksen aikana, kun projektin linkitys sopimusriviin puretaan.
- Kun Dynamics 365 Field Service ja Project Service Automation on asennettu **Lukitse hinta** ja **Käytä nykyistä hinnoittelua** -vaihtoehtoja ei näy samanaikaisesti **Lasku**-sivulla.
- Japaninkielisessä käännöksessä on ristiriita muiden kalenteripohjaisten sivujen kanssa.
- **Aktivoi** ja **Poista aktivointi** on poistettu **Hinnaston liitos** -entiteeteistä Project Service Automationissa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]