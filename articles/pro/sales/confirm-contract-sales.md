---
title: Projektin palvelusopimuksen vahvistaminen
description: Tässä artikkelissa on tietoja sopimuksen vahvistamisesta Project Operationsissa.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e92dc42c4ff6bdc40c479511c80d3e500df781a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929992"
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