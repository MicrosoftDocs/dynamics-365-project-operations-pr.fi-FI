---
title: Toimittajan pidättämisen määrittäminen
description: Tässä artikkelissa käsitellään toimittajien pidätyksen määrittämistä.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f30e8829d8d5d99c81fce730cb93cd7ce31913fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929762"
---
# <a name="set-up-vendor-retention"></a>Toimittajan pidättämisen määrittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä artikkelissa on tietoja siitä, miten toimittajan pidätys määritetään.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Toimittajan pidätystilin luominen kirjanpitoon

1. Siirry Dynamics 365 Financessa kohtaan **Kirjanpito** > **Kirjauksen määritys** > **Automaattisten tapahtumien tilit**.
2. Lisää uusi rivi.
3. Valitse **Kirjaustyyppi**-kentässä **Toimittajan pidätys**.
4. Valitse päätili toimittajan pidätyskirjausta varten.

## <a name="create-vendor-retention-terms"></a>Toimittajan pidätysehtojen luominen

Käytä **Toimittajan pidätysehdot** -sivua määrittääksesi ja ylläpitääksesi toimittajamaksujen pidätysehtoja. Syötä toimittajamaksun prosenttiosuus pidätettäväksi ja prosenttiosuus aiemmin pidätetystä summasta vapautettavaksi. Summat säilytetään automaattisesti toimittajan laskuissa, kunnes palvelusopimus saavuttaa määritetyn valmistumisasteen. Kun toimittajalle on määritetty pidätysehdot, voit kohdistaa ne mihin tahansa projektiin, jossa toimittaja työskentelee.

1. Siirry Financessa kohtaan **Projektinhallinta ja kirjanpito** > **Määritys** > **Pidättäminen** > **Toimittajamaksun pidätysehdot**.
2. Valitse **Uusi**, jos haluat lisätä uuden toimittajan säilytysehdon. Arvo **Säännön tunnus** uuden ehdon kentässä syötetään automaattisesti. 
3. Syötä **Kuvaus**-kenttään uutta ehtoa kuvaava nimi.
4. Valitse **Ehdot**-välilehdessä **Lisää rivi**  syöttääksesi uuden toimittajan pidätysehdon.
5. Syötä  **Toimitettujen yksiköiden prosenttiosuus** -kentässä säännölle valmistumisprosentti. Summat säilytetään automaattisesti toimittajalaskuissa, kunnes valmistumisprosentin vaihe vastaa syötettyä prosenttiosuutta. Jos esimerkiksi kirjoitat 50,00, summat pidätetään, kunnes projektista on 50 prosenttia valmiina.
6. Syötä **Pidätettävä prosenttiosuus** -kentässä toimittajan laskutussumman pidätettävä prosenttiosuus. Esimerkiksi jos syötät arvon 10,00 tähän kenttään, 10 prosenttia toimittajalaskuista pidätetään, kunnes projekti saavuttaa valmistumisprosentin, jonka olet valinnut **Toimitettujen yksiköiden prosenttiosuus** -kenttään.
7. Syötä  **Vapautettava prosenttiosuus** -kenttässä prosenttiosuus mistä tahansa aiemmin pidätetyistä summista vapautettavaksi projektin valmistumisen valitulla tasolla.

> [!NOTE]
> Jos sinulla on useita projektin eri tasojen valmistumisen välitavoitteita, syötä erillinen toimittajan pidätysehdon rivi jokaiseen pidätyssääntöön. Kullekin riville voidaan määrittää eri pidätyksen prosenttiosuus ja eri vapautuksen prosenttiosuus kullekin nimetylle projektin valmistumisasteen tasolle.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Toimittajasopimuksen määrittäminen projektille

Määritä projektia koskevat toimittajan pidätysehdot. Toimittajan säilytysehdot näkyvät myös toimittajalle luotavien ostotilausten yhteydessä.

1. Siirry Financessa kohtaan **Projektinhallinta ja kirjanpito** > **Projektit** > **Kaikki projektit**. 
2. Valitse projekti ja valitse toimintoruudussa **Projektiryhmä** > **Toimittajasopimukset**.
3. Lisää uusi rivi **Toimittajasopimukset**-sivulla.
4. Valitse **tilikoodi**-kentässä jokin seuraavista vaihtoehdoista:
   - **Taulukko**: toimittajan säilytysehdot koskevat yhtä toimittajaa.
   - **Ryhmä**: toimittajan säilytysehdot koskevat kaikkia toimittajaryhmän toimittajia.
   - **Kaikki**: Toimittajan säilytysehdot koskevat kaikkia toimittajia.
5. Valitse **Toimittaja/toimittajaryhmä**-kentässä toimittaja tai toimittajaryhmä, johon toimittajan säilytysehtoja sovelletaan. Jos valitsit edellisessä vaiheessa **Kaikki**, tämä kenttä ei ole käytettävissä.
6. Valitse **Toimittajan pidätysehdot** -kentässä säännön tunnus tähän toimittajaan liittyviä pidätysehtoja varten.

