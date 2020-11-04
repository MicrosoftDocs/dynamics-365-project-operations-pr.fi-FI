---
title: Resurssin varaaminen alustavasti
description: Tämä aihe sisältää tietoja ryhmän jäsenten alustavasta ajoittamisesta tai varaamisesta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: cb506a519dbc490ecdd579edf1e3fa5dd0153bdb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075473"
---
# <a name="soft-book-a-resource"></a>Resurssin varaaminen alustavasti

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Voit ajoittaa tai varata resurssin alustavasti projektiryhmään, jolloin resurssin projektiin delegoimista koskeva suunnitelma näkyy muille. Alustavat varaukset eivät kuluta resurssin käytettävissä olevaa kapasiteettia. Alustavasti varattuja ryhmän jäseniä voi delegoida projektitehtäville. Koska alustava varaus ei kuluta resurssin kapasiteettia, voit yhä varata resurssin sitovasti muihin saman kauden tehtäviin. Yleisiä resursseja ei voi varata alustavasti, eikä alustava varaus voi täyttää yleistä resurssia koskevaa pyyntöä.

**Projekti** -sivun **Ryhmä** -välilehdessä on alustavasti varattujen ryhmän jäsenten luettelo. Jäsenten alustavasti varatut tunnit näkyvät **Nimetyt resurssit** -näkymän **Alustavasti varatut tunnit** -sarakkeessa. Myös aikataulutaulukossa on alustavasti varattujen ryhmän jäsenten luettelo. Aikataulutaulukossa ei näy näiden resurssien kapasiteetin kulutusta, koska resurssit on varattu alustavasti. Alustavasti varattu aika ei näy **Täsmäytys** -välilehdessä eikä aikataulutaulukon **Täsmäytys** -välilehden **Laajenna varaukset** -kentässä. 

Ryhmän jäsenen voi varata projektiin alustavasti kahdella eri tavalla: suoraan aikataulutaulukosta ja lisäämällä ryhmän jäsen **Ryhmä** -välilehdessä. 

## <a name="soft-book-from-the-schedule-board"></a>Alustava varaus aikataulutaulukosta
Resurssi voidaan varata aikataulutaulukosta alustavasti seuraavalla tavalla. 

1. Avaa aikataulutaulukko ja valitse sitten **Varaustarpeet** -paneelin **Projekti** -välilehti.
2. Etsi projekti, jolle haluat varata resurssin alustavasti. Jos luettelossa on suuri määrä projekteja, valitse **Project** -sarakeyksikkö ja käytä suodatinta yhden tai useamman projektin hakuun.
3. Valitse projekti, vedä se resurssin aikaruudukkoon ja pudota projekti sinne.
5. Muuta alkamis- ja päättymispäivää **Luo resurssivaraus** -paneelissa, määritä **Varauksen tila** arvoon **Alustava** ja määritä sitten tunnit. 
6. Valitse **Varaa**. Resurssi näkyy nyt **Ryhmä** -välilehdessä projektin resurssina. Alustavasti varatut tunnit näkyvät **Nimetty ryhmän jäsen** -näkymän **Alustavasti varatut tunnit** -sarakkeessa.

> [!NOTE]
> Huomaa, että voit nyt delegoida alustavasti varatut resurssit tehtäville **Aikataulut** -välilehdessä. **Täsmäytys** -välilehdessä näkyy resurssin varauksen vaje suhteessa sen tehtävän kohdennukseen, koska **Täsmäytys** -välilehdessä otetaan huomioon vain sitovat varaukset. Voit varata resurssin sitovasti **Laajenna varaukset** -toiminnon avulla, jos haluat välttää sitovien varausten vajauksen resurssien delegoinneissa. Resurssin alustava varaus on peruutettava manuaalisesti **Ylläpidä varauksia** -kohdan avulla.

## <a name="soft-book-on-the-team-tab"></a>ALustava varaus Ryhmä-välilehdessä

Voit lisätä ryhmän jäseniä suoraan **Ryhmä** -välilehdessä. Muuta sen jälkeen heidän varaustensa tila arvosta **Sitova** arvoon **Alustava** **Ylläpidä varauksia** -kohdassa. Kun lisäät ryhmän jäsenen näin, jäsen varataan aina sitovasti, ellet valitse kohdennustavaksi **Ei mitään**.

Voit käyttää tätä tapaa seuraavasti:

1. Napsauta **Projekti** -sivun **Tyhmä** -välilehdessä **Uusi**.
2. Valitse varattava resurssi, rooli ja alkamis- ja päättymispäivät.
3. Valitse kohdistustavaksi jokin seuraavista (tapa ei voi olla **Ei mitään** ):
4. Valitse **Tallenna**. Resurssi näkyy ruudukossa. Resurssin tunnit näkyvät **Sitovasti varatut tunnit** -sarakkeessa.
5. Ylläpidä resurssin varauksia valitsemalla **Ylläpidä varauksia**.
6. Kun aikataulutaulukko avautuu, laajenna resurssia niin, että varaukset näkyvät. Varauksen tilana on nyt **Sitova**.
7. Napsauta varausta hiiren kakkospainikkeella ja valitse **Muuta tilaa** -kohdassa **Alustava varaus** \> **Alustava**. Varauksen tila on nyt **Alustava**.
8. Aikataulutaulukon sulkemisen jälkeen näet, että resurssin tunnit siirretään **Ryhmä** -välilehden ruudukon **Sitovasti varatut tunnit** -sarakkeesta **Alustavasti varatut tunnit** -sarakkeeseen, kun esillä on **Nimetyt ryhmän jäsenet** -näkymä.

> [!NOTE]
> Kun käytät **Ylläpidä varauksia** -toimintoa muuttaaksesi tilan arvosta **Sitova** arvoon **Alustava** , varaat resurssin sitovasti ryhmälle ja kohdennat sitten tehtäviä resurssille, resurssin tehtäväkohdennukset säilyvät. **Täsmäytys** -välilehdessä resurssilla on kuitenkin varauksen vajetta, koska vain sitovat varaukset otetaan huomioon varausten ja kohdennusten täsmäytyksessä. Voit varata resurssin sitovasti **Täsmäytys** -välilehden **Laajenna varaukset** -toiminnon avulla, jos haluat välttää sitovien varausten vajauksen resurssien kohdennuksessa. Resurssin alustava varaus on peruutettava **Ylläpidä varauksia** -kohdan avulla.

Kun olet valmis muuttamaan alustavasti varatun ryhmän jäsenen resurssin sitovasti varatuksi ryhmän jäseneksi, tee seuraavat toiminnot:

1. Laajenna aikataulutaulukossa resurssi niin, että varaukset näkyvät. Varauksen tilana näkyy **Alustava**.
2. Napsauta varausta hiiren kakkospainikkeella ja valitse **Muuta tilaa** -kohdassa **Tee sitova varaus** \> **Sitova**. Varauksen tila on nyt **Sitova**.
3. Kun olet sulkenut aikataulutaulukon, palaa projektiin ja avaa **Ryhmä** -välilehti. Tällöin näet, että resurssin tunnit siirretään **Ryhmä** -välilehden **Alustavasti varatut tunnit** -sarakkeesta **Sitovasti varatut tunnit** -sarakkeeseen, kun esillä on **Nimetyt ryhmän jäsenet** -näkymä. Jos resurssi on kohdennettu tehtäville, **Täsmäytys** -välilehdessä ei enää näy varauksen vajetta, koska varaukset ovat nyt sitovia.

