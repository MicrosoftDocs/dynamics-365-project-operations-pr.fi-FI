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
ms.openlocfilehash: c34817181b75b1b0079974f536e4d7b032ae87dd
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181030"
---
# <a name="opportunity-header---lite"></a>Mahdollisuuden otsikko – lite

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