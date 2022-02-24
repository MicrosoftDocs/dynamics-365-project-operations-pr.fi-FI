---
title: Projektin kustannukset ja tuotto
description: Tässä aiheessa on tietoja projektin kustannusten ja tuoton arvioinnista.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 279c1119d334a7f60906e33b3fc7ca22ff9a360d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148324"
---
# <a name="project-costs-and-revenue"></a>Projektin kustannukset ja tuotto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektin arviot tarjoavat taloudellisen näkymän työhän, joka on arvioitu ja aikataulutettu projektin aikataulussa. **Arviot**-välilehti **Projektit**-sivulla näyttää suunnittelemasi työn kustannus- ja tuottovaikutukset. Se sisältää myös tietoja monista esimääritetyistä dimensioista. 

> ![Arviot-välilehti](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Projektin kustannus- ja myyntiarvot

Hinnastot määrittävät projektin roolien kustannukset ja laskutushinnan. Voit määrittää työn kustannus- ja tuottovaikutuksen työtehtävän nimeen liitettyjen roolien sekä tehtävään määritetyn nimetyn resurssin perusteella. Jos on tehtäviä, joihin ei ole osoitettu tekijöitä (yleisiä tai nimettyjä), et voi saada kustannus- tai myyntiarvioita. Kustannus- ja myyntiarvot ottavat huomioon hinnastoissa määritellyn päivämäärän.

### <a name="default-cost-price"></a>Kustannusten oletushinta  

Jokainen projekti kuuluu organisaatioon. Tämä organisaatio näkyy projektin **Hankintayksikkö** -kentässä. Hankintayksikköön liitettyä hinnastoa käytetään yksikkökustannushinnan määrittämiseksi. OIkeiden kustannushintojen määrittämiseksi rooleille sitä päivämäärää varten, joka on määritelty arvioriveillä, etsi roolin, yksikön ja organisaation yksikön yhdistelmää kustannushinnastosta. 

Jotta niiden kustannushinnat voidaan laskea, kaikki tehtävät on kohdennettava resurssille. Kaikkien kohdentamattomien tehtävien kustannushinta on 0,00.

Jos roolien, yksiköiden ja organisaatioyksiköiden yhdistelmä ei palauta kustannushintaa hankintayksikön hinnastosta, järjestelmä ohittaa yksikön. Se hakee sen sijaan vain roolien ja organisaatioyksiköiden yhdistelmän. Jos kustannushinta löytyy, käytetään muuntokertoimia muuntamaan se yksiköksi, jonka valitsit arviorivillä.

Jos roolin ja organisaatioyksikön yhdistelmä ei palauta kustannushintaa, järjestelmä ohittaa organisaatioyksikön. Se hakee sen sijaan roolien ja yksiköiden yhdistelmän, joka määrittää oletushinnan (mahdollisen muunnoksen jälkeen).

Jos järjestelmä ei löydä roolille hintaa, kustannushinta arviorivillä asetetaan oletusarvoon **0,00**. Kaikki projektin kustannusarvioriveillä olevat kustannussummat ovat hankintayksikön valuutassa.

> [!NOTE]
> Microsoft Dynamics 365 tallentaa kustannussummat oletusarvoisesti perusvaluutassasi. **Arviot**-välilehdellä näytettävät kustannussummat ovat kuitenkin hankintayksikön valuutassa.  

### <a name="default-sales-price"></a>Oletusmyyntihinta 

Myyntihinnaston määrittää joko se myyntikohde, johon projekti on liitetty, tai projektin asiakas. Kun projektiin liittyy myyntikohde, kuten mahdollisuus, tarjous tai sopimus, myyntikohteen myyntihinnan määrittää tarjoukseen tai sopimukseen liittyvä hinnasto. Jos tarjouksessa tai sopimuksessa on mukautettu hinnasto, sitä käytetään oletusmyyntihinnastona projektin arvioille. Jos myyntikohteiden kanssa ei ole yhteyttä, parametrien oletusmyyntihinnastoa käytetään projektin oletusmyyntihinnastona, jota vastaa projektissa määritetty asiakasvaluutta.

Kullakin arviorivillä on siihen liittyvä resurssiyksikkö. Resurssiyksikkö osoittaa organisaatioyksikön, josta resurssit on varattu, jotta tehtävä voidaan suorittaa loppuun. Määrittääksesi myyntihinnan liitetyille rooleille etsi roolin, yksikön ja resurssiyksikön yhdistelmää myyntihinnastossa. Jos tehtävässä ei ole kohdennuksia, tehtävän myyntihinta on 0,00.

Jos roolin, yksikön ja resurssiyksikön yhdistelmä ei palauta kustannushintaa myyntihinnastosta, järjestelmä ohittaa yksikön. Se hakee sen sijaan vain roolin ja resurssiyksikön yhdistelmän. Jos myyntihinta löytyy, käytetään muuntokertoimia muuntamaan se yksiköksi, jonka valitsit myynnin arviorivillä. 

Jos roolin, yksikön ja resurssiyksikön yhdistelmä ei palauta myyntihintaa myyntihinnastosta, järjestelmä ohittaa resurssiyksikön. Se hakee sen sijaan roolien ja yksiköiden yhdistelmän, joka määrittää oletushinnan (mahdollisen muunnoksen jälkeen).

Jos järjestelmä ei löydä roolille hintaa, myyntihinta arviorivillä asetetaan oletusarvoon **0,00**.

**Arviot**-välilehdellä on ruudukkonäkymä, jossa näkyvät arviorivit. Ruudukossa on yksikkö-, kokonaiskustannushinta- ja kokonaismyyntihinta-sarakkeet, jotka on esitetty seuraavassa kuvassa. 

> ![Arviot-välilehden ruudukkonäkymä](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Projektin arvioiden aikavaiheistettu näkymä

Projektiarvioiden aikajaksoittain tarkasteltavaan näkymään on määritetty valitsemasi aikajanan arviotiedot, jotka näkyvät aikajanalla ruudukkonäkymässä. Oletusarvoisesti arviotiedot siirretään **Rooli**-dimensioon.

> ![Projektin arvioiden aikavaiheistettu näkymä](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Arvioidun työmäärän kohdennus tehtävätilaan perustuen

Aikajaksotetussa näkymässä jaat kokonaistyömäärän, joka on arvioitu tehtävälle, kohdentamalla työmäärätunnit yksikköaikajaksolle valitulla aikajanalla. Tehtävätila määrittää, kuinka työmäärä kohdennetaan tehtävän keston ajalle. Kaksi kohdistustapaa ovat **Tasainen** ja **Työtunteihin perustuva**.

### <a name="work-hours-based-allocation"></a>Työtunteihin perustuva kohdistus
 
Automaattisesti aikatauluttavassa tehtävätilassa asetetaan päivittäiset oletustunnit tehtäväresursseille täydellä työtuntimäärällä. Tämä tominta pätee, kun työmäärä kohdennetaan jakamalla se tehtävän keston ajalle aikavaiheistetussa näkymässä. Jos esimerkiksi arvioit, että tehtävä suoritetaan loppuun yhdellä resurssilla **Päivä**-aikaskaalalla, päivää kohti kohdennettu työmäärä ei ylitä projektin kalenterissa määritettyjä päiväkohtaisia tunteja. Työmäärän kohdistus varmistaa siksi aina, että resurssit on arvioitu käytettäviksi koko päivän ajan.

### <a name="even-allocation"></a>Tasainen kohdistus

Manuaalisesti ajoitettuun tehtävätilaan ei käytetä työtunteja projektikalenterista. Tehtävän ajoitus perustuu sen sijaan käyttäjän syötteisiin. Tällaisille tehtävillä työmäärän kohdistuksella yksikön aikajaksoa kohti valitulla aikaskaalalla ei ole rajoittavia tekijöitä. Tehtävän kokonaistyömäärä jaetaan ja kohdistetaan jokaiselle yksikön aikajaksolle kohti valitulla aikaskaalalla. Näin tehtävässä määritetty tehtävätila määrittää työmäärän jakamista tai kohdistusta yksikön aikajaksoa kohti aikavaiheistetuissa arvioissa.

## <a name="grouping-and-time-phasing-options"></a>Ryhmittely- ja aikavaiheistusasetukset

Aikavaiheistettu näkymä näyttää työmäärän, kustannusten ja myyntiarvioiden jakautumisen päivittäin, viikoittain, kuukausittain tai vuosittain. Oletusarvoisesti arviotiedot siirretään **Rooli**-dimensioon. Voit kuitenkin käyttää **Ryhmittely**-toimintoa ryhmitelläksesi kahden muun dimension avulla: **Luokka** ja **Resurssi**.

Voit valita sekä ruudukkonäkymässä että aikavaiheisessa näkymässä näytettävät kentät. Kunkin aikalohkon summat näkyvät projektin alalaidassa. Ne näyttävät arvioidun kokonaistyömäärän, kustannukset ja myynnin päivälle, viikolle, kuukaudelle tai vuodelle. Oletus kustannushinta ja myyntihinta ovat voimassa. Toisin sanoen ne muuttuvat kunkin resurssin mukaan valitsemasi aikavaiheisen näkymän perusteella.

## <a name="expense-estimates"></a>Kulujen arviot

**Lisää uusi kuluarvio** -painike ruudukkonäkymässä mahdollistaa sellaisten projektin kulujen kirjaamisen, jotka eivät suoraan liity työvoimaan. Voit kirjata tietyn tehtävän tai koko projektin kuluarviot. Valitse kul luokat ja alustava päivämäärä, jolloin oletat kulun tapahtuvan. Jos liitetyllä kustannushinnastolla ja myyntihinnastolla on oletushinnat (tai hinnankorotuksen prosenttiosuudet määritetään kululuokille), ne asetetaan automaattisesti arvioriville, kun liittäminen tapahtuu.
