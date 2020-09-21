---
title: Määritä projektin kustannusten ja myyntivoiton arviot
description: Projektin kustannus- ja tuottoarvioiden määrittäminen Project Servicessä
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: cfa3c0c6-a57d-4d50-90dd-9a517d380257
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fd581cdb84a3a1c0dbbd1b9b27d87ddd959f883
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751140"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Määritä projektin kustannusten ja myyntivoiton arviot 

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projektien arviot tarjoavat taloudellisen näkymän arvioituun ja aikataulutettuun työhön projektin työrakenteesta. Arviot-näkymä ilmoittaa suunnitellun työn kustannusten ja myyntivoiton vaikutuksen. Arviot-näkymä tarjoaa työkalun jolla voidaan tarkastella tietoja lukuisista ennalta määritetyistä dimensioista, jotka kertovat parhaiten projektin taloudellisista vaikutuksista.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Projektin kustannus ja myyntiarvo  
[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -hinnastot määrittävät projektissa käytettävien roolien kustannukset ja laskutushinnan. Projektin työrakenteen tehtäviin liittyvien roolien perusteella voit määrittää projektiin liittyvän työn kustannusten ja myyntivoiton vaikutukset.  
  
## <a name="cost-price-defaulting"></a>Kustannushinnan oletusarvo  
Jokainen projekti kuuluu organisaatioon (mainittu projektin kohdassa **Omistava yksikkö**). Omistavaan organisaatioyksikköön liittyvä hinnasto määrittää yksikön kustannushinnan. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] määrittää roolien kustannushinnat etsimällä kustannushinnastosta roolin, yksikön ja organisaatioyksikön yhdistelmän, jolla saadaan oikea kustannushinta arviorivien voimassaolopäivälle.  
  
Jos yhdistetty rooli, yksikkö ja organisaatioyksikkö eivät muodosta kustannushintaa omistavan yksikön hinnastosta, yksikön sijaan otetaan huomioon roolin ja organisaatioyksikön yhdistelmä. Jos kustannushinta on olemassa, tämä hinta muunnetaan arviorivillä valituksi yksiköksi.  
  
Jos kustannushintaa ei saada yhdistämällä rooli ja organisaatioyksikkö, organisaatioyksikön sijaan otetaan huomioon roolin ja yksikön yhdistelmä, ja oletushinta määräytyy tarvittaessa suoritettavan muunnon jälkeen.  
  
 Jos tietylle roolille ei ole hintaa, kustannushinnan oletusarvo arviorivillä on 0,00.  
  
 Kaikki projektin kustannusarvioriveillä olevat kustannussummat ovat omistavan organisaatioyksikön valuutassa.  
  
## <a name="sales-price-defaulting"></a>Myyntihinnan oletusarvo  
Myyntihintaluettelo perustuu myynti-entiteettiin, johon projekti on liitetty. Tarjoukseen tai sopimukseen liittyvä myyntihinnasto määrittää yksikön myyntihinnan. Jos tarjouksessa tai sopimuksessa on mukautettu hinnasto, tämä on projektin arvioiden oletusmyyntihinnasto. Jos kytkentää myynti-entiteetteihin ei ole olemassa, parametrien asetuksiin määritetty oletusmyyntihinnasto on projektin oletusmyyntihinnasto. Jokaisella arviorivillä on liittyvä resurssin organisaatioyksikkö, joka osoittaa organisaatioyksikköä, josta resurssit on varattu tehtävän valmistumiseen asti. Liittyvien roolien myyntihinta määritetään etsimällä myyntihinnastosta roolin, yksikön ja resurssin organisaatioyksikön yhdistelmää, jolla saadaan oikea myyntihinta arviorivin voimassaolopäivälle.  
  
Jos roolin, yksikön ja resurssin organisaatioyksikön yhdistelmä ei muodosta myyntihintaa myyntihintaluettelosta, järjestelmä ei huomioi yksikköä ja hakee roolin ja resurssin organisaatioyksikön yhdistelmää. Jos myyntihinta on löytyy, tämä muunnetaan myyntiarviorivillä valituksi yksiköksi.  
  
Jos järjestelmä ei löydä roolille hintaa, myyntihinnan oletusarvon arviorivillä pitää olla 0,00.  
  
Arviot-näkymässä on ruudukkonäkymä, jossa näkyy tasainen ruudukko yksikkö-, kokonaiskustannus- ja myyntihinta-arvioriveineen.  
  
