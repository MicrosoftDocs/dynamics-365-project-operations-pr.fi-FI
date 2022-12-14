---
title: Projektisopimusrivin laskutettavien komponenttien määrittäminen
description: Tässä artikkelissa on tietoja laskutettavan osan lisäämisestä Project Operationsin sopimusriveille.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 33296c93964cc88499e7a98d499b99463e59d62a
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825560"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Projektisopimusrivin laskutettavien komponenttien määrittäminen

_**Koskee:** Lite-käyttöönotto - kaupasta proformalaskutukseen, Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita_

Projektin sopimusriviin on *sisällytetty* komponentteja ja *laskutettavia* osia.

Sisältyvät komponentit ovat komponentteja, joihin liittyy:

  - Laskutustapa ja asiakasjako
  - Ei-ylitettävät rajoitukset 
  - Projektipohjaisella sopimusrivillä määritetyt laskun toistumisasetukset

Sisällytettyjen komponenttien alijoukko voidaan merkitä laskutettaviksi **laskutustyyppi**-kentän avulla. **Laskutustyyppi**-kenttä on asetusjoukko, joka sallii seuraavat arvot sopimusrivin kontekstissa:

  - Veloitettava
  - Ei veloitettava

Laskutettavat komponentit voidaan määrittää tehtäville, rooleille ja tapahtumaluokille.

Maksukyky määritetään projektisopimusrivin tehtäville, ja se koskee kaikkia riviin sisältyviä tapahtumaluokkia. Jos sopimusrivin **Sisällytä tehtävät** -kenttä on tyhjä tai sen asetus on **Koko projekti**, **Veloitettavat tehtävät** -välilehti ei ole käytettävissä.

Projektisopimusrivin rooleihin määritetty maksuvalmius koskee vain **ajan** tapahtumaluokkaa. Jos sopimusrivin **Sisällytä aika** -kentän sen asetus on **Ei**, **veloitettavat roolit** -välilehti ei ole käytettävissä.

Projektisopimusrivin tapahtumakategorioihin määritetty maksuvalmius koskee vain **Kulu** tapahtumaluokkaa. Jos **Sisällytä kulut** -kentän sen asetus on **Ei**, **Veloitettavat kategoriat** -välilehti ei ole käytettävissä.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Projektitehtävän päivittäminen laskutettavana tai ei-laskutettavana

Projektitehtävä voi olla laskutettava tai ei-laskutettava tietyllä sopimusrivillä, joten seuraavat asetukset ovat mahdollisia:

Jos projektiin perustuva sopimusrivi sisältää **Aikaa** ja tietyn tehtävän, **T1** liitetään siihen laskutettavana. Jos on olemassa toinen sopimusrivi, joka sisältää **Kulun**, voit liittää T1-tehtävän sopimusriviin ei-laskutettavana. Tuloksena on se, että kaikki tehtävään kirjatut ajat ovat veloitettavissa ja kaikki kulut eivät ole laskutettavia.

Tehtävän laskutustyyppi voidaan määrittää sopimusrivin **Veloitettavat tehtävät** -välilehdessä päivittämällä **Laskutustyyppi**-kenttä sopimusrivin tehtävien aliruudukossa. Vaihtoehtoisesti **Laskutustyyppi**-kenttä voidaan päivittää sen projektin tehtävän laskutusasetusten aliruudukossa, joka näyttää tehtävään liitetyt sopimusrivit.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Roolin päivittäminen laskutettavana tai ei-laskutettavana

Tietyn sopimusrivin rooli voi olla laskutettava tai ei-laskutettava.

Roolin laskutustyyppi voidaan määrittää sopimusrivin **laskutettavat roolit** -välilehdessä. Se tehdään päivittämällä **Laskutustyyppi**-kenttä **Veloitettavat roolit** -aliruudukossa.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Tapahtumaluokan päivittäminen laskutettavana tai ei-laskutettavana

Tietyn sopimusrivin tapahtumaluokka voi olla laskutettava tai ei-laskutettava.

Tapahtuman laskutustyyppi voidaan määrittää projektipohjaisen sopimusrivin **laskutettavat luokat** -välilehdessä. Se tehdään päivittämällä **Laskutustyyppi**-kenttä **Veloitettavat luokat** -aliruudukossa.

### <a name="resolve-chargeability"></a>Selvitä verosaatavan syntyminen

Aikaa varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos:

   - **Aika** sisältyy sopimusriviin.
   - **Rooli** on määritetty laskutettavaksi sopimusrivillä.
   - **Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** sopimusrivillä.
 
 Jos nämä kolme asiaa ovat tosia, tehtävä määritetään laskutettavaksi. 

Kulua varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos:

   - **Kulu** sisältyy sopimusriviin
   - **Tapahtumaluokka** on määritetty laskutettavaksi sopimusrivillä
   - **Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** sopimusrivillä
  
 Jos nämä kolme asiaa ovat tosia, **Tehtävä** määritetään laskutettavaksi. 

Materiaaleja varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos:

   - **Materiaalit** sisältyy sopimusriviin
   - **Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** sopimusrivillä

Jos nämä kaksi asiaa ovat tosia, **Tehtävä** määritetään laskutettavaksi. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Sisältää ajan</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Sisältää kulun</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Sisältää materiaalit</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Sisällytettävät tehtävät</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Rooli</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Luokka</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tehtävä</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Laskutettavuusvaikutus</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="78" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="63" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="75" valign="top">
                <p>
Koko projekti </p>
            </td>
            <td width="65" valign="top">
                <p>
Veloitettava </p>
            </td>
            <td width="70" valign="top">
                <p>
Veloitettava </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei voida määrittää </p>
            </td>
            <td width="350" valign="top">
                <p>
