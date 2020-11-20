---
title: Proformalaskun vahvistaminen – lite
description: Tämä aihe tarjoaa tietoja Project Operationsin proformalaskujen vahvistamisesta.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176517"
---
# <a name="confirm-a-proforma-invoice---lite"></a>Proformalaskun vahvistaminen – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_


Kun proformalasku on vahvistettu, projektilaskun päivitysten tila on **Vahvistettu**. Kun lasku on vahvistettu, se on vain luku -tilassa. Jatkossa lasku voidaan oikaista vain, jos asiakkaalle on aloitettu korjauksia tai hyvityksiä tai jos lasku on merkitty maksetuksi.

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
Täsmäyttämisen yhteydessä käytettävä maksun tai ennakon negatiivinen summa, jota ei ole laskutettu.
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
Uusi laskuttamaton tosiasiallinen myynti, josta ei veloiteta jäljellä olevia tunteja ja määrää sen jälkeen, kun vähennetään korjatut luvut muokatun laskurivin yksityiskohdissa, tosiasiallisen myynnin palautus ja vastaava laskutettu todellinen myynti.
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
Laskutettu toteutunut myynti määrälle ja summalle alkuperäisen kuluhyväksynnän perusteella </p>
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
        <tr>
            <td width="216" valign="top">
                <p>
Tuotepohjaisen sopimusrivin laskuttaminen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tuoteriviltä laskutettu myynti, jolla on tuotepohjaisen sopimusrivin määrä ja summa.
                </p>
            </td>
        </tr>
    </tbody>
</table>
