---
title: Projektibudjettien siirtäminen tilikauden lopussa
description: Tässä artikkelissa annetaan tietoja jäljellä olevien budjettisummien siirtämisestä tuleville vuosille ja budjettirekisteritietojen luomisesta.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5b4e768cb78d6a6cb76b3c338fd76363d5290ebd
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684040"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Projektibudjettien siirtäminen tilikauden lopussa

[!include [banner](../includes/banner.md)]

Kun työskentelet usean vuoden projektissa, tilikausi lopussa voi olla jäljellä oleva budjetti. Voit siirtää jäljellä olevat budjetin summat tulevalle vuodelle ja luoda budjettirekisteritiedot liittyvien kirjanpitotilien summille. Ennen jäljellä olevien summien siirtämistä voit tarkastella ja analysoida jäljellä olevia budjetin summia.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Jäljellä olevien budjettisummien tarkistaminen ja analysoiminen

Tarkista projektien vuoden lopun budjettisummat tekemällä seuraavat toimet, mutta älä siirrä summia eteenpäin.

1. Siirry kohtaan **projektinhallinta ja kirjanpito** > **kausittaiset** > **budjetit** > **Siirrettävät budjetit**. 
2. Tarkista **Projektibudjetin siirtoprosessi** -sivun **vuoden lopun asetukset** -välilehdessä, että **Siirrä jäljellä olevat projektibudjetin summat** ei ole käytössä.
3. Valitse **parametrit**-välilehden **Projektibudjettivuosi**-kentässä tilikausi, jonka jäljellä olevan budjetin summan haluat nähdä. 
4. Valitse **Avaava tilikausi** -kentästä tilivuosi, jolle haluat tarkastella jäljellä olevaa budjettisummaa. 
5. Valitse **mistä ennustemalli** -kentässä **jäljellä oleva budjetti**. 
6. Jos haluat lisätä projekteja, jotka vastaavat valittuja ehtoja ja joilla ei ole jäljellä olevaa budjettia, valitse **Näytä nolla jäljellä**.  
7. Valitse **Valitse budjetit** -välilehdessä **Nouda kaikki budjetit**, jos haluat ladata kaikki valittuja ehtoja vastaavat budjetit, ja valitse sitten **Käsittele**. 
8. Jos haluat suunnitella tietokantakyselyn, joka lataa tietyn budjettijoukon ruutuun, valitse **Nouda valitut budjetit**.

Jos haluat lisätietoja tietystä ruudun rivistä, valitse rivi ja valitse sitten **Näytä budjetin tiedot** tai **Näytä tilit**.

## <a name="carry-forward-remaining-budget-amounts"></a>Siirrä jäljellä olevat budjettisummat 

