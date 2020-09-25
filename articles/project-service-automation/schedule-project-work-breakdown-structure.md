---
title: Ajoita projekti työrakenteen kanssa
description: Projektin aikatauluttaminen työrakenteen kanssa Project Servicessä
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ca9b899c-7791-4990-b02e-cdff7f652621
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 003a1c543163b7ef1df1221d0b633a078e6619cf
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751223"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Ajoita projekti työrakenteen (Project Service) kanssa

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projektiaikataulu ilmaisee, mikä työ on suoritettava, mitkä resurssit suorittavat työn, ja aikajakson, jossa tämä työ on suoritettava. Projektiaikataulu kuvastaa kaikkea työtä, joka liittyy projektin toimittaminen oikeaan aikaan. Yksi projektin ensimmäisistä vaiheista on projektiaikataulun laatiminen. Projektin aikataulun määrittämiseksi on luotava työrakenne.  
  
 Luo projektirakenne ja työrakenne, jonka avulla voit:  
  
- jakaa työn hallittaviksi tehtäviksi  
  
- arvioida tehtävän suorittamiseen tarvittavan ajan  
  
- määrittää tehtävän riippuvuudet ja keston  
  
- määrittää kunkin tehtävän suorittamiseen tarvittavat roolit  
  
  Työrakenteen projektiaikataulun ulkoasu on tuttu ja täydennetty vuorovaikutteisella Gantt-kaaviolla.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Luo projektin työrakenne  
 Luo työrakenne kuvaamaan projektin tehtäväjärjestystä. Työrakenne sisältää tehtävät, kunkin tehtävän vaatimukset ja tuotto- ja kustannustiedot. Voit lisätä työrakenteeseen:  
  
-   Hierarkian tehtävien järjestys  
  
-   Muut tehtävät, jos sellaisia on, jotka on suoritettava, ennen kuin tehtävä voidaan aloittaa  
  
-   Alkamispäivämäärä, lopetuspäivämäärä ja tehtävän kesto  
  
-   Tehtävän edellyttämä tuntimäärä  
  
-   Mahdollisesti tarvittavat työntekijöiden taidot ja koulutus  
  
-   Työntekijät, joille tehtävä on määritetty  
  
-   Arvioitu tuotto ja kustannukset  
  
## <a name="task-types"></a>Tehtävätyypit  
Seuraavia tehtävätyyppejä käytetään luotaessa omaa työrakennetta:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Projektin pääsolmu** | Projektin ylätason yhteenvetotehtävä. Kaikki muut projektitehtävät luodaan sen alaisuuteen. Projektinimi on juuressa olevan tehtävän nimi. Pääsolmun työmäärä, päivämäärä ja kesto perustuvat sen alapuolella hierarkiassa oleviin arvoihin. Et voi muokata pääsolmun ominaisuuksia etkä poistaa pääsolmua. | 
| **Yhteenvetotehtävät tai säilössä olevat tehtävät** | Yhteenvetotehtävä on tehtävä, jolla on alitehtäviä. Yhteenvetotehtävällä ei ole omaa työmäärää eikä kustannuksia. Sen työmäärä ja kustannukset ovat kooste alitehtävistä. Voit muuttaa yhteenvetotehtävän nimeä, mutta et voi muuttaa työmäärää, päivämääriä tai kestoa, koska ne lasketaan automaattisesti. Yhteenvetotehtävän poistaminen poistaa tehtävän ja kaikki sen alitehtävät.|  
| **Lehtisolmutehtävät** | Lehtisolmutehtävä edustaa projektin tarkimmin eriteltyä työtä. Sillä on arvioitu työmäärä, suunniteltu määrä resursseja, suunnitellut alkamis- ja päättymispäivämäärät ja kesto.|

  
## <a name="task-hierarchy"></a>Tehtävähierarkia  
 Tehtävähierarkian luomisen vaihtoehdot:  
  
- **Lisää tehtävä**   Voit lisätä tehtävän haluamaasi paikkaan tehtävähierarkiassa. Jos et valitse paikkaa, uusi tehtävä näkyy lopussa.  
  
- **Sisennä tehtävä**.   Sisennä tehtävä, josta tulee sen yläpuolella olevan tehtävän alitehtävä.  
  
- **Ulonna tehtävä**   Ulonna tehtävä, jotta se ei enää ole alkuperäisen ylätason tehtävän alitehtävä.  
  
- **Siirrä ylöspäin ja Siirrä alaspäin**.   Siirtää tehtäviä ylös-ja alaspäin päätehtävän hierarkiassa. Tehtävän siirtäminen ylös- tai alaspäin ole vaikuta sen työmäärään, kustannuksiin, päivämääriin eikä kestoon.  
  
## <a name="task-attributes"></a>Tehtävän määritteet  
 Tehtävän nimi kuvaa keskeneräistä työtä. Tehtävän määritteiden avulla kuvataan tehtävän aikataulua ja henkilöstötarpeita.  
  
### <a name="schedule-attributes"></a>Aikataulun määritteet

 - Määritä tehtävän aikataulu antamalla arvot kohtiin **Työtunnit**, **Resurssien määrä**, **Alkamispäivämäärä**, **Lopetuspäivämäärä** ja **Kesto**. 
 - **Työmäärä** on arvioitu tuntimäärä, jonka tehtävän suorittaminen kestää.
 - **Resurssien määrä** on arvio, jonka projektipäällikkö asettaa tehtävälle parhaan mahdollisen aikataulun aikaansaamiseksi. 
 - **Kesto** (päivinä) ilmaisee työpäivien määrän, jonka tehtävän suorittaminen kestää.  
  
