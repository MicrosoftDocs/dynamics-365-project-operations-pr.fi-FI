---
title: Proformalaskun vahvistaminen
description: Tässä aiheessa on tietoja proformalaskun vahvistamisesta.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128099"
---
# <a name="confirm-a-proforma-invoice"></a>Proformalaskun vahvistaminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Kun proformalasku on vahvistettu, projektilaskun päivitysten tila on **Vahvistettu**. Kun lasku on vahvistettu, se on vain luku -tilassa. Jatkossa lasku voidaan oikaista vain, jos asiakkaalle on aloitettu korjauksia tai hyvityksiä tai kun se on merkitty maksetuksi.

Seuraavassa taulukossa on lueteltu järjestelmän luomat toteutuneet arvot. Nämä toteutuneet arvot luodaan, kun projektilaskulle tehdään tiettyjä toimintoja ennen sen vahvistamista.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Skenaario</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Vahvistuksen yhteydessä luodut toteutuneet arvot</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Aikatapahtuman laskuttaminen muokkaamatta laskuluonnokseen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskuttamattoman myynnin peruutus tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Laskutettu toteutunut myynti tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Määrän pienentämiseen muokatun aikatapahtuman laskutus.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskuttamattoman myynnin peruutus tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton todellinen myynti, joka on veloitettavissa laskutettujen laskurivien tiedoille, peruutetun myynnin toteutumiselle ja laskutettavalle myynnille.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton tosiasiallinen myynti, josta ei veloiteta jäljellä olevia tunteja ja määrää sen jälkeen, kun vähennetään korjatut luvut muokatun laskurivin yksityiskohdissa, laskutetun myynnin tosiasiallinen palautus ja vastaava laskutettu todellinen myynti.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Määrän lisäämiseen muokatun aikatapahtuman laskutus.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskuttamattoman myynnin peruutus tunnille ja summalle alkuperäisen aikahyväksynnän perusteella.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton todellinen myynti, joka on veloitettavissa laskutettujen laskurivien tiedoille, peruutetun myynnin toteutumiselle ja laskutettavalle myynnille.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Kulutapahtuman laskuttaminen muokkaamatta laskuluonnokseen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskuttamattoman myynnin peruutus määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Laskutettu toteutunut myynti määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Määrän pienentämiseen muokatun kulutapahtuman laskutus.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskuttamattoman myynnin peruutus määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton todellinen myynti, joka on veloitettavissa muokatun laskurivin tiedoissa olevasta määrästä ja summasta, laskuttamattoman tosiasiallisen myynnin palautuksesta ja vastaavan laskutetun myynnin todellisesta arvosta. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton tosiasiallinen myynti, josta ei veloiteta jäljellä olevaa määrää ja summaa sen jälkeen, kun vähennetään korjatut luvut muokatun laskurivin yksityiskohdissa, laskutetun myynnin tosiasiallisesta palautuksesta ja vastaavasta laskutetusta todellisesta myynnistä.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Määrän kasvattamiseen muokatun kulutapahtuman laskutus.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskuttamattoman myynnin peruutus määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton todellinen myynti, joka on veloitettavissa muokatun laskurivin tiedoissa olevasta määrästä ja summasta, muokkaamattoman tosiasiallisen myynnin palautuksesta ja vastaavan laskutetun myynnin todellisesta arvosta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Maksun laskuttaminen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskuttamattoman myynnin peruutus maksusummalle alkuperäisellä kirjauskansion rivillä.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Laskutettu toteutunut myynti määrälle ja summalle alkuperäisen palkkion kirjauskansion riville.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Välitavoitteen laskutus.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Välitavoitteen summaa koskeva laskutettu myynti, joka on projektisopimusrivin alkuperäisessä välitavoitteessa.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]