## <a name="time-phased-view-of-project-estimates"></a>Projektin arvioiden aikavaiheistettu näkymä  
Projektin arvioiden aikavaiheistetussa näkymässä ruudukkonäkymän arvioiden tiedot muunnetaan oletusarvoisesti rooleittain Pivot-taulukkoon ja näytetään arvioitujen tietojen levitys aikajanalla, valitulla aika-asteikolla.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Tehtävätilaan perustuva työmäärän arvioitu kohdistus  
Aikajaksotetussa näkymässä arvioitu tehtävän kokonaistyömäärä jaetaan kohdistamalla tietty määrä työtunteja valitun aika-asteikon yksikön aika-arvoa kohti. Project Service -sovelluksessa tehtävätila määrittää, miten työmäärä jaetaan tehtävän keston ajalle. Kaksi kohdistustapaa ovat tasainen kohdistus ja työtuntien perusteella tehtävä kohdistus  
  
## <a name="work-hours-based-allocation"></a>Työtuntien perusteella tehtävä kohdistus  
Automaattinen tehtävän aikataulutustila ohjaa arvioitujen tehtäväresurssien määrää siten, että ne arvioidaan käytettäviksi koko päivittäisen työajan puitteissa. Tämä pätee määrättäessä myös työmäärää jakamalla sen töiden keston mukaan myös aikavaiheistetussa näkymässä. Esimerkiksi "Päivä"-aika-asteikolla yhden resurssin suorittamaksi arvioidun tehtävän päivää kohti kohdistettu työmäärä ei ylitä päivittäisten työtuntien määrää, joka on määritetty projektin kalenterissa. Työmäärän kohdistus varmistaa aina, että resurssit on arvioitu käytettäviksi koko päivänä.  
  
## <a name="even-distribution"></a>Tasainen jakelu  
Manuaalisesti ajoitettava tehtävätila ei noudata työaikaa, projektikalenteria eikä tehtävälle määritettyjä resursseja. Tehtävän ajoitus perustuu käyttäjän syötteisiin. Tällaisten tehtävien osalta työmäärän kohdistuksella yksikön aika-arvoa kohti valitulla aika-asteikolla ei ole rajoittavia tekijöitä. Tehtävän kokonaistyö jaetaan ja kohdistetaan tasaisesti yksikön aika-arvoa kohti valitulla aika-asteikolla.  
  
Näin määritetty tehtävätila määrittää työmäärän jakamista tai kohdistusta yksikön aika-arvoa kohti aikavaiheistetuissa arvioissa.  
  
## <a name="grouping-and-time-phasing-options"></a>Ryhmittely- ja aikavaiheistusasetukset  
Tämä näkymä auttaa ymmärtämään työmäärän, kustannusten ja myynnin arvioiden jakautumista päivittäin, viikoittain, kuukausittain tai vuosittain. Group By -asetus sallii arviointien tietojen Pivot-taulukoinnin kahdella muulla ulottuvuudella: luokka ja resurssi. Voit valita näytettävät kentät sekä ruudukkonäkymässä että aikajaksotetussa näkymässä. Alareunassa näkyvät aikalohkojen arvioitu kokonaistyömäärä ja -summat, sekä päivä-, viikko-, kuukausi- tai vuosimyynti.  
  
Kustannuksen ja myynnin oletushinta määräytyy voimassaolopäivän mukaan: kun roolien hinnat muuttuvat, ne ovat läpinäkyvämpiä aikajaksotetussa näkymässä, kun arvioituja tietoja tarkastellaan "Resurssi" Pivot-taulukkoon muunnettuna ja viikoittain aikajaksotettuina.  
  
## <a name="expense-estimates"></a>Kulujen arviot  
Mahdolliset projektissa aiheutuvat kustannukset, joka eivät suoraan liity työhön, voidaan tallentaa projektin arviot ruudukkonäkymässä. Voit tehdä tämän käyttämällä **Lisää kuluarvio** asetusta ruudukkonäkymässä. Kuluarvioita voidaan tallentaa tietyn tehtävän tai koko projektin osalta; voit valita kululuokat näillä riveillä ja valita alustava päivämäärä, jolloin kulun odotetaan syntyvän. Jos liittyvillä kustannuksilla ja myyntihinnastolla on oletushinnat tai hinnankorotuksen prosenttiosuudet määritetään kululuokille, ne asetetaan oletusarvoisesti yhdistetylle arvioriville.  
  
### <a name="see-also"></a>Katso myös  
 [Projektipäällikön opas](../project-service/project-manager-guide.md)
