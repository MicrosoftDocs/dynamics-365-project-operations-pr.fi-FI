---
title: Tarjousrivin laskutettavan komponentin määrittäminen
description: Tässä artikkelissa on tietoja laskutettavan ja ei-laskutettavan komponentin määrittämisestä projektipohjaisella tarjousrivillä.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d4829055f429546c7911a05a765bc28ae085afa1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930038"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Tarjousrivin laskutettavan komponentin määrittäminen 

_**Koskee:** Lite-käyttöönotto - kaupasta proformalaskutukseen, Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita_

Projektipohjaiseen tarjousrivillä on *sisällytettyjen* osien ja *laskutettavien* osien käsitteet.

Sisällytettyjä osia voivat olla seuraavat:

  - Laskutustapa ja asiakasjako
  - Ei-ylitettävät rajoitukset 
  - Projektipohjaisella tarjousrivillä määritetyt laskun toistumisasetukset

Sisällytettyjen komponenttien alijoukko voidaan merkitä laskutettaviksi **laskutustyyppi**-kentän avulla. **Laskutustyyppi**-kenttä on asetusjoukko, joka sallii seuraavat arvot tarjousrivin kontekstissa:

  - Veloitettava
  - Ei veloitettava

Laskutettavat komponentit voidaan määrittää tehtäville, rooleille ja tapahtumaluokille.

Maksukyky määritetään tarjousrivin tehtäville, ja se koskee kaikkia siihen riviin sisältyviä tapahtumaluokkia. Jos sopimusrivin **Sisällytä tehtävät** -kentän asetus on **Koko projekti** tai se on jätetty tyhjäksi, **Veloitettavat tehtävät** -välilehti ei ole käytettävissä.

Laskutettavuus määritetään tarjousrivin rooleissa, ja se koskee vain **Ajan** tapahtumaluokkaa. Jos **Sisällytä aika** -kentän asetus on **Ei** projektitarjousrivillä, **Veloitettavat roolit** -välilehti ei ole käytettävissä.

Veloitettavuus määritetään tarjousrivin tapahtumaluokissa ja koskee vain **Kulu**-tapahtumaluokkaa. Jos **Sisällytä kulut** -kentän asetus on **Ei** projektitarjousrivillä, **Veloitettavat luokat** -välilehti ei ole käytettävissä.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Projektitehtävän päivittäminen laskutettavaksi tai ei-laskutettavaksi

Projektitehtävä voi olla laskutettava tai ei-laskutettava tietyn projektipohjaisen tarjousrivin yhteydessä, mikä mahdollistaa seuraavan asennuksen.

Jos projektiin perustuva tarjousrivi sisältää **Ajan** ja tehtävän **T1**, tehtävä liitetään tarjousriviin laskutettavana. Jos on olemassa toinen tarjousrivi, joka sisältää **Kulut**, voit liittää **T1**-tehtävän tarjousriviin ei-laskutettavana. Tuloksena on, että kaikki tehtävään kirjattu aika on laskutettavaa ja kaikki tehtävään kirjatut kulut ovat ei-laskutettavia.

Tehtävän laskutustyyppi voidaan määrittää projektipohjaisen tarjousrivin **Veloitettavat tehtävät** -välilehdessä päivittämällä **Laskutustyyppi**-kenttä **Tarjousrivin tehtävät** -aliruudukossa. Vaihtoehtoisesti projektitehtävän laskutustyyppi voidaan päivittää sen aliruudukon **Laskutustyyppi**-kentässä, joka on tehtävään liitetyt tarjousrivit näyttävän projektin tehtävän laskutusasetuksissa.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Roolin päivittäminen laskutettavaksi tai ei-laskutettavaksi

Rooli voi olla laskutettava tai ei-laskutettava tietyn projektipohjaisen tarjousrivin kontekstissa.

Roolin laskutustyyppi voidaan määrittää tarjousrivin **Veloitettavat roolit** -välilehdessä päivittämällä **Laskutustyyppi**-kenttä **Veloitettavat roolit** -aliruudukossa.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Päivitä tapahtumaluokka laskutettavaksi tai ei-laskutettavaksi

Tietyn tarjousrivin tapahtumaluokka voi olla laskutettava tai ei-laskutettava.

Tapahtuman laskutustyyppi voidaan määrittää tarjousrivin **Veloitettavat luokat** -välilehdessä päivittämällä **Laskutustyyppi**-kenttä **Veloitettavat luokat** -aliruudukossa.

### <a name="resolve-chargeability"></a>Selvitä verosaatavan syntyminen
Aikaa varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos:

   - **Aika** sisältyy tarjousriviin.
   - **Rooli** on määritetty laskutettavaksi tarjousrivillä.
   - **Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** tarjousrivillä. 

Jos nämä kolme asiaa ovat tosia, **Tehtävä** määritetään myös laskutettavaksi. 

Kulua varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos: 

   - **Kulu** sisältyy tarjousriviin.
   - **Tapahtumaluokka** on määritetty laskutettavaksi tarjousrivillä.
   - **Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** tarjousrivillä.

Jos nämä kolme asiaa ovat tosia, **Tehtävä** määritetään myös laskutettavaksi. 

Materiaalia varten luotu arvio tai todellinen arvo katsotaan laskutettavaksi vain, jos:

   - **Materiaalit** sisältyy tarjousriviin.
   - **Sisältyvät tehtävät** on määritetty **Valituiksi tehtäviksi** tarjousrivillä.

Jos nämä kaksi asiaa ovat tosia, **Tehtävä** tulisi myös määrittää laskutettavaksi. 


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
Ei voi määrittää </p>
            </td>
            <td width="350" valign="top">
                <p>
Laskutus toteutuneesta ajasta: Laskutettava </p>
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
Veloitettava </p>
            </td>
            <td width="350" valign="top">
                <p>
Laskutus toteutuneesta ajasta: Laskutettava </p>
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
Ei voi määrittää </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Veloitettava</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei voi määrittää </p>
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
Ei voi määrittää </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Ei-laskutettava</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei voi määrittää </p>
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
Ei voi määrittää </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei voi määrittää </p>
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
Ei voi määrittää </p>
            </td>
            <td width="65" valign="top">
                <p>
Ei voi määrittää </p>
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
Ei voi määrittää </p>
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
Ei voi määrittää </p>
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
