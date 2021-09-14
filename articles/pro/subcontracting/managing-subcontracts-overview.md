---
title: Alihankintasopimusten hallinta Project Operationsissa
description: Tämä aihe tarjoaa yleiskatsauksen alihankintojen hallintaprosessista, joka on tyypillinen projektipohjaisille organisaatioille.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 993edfd064279a970d7c42d5fcefd794e949a931
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323592"
---
# <a name="subcontract-management-in-project-operations"></a>Alihankintasopimusten hallinta Project Operationsissa

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Tämä aihe tarjoaa yleiskatsauksen alihankintojen hallintaprosessista projektipohjaisissa organisaatioissa. Palveluiden alihankinta seuraa yleensä liiketoimintaprosessia, joka on kuvattu seuraavassa kaaviossa.

![Alihankintaprosessin työnkulku](../media/SubcontractingProcessFlow.png)

Seuraavassa luettelossa on alihankintaprosessin vaiheittainen kuvaus.

1. Projektipäällikkö luo alihankintasopimuksen toimittajan kanssa. Alihankintasopimuksessa käytetään oletusarvoisesti toimittajatietueeseen liitettyjä hinnastoja. Toimittajatilin suhdetyyppi on **Toimittaja** tai **Alihankkija**.
2. Projektipäällikkö voi määrittää kaikki ostot alihankkijan rivinimikkeiksi. Alihankkijarivit voivat olla ajan, kulujen tai tuotteiden rivejä. Kukin alihankintarivin tapahtumaluokka määrittää rivin.
3. Toimittajan asiakaspäällikkö ja projektipäällikkö voivat iteroita alihankkijan yli. Hinnoittelua voidaan säätää alihankintasopimukseen liitetyissä ostohinnoissa.
4. Tässä vaiheessa tai myöhemmin prosessin aikana, jos alihankintarivi on määräaikainen, toimittajien asiakkuuspäällikkö liittää toimittajan yhteyshenkilöt kuhunkin alihankintariviin. Tämä liitos antaa tietoja alihankintapäällikölle, joka laatii alihankintasopimusta. Kun toimittaja liitetään alihankintariviin, järjestelmä luo automaattisesti yhteyshenkilöltä varattavissa olevan resurssin, jos varaavaa resurssia ei vielä ole.
5. Kunkin alihankkijarivin laskutustapa voi olla **Kiinteä hinta** tai **Aika ja Materiaali**. Kiinteähintaisia alihankintarivejä varten määritetään välitavoitteeseen perustuva laskuaikataulu.
6.  Kun alihankinta on määritetty ja neuvottelu on valmis, se vahvistetaan. Vahvistettua alihankintaa ei voi muokata, mutta jos muutoksia tapahtuu, alihankinta voidaan "avata uudelleen muokkaamista varten", jolloin tila muuttuu tilasta **Vahvistettu** takaisin tilaan **Luonnos**, ja neuvottelun voi avata uudelleen. 
7.  Kun luot projektiin yleisen ryhmän jäsenen, ryhmän jäsenen voi liittää alihankintariviin. Tämä tarkoittaa sitä, että yleiselle ryhmän jäsenelle on saatava alihankkijakapasiteetti.
8.  Nimetyt ryhmän jäsenet voidaan luoda suoraan projektiin tai luoda varaamalla heidät käyttämällä resurssien aikataulutusta. Jos nimetty projektiryhmän jäsen on sopimustyöntekijä, se voidaan liittää alihankintariviin. Tämä vähentää alihankintarivillä käytössä olevaa kapasiteettia.
9.  Alihankkijaresurssit voivat kirjata aikaa, kuluja ja materiaalin käyttä projekteissa ja projektitehtävissä ja sitten lähettää tiedot hyväksyttäviksi. Sama koskee työntekijöitä. Ajan kirjaamisen yhteydessä sopimustyöntekijä voi valita tietyn alihankinnan tai ja alihankintarivin.
10. Hyväksynnän yhteydessä alihankintojen hyväksymä aika kirjaa projektin toteutuneet kustannukset perustuen sopimustyöntekijän ostohintaan tai hänen rooliinsa projektissa.
11. Toimittajan laskut ja toimittajan laskun rivinimikkeet voidaan tallentaa järjestelmään toimittajaresurssien suorittamista töistä tai toimittajan toimittamista tuotteista. Toimittajan laskurivien on oltava projektikohtaisia ja tapahtumatyypin on oltava aika, kustannus, tuote/materiaali, välitavoite tai palkkio. Vaihtoehtoisesti toimittajan laskurivi voi viitata alihankintariviin.
12. Järjestelmä liittää automaattisesti toimittajan laskuun kaikki toteutuneet kustannukset, jotka vastaavat alihankkijariviä ja projektia. Tämä avustaa kolmisuuntaista vastaavuus- ja tarkistusprosessia.
13. Tämän jälkeen projektipäällikkö voi tarkistaa automaattisesti vastaavat projektin toteutuneet arvot, poistaa tai lisätä muita toteutuneita projektikustannuksia ja suorittaa tarkistusprosessin loppuun.
14. Kun tarkistusprosessi on valmis kaikilla riveillä, toimittajan lasku merkitään tilaan **Valmis maksettavaksi**. Tässä vaiheessa toimittajan lasku ja rivit voidaan siirtää kirjanpidon tai ostovelkojen järjestelmään, jotta maksu voidaan käsitellä toimittajalle. Aiemmin tallennetut projektikustannukset peruutetaan ja toimittajan laskurivin toteutuneet kustannukset kirjataan projektiin.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Määräpohjaiset alihankkijarivit ja työpohjaiset alihankkijarivit

Alihankintarivi voi perustua määrään tai töihin. 

Kun alihankintarivi on **määräpohjainen**, alihankintarivillä ostettavaa aika-, kustannus tai materiaalimäärää voi käyttää missä tahansa projektissa.

Kun alihankintarivi on **työpohjainen**, alihankintarivi yhdistää työmäärään, jota projektisuunnitelmassa edustaa solmu. Alihankintarivin arvo on summa kaikista niistä komponenteista, jotka tarvitaan työn suorittamiseen. Nämä mallinnetaan alihankintarivin tiedoiksi ja ne voivat olla aika-, kustannus- tai materiaalikokoelmia. Työpohjaisessa alihankintarivissä alihankkijarivi myös kuuluu yhteen projektiin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

