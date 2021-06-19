---
title: Käteisennakko
description: Tässä aiheessa on tietoja käteisennakoista.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c610fdda8f337e0c16fe5010770aca678201c328
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002142"
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

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Kuluihin kohdistuvien käteisennakkojen valinta
Ennen kuluraportin lähettämistä voit valita käteisennakon, joka kohdistuu raportin kulutapahtumiin. Tätä toimintoa varten on otettava käyttöön seuraavat kaksi ominaisuutta **Ominaisuuksien hallinta** -työtilassa:

  - Uudistetut kuluraportit
  - Mahdollisuus yhdistää käteisennakkoja kuluriveille
 
 Kun nämä ominaisuudet on otettu käyttöön:
 
  - Kutakin kuluriviä varten voidaan lisätä yksi tai useampia käteisennakoita.
  - Käteisennakon käytettävissä oleva summa näkyy reaaliaikaisesti, kun kuluraportti tallennetaan. Näin voit käsitellä kulutapahtumia ja palautuksen käteistapahtumia samanaikaisesti.
  - Yhtä kulutapahtumaa varten voidaan valita yksi tai useampia käteisennakoita.
  - Käteisennakon täsmäytystiedot ovat käytettävissä kyselyn avulla. 
 
Jos et käytä näitä ominaisuuksia, toiminnot säilyvät samoina siten, että aiemmin luodut käteisennakot vähennetään automaattisesti kulun lähetyksen jälkeen.

### <a name="example"></a>Esimerkiksi 
Aiot matkustaa Seattlesta New York Cityyn konferenssia varten. Luot 3 000,00 USD:n käteisennakkopyynnön konferenssilipun, hotellin, aterioiden ja taksin arvioitujen kustannusten perusteella. Sinulle ei makseta, ellei esimiehesi hyväksy tätä pyyntöä. Kun esimies on hyväksynyt pyynnön, käteisennakko 3 000,00 USD maksetaan pankkitilillesi. Sen jälkeen osallistut konferenssiin. Kun olet suorittanut matkasi, huomaat, että kokonaiskulut olivat vain 2 790,00 USD. Valitse **Käteinen** **Maksutapa**-kentässä ja lähetä kulut 2 790,00 USD. Lähetetty kulusumma oikaistaan automaattisesti sinulle lainattua 3 000,00 USD käteisennakkoa vastaan. Nyt olet velkaa 210,00 USD (3 000,00 - 2 790,00), jonka voit palauttaa yritykselle käyttämällä **Käteisen palautus** -kululuokkaa.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