Kun käsitellään jäljellä olevia budjettisummia, voit luoda pääkirjanpitoon tapahtumia, joita olet tekemässä. Jos haluat luoda kirjanpitotapahtumia, täytä osan vaiheet, [Siirrä budjettisummat ja luo kirjanpitotapahtumat](#carry-forward). 

> [!NOTE]
> Siirretyt budjettisummat siirretään **ennustemallit**-sivussa valittuun ennustemalliin siirrettäväksi ennuste malliksi.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Siirrä budjettisummat ja luo kirjanpitotapahtumat

1.  Valitse **projektinhallinta ja kirjanpito** > **kausittaiset** > **budjetit** > **Siirrettävät budjetit**. 
2. Valitse **projektibudjetin siirtoprosessi** -sivulla **vuoden loppu** ja ota sitten **Siirrä jäljellä olevat projektibudjetin summat** käyttöön ja **Luo budjettirekisterimerkinnät kirjanpitoon**. 
3. Valitse **Parametrit**-välilehdestä **Projektiparametrit**-kenttäryhmä ja valitse seuraava:

   - **Projektibudjettivuosi**: Valitse sen tilivuoden alku, jolle haluat tarkastella jäljellä olevia budjettisummia. 
   - **Voitto ja tappio**: Luo tulostapahtumia pääkirjanpitoon. 
   -  **KET**: Luo keskeneräisten töiden (KET) tapahtumia pääkirjaan.
   -  **Palkanlaskenta**: Palkanlaskennan kohdistustapahtumien luominen pääkirjaan. 

5. Anna **Pääkirjanpito**-kenttäryhmässä seuraavat tiedot: 

   - Valitse **Avaava tilikausi** -kentästä tilikausi, jolle haluat siirtää jäljellä olevat budjettisummat projekteille. Oletusarvo on yksi vuosi **projektin budjettivuosi** -kentän arvon jälkeen.
   -  **Valitse siirrettävä kausi** -kentässä kausi, jolle haluat luoda budjettirekisterin tiedot pääkirjaan. Tämä on yleensä ensimmäinen kausi uudella tilikaudella.

6. Anna **Kopioi kohteesta/kohteeseen**-kenttäryhmässä seuraavat tiedot:

   - Valitse **mistä ennustemalli** -kentässä projektibudjetin ennustemalli, joka liittyy jäljellä oleviin budjettisummiin, jotka haluat siirtää projekteille. 
   - Valitse **Kirjanpidon budjettimalliin** -kentässä kirjanpidonbudjettimalli, joka liittyy jäljellä oleviin budjettisummiin, jotka haluat siirtää kirjanpitoon. 
   -  Valitse **Siirrä myyntivaluutta**, jos haluat käyttää projektin myyntivaluuttaa kirjanpitotapahtumissa, jotka luodaan, kun siirrät projektien budjettisummat. Jos vaihtoehtoa ei ole valittu, tapahtumat käyttävät kirjanpitovaluuttaa. 
   -  Valitse **Näytä nolla jäljellä**, jos haluat lisätä projektit, joilla ei ole jäljellä olevia budjettisummia, mutta jotka täyttävät muut ehdot, jotka valitset alaruudussa näytettävistä projekteista.

7. Valitse **Valitse budjetit** -välilehdessä **Nouda kaikki budjetit**, jos haluat ladata kaikki valittuja ehtoja vastaavat budjetit. Jos haluat mieluummin suunnitella tietokantakyselyn, joka lataa tietyn projektibudjetin ruutuun, valitse **Nouda valitut budjetit**.
8. Jos haluat käsitellä kutakin käsiteltävää projektia, valitse vaihtoehto projektirivin alussa.

    > [!TIP]
    > Jos haluat valita kaikki projektit tai useimmat niistä, valitse vasemmassa yläkulmassa oleva valintaruutu. Jos et halua käsitellä yhtään projektia, poista kyseisen projektin valintamerkki.

9. Jos haluat siirtää valittujen projektien jäljellä olevat budjettisummat valittuun tilikauteen ja luoda budjettirekisterin tiedot pääkirjaan, valitse **prosessi**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Siirrä budjettisummat luomatta kirjanpitotapahtumia

1. Siirry kohtaan **projektinhallinta ja kirjanpito** > **kausittaiset** > **budjetit** > **Siirrettävät budjetit**.
2. Valitse **Projektibudjetin siirtoprosessi** -sivun **vuoden lopun asetukset** -kentässä **Siirrä jäljellä olevat projektibudjetin summat**.
3. Valitse **parametrit**-ryhmän **Projektibudjettivuosi**-kentässä tilikausi, jonka jäljellä olevat budjettisummat haluat nähdä.
4. Anna **Kopioi kohteesta/kohteeseen**-ryhmässä seuraavat tiedot:

   - Valitse **mistä ennustemalli** -kentässä projektibudjetin ennustemalli, joka liittyy jäljellä oleviin budjettisummiin, jotka haluat siirtää projekteille. 
   - Valitse **Näytä nolla jäljellä**, jos haluat sisällyttää hankkeita, joissa ei ole jäljellä olevia budjettisummia, mutta jotka täyttävät muut valitsemasi ehdot.
   - Valitse **Valitse budjetit** -ryhmässä **Nouda kaikki budjetit**, jos haluat ladata kaikki valittuja ehtoja vastaavat budjetit. Jos haluat suunnitella tietokantakyselyn, joka lataa tietyn projektibudjettijoukon ruutuun, valitse **Nouda valitut budjetit**.

5. Jos haluat käsitellä kutakin käsiteltävää projektia, valitse vaihtoehto projektirivin alussa. 
6. Valitse **prosessi**, jos haluat siirtää valittujen projektien jäljellä olevat budjettisummat valittuun tilikauteen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
