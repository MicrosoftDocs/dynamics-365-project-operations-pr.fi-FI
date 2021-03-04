---
title: Käteisennakko
description: Tässä aiheessa on tietoja käteisennakoista.
author: suvaidya
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 58864790720824cecad8ce1ff7ff0a335a42cc03
ms.sourcegitcommit: 7aa0b7fb22213d8baa2d69efece9a636d9f62493
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098880"
---
# <a name="cash-advance"></a>Käteisennakko

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Käteisennakko mahdollistaa sen, että työntekijät voivat lainata rahaa yritykseltä ennen kulujen kerryttämistä. Kun pyydetty käteisennakko on hyväksytty ja maksettu, työntekijä voi käyttää rahaa niihin liiketoimintakuluihin, joita he saattavat aiheuttaa. 

## <a name="create-and-submit-a-cash-advance-request"></a>Käteisennakkopyynnön luominen ja lähettäminen
Luo uusi käteisennakko ja lähetä käteisennakkopyyntö seuraavasti: 

1. Valitse **Omat kulut** -kohdassa **Käteisennakot** > **Uusi**. 
2. Kirjoita **Uusi käteisennakkopyyntö** -sivulla kulun tarkoitus ja valitse sitten sijainti, josta kulu syntyy.
3. Kirjoita pyydetty summa ja valuutta ja valitse sitten **Tallenna**. 
4. Kun olet valmis lähettämään käteisennakkopyynnön, valitse **Käteisennakkopyyntö**  sivulla **Työnkulku** > **Lähetä**.

## <a name="modify-a-cash-advance-request"></a>Käteisennakkopyynnön muokkaaminen

Voit muokata käteisennakkopyyntöä, jos sitä ei ole lähetetty hyväksyttäväksi.

1. Etsi **Omat kulut: Käteisennakot** -kohdassa muokattava käteisennakko ja valitse se.
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

Kun luot ja lähetät kuluraportin jo saadusta käteisennakosta, kulut oikaistaan automaattisesti tähän ennakkoon. Jos käteisennakko on suurempi kuin kuluksi kirjattu summa, saldo on palautettava yritykselle käyttämällä **Palauta käteistä** -kululuokkaa. Jos yrityksen maksama käteisennakko on pienempi kuin kuluttamasi summa, yrityksen on maksettava saldo takaisin. 

### <a name="example"></a>Esimerkiksi
Aiot matkustaa Seattlesta New York Cityyn konferenssia varten. Luot 3 000,00 USD:n käteisennakkopyynnön konferenssilipun, hotellin, aterioiden ja taksin arvioitujen kustannusten perusteella. Sinulle ei makseta, ellei esimiehesi hyväksy tätä pyyntöä. Kun esimies on hyväksynyt pyynnön, käteisennakko 3 000,00 USD maksetaan pankkitilillesi. Sen jälkeen osallistut konferenssiin. Kun olet suorittanut matkasi, huomaat, että kokonaiskulut olivat vain 2 790,00 USD. Valitse **Käteinen** **Maksutapa**-kentässä ja lähetä kulut 2 790,00 USD. Lähetetty kulusumma oikaistaan automaattisesti sinulle lainattua 3 000,00 USD käteisennakkoa vastaan. Nyt olet velkaa 210,00 USD (3 000,00 - 2 790,00), jonka voit palauttaa yritykselle käyttämällä **Käteisen palautus** -kululuokkaa.



[!INCLUDE[footer-include](../includes/footer-banner.md)]