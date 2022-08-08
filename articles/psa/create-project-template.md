---
title: Luo projektimalli
description: Projektimallin luominen (Project Service)
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 07/19/2022
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
ms.openlocfilehash: 8159e0390441e5029f9beb0228cffcbc4d683479
ms.sourcegitcommit: 278740b352f1ed9618ee5c79597c8f449984d6f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177421"
---
# <a name="create-a-project-template-project-service"></a>Luo projektimalli (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projektimallit säästävät aikaa, jos yritys tekee säännöllisesti samankaltaisia hankkeita. Ne tarjoavat standardit roolit ja arvioidut tunnit projektityypille. Asiakaspäälliköt ja projektipäälliköt voivat luoda projektimallin mukaisia projekteja tai he voivat kopioida mallin ja tehdä omia.  
  
## <a name="components-of-project-template"></a>Projektimallin osat
 Projektimalli koostuu kolmesta osasta:  
  
- **Työrakenne**:Projektimallin työrakenteessa on samoja elementtejä kuin projektissa. Voit luoda tehtävähierarkian, liittää roolit tehtäville, määrittää aikataulu-ominaisuuksia, luoda riippuvuuksia ja tarkastella kaikkia tietoja Gantt-kaaviossa. Projektimallien työrakenteet tukevat myös tehtävätiloja kullekin tehtävälle. Projektimallilla ja projektilla ei ole eroa luotaessa työaikataulua.  
  
- **Projektiarviot**: Projektiarviot toimivat projektimallissa samoin kuin projekteissa, paitsi että oletusarvoiset kustannus- ja myyntihinnat sisältävät hinnastot ovat aina [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -parametreissa määritetyt oletuskustannus- ja myyntihinnastot. Loput toiminnallisuudet ovat samoja, kuin projektissa.  
  
- **Projektiryhmän muodostuminen**: kun muodostat projektiryhmää projektimallille et voi varata nimettyä resurssia mallissa. Voit käyttää **Luo projektiryhmä** -valintaa työrakenteessa yleisten resurssijoukkojen luomiseksi. Voit myös määrittää tarvittavat taidot ja ammattitaidot yleisiä resursseja varten. Ei voi korvata yleistä resurssia varattavalla resurssilla projektimalleissa.  

## <a name="create-a-project-template-from-an-existing-project"></a>Uuden projektimallin luominen aiemmin luodun projektin pohjalta
Voit luoda projektimallin projektista seuraavilla tavoilla:

- **Työrakenne**: Projektista johdetun mallin työrakenne kopioidaan kaikkiin tehtäviin ja riippuvuuksiin. Luodut määritykset perustuvat yleisen ryhmän jäseniin, jotka lisätään projektiryhmään projektimallin luomisen yhteydessä.
- **Projektin arviot**: Kun projektimalli luodaan olemassa olevasta projektista, lähdeprojektin arviot kopioidaan projektimalliin.
- **Projektiryhmän jäsenet**: Kun malli luodaan olemassa olevasta projektista, kaikki nimetyt ryhmän jäsenet korvataan organisaation yleisellä resurssilla. Kaikkia toimien nimiä ja rooleja ylläpidetään.

## <a name="create-a-project-from-a-template"></a>Luo projekti mallista  
 Voit luoda projektin mallista seuraavilla tavoilla:  
  
-   Kun luot projektia tarjouksesta voit valita projektimallin projektin pikaluontilomakkeesta.  
  
-   projektilomake näytetään, ennen kuin tallennat tietueen, kun luot projektin napsauttamalla **uusi projekti** Täältä voit valita **valitse malli** -kentän, jos haluat valita ennalta määritettyjä projektimalleja organisaation luettelosta.  
  
-   Valitse **Luo projekti mallista** **Projektimalli** -sivulla, kun haluat luoda projektin mallista.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Projektimallin osien kopiointi projektiin  
 On muutamia asioita joita sinun tulisi tietää, kun kopioit projektimallin osia.  
  
 **Työrakenteen kopiointi**: kun kopioit työrakenteen projektimallista, jos projektissa on eri projektikalenteri kuin mallissa, tehtävien ajoitus kohdistetaan projektin kalenterin työaikaan. Tämä muuttaa aikataulun varmistavaan projektikalenteriin. Vastaavasti ensimmäinen työrakenteen tehtävä saa projektin alkamispäivän, joten loput tehtävän hierarkia-aikataulusta päivitetään määritetyn mallin työrakenteen keston ja riippuvuuksien perusteella.  
  
 **Projektien arvioiden kopiointi**: Kun kopioit koko projektin arvioiden rivit, hinnastot on päivitetty hankkeen omistavan yksikön kustannushinnaston ja asiakkaan myyntihinnaston perusteella. Yksikön kustannus- ja myyntihinnat määritetään projekteille, jotka liittyvät myyntientiteetin näin hinnastoihin.  
  
 **Projektiryhmän kopiointi**: Kun kopioit projektiryhmän projektimallista, yleisiä resursseja kopioidaan yli yhdessä mallissa määritettyjen taitojen ja ammattitaitojen kanssa. Projektimallissa säilytetään myös yleisiä resurssivarauksia.  
  
### <a name="see-also"></a>Katso myös  
 [Projektipäällikön opas](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
