---
title: Kulukäytäntöjen määrittäminen
description: Voit määrittää kulukäytäntöjä, joita työntekijöiden on seurattava kuluraporttien ja matkustusehdotusten syöttämisessä ja lähettämisessä Microsoft Dynamics 365 Financessa.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075495"
---
# <a name="set-up-expense-policies"></a>Kulukäytäntöjen määrittäminen

[!include [banner](../includes/banner.md)]

Voit määrittää kulukäytäntöjä, joita työntekijöiden on noudatettava kuluraporttien ja matkustusehdotusten syöttämisessä ja lähettämisessä.         
Kulukäytäntöjen käyttäminen voi olla avuksi kulujen tehokkaassa hallinnassa.         

Voit määrittää esimerkiksi New Yorkin hotellikuluille käytännön, jonka mukaan yökohtainen kulu saa olla enintään 250 dollaria.       
Jos työntekijä lähettää kuluraportin tai matkustusehdotuksen, jossa huoneen hinta ylitää tämän summan, järjestelmä ilmoittaa        
työntekijälle, että kulun summa ylittää käytännön määrittämän summan. Voit määrittää viestin, jonka työntekijä saa, kun        
määrität käytännön.      
        
Voit määrittää seuraavia kolmentyyppisiä käytäntöjä:         
        
- Varoitus – Antaa työntekijälle mahdollisuuden lähettää kuluraportin tai matkustusehdotuksen, mutta kulu merkitään kaikille hyväksyjille ja        
  myöhempää raportointia varten.        

- Virhe – Vaatii työntekijää tarkistamaan, että kulu noudattaa käytäntöä, ennen kuin kuluraportti tai matkustusehdotus lähetetään.       
 
 - Peruste – Vaatii työntekijää tai esimiestä antamaan perustelun käytäntösumman ylittämiselle ennen kuluraportin tai matkustusehdotuksen lähettämistä.        

## <a name="policy-tips"></a>Käytäntöä koskevat vihjeet
Seuraavassa kerrotaan muutamia ehdotuksia, jotka voivat auttaa kulujen hallinnan uusien käytäntöjen luomisessa. 
* Käytännöt ovat voimassa voimaantulopäivänä, eivätkä ne tule voimaan, jos käytäntö luodaan kulutuspäivän jälkeen. Jos olet esimerkiksi luomassa uutta käytäntöä, jonka mukaan 50 $ on mahdollisimman paljon ateriakuluja, kaikkia eilisestä lähtien määritettyjä kuluja ei voi tarkistaa tästä käytännöstä.
* Kun eriteltävälle kululuokalle luodaan käytäntö, voit lisätä kulurivin tyypille ehdon. Joissakin sellaisissa käytännöissä, kuten kuittauksen vaatiminen, ei ehkä kannata määrittää eriteltyjä rivejä, vaan ne tulisi kohdistaa vain otsikkoriville tai ei-eritellylle riville. 
* Kulujen hallintakäytännöt arvioidaan lähde-entiteetin perusteella oletusarvoisesti. Voit määrittää konsernin skenaarioiden käytännön niin, että se arvioidaan sen sijaan kohde-entiteetin (lainaava entiteetti) avulla. Jos haluat suorittaa käytäntöjä kohde-entiteetin avulla, ota käyttöön Arvioi kulukäytäntö lainaavan yrityksen entiteetin avulla -ominaisuus **Ominaisuuksien hallinta** -työtilassa.

## <a name="when-to-evaluate-policies"></a>Käytäntöjen arvioimisajankohta

Kustannushallintaparametreissa on mahdollisuus joko arvioida kustannusten hallintakäytännöt, kun rivi tallennetaan tai kun kustannusraportti lähetetään. Jos päätät arvioida, kun rivi tallennetaan, se varmistaa, että käyttäjillä on aikaisempi näkyvyys siitä, mitä heidän on tehtävä, jotta kuluraportti voidaan täydentää kerralla. Muussa tapauksessa voit viivästyttää käytännön arviointia ja säästää aikaa suorittamalla tarkistuksen lopussa työnkulun lähettämisen aikana.
