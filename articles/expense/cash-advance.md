---
title: Käteisennakko
description: Tässä aiheessa on tietoja käteisennakoista.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c5839fbdab58903555936324139b76f4c94b6c35
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122745"
---
# <a name="cash-advance"></a>Käteisennakko

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Käteisennakko mahdollistaa sen, että työntekijät voivat lainata rahaa yritykseltä ennen kulujen kerryttämistä. Kun pyydetty käteisennakko on hyväksytty ja maksettu, työntekijä voi käyttää rahaa niihin liiketoimintakuluihin, joita he saattavat aiheuttaa. 

## <a name="create-and-submit-a-cash-advance-request"></a>Käteisennakkopyynnön luominen ja lähettäminen

1. Valitse **Omat kulut** -kohdassa **Käteisennakot** > **Uusi**, kun haluat luoda uuden käteisennakon. 
2. Kirjoita **Uusi käteisennakkopyyntö** -sivulla kulun tarkoitus ja valitse sitten sijainti, josta kulu syntyy.
3. Kirjoita pyydetty summa ja valuutta ja valitse sitten **Tallenna**. 
4. Kun olet valmis lähettämään käteisennakkopyynnön, valitse **Käteisennakkopyyntö**  sivulla **Työnkulku** > **Lähetä**.

## <a name="modify-a-cash-advance-request"></a>Käteisennakkopyynnön muokkaaminen

Voit muokata käteisennakkopyyntöä, jos sitä ei ole lähetetty hyväksyttäväksi.

1. Etsi ja valitsekäteis ennakko, jota haluat muokata kohdassa **Omat kulut: käteisennakot**.
2. Valitse **Muokkaa** ja tee käteisennakkopyyntöön tarvittavat muutokset. 
3. Valitse **Tallenna ja sulje**.


## <a name="view-cash-advance-requests"></a>Näytä käteisennakkopyynnöt
Voit tarkistaa kaikkien luonnos-, lähetetty-, tarkistus- tai maksettu-tilan käteisennakoiden luettelon kohdassa **Omat kulut: käteisennakot**. 

## <a name="approve-cash-advance-requests"></a>Hyväksy käteisennakkopyyntöjä

Työnkulussa hyväksyjiksi määritetyt esimiehet tai käyttäjät voivat hyväksyä heille tarkistettavaksi lähetetyt käteisennakot. 

1. Jos haluat hyväksyä käteisennakon, valitse **Käsittele käteisennakot** -kohdassa **Omat tarkistettavat käteis ennakot**.
2. Valitse käteisennakko, jonka haluat tarkistaa, ja valitse **Hyväksy**.  

## <a name="pay-cash-advances"></a>Käteisennakon maksaminen 
Seuraavan menettelyn suorittaa yleensä kirjanpitäjä tai käyttäjä, jolla on kirjanpito-oikeudet.

1. Jos haluat kirjata hyväksytyt käteisennakot, valitse **Hyväksytyt käteisennakot** ja valitse sitten **Maksa ja siirrä**.  
2. Anna tiedot käteisennakoiden kirjauskansioon ja valitse sitten **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Kuluraportin lähettäminen maksettua käteisennakkoa vastaan 

Kun luot ja lähetät kuluraportin jo vastaanottamasi käteisennakon osalta, kulut oikaistaan automaattisesti kyseistä ennakkomaksua vastaan. Jos käteisennakko on suurempi kuin kuluksi kirjattu summa, saldo on palautettava yritykselle käyttämällä **Palauta käteistä** -kululuokkaa. Jos yrityksen maksama käteisennakko on pienempi kuin kuluksi kirjattu summa, yrityksen on hyvitettävä saldo. 

### <a name="example"></a>Esimerkiksi
Suunnittelet matkustavasi Seattlesta konferensiin New Yorkissa. Voit luoda 3 000,00 USD:n käteisennakkopyynnön, kun olet arvioinut, kuinka paljon kokouslipusta, lennoista, hotellista, aterioista ja taksista kertyy arviolta kuluja. Sinulle ei makseta, ellei esimiehesi hyväksy tätä pyyntöä. Kun esimies on hyväksynyt pyynnön, käteisennakko 3 000,00 USD maksetaan pankkitilillesi. Sen jälkeen osallistut konferenssiin. Kun olet suorittanut matkasi, huomaat, että kokonaiskulut olivat vain 2 790,00 USD. Valitse **Maksutapa** -kentässä **Käteinen** ja lähetä kulut summalle 2 790,00 USD. Lähetetty kulusumma oikaistaan automaattisesti sinulle lainattua 3 000,00 USD käteisennakkoa vastaan. Olet nyt velkaa yritykselle saldon 210,00 USD (3 000,00-2 790,00), jonka voit palauttaa yritykselle käyttämällä **Palauta käteistä** -kululuokkaa. 
