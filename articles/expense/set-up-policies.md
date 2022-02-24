---
title: Kulukäytäntöjen määrittäminen
description: Voit määrittää kulukäytäntöjä, joita työntekijöiden on seurattava kuluraporttien ja matkustusehdotusten syöttämisessä ja lähettämisessä.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c55cec132649daf9ee08ea4d8db3668860247934
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128414"
---
# <a name="define-expense-policies"></a>Kulukäytäntöjen määrittäminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Voit määrittää kulukäytäntöjä, joita työntekijöiden on noudatettava kuluraporttien ja matkustusehdotusten syöttämisessä ja lähettämisessä.         
Kulukäytäntöjen käyttäminen voi olla avuksi kulujen tehokkaassa hallinnassa.         

Voit määrittää esimerkiksi New Yorkin hotellikuluille käytännön, jonka mukaan yökohtainen kulu saa olla enintään 250 dollaria.       
Jos työntekijä lähettää kuluraportin tai matkustusehdotuksen, jossa huoneen hinta ylitää tämän summan, järjestelmä ilmoittaa         
työntekijälle, että kulun summa ylittää käytännön määrittämän summan. Voit määrittää viestin, jonka työntekijä saa, kun        
määrität käytännön.      
        
Voit määrittää seuraavia kolmentyyppisiä käytäntöjä:         
        
- **Varoitus** : Antaa työntekijälle mahdollisuuden lähettää kuluraportin tai matkustusehdotuksen, mutta kulu merkitään kaikille hyväksyjille ja         
  myöhempää raportointia varten.        

- **Virhe**: Vaatii työntekijää tarkistamaan, että kulu noudattaa käytäntöä, ennen kuin kuluraportti tai matkustusehdotus lähetetään.        
 
 - **Peruste**: Vaatii työntekijää tai esimiestä antamaan perustelun käytäntösumman ylittämiselle ennen kuluraportin tai matkustusehdotuksen lähettämistä.        

## <a name="policy-tips"></a>Käytäntöä koskevat vihjeet
Seuraavassa kerrotaan muutamia ehdotuksia, jotka voivat auttaa kulujen hallinnan uusien käytäntöjen luomisessa: 

- Käytännöt ovat voimassa tiettynä ajankohtana. Se tarkoittaa sitä, että käytäntö ei ole voimassa, jos se on luotu kulun tapahtumisen jälkeen. Voit esimerkiksi luoda uuden käytännön, jonka mukaan suurin mahdollinen ateriakulu on 50 dollaria. Aiemmin syötettyjä kuluja ei tarkisteta tämän käytännön perusteella.
- Kun eriteltävälle kululuokalle luodaan käytäntö, voit lisätä kulurivin tyypille ehdon. Jotkin käytännöt, kuten kuitin vaatiminen, eivät toimi eriteltävien rivien kohdalla. Tässä tilanteessa käytäntö kohdistetaan vain otsikkoriviin tai muihin kuin eriteltyihin riveihin. 
- Kulujen hallintakäytännöt arvioidaan lähde-entiteetin perusteella oletusarvoisesti. Voit määrittää konsernin skenaarioiden käytännön niin, että se arvioidaan sen sijaan kohde-entiteetin (lainaava entiteetti) avulla. Jos haluat suorittaa käytäntöjä kohde-entiteetin avulla, ota käyttöön **Arvioi kulukäytäntö lainaaavan yrityksen entiteetin avulla** -ominaisuus **Ominaisuuksien hallinta** -työtilassa.

## <a name="when-to-evaluate-policies"></a>Käytäntöjen arvioimisajankohta

Voit valita kulujen hallinnan parametreissa kulujen hallintakäytäntöjen arvioimisen, kun rivi on tallennettu tai kun kuluraportti on lähetetty. Jos haluat tehdä arvioinnin rivin tallennuksen yhteydessä, käyttäjät näkevät suoritettavat toiminnot aiemmin ja voivat viimeistellä kuluraportin kerralla. Muussa tapauksessa voit viivästyttää käytännön arviointia ja säästää aikaa suorittamalla tarkistuksen lopussa työnkulun lähettämisen aikana.
