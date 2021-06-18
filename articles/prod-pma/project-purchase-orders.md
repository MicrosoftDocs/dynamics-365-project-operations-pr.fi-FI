---
title: Projektin ostotilaukset
description: Tässä artikkelissa on kuvattu eri menetelmiä, joiden avulla voit luoda projektille ostotilauksia. Käytettävä menetelmä riippuu ostotilauksen tarkoituksesta sekä siitä, milloin ostetut nimikkeet käytetään ja veloitetaan projektilta.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c3ce2d0c0fb3cecf22157db5cb37eb744027d0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999352"
---
# <a name="purchase-orders-for-a-project"></a>Projektin ostotilaukset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on kuvattu eri menetelmiä, joiden avulla voit luoda projektille ostotilauksia. Käytettävä menetelmä riippuu ostotilauksen tarkoituksesta sekä siitä, milloin ostetut nimikkeet käytetään ja veloitetaan projektilta.

### <a name="methods-for-creating-a-purchase-order"></a>Ostotilausten luontitavat

Voit luoda ostotilauksen projektinhallinnassa ja kirjanpidossa jollakin seuraavista menetelmistä. Ostotilauksen tarkoitus määrittää, milloin ostotilaus kulutetaan, ja näin ollen, kun nimikkeitä laskutetaan projektilta.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tapa</th>
<th>Tarkoitus</th>
<th>Nimikkeiden kulutus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Uuden ostotilauksen luominen suoraan projektista.</td>
<td>Käytä tätä menetelmää nimikkeiden ostamiseen ulkoiselta toimittajalta projektin kulutusta varten. Voit luoda ostotilauksen kahdella tavalla:
<ul>
<li>Projektista itsestään. Tällöin projekti on jo määritetty ostotilaukselle.</li>
<li>Siirtymällä projektin ostotilaukseen. Sinun täytyy valita sekä toimittaja että projekti, jolle ostotilaus luodaan.</li>
</ul></td>
<td>Nimikkeet kulutetaan, kun toimittajan lasku päivitetään.</td>
</tr>
<tr class="even">
<td>Ostotilauksen luominen myyntitilauksesta.</td>
<td>käytä tätä menetelmää nimikkeiden ostamiseen, kun luot myyntitilauksen projektista.</td>
<td>Nimikkeet kulutetaan, kun myyntitilaus laskutetaan asiakkaalta.</td>
</tr>
<tr class="odd">
<td>Ostotilauksen luominen nimiketarpeesta.</td>
<td>käytä tätä menetelmää nimikkeiden ostamiseen, kun nimiketarpeen projektista.</td>
<td>Nimikkeet kulutetaan, kun nimiketarpeen pakkausluettelo päivitetään.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Kun päivität toimittajan laskun tai pakkausluettelon, järjestelmä pyytää päivittämään nimiketarpeen pakkausluettelon.

Lisätietoja: [Nimikkeiden vastaanotto nimiketarpeeseen perustuvan ostotilauksen perusteella](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]