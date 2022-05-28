---
title: Projektin palvelusopimuksen vahvistaminen
description: Tämä aihe tarjoaa tietoja sopimuksen vahvistamisesta Project Operationsissa.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f5dab041bab1268235ed542f06d1b4b4cd240305
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599312"
---
# <a name="confirm-a-project-contract"></a>Projektin palvelusopimuksen vahvistaminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operationsissa oleva projektisopimus voi olla aktiivinen syyllä **Vahvistettu** tai suljettu syyllä **Hävitty**. Kun vahvistat projektisopimuksen, tila päivittyy **luonnoksesta** **aktiiviseksi** ja tilan syy **vahvistetaan**. Aktiivista tai suljettua palvelusopimusta ei voi muokata eikä avata uudelleen. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Projektisopimuksen vahvistamisen taloudellinen vaikutus

Kun projektisopimus on vahvistettu, sovellus laskee kustannukset uudelleen peruuttaen vanhat toteutuneet kustannukset ja luoden uudelleen uudet toteutuneet kustannukset. Uudet kustannuslaskelmat käsitellään sitten liittyvän projektisopimusrivin laskutustavan perusteella. Jos todelliset kustannukset viittaavat aika- ja materiaalisopimusriviin, sovellus luo automaattisesti uudelleen vastaavat laskuttamattomat toteutuneet myynnit. Jos kustannusten todelliset tiedot viittaavat kiinteään hintasopimusriviin, sovellus lopettaa kustannusten uudelleenkäsittelyn.

Arvot, joita ei voida ylittää, sekä toteutuneiden hintojen ja kustannuslaskennan arvot arvioidaan ja päivitetään sitten osana vahvistuksia.

## <a name="close-a-project-contract-as-lost"></a>Palvelusopimuksen sulkeminen hävittynä

Kun suljet projektisopimuksen hävittynä, palvelusopimuksen tilaksi päivittyy **Suljettu** ja tilan syyksi **Hävitty**. Projektisopimus muuttuu vain luku -tilaan. Vahvistusikkuna on käytettävissä, ennen kuin muutokset ovat valmiina, koska suljettua projektisopimusta ei voi avata uudelleen.

Jos menetetty projektisopimus viittaa sen riveillä olevaan projektiin, kyseinen projekti merkitään myös suljetuksi. Kaikki kyseisestä päivästä eteenpäin tehdyt varaukset peruutetaan. Kaikki projektisopimuksen laskuttamattomat myynnin todelliset arvot, joita ei vielä ole laskussa, peruutetaan.

> [!NOTE]
> Projektisopimuksen sulkeminen hävittynä Dynamics 365 Project Operationsissa ei vaikuta siihen liittyvän mahdollisuuden tilaan. Mahdollisuus säilyy avoimena, ja se täytyy sulkea manuaalisesti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]