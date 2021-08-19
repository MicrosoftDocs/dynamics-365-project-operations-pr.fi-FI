---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 26, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 26, V3.
author: ruhercul
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
ms.openlocfilehash: fa526e97a366c01dae2547d79d0eda2fb204e07d0f6383b991165b9eecd836e9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004262"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation -päivitysjulkaisu 26, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automationin Päivitysjulkaisussa 26, V3. Tämän version koontiversionumero on V3.10.44.59 ja se on yleisesti saatavilla omatoimipäivityksenä joulukuussa 2020.

## <a name="update-release-26"></a>Päivitysjulkaisu 26

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

**Aika ja kulu**

Seuraavat ongelmat on korjattu:

- Käyttäjät voivat muuttaa tehtävää hyväksytyssä/lähetetyssä aikamerkinnässä.
- "Objektin viittausta ei ole määritetty" -virhe tallennettaessa aikamerkintää.
- Aikamerkinnän tuonti resurssivarauksista luo aikamerkintöjä, joilla on väärät DateTime-arvot.
- Kun Project Service Automation ja Field Service -sovellukset on molemmat asennettu, **Uusi**-painike näkyy kahdesti komentopalkissa Field Service -sovelluksen aikamerkinnöille.
- **Salli yksikkö** ja **Yksikköryhmä** -solujen päivityksen toimivat nyt **Kuluarvio**-ruudukossa.
- **Päivitä aikamerkinnän muokkaus** -lomake sisältää **Aikajanan**.
- Ajan hyväksyminen projektiin liittymättömille aikamerkinnöille tukkii järjestelmän, kun projektin hyväksyjän roolia etsitään.

**Resurssienhallinta**

Seuraavat ongelmat on korjattu:

- Lisätty oikeellisuustarkistus **PostProjectCreate**-laajennukseen tarkistamaan ensisijainen vaatimus ennen sellaisen luomista.
- **Projektiryhmän jäsenen** pikaluontilomake luo tyhjäarvoisen viittauksen poikkeuksen, jos kentät poistetaan lomakkeesta.
- Vaatimusten luonti 12 tuntua yli 1 vuoden epäonnistuu.
- Parannettu virhesanoma tyhjäarvoisen viittauksen poikkeukselle resurssitarpeen luonnin aikana.

**Projektinhallinta**

Seuraavat ongelmat on korjattu:

- Parannettu oikeellisuustarkistus korjaamaan tyhjäarvoisen viittauksen poikkeuksen **PreProjectUpdate**-laajennuksessa.
- Microsoft Project Desktop -laajennuksen julkaisemat projektit poistavat delegoimattomat varaukset.
- Lisätty uusi oikeellisuustarkistus, kun tehtävän projektiviittaus on virheellinen tyhjäarvoisen viittauksen poikkeuksesta johtuen **PreValidateProjectTaskUpdate**-laajennuksessa.
- Ryhmän jäsen -ruudukko ei näytä erillisiä varauksia ryhmän jäsen -tietueessa.
- Lisätty uusia tarkistus- ja virhesanomia, jotka johtuvat tyhjäarvoisen viittauksen poikkeuksesta **PreProjectTaskDelete**-laajennuksessa.

**Sales**

Seuraavat ongelmat on korjattu:

- Kun projektiin perustuva rivi valitaan tarjouksessa tai sopimuksessa, **Ehdotus**-painikkeen tulisi olla näkyvissä ainoastaan silloin, kun valitaan tuotteeseen perustuva rivi, joka liittyy olemassa olevaan tuotteeseen.
- Erota **Create_Product** -oikeus **Create_ProjectContract**-oikeudesta.
- Laskun rivin poistaminen aiheuttaa tyhdäarvoisen viittauksen epäonnistumisen kohteessa **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]