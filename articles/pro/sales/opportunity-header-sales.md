---
title: Mahdollisuuden asetukset – lite
description: Tässä aiheessa on tietoja projektipohjaisista kaupoista ja projektipohjaisista mahdollisuusriveistä.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6631e136572b958ca616d708a5e3c3c2d9f2675c
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663815"
---
# <a name="header-details-for-project-opportunities"></a>Projektimahdollisuuksien otsikkotiedot

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Mahdollisuuden otsikko sisältää yleisiä tietoja projektipohjaisesta sopimuksesta, joka koskee kaikkia projektipohjaisen mahdollisuuden rivejä.

Dynamics 365 Project Operationsin projektipohjaiset mahdollisuudet ovat Dynamics 365 Salesin mahdollisuuksien laajennuksia. Nämä laajennukset sisältävät lisätoimintoja, joita projektipohjaisiin mahdollisuudet edellyttävät. Nämä laajennukset voivat sisältää uusia kenttiä ja valintanauhatoimintoja, jotka ovat käytettävissä projektipohjaisissa mahdollisuuksissa. Jotkin Salesissa käytettävissä olevat kentät, toiminnot tai oletuslogiikka eivät ole käytettävissä Project Operationsissa.

Seuraavassa taulukossa on esitetty projektipohjaisen mahdollisuuden kentät, jotka ovat käytössä vain Project Operationsissa tai joiden toiminnassa on merkittäviä muutoksia verrattuna Salesiin.

| **Kenttä** | **Sijainti** | **Kuvaus** | **Loppupään vaikutus** |
| --- | --- | --- | --- |
| Laji | Yleiset-välilehti (piilotettu) | Tässä asetusjoukkokentässä on seuraavat vaihtoehdot:</br>– Työperusteinen (käytettävissä vain Project Operationsissa)</br>– Nimikepohjainen (käytettävissä vain, kun Project Operations ja Sales on asennettu)</br>– Palvelun ylläpitoon perustuva (käytettävissä, kun Field Service on asennettu) | Kun käytät Project Operations -sovellusta, tämän kentän arvoksi määritetään automaattisesti **Työperusteinen**, joka määrittää mahdollisuuden projektipohjaiseksi. Mahdollisuuden on oltava projektipohjainen, jotta kaikki projektikohtaiset laajennukset ja toiminnot voidaan ottaa käyttöön tämän sopimuksen loppupään myyntiprosessissa. |
| Ota yhteyttä | Yleiset-välilehti | Viittaus asiakkaan ensisijaiseen yhteyshenkilöön tähän sopimukseen liittyen. | |
| Tili | Yleiset-välilehti | Viittaus asiakkaan yritykseen tai asiakastietueeseen. | |
| Asiakaspäällikkö | Yleiset-välilehti | Tämä projektipohjaisen mahdollisuuden asiakaspäällikön nimi. | Asiakkuuspäällikkö vastaa asiakassuhteen hallinnasta koko projektin elinkaaren ajan. Asiakkuuspäällikköön sidotun varattavan resurssin tietueen perusteella sopimusyksikkö on oletusarvo. |
| Sopimusyksikkö | Yleiset-välilehti | Organisaatioyksikkö, joka on vastuussa tähän sopimukseen liittyvän projektin tai liittyvien projektien toimituksesta. | Sopimusyksikkö on sen yrityksen osasto, joka suorittaa projektit, kun sopimus on tehty. Jokaisella sopimusyksiköllä on valuutta, ja tätä valuuttaa käytetään projektin aikana arvioitujen ja todellisten kustannusten raportoimiseen. |

Kaikki muut mahdollisuuden **Yhteenveto**-välilehden kentät ja osat – lisätietoja: [Mahdollisuuksien luominen tai muokkaaminen (Sales ja myyntikeskus)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
