---
title: Valuutta
description: Tässä aiheessa on tietoja siitä, miten valuuttatyyppejä lisätään ja poistetaan Project Operationsissa.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0a5ae29f1a11f62c6edfca64c4751338f42a26f24c4f8230018b0b45a4ee2ddb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999582"
---
# <a name="currency"></a>Valuutta

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Valuutat määrittävät tuotteiden hinnat tuoteluettelossa sekä erilaisten tapahtumien, kuten myyntitilausten, kustannukset. Jos asiakkaat ovat jakautuneet eri maantieteellisille alueille, lisää asiakkaiden valuutat, jotta voit hallita tapahtumia. Lisää valuutat, jotka sopivat parhaiten liiketoiminnan nykyisiin ja tuleviin tarpeisiin.  

> [!NOTE]
> Jos ympäristö on Common Data Service, olet Power Platform -hallintakeskuksessa ja valitset **Valuutat**-sivun (**Ympäristöt** > [valitse ympäristö] > **Asetukset** > **Liiketoiminta** > **Valuutat**), sivu on tyhjä. Tämä johtuu siitä, että Common Data Service -ympäristöt eivät tue valuutan määrittämistä.

## <a name="add-a-currency"></a>Valuutan lisääminen  
Ennen kuin aloitat nämä toimet, tarkista, että käyttöoikeusrooli sisältää järjestelmänvalvojan oikeudet. 

1. Valitse ympäristö Power Platform -hallintakeskuksessa. 
2. Valitse **Asetukset** > **Yritys**.
3. Valitse **Valuutat**.  
4. Valitse **Uusi**.  
5. Täytä tarvittavat tiedot.  


   |          Kenttä          |                                                                                                                                                                                                                                                                                                                                                                            Kuvaus                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Valuuttatyyppi**    | - **Järjestelmä** - Valitse tämä vaihtoehto, jos haluat käyttää Dynamics 365:n mallipohjaisissa sovelluksissa käytettävissä olevia valuuttoja. Voit hakea valuuttaa valitsemalla **Valinta**-kohdan. Kun valitset valuuttakoodin, valittuun valuuttaan lisätään automaattisesti **valuutan nimi**- ja **rahayksikön tunnus**.<br />- **Mukautettu** - Valitse tämä vaihtoehto, jos haluat lisätä valuutan, joka ei ole käytettävissä Dynamics 365:n mallipohjaisissa sovelluksissa. Tällöin **Valuuttakoodi**-, **Rahasummien desimaalien määrä**-, **Valuutan nimi**-, **Rahayksikön symboli**- ja **Valuutan muuntaminen** -kohdan arvo on syötettävä manuaalisesti. |
   |    **Valuuttakoodi**    |                                                                                                                                                                                                                                                                                                                                            Valuutan lyhyt muoto. Esimerkiksi **USD**, kun kyseessä on Yhdysvaltojen dollari.                                                                                                                                                                                                                                                                                                                                            |
   | **Rahasummien desimaalien määrä**  |                                                                                                                                                                                  Anna valuutassa käytettävien desimaalien määrä.  Voit lisätä arvon väliltä 0–4. **Huomautus:** Jos olet määrittänyt tarkkuusarvon **Järjestelmäasetukset**-valintaikkunassa, arvo näkyy tässä.                                                                                                                                                                                  |
   |    **Valuutan nimi**    |                                                                                                                                                                                                                                         Jos valitsit valuuttakoodin Dynamics 365:n mallipohjaisissa sovelluksissa käytettävissä olevien valuuttojen luettelosta, valitun koodin valuutan nimi näkyy tässä. Jos valitsit valuuttatyypiksi **Mukautettu**, anna valuutan nimi.                                                                                                                                                                                                                                          |
   |   **Rahayksikön tunnus**   |                                                                                                                                                                                                                                                                      Jos valitsit valuuttakoodin käytettävissä olevien valuuttojen luettelosta, valitun valuutan tunnus näkyy tässä. Jos valitsit valuuttatyypiksi **Mukautettu**, anna uuden valuutan tunnus.                                                                                                                                                                                                                                                                       |
   | **Valuutan muuntaminen** |                                                                                                                                                                                                                                     Anna valitun valuutan arvo suhteessa yhteen Yhdysvaltojen dollariin. Tämä on summa, jossa valittu valuutta muunnetaan perusvaluutaksi. **Tärkeää:** Varmista, että päivität tämän arvon aina tarvittaessa, jotta tapahtumien laskelmat ovat ajan tasalla.                                                                                                                                                                                                                                      |


6. Kun olet valmis, valitse komentopalkista **Tallenna** tai **Tallenna ja sulje**.  

   > [!TIP]
   >  Voit muokata valuuttaa valitsemalla valuutan ja antamalla tai valitsemalla uudet arvot.  

## <a name="delete-a-currency"></a>Valuutan poistaminen  

1. Valitse ympäristö Power Platform -hallintakeskuksessa. 
2. Valitse **Asetukset** > **Yritys**.
3. Valitse **Valuutat**.  
4. Valitse näytettävästä valuuttaluettelosta poistettava valuutta.  
5. Valitse **Poista**.  
6. Vahvista poisto.  

> [!IMPORTANT]
>  Muiden tietueiden käytössä olevia valuuttoja ei voi poistaa. Vain niiden aktivointi voidaan poistaa. Valuuttatietueiden aktivoinnin poistaminen ei poista nykyisiin tietueisiin, kuten mahdollisuuksiin tai tilauksiin, tallennettuja valuuttatietoja. Et kuitenkaan voi valita uusille tapahtumille valuuttaa, jonka aktivointi on poistettu.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]