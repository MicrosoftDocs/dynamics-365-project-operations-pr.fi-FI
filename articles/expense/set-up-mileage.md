---
title: Kilometrikorvausten määrittäminen kilometrikorvaustasoilla
description: Tässä artikkelissa on tietoja kilometrikorvauksista ja kilometrikorvaustasoista.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9689bbaf4c4f88ad9f746c3f98676f97e634ab6c
ms.sourcegitcommit: 5e1f549a2e55a87351b2979e3aff402ed35487e1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9064274"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Kilometrikorvausten määrittäminen kilometrikorvaustasoilla

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Kun kulu raportoidaan ja valittu kululuokka on **Kilometrikorvaus**, kyseisen kulurivin summa lasketaan *hinta per kilometri* -summaa. Tämä summa lasketaan käyttämällä määritettyjä kilometrikorvaustasoja. Jos kilometrikorvaustasoja ei ole määritetty, käytetään kilometrikorvausten vakiohintaa. 

Kilometrikorvaustasot voidaan määrittää kohdasta **Kulujen hallinta** > **Määritys** > **Yleiset** > **Kululuokat** > **Kilometrikorvaus** > **Luokka-asetukset**.

Kun olet päivittänyt versioon 10.0.18 ja organisaatiosi käyttää kilometrikorvausten kululuokkaa, harkitse kilometrikorvausten ominaisuuden ottamista käyttöön, kun olet tarkistanut alla olevat rakennemuutokset. 

Kilometrikorvaustasojen uusi rakenne vaikuttaa **Määrä**-kentän arvon käsittelytapaan. Ennen 10.0.18-version julkaisua **Määrä**-kentän arvoa pidettiin alarajana. Kun lukema ylitti tämän arvon, käytettiin vastaavaa hintaa.  Versiosta 10.0.18 alkaen **Määrä**-kentän arvoa pidetään ylärajana. Vastaavaa hintaa käytetään, kun kilometrilukema on pienempi kuin **Määrä**-kentän arvo.  Uusi kilometrikorvaustasojen malli auttaa yhdenmukaistamaan kilometrikorvaustasot ja parantaa käytettävyyttä.   

Kaikki hyväksytyt kuluraportit lasketaan uudelleen kirjauksen aikana uuden rakenteen mukaisesti.

## <a name="example"></a>Esimerkiksi
 
### <a name="before-version-10018"></a>Ennen versiota 10.0.18
Kun kilometrikorvaustasoja on kaksi, kunkin tason **Määrä**-kenttä osoittaa kilometrikorvauksen alarajan. Tällä hetkellä tason yksi arvo on nolla (0) ja hinta 0,45, ja tason kaksi arvo on 1 000 ja hinta 0,25. Jos maili- tai kilometrilukema ylittää kentässä olevan arvon, käytetään asiaan liittyvää hintaa. Jos minkään rivin määrä ei ole nolla, järjestelmä käyttää Kulujen hallinta -osiossa määritettyä kilometrihintaa. 
 
Jos työntekijä lähettää 1 500 mailin kuluraportin, kirjatun kuluraportin kaksi kilometrikorvausriviä olisivat: 1 000 (hinta 0,45) + 500 (hinta 0,25) = 575,00.

### <a name="after-version-10018"></a>Version 10.0.18 jälkeen
Versiossa 10.0.18 kunkin tason **Määrä**-kenttä osoittaa tason ylärajan. Tällä hetkellä tason yksi arvo on 999 ja hinta 0,45, ja tason kaksi arvo on 999 999 999,00 ja hinta 0,25. Jos maili- tai kilometrilukema ylittää **Määrä**-kentässä olevan arvon, käytetään asiaan liittyvää hintaa. Jos kaikki ylärajoitukset ylittyvät, järjestelmä käyttää Kulujen hallinta -osiossa määritettyä kilometrihintaa. 
 
Saman skenaarion laskeminen oikein edellyttää tason asetusten muuttamista. Tason yksi **Määrä**-kentän arvo on 999,0 ja tason kaksi arvo on 999 999 999,00. Jos työntekijä ylittää tason yksi mailien tai kilometrien kokonaismäärän, järjestelmä käyttää Kulujen hallinta -osiossa määritettyä kilometrihinta. 
  
Jos työntekijä lähettää 1 500 mailin kuluraportin, kirjatun kuluraportin kaksi kilometrikorvausriviä olisivat: 1 000 (hinta 0,45) + 500 (hinta 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Kilometrikorvauksen summan laskeminen useille samaa hintaa käyttäville kilometrikorvaustasoille -ominaisuuden ottaminen käyttöön

**Kilometrikorvauksen summan laskeminen useille samaa hintaa käyttäville kilometrikorvaustasoille** -ominaisuus parantaa kilometrikorvausten laskentaa. Ota tämä ominaisuus käyttöön noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Työtilat** > **Ominaisuuksien hallinta**. 
2. Etsi ja valitse luettelosta **Kilometrikorvauksen summan laskeminen useille samaa hintaa käyttäville kilometrikorvaustasoille** ja valitse sitten **Ota käyttöön nyt**.

Kun olet ottanut ominaisuuden käyttöön, palauta kilometrikorvaustasot vastaamaan **Määrä**-kentän arvoa oikein. 

## <a name="enable-the-mileage-totals-calculation-by-fiscal-year-feature"></a>Välitavoitteen summien laskennan käyttöönotto tilikauden mukaan -ominaisuus

**Välitavoitteen summien laskennan käyttöönotto tilikauden mukaan** -ominaisuus ottaa käyttöön uuden asetuksen kulujen hallintaparametreissa. Se suorittaa välitavoitteen summien laskennan tilikauden mukaan kalenterikauden sijaan. Ota tämä ominaisuus käyttöön noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Työtilat** > **Ominaisuuksien hallinta**.
1. Etsi ja valitse luettelosta **Välitavoitteen summien laskennan käyttöönotto tilikauden mukaan** ja valitse sitten **Ota käyttöön nyt**.
1. Siirry kohtaan **Kulujen hallinta** > **Määritys** > **Yleiset** > **Kulujen hallintaparametrit**.
1. Etsi ja valitse **Kulujen hallintaparametrit** -sivulta **Käytä tilikautta välitavoitteen summissa**.

Kun **Käytä tilikautta välitavoitteen summissa** -kohta on otettu käyttöön, välitavoitteen summat lasketaan tilikauden mukaan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]