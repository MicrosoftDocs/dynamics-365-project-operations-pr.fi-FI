---
title: Projektin resurssien aikatauluttaminen
description: Projektin resurssien aikatauluttaminen Project Servicessä
author: JohnPBurrows
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
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: f3b7ea1a2b81b86bedc85b77689145ba5afb579d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583120"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Projektin resurssien aikatauluttaminen (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Voit tarkistaa resurssien käytettävyyden, jotta saat yleisen käsityksen siitä, miten varattuja resurssit ovat, tai voit suodattaa näkymän taitojen, ryhmän, sijainnin ja muiden asetusten mukaan.  
  
Aikataulutaulukossa on luettelo resursseista ja heidän saatavuudestaan. Valitse tila näyttämään saatavuus **tuntien**, **päivän**, **viikon** tai **kuukauden** mukaan.  
  
Aikataulutaulukko on määritettävä, ennen kuin sitä voi käyttää. Lisätietoja on aiheessa [Aikataulutaulukon määrittäminen (Field Service tai Project Service Automation)](/dynamics365/field-service/configure-schedule-board).
  
Jos käytät vanhaa versiota, lisätietoja resurssien saatavuudesta on ohjeaiheessa [Resurssien saatavuuden näyttäminen](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Aikataulutaulukon varaustoiminnon, osoitteiden maantieteellisten koodien ja sijaintipalvelujen käyttöä varten kartat on otettava käyttöön.  
> 
> 1. Valitse päävalikosta **Resurssien aikataulutus** > **Hallinta**.  
> 2. Valitse **Aikataulutuksen parametrit**.  
> 3. Avaa tietue ja vieritä alas **Resource Scheduling Optimization** -osaan.  
> 4. Valitse **Muodosta yhteys Mapsiin** -kentässä **Kyllä**.  
> 5. Hyväksy ehdot ja tallenna tietue.  
> 6. Valitse päävalikosta **Project Service** > **Aikataulutaulukko**. Varaustarpeen voi tämän jälkeen aikatauluttaa manuaalisesti eri tavoin. Valitse tapa, joka sopii sinulle.
  
## <a name="find-available-resources"></a>Etsi käytettävissä olevat resurssit

1.  Napsauta hiiren kakkospainikkeella **Varaustarve**-luettelossa aikatauluttamatonta varausta ja valitse jokin seuraavista:  
  
- Etsi käytettävissä olevat resurssit aikataulutaulukon luettelosta valitsemalla **Etsi saatavuus – nykyiset resurssit**.  
- Etsi käytettävissä oleva resurssi järjestelmän resursseista valitsemalla **Etsi saatavuus – nykyiset resurssit**.  
   > [!NOTE]
   >  Kun toimit näin, suodattimet näyttävät valitun varaustarpeen vaihtoehdot.  
  
2. Kun havaitset käytettävissä olevan ajankohdan, napsauta sitä aikataulutaulukosta hiiren kakkospainikkeella ja valitse **Varaa tässä**. Vaihtoehtoisesti voit vetää ja pudottaa varaustarpeen käytettävissä olevaan ajankohtaan.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Resurssin varaaminen päivittäisessä näkymässä ja alivarattujen resurssien etsiminen
  
1.  Valitse aikataulutaulukosta ensin **Näyttötila** ja sitten **Päivät**.  
  
    Näkyviin tulee ruudukkonäkymä resurssin päiväkohtaisista varaustunneista ja vapaista päivistä.  
  
2.  Napsauta varattavan resurssin nimeä ja valitse sitten **Varaa**.  
  
3.  Valitse **Resurssivaraus (luonti)** -valintaikkunasta projekti, jolle haluat varata resurssin, sekä varaustapa ja aloitus- ja päättymisajat.  
  
4.  Kun olet valmis, valitse **Varaa**.  
  
## <a name="view-to-the-schedule-board"></a>Aikataulutaulukon tarkasteleminen
  
1.  Valitse alareunan luettelosta aikatauluttamaton resurssitarve.  
  
2.  Vedä varaustarve vapaaseen resurssiin/ajankohtaan aikataulutaulukossa.  
  
3.  Kun olet valmis, valitse **Varaa**.  
  
### <a name="additional-resources"></a>Lisäresurssit  
 [Resurssipäällikön opas](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
