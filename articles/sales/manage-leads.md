---
title: Liidien hallinta
description: Tässä aiheessa on tietoja projektipohjaisten liidien hallinnasta.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a10be42f4ae1ecc8ae5613ed8fdc669304e0ec72
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898617"
---
# <a name="manage-leads"></a>Liidien hallinta

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Projektipohjaisia liidejä voi hallita ja hyväksyä Project Operationsissa. Liidienhallintaprosessi sisältää työpohjaisten liidien luonnin ja liidien hyväksymisen. 

## <a name="project-sales-leads"></a>Projektimyyntiliidit

Avaa **Myynti**-osan vasemmanpuoleisen siirtymisruudun **Liidit**-luettelosivu, jossa voit tarkastella järjestelmän kaikkien liiditietueiden luetteloa. Näkyvissä olevassa liidien luettelossa on työpohjaisia ja muuntyyppisiä liidejä, jotka voidaan luoda, jos käytössäsi on myös Dynamics 365 Sales- tai Dynamics 365 Field Service -sovellus.

Voit luoda suodatetun näkymän, jos haluat nähdä vain projektipohjaiset liidit luomalla suodattimen **Tyyppi**-arvolle. Voit esimerkiksi valita, näytetäänkö vain työpohjaiset liidit.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Uuden liidin luominen projektipohjaiselle sopimukselle

Kun projektipohjainen liidi hyväksytään, luodaan mahdollisuus ja asiakkuus. Projektipohjainen mahdollisuus on myyntiaktiviteettien aloituskohta mahdollisuusvaiheessa. Projektipohjaisilla mahdollisuuksilla on yksilölliset ominaisuudet, joita tarvitaan projektityön myymiseen. Näitä ominaisuuksia ovat seuraavat:

- Aika- ja materiaali- sekä kiinteähintainen laskutustapa
- Useita päivien mukaan voimassaolevia hinnastoja projekteissa kertyneille henkilöstöresursseille, kuluille ja materiaaleille

Jos haluat, että hyväksytty liidi luo mahdollisuuden automaattisesti, määritä **Tyyppi**-määritteeksi **Työperusteinen**, kun luot liidin. Jos valitset toisen tyypin, liidi ei luo projektipohjaista mahdollisuutta, kun se hyväksytään. Jos projektipohjaista mahdollisuutta ei luoda, projektikohtaiset toiminnot eivät ole käytettävissä loppupään myyntiprosesseissa.

Seuraavassa taulukossa on esitetty liidin tärkeitä kenttätietoja ja näiden kenttien vaikutuksia loppupäähän.
 
| **Kenttä** | **Sijainti** | **Relevanssi, tarkoitus ja opastus** | **Loppupään vaikutus** |
| --- | --- | --- | --- |
| Aihe | Yleiset-välilehti | Tässä tekstikentässä on oltava lyhyt kuvaus sopimuksesta. | Liidin aiheen oletusarvo on mahdollisuuden aihe sekä tarjouksen ja projektisopimuksen nimi. |
| Laji | Yleiset-välilehti | Tässä asetusjoukkokentässä on seuraavat vaihtoehdot:</br>– Työperusteinen (käytettävissä vain, kun Project Operations on asennettu)</br>– Nimikepohjainen (käytettävissä vain, kun Project Operations ja Sales on asennettu)</br>– Palvelun ylläpitoon perustuva (käytettävissä, kun Field Service on asennettu) | Kun tämän kentän arvoksi määritetään liidissä **Työperusteinen**, liidi hyväksytään, jotta luodaan projektipohjainen mahdollisuus. Projektiin perustuva mahdollisuus tarvitaan, jotta kaikki projektikohtaiset laajennukset ja toiminnot voidaan ottaa käyttöön tämän sopimuksen loppupään myyntiprosessissa. |
| Etunimi | Yleiset-välilehti | Prospektin yhteyshenkilön etunimi | Kun liidi hyväksytään, luodaan asiakkuus, yhteyshenkilö ja mahdollisuus. Yhteyshenkilön etunimi on tässä määritetty arvo. |
| Sukunimi | Yleiset-välilehti | Prospektin yhteyshenkilön sukunimi | Kun liidi hyväksytään, luodaan asiakkuus, yhteyshenkilö ja mahdollisuus. Yhteyshenkilön sukunimi on tässä määritetty arvo. |
| Yritys | Yleiset-välilehti | Prospektin asiakkaan yrityksen nimi | Kun liidi hyväksytään, luodaan asiakkuus, yhteyshenkilö ja mahdollisuus. Luodun asiakkuuden nimi on tässä määritetty arvo. |
| Valuutta | Tietovälilehti | Prospektin asiakkaan valuutta | Kun liidi hyväksytään, luodaan asiakkuus, yhteyshenkilö ja mahdollisuus. Luodun asiakkuuden valuutta on tässä määritetty arvo. |

