---
title: Projektiluokkien määrittäminen
description: Tässä aiheessa on tietoja projektiluokkien määrityksestä.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b7adf61a82714a0148d9c8b1d2b2b37fd611c1cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287504"
---
# <a name="configure-project-categories"></a>Projektiluokkien määrittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Project Operations tarjoaa tehokkaat ominaisuudet tuottojen ja kulujen luokittelemiseen projekteissa. Luokat antavat mahdollisuuden raportoida ja analysoida projektitapahtumia sekä edistää kirjauksia pääkirjanpitoon.

Seuraavassa kaaviossa on kuvattu tapahtumaluokkien, jaettujen luokkien ja projektiluokkien väliset vastaavuudet. 

Tapahtumaluokat ovat projektitapahtumien perusryhmittely. Kyseisessä ryhmittelyssä on joukko jaettuja luokkia, jotka voidaan jakaa eri sovelluksissa ja moduuleissa. Tarkemmalla tasolla projektiluokat ovat kaikkein täsmällisimpiä luokkia. Projektiluokat ovat yritys-, moduuli- ja sovelluskohtaisia.

![Tapahtumaluokkien, jaettujen luokkien ja projektiluokkien väliset vastaavuudet](media/project-categories.png)

## <a name="transaction-categories"></a>Tapahtumaluokat

Tapahtumaluokat edustavat projektitapahtumien perusryhmittelyä, eivätkä ne ole yritys- tai tapahtumakohtaisia. Contoso Robotics käyttää esimerkiksi Suunnittelu-, Matka-, Asennus- ja Palvelu -tapahtumaluokkia projektitapahtumien ryhmittelyssä.

Tapahtumaluokat määritetään Project Operations -moduulissa. 
1. Avaa lomake siirtymällä kohtaan **Asetukset** \>**Tapahtumaluokat**. 
2. Voit luoda uuden tapahtumaluokan joko valitsemalla **Uusi** tai valitsemalla **Tuo Excelistä**.

## <a name="shared-categories"></a>Jaetut luokat

Dynamics 365 luokittelee kulut eri sovelluksissa, kuten Dynamics 365 Financessa, Dynamics 365 Supply Chainissa ja Dynamics 365 Project Operationsissa, käyttämällä Jaetut luokat -käsitettä. Kullekin luodulle tapahtumaluokalle Project Operations luo automaattisesti neljä toisiinsa liittyvää jaettua luokkaa: Tunnit, Kulut, Maksut ja Nimike. Voit tarkastella ja muokata jaettuja luokkia siirtymällä kohtaan **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Luokat** \> **Jaetut luokat**.

## <a name="project-categories"></a>Projektiluokat

Projektiluokat edustavat kaikkein tarkimpia luokkamäärityksiä, ja projektin kirjanpitäjän täytyy määrittää ne erikseen ja kullekin yritykselle.

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Luokat** \> **Projektiluokat**.
2. Valitse **Uusi**.
3. Valitse edellisessä osassa luodun jaetun luokan **Luokan tunnus**. Project Operationsin avulla voi käyttää vain niitä jaettuja luokkia, jotka liittyvät tapahtumaluokkiin.
4. Valitse luokan ryhmä.

## <a name="category-groups"></a>Luokaryhmät

Luokkayhmien avulla voidaan jakaa ominaisuuksia, ensisijaisesti kirjausprofiileja, toisiinsa liittyvien projektiluokkien välillä. Kullakin tapahtumatyypillä on oltava vähintään yksi luokkaryhmä, ja kullekin projektiluokalle on määritetty ryhmä.

Project Operationsin kirjausmääritykset määräytyvät projektin kustannus- ja tuottoprofiilin sääntöjen, projektiluokkien ja luokkaryhmien mukaan. Voit määrittää luokkaryhmiä siirtymällä kohtaan **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Luokat** \> **Luokkaryhmät**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]