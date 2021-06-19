---
title: Matkalaskun henkilökohtaisten kulujen käsittely
description: Tässä aiheessa on tietoja siitä, miten työntekijöiden työmatkoihin liittyvät henkilökohtaiset kulut voidaan käsitellä.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025680"
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
