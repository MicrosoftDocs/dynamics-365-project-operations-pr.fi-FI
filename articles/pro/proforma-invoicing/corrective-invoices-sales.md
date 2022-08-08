---
title: Oikaisevat projektilaskut
description: Tässä artikkelissa on tietoja korjaavien projektipohjaisten laskujen luomisesta Project Operationsissa.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3e8e10d69368f4704ec6121106fbfd35394dc441
ms.sourcegitcommit: 95dacb0e74fa8970f56fdb1cbaa915d3fbec6e0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2022
ms.locfileid: "9023655"
---
# <a name="corrective-project-invoices"></a>Oikaisevat projektilaskut

_**Koskee:** Lite-käyttöönotto - kaupasta proformalaskutukseen, Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita_

Vahvistettu projektilasku voidaan korjata käsittelemään muutoksia tai hyvityksiä neuvoteltuna asiakkaan ja projektipäällikön kanssa.

Voit tehdä muokkauksia vahvistettuun laskuun avaamalla vahvistetun laskun ja valitsemalla **Korjaa tämä lasku**. 

> [!NOTE]
> Tämä valinta ei ole käytettävissä, ellei projektilaskua vahvisteta.

Uusi laskuluonnos luodaan vahvistetusta laskusta. Kaikki aiemmin vahvistetun laskun laskurivin tiedot kopioidaan uuteen luonnokseen. Seuraavassa on joitakin tärkeitä tietoja uuden korjatun laskun rivitiedoista:

- Kaikki määrät päivitetään nollaksi. Sovellus olettaa, että kaikki laskutetut nimikkeet hyvitetään kokonaan. Voit tarvittaessa päivittää nämä määrät manuaalisesti niin, että ne vastaavat laskutettavaa määrää eikä hyvitettävän määrän määrää. Sovellus laskee hyvitetyn määrän syöttämiesi määrien perusteella. Tämä summa heijastuu todellisiin arvoihin, jotka luodaan korjatun laskun vahvistuksen yhteydessä. Jos teet verosummaan muutoksia, sinun täytyy syöttää oikea verosumma eikä hyvitettävää verosummaa.
- Aiemmin vahvistettuja tuotepohjaisia sopimusrivejä ei kopioida. Tuotepohjaisen projektilaskun korjausten käsittelyä ei tueta.
- Välitavoitekorjaukset käsitellään aina täysinä hyvityksinä.
- Pidätys- tai ennakkosummat voidaan oikaista, jos asiakasta on laskutettu virheellisen määrän takia.
- Pidätysmaksujen ja ennakoiden täsmäytykset voidaan oikaista, jos aiemmin vahvistetun laskun kulujen täsmäyttämiseen käytettiin virheellistä määrää.

> [!IMPORTANT]
> Laskurivin tiedot, jotka ovat korjauksia muihin jo laskutettuihin kuluihin, saavat kentän **korjauksen** arvoksi **Kyllä**. Laskuilla, joiden laskurivitiedot on korjattu on kenttä nimeltä **korjaukset**, joiden arvo on myös **Kyllä**.

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
            <td width="216" rowspan="4" valign="top">
                <p>
Vahvista laskutettu ennakko tai pidätys.<strong></strong>
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
Laskutetun myynnin peruutuksen todellinen arvo luodaan ennakkomaksun tai ennakon peruutuksesta alkuperäistä laskutettavaa myyntiä varten.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Korjatulle summalle luodaan uusi laskutettu myyntiennuste pidätykselle tai ennakkoon perustuvalle korjatulle laskuriville.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Laskuttamattoman myynnin todellisen negatiivisen määrän pidätys tai ennakkoon perustuva korjattu laskurivi, jota käytetään täsmäytykseen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Vahvistus korjauksesta, joka on aiemmin täsmäytetyn pidätys- tai ennakkomaksun korjaus.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Täsmäytystä varten luodun pidätyksen tai ennakkomaksun laskuttamattoman myynnin peruutus. Tämä summa on positiivinen ja sen tarkoitus on kumota aiemman täsmäytyksen yhteydessä luotu negatiivinen tulos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Laskutetun myynnin peruutuksen todellinen summa aiemmassa laskussa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Todellinen uusi laskutettu myynti korjatulle pidätyssummalle, joka otetaan käyttöön korjatussa laskussa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Laskuttamaton todellinen myynti negatiivisella summalla korjatusta jäljellä olevasta pidätyksestä tai ennakosta, jota käytetään myöhempien laskujen täsmäytykseen.
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
Ei tuettu </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Aiemmin laskutetun tuotepohjaisen sopimusrivin hyvitykset ja korjaukset.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Ei tuettu </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
