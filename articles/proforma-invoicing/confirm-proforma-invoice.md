---
title: Proformamuotoisen projektipohjaisen laskun vahvistaminen
description: Tässä aiheessa on tietoja proformamuotoisen projektipohjaisen laskun vahvistamisesta.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 46db66be0c346b9ad0006efc3ca2f3019a467daa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580498"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>Proformamuotoisen projektipohjaisen laskun vahvistaminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Kun proformalasku on vahvistettu, projektilaskun päivitysten tila on **Vahvistettu**. Kun lasku on vahvistettu, se on vain luku -tilassa. Edelleen lasku voidaan korjata vain, jos on asiakkaan aloittamia korjauksia tai hyvityksiä.

Seuraavassa taulukossa on lueteltu järjestelmän luomat toteutuneet arvot. Nämä toteutuneet arvot luodaan, kun projektilaskulle tehdään tiettyjä toimintoja ennen sen vahvistamista.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Skenaario</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Vahvistuksen yhteydessä luodut toteutuneet arvot</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Ennakkomaksun tai ennakkomaksuun perustuvan maksun laskuttaminen </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskutetun todellisen myynnin tyyppi, <strong>Pidätyskohde</strong> luodaan ennakkomaksulle tai pidätyskohteelle.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Laskuttamaton toteutunut myynti, jonka ennakkomaksun tai ennakkon täsmäytykseen käytettävä summa on negatiivinen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Sen jälkeen, kun olet täysin täsmäyttänyt laskun pidätyksen tai ennakkomaksun.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Täsmäytystä varten luodun pidätyksen tai ennakkomaksun laskuttamattoman myynnin peruutus. Tämä summa on positiivinen, koska sen tarkoitus on kumota pidätyksen tai ennakkomaksun yhteydessä luotu negatiivinen tulos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Laskutetun myynnin todellinen summa laskussa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Sen jälkeen, kun olet osittain täsmäyttänyt laskun pidätyksen tai ennakkomaksun.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Täsmäytystä varten luodun pidätyksen tai ennakkomaksun laskuttamattoman myynnin peruutus. Tämä summa on positiivinen, koska sen tarkoitus on kumota pidätyksen tai ennakkomaksun yhteydessä luotu negatiivinen tulos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Laskutetun myynnin todellinen summa laskussa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Negatiivisen laskuttamattoman myynnin todellinen jäljellä olevan pidätys tai ennakkomäärä, jota käytetään tulevissa laskuissa.
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
Uusi laskuttamaton todellinen myynti, joka veloitetaan muokatun laskurivin tiedoissa olevista tunneista ja summasta, myynnin tosiasiallinen palautus ja vastaava laskutetun myynnin toteutuma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton myynnin toteutunut arvo, joka ei ole laskutettava jäljellä olevilta tunneilta ja summalta sen jälkeen, kun muokatun laskurivin tiedot, toteutuneiden myyntien peruutus ja vastaava laskutettu myynti on vähennetty.
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
Uusi laskuttamaton todellinen myynti, joka on veloitettavissa muokatun laskurivin tiedoissa olevasta määrästä ja summasta, laskuttamattoman tosiasiallisen myynnin palautuksesta ja vastaavan laskutetun myynnin todellisesta arvosta. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Materiaalitapahtuman laskutus ilman laskuluonnoksen muokkauksia.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskuttamattoman myynnin peruutus alkuperäisen materiaalin käytön hyväksynnän määrälle ja summalle.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Laskutetun myynnin todellinen arvo alkuperäisen materiaalin käytön hyväksynnän määrälle ja summalle.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Muokatun materiaalitapahtuman laskutus, kun sitä muokattiin määrän pienentämiseksi.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskuttamattoman myynnin peruutus alkuperäisen ajan käytön hyväksynnän määrälle ja summalle.
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
Muokatun materiaalitapahtuman laskutus, kun sitä muokattiin määrän kasvattamiseksi.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskuttamattoman myynnin peruutus alkuperäisen materiaalin käytön hyväksynnän määrälle ja summalle.
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
