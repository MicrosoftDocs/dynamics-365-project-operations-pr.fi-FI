---
title: Korjaavat projektipohjaiset laskut
description: Tässä artikkelissa on tietoja korjaavien projektipohjaisten laskujen luomisesta ja vahvistamisesta Project Operationsissa.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eecaf3dedeab5ff72d12808eb3144f9161313009
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931096"
---
# <a name="corrective-project-based-invoices"></a>Korjaavat projektipohjaiset laskut

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Vahvistettu projektilasku voidaan korjata käsittelemään muutoksia tai hyvityksiä neuvoteltuna asiakkaan ja projektipäällikön kanssa.

Voit tehdä muokkauksia vahvistettuun laskuun avaamalla vahvistetun laskun ja valitsemalla **Korjaa tämä lasku**. 

> [!NOTE]
> Valinta ei ole käytettävissä, ellei projektilaskua ole vahvistettu tai projektipohjaisessa laskussa on ennakkoja tai ennakkomaksuja tai ennakoiden tai ennakkomaksujen täsmäytyksiä.

Uusi laskuluonnos luodaan vahvistetusta laskusta. Kaikki aiemmin vahvistetun laskun laskurivin tiedot kopioidaan uuteen luonnokseen. Seuraavassa on joitakin tärkeitä tietoja uuden korjatun laskun rivitiedoista:

- Kaikki määrät päivitetään nollaksi. Dynamics 365 Project Operations olettaa, että kaikki laskutetut nimikkeet hyvitetään kokonaan. Voit tarvittaessa päivittää nämä määrät manuaalisesti niin, että ne vastaavat laskutettavaa määrää eikä hyvitettävän määrän määrää. Sovellus laskee hyvitetyn määrän syöttämiesi määrien perusteella. Tämä summa heijastuu todellisiin arvoihin, jotka luodaan korjatun laskun vahvistuksen yhteydessä. Jos teet verosummaan muutoksia, sinun täytyy syöttää oikea verosumma eikä hyvitettävää verosummaa.
- Välitavoitekorjaukset käsitellään aina täysinä hyvityksinä.


> [!IMPORTANT]
> Jos laskurivin tiedot ovat korjauksia muihin jo laskutettuihin kuluihin, **Korjaus**-kentän arvoksi määritetään **Kyllä**. Jos laskurivin tiedot ovat korjauksia, **Onko korjaus**-kentän arvoksi määritetään **Kyllä**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Toteutuneet arvot, jotka luodaan, kun korjauslasku vahvistetaan

Seuraavassa taulukossa on esitetty toteutuneet arvot, jotka luodaan korjauslaskun vahvistuksen yhteydessä.

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
Aiemmin laskutetun ajan tapahtuman täyden hyvityksen laskuttaminen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskutetun myynnin peruutus tunnille ja summalle alkuperäisen ajan laskurivitiedon perusteella.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamattoman todellinen myynti tunnille ja summalle alkuperäisen ajan laskurivitiedon perusteella.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Osittaisen hyvityksen laskuttaminen aikatapahtumasta.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskutettu myynnin peruutus tunneista ja summista, joka laskutetaan alkuperäisellä laskurivillä.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton todellinen myynti, joka veloitetaan muokatun laskurivin tiedoissa olevista tunneista ja summasta, tämän palautus ja vastaava laskutetun myynnin toteutuma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton toteutunut myynti, joka on veloitettavissa jäljellä olevista työajoista ja määrästä, kun laskun rivitiedoista on vähennetty korjatut luvut.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Aiemmin laskutetun kulun tapahtuman täyden hyvityksen laskuttaminen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskutettu myynnin peruutus määrästä ja summista kulun alkuperäisellä laskurivillä.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton myynnin todellinen määrä ja summista kulun alkuperäisellä laskurivillä.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Aiemmin laskutetun kulun tapahtuman osittaisen hyvityksen laskuttaminen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskutettu myynnin peruutus laskutetusta määrästä ja summista kulun alkuperäisellä laskurivillä.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton todellinen myynti, joka veloitetaan korjatun laskurivin tiedoissa olevista määristä ja summasta, tämän palautus ja vastaava laskutetun myynnin toteutuma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton toteutunut myynti, joka on veloitettavissa jäljellä olevista määristä ja summista, kun laskun rivitiedoista on vähennetty korjatut luvut.
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Aiemmin laskutettujen materiaalitapahtumien täydellisen hyvityksen laskuttaminen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskutetun myynnin peruutus määrälle ja summalle alkuperäisen materiaalin laskutusrivin tiedoissa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamattoman myynnin toteutunut arvo määrälle ja summalle alkuperäisen materiaalin laskutusrivin tiedoissa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Materiaalitapahtuman osittaisen hyvityksen laskutus.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskutetun myynnin peruutus määrälle ja summalle, jotka on laskutettu alkuperäisen materiaalin laskutusrivin tiedoissa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton myynnin todellinen arvo, joka on laskutettava muokatun laskun rivin määrälle ja summalle, tämän peruutus ja vastaava laskutettu myynnin toteutunut arvo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton toteutunut myynti, joka on veloitettavissa jäljellä olevista määristä ja summista, kun laskun rivitiedoista on vähennetty korjatut luvut.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Aiemmin laskutetun palkkion tapahtuman täyden hyvityksen laskuttaminen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskutettu myynnin peruutus määrästä ja summista palkkion alkuperäisellä laskurivillä.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton myynnin todellinen määrä ja summista palkkion alkuperäisellä laskurivillä.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Aiemmin laskutetun palkkion tapahtuman osittaisen hyvityksen laskuttaminen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskutettu myynnin peruutus määrästä ja summista palkkion alkuperäisellä laskurivillä.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uusi laskuttamaton todellinen myynti, joka veloitetaan muokatun ja korjatun laskurivin tiedoissa olevista määristä ja summasta, tämän palautus ja vastaava laskutetun myynnin toteutuma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Aiemmin laskutetun virstanpylvään täyden hyvityksen laskuttaminen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Laskutetun myynnin peruutus summalle alkuperäisen virstanpylvään laskurivitiedon perusteella.
                </p>
                <p>
Välitavoitteen laskun tila päivittyy arvosta <b>Kirjattu asiakaslasku</b> tilaksi <b>Valmis laskutettavaksi</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Aiemmin laskutetun virstanpylvään osittaisen hyvityksen laskuttaminen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tätä skenaariota ei tueta.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