### <a name="staffing-attributes"></a>Henkilöstömääritteet

 - **Rooli**, **Resurssin organisaatioyksikkö**, **Resurssien määrä** ja **Resurssit** kuvaavat tehtävän henkilöstötarpeita. 
 - **Rooli** kuvaa tehtävän suorittamiseen tarvittavaa resurssityyppiä. 
 - **Resurssin organisaatioyksikkö** osoittaa organisaatioyksikön, josta henkilöstöresurssit tulee valita kyseiseen tehtävään. Tämä myös vaikuttaa tehtävän kustannus- ja myyntiarvioon, koska tämä kirjataan määritettäessä resurssin yksikkömyyntihintaa. 
 - **Resurssit** sisältää yleisen resurssin tai nimetyn resurssin, kun sellainen löytyy.  
  
## <a name="task-dependencies"></a>Tehtävän riippuvuudet  
 Voit luoda edeltäjäsuhteita yhden tai useamman tehtävän välille työrakenteeseen. Voit määrittää edeltäjä-kenttään useita arvoja tehtäville ilmaisemaan tehtäviä, joista se on riippuvainen. Kun määrität tehtävälle edeltäjäarvon, tehtävän voi aloittaa vasta kun edeltäjätehtävät on suoritettu. Tämän riippuvuuden määrittäminen tehtävälle johtaa tehtävän suunnitellun alkamispäivän sekä kaikkien sen edeltäjien myöhäisimmän päättymispäivämäärän uudelleenlaskentaan. Tehtävälle määritetty tehtävätila ei rajoita edeltäjiin liittyviä vaikutuksia aikatauluun.  
  
## <a name="task-mode"></a>Tehtävätila  
 Tehtävätila on yksi tärkeitä tekijöitä, jotka määrittävät lehtisolmun tehtävien ajoituksen. Jokaiseen tehtävälle on kaksi tehtävätilaa: automaattinen aikataulutustila ja manuaalisen aikataulutustila.  
  
-   **Automaattinen aikatauluttaminen**   Kun määrität tehtävätilan arvoksi Automaattisesti aikataulutettu, ajoitusmoduuli käyttää ajoitussääntöjä seuraaviin tehtävän määritteisiin määrittäessään tehtävän ajoitusta:  
  
    -   Edeltäjät  
  
    -   Työmäärä  
  
    -   Resurssien määrä  
  
    -   aloitus- ja päättymispäivät  
  
-   **Omat ajoitussäännöt**.   Lehtisolmutehtävän, jolla ei ole edeltäjiä, aloituspäivämäärän oletusarvo on projektin ajoituksen aloituspäivämäärä. Lehtisolmutehtävän kesto vastaa aina alkamis- ja päättymispäivämäärien välisten työpäivien lukumäärää. Kun tehtävä ajoitetaan automaattisesti, aikataulutusmoduuli noudattaa seuraavia sääntöjä:  
  
    -   Tehtävän alkamis- ja päättymispäivien on aina oltava projektin ajoituskalenterin mukaisia työpäiviä  
  
    -   Tehtävän, jolla on edeltäjiä, aloituspäivämäärän oletusarvo on sen edeltäjien myöhäisin lopetuspäivämäärä.  
  
    -   Työmäärä = Henkilömäärä * kesto * projektikalenterin normaalin työpäivän tuntimäärä  
  
-   **Manuaalinen aikataulutus**.   Joissakin tapauksissa haluat ehkä poiketa näistä säännöistä. Näissä tapauksissa voit määrittää tehtävän tehtävätilan manuaalisesti ajoitettavaksi. Tämä estää aikataulutusmoduulia laskemasta muiden ajoitusmääritteiden arvoja. Tehtävien edeltäjien määrittäminen vaikuttaa aina riippuvaisen tehtävän alkamispäivämäärän.  
  
## <a name="create-a-work-breakdown-structure"></a>Luo työrakenne  
  
1.  Siirry kohtaan **Project Service > Projektit**.  
  
2.  Napsauta käsiteltävää projektia.  
  
3.  Valitse näytön yläosassa olevassa palkissa, projektin nimen vieressä oleva alanuoli ja valitse sitten työrakenne.  
  
4.  Lisää tehtävä valitsemalla **Lisää tehtävä**. Täytä tehtävän kenttien tiedot ja valitse **Tallenna**.  
  
5.  Jatkaa tehtävien lisäämistä kunnes työrakenne on valmis. Luodessasi työrakennetta voit järjestää tehtäviä seuraavasti:  
  
    -   Valitse tehtävä ja siirrä se toisen tehtävän alapuolelle valitsemalla **Sisennä** tai siirrä se yhden tason verran taaksepäin valitsemalla Poista sisennys.  
  
    -   Valitse tehtävä ja siirrä sitä ylös- tai alaspäin luettelossa valitsemalla **Siirrä ylöspäin** tai **Siirrä alaspäin**.  
  
    -   Piilota Gantt-kaavio valitsemalla **Piilota Gantt-kaavio** ja valitse **Näytä Gantt-kaavio** kun haluat näyttää sen uudelleen.  
  
    -   Valitse eri aikaväli Gantt-kaaviolle kohdassa **Aika-asteikko**.  
  
6.  Lisää rooleja, jotka määritit projektin ryhmän jäsenille työrakenteessa, valitsemalla **Luo projektiryhmä**.  
  
7.  Valitse **Tallenna** näytön oikeassa alakulmassa, kun olet tehnyt kaikki muutokset.  
  
### <a name="see-also"></a>Katso myös  
 [Projektipäällikön opas](../project-service/project-manager-guide.md)