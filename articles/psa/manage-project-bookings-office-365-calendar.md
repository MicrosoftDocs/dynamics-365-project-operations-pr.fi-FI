---
title: Projektien ja varausten hallinta Office 365 -kalenterissa
description: Projektien ja varausten hallintatapa Office 365 -kalenterissa
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1df4864ca8dbf6948ca88a7c82a6c0a676e3bd53
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275039"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Projektien ja varausten hallinta kalenterissa (Project Service)

> [!Note]
> VANHENTUNUT: Tämä ominaisuus on vanhentunut, eikä se ole enää käytettävissä.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Voit tarkastella henkilökohtaisia tapaamisia, projektityön varauksia ja Field Service -sovelluksen työtilausten delegointeja [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] -kalenterin avulla.  
  
 Päiväohjelmaa on helppo hallita, kun kaikki on keskitetysti samassa paikassa. Kokoukset, tapaamiset, varaukset ja tehtävät ovat kaikki saatavilla [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenterissa.  
  
 Jos käytössä [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], voit lisätä myös henkilökohtaiset tapaamiset Project Servicen aikamerkintänäkymään. Tällä tavoin projekti- ja resurssipäälliköt tietävät, oletko käytettävissä projekteihin. Se myös säästää aikaa, koska sinun ei tarvitse lisätä henkilökohtaisten tapaamisten tietoja kahdesti. Sinun tarvitsee vain tuoda henkilökohtaiset tapaamiset kalenterista Project Servicen aikamerkintänäkymään.  
  
 Kalenteri synkronoi projekti- ja työtilausvaraukset kuluvasta päivästä neljän viikon päähän. Tätä asetusta ei voi muuttaa.  
  
 Vain synkronointia PSA:sta [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] -kalenteriin tuetaan. Voit synkronoida päinvastaisessa järjestyksessä. 
  
 Lisätietoja [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] -kalenterin käytöstä on ohjeaiheessa [Outlookin verkkokalenterin käyttö liiketoiminnassa](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Määritys  
 Ennen varauksien tarkastelua ja hallintaa [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]:n kalenterissa tietyt asiat on määritettävä.  
  
- Tarvitset [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]:n yleisen järjestelmänvalvojan tai järjestelmänvalvojan tunnistetiedot.  
  
- Järjestelmänvalvojan on määritettävä sähköpostipalvelinprofiili ja jokaisen käyttäjän on määritettävä postilaatikkonsa. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Sähköpostin käsittelyn asettaminen palvelinpään synkronoinnille](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Synkronoinnin ottaminen käyttöön organisaatiossa (järjestelmänvalvojan tehtävä)  
  
1.  Valitse päävalikosta **Asetukset** > **Hallinto**.  
  
2.  Valitse **Järjestelmäasetukset**.  
  
3.  Valitse **Synkronointi**-välilehti.  
  
4.  Valitse **Valitse otetaanko käyttöön resurssivarauksien synkronointi** -kohdassa **Synkronoi resurssivaraukset Outlookin kanssa**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Synkronoinnin ottaminen käyttöön käyttäjäprofiilissa (käyttäjätehtävä)  
  
1.  Napsauta **Asetukset**-painiketta näytön oikeassa yläkulmassa.  
  
2.  Valitse **Asetukset**.  
  
3.  Valitse **Synkronointi**-välilehti.  
  
4.  Valitse **Synkronoi resurssivaraukset Outlookin kanssa** -kohdassa **Synkronoi resurssivaraukset Outlookin kanssa**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Henkilökohtaisten tapaamisien tuominen (käyttäjätehtävä)  
 Voit tuoda henkilökohtaiset tapaamiset kalenterista Project Service Automationin aikamerkintänäkymään.  
  
1. Avaa [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]:n kalenteri ja valitse **Tuo tiedot**.  
  
2. Valitse Suodattimet-näytössä ensin **Tapaamiset Exchangesta** ja sitten **Käytä**.  
  
3. Järjestelmä hakee kuluvan viikon tapaamiset aikamerkintänäkymään ehdotettuina merkintöinä. Voit lisätä toisen viikon tapahtumia valitsemalla **Edellinen** tai **Seuraava**.  
  
4. Valitse Project Service Automationin aikamerkintänäkymään lisättävä tapaaminen.  
  
5. Valitse avautuvassa **Aikamerkintä**-ruudussa sopivat asetukset tapaamisen muuntamiseksi Project Service Automationin aikamerkintänäkymään.  
  
6. Valitse **Tallenna**.  
  
### <a name="see-also"></a>Katso myös  
 [Aika-, kulu- ja yhteistyöopas](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]