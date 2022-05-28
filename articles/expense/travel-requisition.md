---
title: Matkustusehdotukset
description: Tässä aiheessa on tietoja matkustusehdotuksista.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 45d303d482f6c034cad2c3423c3e505fc62950a4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585650"
---
# <a name="travel-requisitions"></a>Matkustusehdotukset

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Matkustusehdotuksessa on luettelo kuluista, jotka aiheutuvat matkustamisen tarkoituksesta. Matkustusehdotus lähetetään tarkistettavaksi, ja sitä voidaan käyttää kulujen valtuuttamiseen.

Sinun täytyy ehkä lähettää matkaehdotus, ennen kuin sinulle aiheutuu kuluja, jotka veloitetaan organisaatiolta. Tämä vaatimus pätee riippumatta siitä, veloitatko kuluja yrityksen luottokortilta, käytätkö käteisennakon käteistä vai kerrytätkö organisaation korvaamia kuluja omalla käteiselläsi.

Matkaehdotusten ja käytäntöjen avulla voit hallita organisaation kuluja. Jos organisaatiosi esimerkiksi työstää kiinteähintaista projektia, jotka edellyttää matkustamista, projektiryhmän jäsenten matkakulujen on sovittava yhteen projektibudjetin kanssa. Vaatimalla, että matkakulut hyväksytään ennen niiden syntymistä, organisaatio voi auttaa varmistamaan, että projekti säilyy budjetissa.

## <a name="configuration"></a>Määritys 

Matkaehdotukset voidaan määrittää "pakollisiksi" ottamalla käyttöön Matkan valtuutus etukäteen on pakollista -parametrin kulujen hallinnan parametreissa. 

## <a name="create-and-submit-a-travel-requisition"></a>Matkustusehdotuksen luominen ja lähettäminen

1. Siirry kohtaan **Omat kulut: matkustusehdotus** ja valitse **Uusi matkustusehdotus**.
2. Määritä ehdotuksen tarkoitus ja kohde.
3. Kirjoita **Matkan kuvaus** -kenttään mahdolliset lisätiedot. 
4. Luo kulurivinimike kullekin oletetulle kustannukselle, kuten lennoille, aterioille tai auton vuokralle. Sisällytä kullekin kululle arvioitu päivämäärä, arvioitu summa ja valuutta. 
5. Kun olet lisännyt oletetut kulut, valitse **Tallenna**.
6. Kun olet valmis lähettämään matkustusehdotuksen, valitse **Työnkulku** > **Lähetä**.

Voit tarkastella hyväksyttyjä matkustusehdotuksia **Omat kulut: matkustusehdotus** -kohdassa. 

## <a name="view-available-travel-requisitions"></a>Käytettävissä olevien matkaehdotusten tarkasteleminen

Voit tarkastella kaikkia matkustusehdotuksiasi **Omat kulut: matkustusehdotukset** -kohdassa.

## <a name="approve-travel-requisitions"></a>Matkustusehdotusten hyväksyminen

Valitse hyväksyttävä matkustusehdotus ja valitse sitten **Työnkulku** > **Hyväksy**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Kuluraportin lähettäminen käyttäen hyväksyttyä matkaehdotusta

1. Luo uusi kuluraportti ja valitse kuluraportin otsikossa hyväksyttyjen matkaehdotusten luettelosta **Yhdistä matkustusehdotukseen**.
2. **Matkustusehdotuksen summa** -kenttä päivittyy automaattisesti kuluraportin otsikossa.
3. Lisää kaikki matkasta aiheutuneet kulut. Jos **Valtuutettu etukäteen** -kenttä on käytössä, tietyn kululuokan täsmäytetty summa ja valtuutettu summa päivitetään.

> [!NOTE]
> Kun yhdistät kuluraportin hyväksyttyyn matkaehdotukseen, tapahtuman summa ei voi olla suurempi kuin valtuutettu summa. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]