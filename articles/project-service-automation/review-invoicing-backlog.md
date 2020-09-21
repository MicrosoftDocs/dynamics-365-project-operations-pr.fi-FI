---
title: Laskutusjonon tarkasteleminen projekteissa ja projektisopimuksissa
description: Tässä aiheessa on tietoja ajan, kulujen ja tuotteiden jonojen tarkastelusta sekä siitä, miten ne voidaan merkitä laskutusvalmiiksi.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: db15ea136b9939c0a0631936bcadab538bf2dd4a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751224"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Laskutusjonon tarkasteleminen projekteissa ja projektisopimuksissa

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kun tapahtuma on valmis laskun luomista ja käsittelyä varten, tapahtuma tulisi merkitä **Laskutusvalmiiksi**. Tässä aiheessa kuvataan, minkä tyyppisiä tapahtumia voidaan luoda.

## <a name="review-the-time-and-material-billing-backlog"></a>Tarkastele aika-ja materiaalipohjaisen laskutuksen jonoa

Kun aika- tai kulumerkintä lähetetään ja hyväksytään projektille, PSA luo projektin nykyarvon. Jos projektin ja tapahtumaluokan yhdistelmä on yhdistetty aika- ja materiaaliprojektin sopimu riviin, luodaan kaksi todellista arvoa, kun tapahtuma hyväksytään:

- Kulujen nykyarvo 
- Laskuttamattoman myynnin nykyarvo

Laskuttamattoman myynnin nykyarvot edustavat laskutusjonoa, ja niiden laskutustilaksi on asetettava **Laskutusvalmis**. Projektilaskua luotaessa laskuttamattomat myynnin nykyarvot, jotka on merkitty **Laskutusvalmiiksi** kopioidaan laskurivien tiedoiksi.

Tarkastellaksesi laskutusjonoa aikaa ja materiaaleja varten, siirry kohtaan **Myynti** \> **Laskutus** \> **Ajan ja materiaalien laskutuksen jono**. Valitse kaikki laskuttamattomat myynnin nykyarvot, jotka ovat valmiita laskutettaviksi, ja valitse sitten **Laskutusvalmis**. Näiden nykyarvojen laskutustilaksi vaihtuu **Laskutusvalmis**.

![Ajan ja materiaalien laskutuksen jono](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Tarkastele tuotteiden laskutuksen jonoa

Kun projekti opimuksessa on PSA-järjestelmässä tuotepohjaisia sopimusrivejä, kyseiset rivit katsotaan laskutettaviksi aina, kun projekti opimukselle luodaan lasku. Mikä tahansa tuote, jolla on sopimusrivejä, jotka on merkitty **Laskutusvalmiiksi** kopioidaan projektilaskuun projektilaskun riveiksi.

Jos haluat tarkastella tuotteiden laskutusjonoa, siirry kohtaan**Myynti**\>**Laskutus**\>**Tuotteiden laskutuksen jono**. Valitse kaikki tuotepohjaiset sopimusrivit, jotka ovat valmiita laskutettaviksi, ja valitse sitten **Laskutusvalmis**. Näiden rivien laskutustilaksi vaihtuu **Laskutusvalmis**.

![Tuotteiden laskutuksen jono](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Kiinteähintaisten palvelusopimusten laskutuksen välitavoitteiden tarkasteleminen

Jokaiselle projektisopimusrivin, jolla on kiinteähintainen laskutusmenetelmä, on määritettävä sopimuksen välitavoitteet. Nämä sopimuksen välitavoitteet voidaan laskuttaa vain, jos ne on merkitty **Laskutusvalmiiksi**. 

Voit tarkastella laskutuksen välitavoitteita siirtymällä kohtaan**Myynti**\> **Laskutus**\> **Kiinteän hinnan välitavoitteet**. Valitse kaikki välitavoitteet, jotka ovat valmiita laskutettaviksi, ja valitse sitten **Laskutusvalmis**. Näiden välitavoitteiden laskutustilaksi vaihtuu **Laskutusvalmis**.

![Kiinteän hinnan välitavoitteet](media/FPBacklog.png)
