---
title: Matkalaskun henkilökohtaisten kulujen käsittely
description: Tässä aiheessa on tietoja siitä, miten työntekijöiden työmatkoihin liittyvät henkilökohtaiset kulut voidaan käsitellä.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 5e1162133eec5a85675bf686855d420c50de0eaf045d81c4b417b6fe66ee19fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993147"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>Matkalaskun henkilökohtaisten kulujen käsittely

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Työmatkalla työntekijä saattaa maksaa henkilökohtaisia kuluja yrityksen luottokortilla. Jos henkilökohtaisten kulujen käsittelyä varten ei ole määritetty prosessia, kuluraportin hyväksyntäprosessi voi keskeytyä, kun työntekijä lähettää eritellyn kuluraportin.

Työntekijän henkilökohtaiset kulut voidaan käsitellä kahdella tavalla:

  - **Työntekijän maksama**: organisaatiosi ei maksa henkilökohtaisia kuluja, jotka näkyvät yrityksen luottokorttilaskussa. Työntekijä maksaa kulut suoraan luottokortin toimittajalle. 
  - **Yrityksen maksama**: organisaatio maksaa yrityksen luottokorttilaskun kokonaan ja veloittaa sitten työntekijän tililtä henkilökohtaiset kulut.

Voit valita menetelmän, jota organisaatiosi käyttää **kulun hallinnan parametrit** -sivulla.


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>Ota käyttöön kulujen jakotoiminto, kun henkilökohtaisen summan kentässä on arvo

**Ota käyttöön kulujen jakotoiminto, kun henkilökohtaisen summan kentässä on arvo** -ominaisuus koskee vain kuluraportteja, jotka on hyväksytty käyttämällä rivitason työnkulkua. Raportit hyväksytään kohdasta **Käsittele kuluraportit** > **Minulle liitetyt kuluraportit** > **Avaa kuluraportti**. 

Jos haluat ottaa tämän ominaisuuden käyttöön, avaa **Työtilat** > **Ominaisuuksien hallinta**, valitse **Ota käyttöön kulujen jakotoiminto, kun henkilökohtaisen summan kentässä on arvo** ja valitse sitten **Ota käyttöön nyt**. 

Kun ominaisuus on käytössä, tätä toimintoa käyttävät kulurivit luovat kaksi riviä, kun raportti lähetetään. Nämä kaksi riviä luodaan, jotta hyväksyjä voit hyväksyä ne molemmat erikseen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