Laskutus ajan toteutuneella arvolla: <strong>Laskutettava</strong>
                </p>
                <p>
Laskutustyyppi kulun toteutuneella arvolla: <strong>Laskutettava</strong>
                </p>
                <p>
Laskutustyyppi materiaalin toteutuneella arvolla: <strong>Laskutettava</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="78" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="63" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="75" valign="top">
                <p>
Vain valitut tehtävät </p>
            </td>
            <td width="65" valign="top">
                <p>
Veloitettava </p>
            </td>
            <td width="70" valign="top">
                <p>
Veloitettava </p>
            </td>
            <td width="65" valign="top">
                <p>
Veloitettava </p>
            </td>
            <td width="350" valign="top">
                <p>
Laskutus ajan toteutuneella arvolla: <strong>Laskutettava</strong>
                </p>
                <p>
Laskutustyyppi kulun toteutuneella arvolla: <strong>Laskutettava</strong>
                </p>
                <p>
Laskutustyyppi materiaalin toteutuneella arvolla: <strong>Laskutettava</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="78" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="63" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="75" valign="top">
                <p>
Vain valitut tehtävät </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ei-laskutettava</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Veloitettava </p>
            </td>
            <td width="65" valign="top">
                <p>
Veloitettava </p>
            </td>
            <td width="350" valign="top">
                <p>
Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </p>
                <p>
Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava </p>
                <p>
Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="78" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="63" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="75" valign="top">
                <p>
Vain valitut tehtävät </p>
            </td>
            <td width="65" valign="top">
                <p>
Veloitettava </p>
            </td>
            <td width="70" valign="top">
                <p>
Veloitettava </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ei-laskutettava</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </p>
                <p>
Laskutustyyppi kulujen toteutuneista arvoista: <strong>Ei-laskutettava</strong>
                </p>
                <p>
Laskutustyyppi materiaalin toteutuneista arvoista: <strong>Ei-laskutettava</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="78" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="63" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="75" valign="top">
                <p>
Vain valitut tehtävät </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ei-laskutettava</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Veloitettava </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ei-laskutettava</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </p>
                <p>
Laskutustyyppi kulujen toteutuneista arvoista: <strong>Ei-laskutettava</strong>
                </p>
                <p>
Laskutustyyppi materiaalin toteutuneista arvoista: <strong> Ei-laskutettava</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="78" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="63" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="75" valign="top">
                <p>
Vain valitut tehtävät </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ei-laskutettava</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Ei-laskutettava</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Veloitettava </p>
            </td>
            <td width="350" valign="top">
                <p>
Laskutus toteutuneesta ajasta: <strong>Ei-laskutettava</strong>
                </p>
                <p>
Laskutustyyppi kulujen toteutuneista arvoista: <strong> Ei-laskutettava</strong>
                </p>
                <p>
Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="63" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="75" valign="top">
                <p>
Koko projekti </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei voida määrittää </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Veloitettava</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei voida määrittää </p>
            </td>
            <td width="350" valign="top">
                <p>
Laskutus ajan toteutuneesta arvosta: <strong>Ei saatavilla</strong>
                </p>
                <p>
Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava </p>
                <p>
Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="63" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="75" valign="top">
                <p>
Koko projekti </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei voida määrittää </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Ei-laskutettava</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei voida määrittää </p>
            </td>
            <td width="350" valign="top">
                <p>
Laskutus ajan toteutuneesta arvosta: <strong>Ei saatavilla</strong>
                </p>
                <p>
Laskutustyyppi kulujen toteutuneista arvoista: <strong> Ei-laskutettava</strong>
                </p>
                <p>
Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="75" valign="top">
                <p>
Koko projekti </p>
            </td>
            <td width="65" valign="top">
                <p>
Veloitettava </p>
            </td>
            <td width="70" valign="top">
                <p>
Ei voida määrittää </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei voida määrittää </p>
            </td>
            <td width="350" valign="top">
                <p>
Laskutus toteutuneesta ajasta: Laskutettava </p>
                <p>
Laskutustyyppi kulujen toteutuneista arvoista:<strong> Ei saatavilla</strong>
                </p>
                <p>
Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="75" valign="top">
                <p>
Koko projekti </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ei-laskutettava</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Ei voida määrittää </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei voida määrittää </p>
            </td>
            <td width="350" valign="top">
                <p>
Laskutus ajan toteutuneesta arvosta: <strong>Ei-laskutettava </strong>
                </p>
                <p>
Laskutustyyppi kulujen toteutuneista arvoista:<strong> Ei saatavilla</strong>
                </p>
                <p>
Laskutustyyppi materiaalin toteutuneella arvolla: Laskutettava </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="78" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Koko projekti </p>
            </td>
            <td width="65" valign="top">
                <p>
Veloitettava </p>
            </td>
            <td width="70" valign="top">
                <p>
Veloitettava </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei voida määrittää </p>
            </td>
            <td width="350" valign="top">
                <p>
Laskutus toteutuneesta ajasta: Laskutettava </p>
                <p>
Laskutustyyppi tosiasiallisista kustannuksista: Laskutettava </p>
                <p>
Laskutustyyppi materiaalin toteutuneista arvoista: <strong> Ei saatavilla</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="78" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Koko projekti </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ei-laskutettava</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Ei veloitettava</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei voida määrittää </p>
            </td>
            <td width="350" valign="top">
                <p>
Laskutus ajan toteutuneesta arvosta: <strong>Ei-laskutettava </strong>
                </p>
                <p>
Laskutustyyppi kulujen toteutuneista arvoista:<strong> Ei-laskutettava </strong>
                </p>
                <p>
Laskutustyyppi materiaalin toteutuneista arvoista:<strong> Ei saatavilla</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
