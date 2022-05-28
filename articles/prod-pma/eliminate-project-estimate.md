---
title: Projektiarvion poistaminen
description: Tässä aiheessa on tietoja siitä, miten projektiarvion voi poistaa, kun se on valmis.
author: Yowelle
ms.date: 05/26/2020
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
ms.openlocfilehash: 267b5ffab7ef3a6776c31100deea81fb523752b6
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684086"
---
# <a name="eliminate-a-project-estimate"></a>Projektiarvion poistaminen

[!include [banner](../includes/banner.md)]

Projektin arviot tarjoavat taloudellisen näkymän työhön, joka on arvioitu ja aikataulutettu projektille. Projektiin liittyvien arvioiden käsitteleminen edellyttää, että projekti liitetään arviointiprojektiin. Arviointiprojekti perustuu aina aiemmin luotuun projektiin, mutta useat projektit voivat viitata yksittäiseen arviointiprojektiin. Vain kiinteähintaiset ja investointiprojektit voidaan liittää arviointiprojekteihin, ja näiden projektien on kuuluttava samaan projektiryhmään kuin arviointiprojekti.

Jotta arviointiprojekti voidaan poistaa, sen on oltava valmis. Seuraavassa kerrotaan, miten arvio voidaan poistaa.

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kaikki projektit** ja avaa projekti. 
2. Valitse **hallinta**-välilehdessä **arviot** ja valitse sitten **arvio**-sivulla **Poista**.
3. Määritä **yleiset**-välilehden **Poista arvio**-sivulla seuraavat asetukset:

   - **Kausikoodi**: Valitse kausikoodi, jos haluat valita sopivat arviointiprojektit. 
   - **Arviopäivämäärä**: Valitse eliminoinnin arviopäivä.
   - **Eliminoiminen KET-varoituksilla**: Ota tämä asetus käyttöön, jos haluat ilmoittaa, kun keskeneräiseen työhön (KET) liittyvä arvio poistetaan. Kun tämä vaihtoehto ei ole käytössä, eliminointi ei voi jatkua, jos yhtään ei-arvioitua tapahtumaa on olemassa. 
   > [!NOTE]
   > Tämä vaihtoehto on käytettävissä vain, kun eliminointi kohdistetaan arviointiprojektiin. Se ei ole käytettävissä, jos käytät kausittaisia kirjauksia. Tämä asetus toimii **Projektiparametrit**-sivun **arvio**-välilehden asetusten **Salli eliminointi, kun ei-arvioituja tapahtumia on** -kenttäryhmässä.
   - **Aseta vaihe valmiiksi**: Ota tämä asetus käyttöön, kun haluat määrittää arviointiprojektin vaiheen **päättyneeksi**, kun olet suorittanut eliminoinnin.
   - **Tulosta arvioluettelo**: Valitse tiedot, jotka sisällytetään, kun arvioluettelo tulostetaan.
   - **Näytä infoloki**: Ota tämä asetus käyttöön, kun haluat näyttää infolokin.
   - **Kirjauspvm**: Valitse arvion kirjanpidon kirjauspäivä.

4.  Valitse **OK**.
5. Kun eliminointiprosessi on valmis, eliminoitu arviointiprojekti näytetään negatiivisena. 

Jos et aio poistaa arviota, voit valita eliminoidun arvion ja valita **Peruuta eliminointi**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]