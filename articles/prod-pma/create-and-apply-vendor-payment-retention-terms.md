---
title: Toimittajan maksun pidätysehtojen luominen ja käyttäminen
description: Tässä aiheessa on tietoja toimittajamaksujen säilytysehtojen määrittämisestä ja ylläpidosta.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075485"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Toimittajan maksun pidätysehtojen luominen ja käyttäminen

[!include [banner](../includes/banner.md)] 

Toimittajamaksun pidätysehtojen määrittäminen projektille on hyödyllistä silloin, kun organisaatio haluaa säilyttää osan toimittajalle tehdyistä maksuista. Jos esimerkiksi haluat pidättää maksun toimittajalle, kunnes toimitetut tuotteet vastaavat odotuksiasi. Toimittajan maksun säilytysehdot voidaan määrittää, kun neuvotellaan toimittajasopimuksesta.

## <a name="create-vendor-payment-retention-terms"></a>Toimittajan maksun pidätysehtojen luominen

Voit syöttää toimittajan maksun prosenttiosuuden pidätyksestä ja prosenttiosuuden aiemmin pidätetyistä vapautettavista summista. Summat säilytetään automaattisesti toimittajan laskuissa, kunnes palvelusopimus saavuttaa määritetyn valmistumisasteen. Kun olet määrittänyt säilytysehdot, voit kohdistaa ne mihin tahansa kyseisen toimittajan projektiin.

Seuraavien vaiheiden avulla voit määrittää ja ylläpitää toimittajan maksujen säilytysehtoja. 

1. Siirry kohtaan **projektinhallinta ja kirjanpito** > **säilyttäminen** > **Toimittajamaksujen säilytysehdot**.
2. Valitse **Uusi** , jos haluat lisätä uuden toimittajan säilytysehdon. Uuden termin **sääntötunnus** -arvo syötetään automaattisesti. 
3. Kirjoita lyhyt kuvaus **kuvaus** -kenttään ja valitse **ehdot** -pikavälilehdessä **Lisää rivi** , jos haluat määrittää termin arvot seuraaville:

   - **Toimitettujen yksiköiden prosenttimäärä** : Kirjoita termin valmistumisprosentti. Summat säilytetään automaattisesti toimittajan laskuissa, kunnes projektin valmistumisvaihe on sama kuin määritetty prosenttiosuus. Jos esimerkiksi kirjoitat 50,00, summat pidätetään, kunnes projektista on 50 prosenttia valmiina.
   - **Pidätettävä prosentti** : Anna toimittajan laskun määrän pidätettävä prosenttiosuus. Jos esimerkiksi kirjoitat 10,00, 10 prosenttia toimittajan laskusta pidätetään, kunnes projektin valmistumisprosentti on sama kuin määritetty **toimitetut yksiköt prosentteina -kentässä**.
   - **Vapautettava prosentti** : Valitse **Lisää rivi** , jos haluat määrittää, kuinka monta prosenttia aiemmin kertyneistä summista vapautetaan valitun projektin valmistumisasteen mukaan.

> [!NOTE]
> Jos projektin valmistumisen eri tasoilla on useampi kuin yksi välitavoite, kirjoita kullekin säilytyssäännölle erillinen toimittajan säilytysajan rivi. Kullakin rivillä voidaan määrittää eri säilytysprosentti ja eri vapautusprosentti kullekin projektin valmistumistasolle.

Kun olet luonut toimittajan pidätysehdot, voit kohdistaa ehdot projektiin.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Toimittajan säilytysehtojen soveltaminen projektiin

1. Siirry kohtaan **projektinhallinta- ja kirjanpito** > **projektit** > **kaikki projektit** ja avaa projekti projektiluettelo-sivulla.
2. Valitse **toimittajasopimukset** -pikavälilehdessä **Lisää rivi**.
3. Valitse **tilikoodikentässä** jokin seuraavista vaihtoehdoista: 

   - **Taulukko** : toimittajan säilytysehdot koskevat yhtä toimittajaa.
   - **Ryhmä** : toimittajan säilytysehdot koskevat kaikkia toimittajaryhmän toimittajia.
   - **Kaikki** : Toimittajan säilytysehdot koskevat kaikkia toimittajia.

4. Valitse **toimittaja/toimittajaryhmä -kentässä** toimittaja tai toimittajaryhmä, johon toimittajan säilytysehtoja sovelletaan. Jos valitsit edellisessä vaiheessa **Kaikki** , tämä kenttä ei ole käytettävissä.
5. **Valitse toimittajan säilytysehdot** -kentässä edellisessä toimintosarjassa luomasi säilytysehdot.
6. Jos projektilla on myös toimittajalle määritetty maksu, kun maksettu (PWP) -ehdot, kirjoita projektin kynnysprosentti **PWP-kynnysprosentti** -kenttään.

Toimittajan säilytysehdot näkyvät myös toimittajalle luotavien ostotilausten yhteydessä.
