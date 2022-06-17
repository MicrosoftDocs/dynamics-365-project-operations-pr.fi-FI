---
title: Projektiluokkien määrittäminen
description: Tässä artikkelissa on tietoja projektiluokkien määrityksestä.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 440fc712750c07e8426d54e3a1f994f506879e3c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933580"
---
# <a name="configure-project-categories"></a>Projektiluokkien määrittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Project Operations tarjoaa tehokkaat ominaisuudet tuottojen ja kulujen luokittelemiseen projekteissa. Luokat antavat mahdollisuuden raportoida ja analysoida projektitapahtumia sekä edistää kirjauksia pääkirjanpitoon.

Seuraavassa kaaviossa on kuvattu tapahtumaluokkien, jaettujen luokkien ja projektiluokkien väliset vastaavuudet. 

Tapahtumaluokat ovat projektitapahtumien perusryhmittely. Kyseisessä ryhmittelyssä on joukko jaettuja luokkia, jotka voidaan jakaa eri sovelluksissa ja moduuleissa. Tarkemmalla tasolla projektiluokat ovat kaikkein täsmällisimpiä luokkia. Projektiluokat ovat yritys-, moduuli- ja sovelluskohtaisia.

![Tapahtumaluokkien, jaettujen luokkien ja projektiluokkien väliset vastaavuudet.](media/project-categories.png)

## <a name="transaction-categories"></a>Tapahtumaluokat

Tapahtumaluokat edustavat projektitapahtumien perusryhmittelyä, eivätkä ne ole yritys- tai tapahtumakohtaisia. Contoso Robotics käyttää esimerkiksi Suunnittelu-, Matka-, Asennus- ja Palvelu -tapahtumaluokkia projektitapahtumien ryhmittelyssä.

Tapahtumaluokat määritetään Project Operations -moduulissa. 
1. Avaa lomake siirtymällä kohtaan **Asetukset** \>**Tapahtumaluokat**. 
2. Voit luoda uuden tapahtumaluokan joko valitsemalla **Uusi** tai valitsemalla **Tuo Excelistä**.

## <a name="shared-categories"></a>Jaetut luokat

Dynamics 365 luokittelee kulut Jaetut luokat -käsitteen avulla eri sovelluksiin, kuten Dynamics 365 Financeen, Dynamics 365 Supply Chain Managementiin ja Dynamics 365 Project Operationsiin. Kullekin luodulle tapahtumaluokalle Project Operations luo automaattisesti neljä toisiinsa liittyvää jaettua luokkaa: Tunnit, Kulut, Maksut ja Nimike. Voit tarkastella ja muokata jaettuja luokkia siirtymällä kohtaan **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Luokat** \> **Jaetut luokat**.

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