## <a name="qualify-a-new-project-based-lead"></a>Uuden projektipohjaisen liidin hyväksyminen

Liidejä, joiden **Tyyppi**-arvoksi on määritetty **Työperusteinen**, kutsutaan projektipohjaiksi liideiksi. Kun projektipohjainen liidi hyväkstyään, luodaan seuraava:

- Asiakkuus, joka käyttää liidin **Yritys**-kenttää.
- Asiakkaaseen liittyvä yhteyshenkilötietue, joka perustuu liidin **Etunimi**- ja **Sukunimi**-kenttien arvoihin.
- Projektipohjainen mahdollisuudessa **Tyyppi**-kentän arvoksi on määritetty &quot;**Työperusteinen**.

Lisätietoja liidien hyväksymisestä on aiheessa [Liidien hyväksyminen tai muuntaminen](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Liidin hyväksyntä ja yrityksen tiedot 

Kun suoritat Project Operationsia resurssien/ei-varastoitavien skenaarioiden käyttöönottotilassa, kukin asiakas ja mahdollisuus tarvitsevat **Omistava yritys** -kentän määritetyksi. Omistava yritys on organisaatiosi oikeusenkilö, joka omistaa projektin toimituksen. Jokaisella asiakkaalla tai asiakkuudella, jolla on suhdetyyppi Asiakas, on oltava **Omistavan yritys** -kenttään määritettynä yritys, joka tekee sopimuksen ja neuvottelee tämän asiakkaan kanssa. Asiakas voi olla vain yhdessä yrityksessä.

Kun liidi hyväksytään, luotujen asiakas- ja mahdollisuustietueiden **Omistava yritys** -kentän arvoksi on määritetty nykyisen käyttäjän varattavan resurssitietueen yritys.

Jos nykyisen käyttäjän varattavissa oleva resurssitietue on tyhjä, asiakas- ja mahdollisuustietueisiin käytetään oletusarvona käyttäjätietueen **Omistava yritys** -kentän arvoa.

## <a name="business-process-flow-for-project-based-deals"></a>Projektiin perustuvien tarjousten liiketoimintaprosessi

Seuraavat liiketoimintaprosessit ovat tuettuja Project Operationsin projektipohjaisille sopimuksille:

- Liidistä mahdollisuudeksi -liiketoimintaprosessi
- Mahdollisuuden myynti prosessi

Liidistä mahdollisuudeksi -liiketoimintaprosessi tukee seuraavia vaiheita:

| Vaiheen nimi | Yhdistetty entiteetti | Toiminnallisuus |
| --- | --- | --- |
| Hyväksy | Liidi | Hyväksy liidi, jotta luodaan asiakkuus, yhteyshenkilö ja mahdollisuus. |
| Kehitä | Mahdollisuus | Kehitä mahdollisuutta lisäämällä tietoja liittyvistä töistä, keskeisistä sidosryhmistä ja kilpailijoista. |
| Ehdota | Mahdollisuus | Laadi ehdotus ja hanki hyväksyntä sisäiseltä tarkistusryhmältä. |
| Sulje | Mahdollisuus | Kun mahdollisuus voitetaan, sopimus suljetaan. |
