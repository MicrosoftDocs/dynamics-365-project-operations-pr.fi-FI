---
title: Laskutettavien projektien kirjanpidon määrittäminen
description: Tässä aiheessa on tietoja laskutettavien projektien kirjanpitovaihtoehdoista.
author: sigitac
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1159a31ba4f30f09734bf9c5a9e594b5c77a831e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596460"
---
# <a name="configure-accounting-for-billable-projects"></a>Laskutettavien projektien kirjanpidon määrittäminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations tukee erilaisia kirjanpitovaihtoehtoja laskutettaviin projekteihin, jotka sisältävät aika- ja materiaali- sekä kiinteähintaisia tapahtumia.

- **Aika- ja materiaalitapahtumat**: Nämä tapahtumat laskutetaan työn edetessä projektin tuntien, kulujen, nimikkeiden tai maksujen perusteella. Nämä tapahtumakustannukset voidaan täsmätä kunkin tapahtuman tuoton kanssa, ja projekti laskutetaan työn edetessä. Projektin tuottoa voidaan myös jaksottaa tapahtumahetkellä. Laskutuksen aikana tuotto kirjataan ja mahdollinen jaksotettu tuotto palautetaan.
- **Kiinteähintaiset tapahtumat**: Nämä tapahtumat laskutetaan projektisopimukseen perustuvan laskutusaikataulun mukaan. Kiinteähintaisten tapahtumien tuotto voidaan kirjata laskutuksessa, tai se voidaan laskea ja kirjata jaksoittain **valmiin sopimuksen** tai **valmistumisprosentin** mukaan.

Projektia pidetään laskutettavana, kun se liittyy yhteen tai useampaan sopimusriviin. Projektin sopimusrivi määrittää itse, mitä laskutustapoja ja tapahtumatyyppejä sallitaan.

Esimerkiksi Fabrikam Robotics on voittanut projektisopimuksen Adatum Corporationin kanssa laitteiden optimoinnista. Adatum maksaa kiinteän summan 10 000 USD kattamaan projektikuluja. Tämä on kiinteähintainen laskutustapa. Projektin aika ja maksut laskutetaan käytön mukaan. Tämä on aika- ja materiaaliperusteinen laskutustapa. Kaikkia töitä voidaan seurata yhdessä projektissa nimeltään Adatumin laitteiden optimointi.

Projektitiimin jäsen lähettää kahdeksan työtuntia Adatumin laitteiden optimointi -projektiin. Kun projektipäällikkö hyväksyy tämän ajan, järjestelmä käyttää aika- ja materiaalilaskutusmenetelmää todellisten tapahtumien, laskun ja asiakkaan luomiseen. Tätä tapahtumaa ei sisällytetä kiinteähintaisen tuoton arvion laskentaan.

Toinen projektitiimin jäsen lähettää 2 000,00 dollarin matkakulun Adatumin laitteiden optimointi -projektille. Kun projektipäällikkö hyväksyy tämän merkinnän, järjestelmä käyttää kiinteähintaista laskutusmenetelmää todellisten tapahtumien ja asiakkaan luomiseen tälle projektikululle. Asiakasta ei laskuteta tämän tapahtuman perusteella. Sen sijaan asiakasta laskutetaan käyttämällä erikseen määritettyjä laskutuksen välitavoitteita. Tämä kulutapahtuma sisällytetään kuluarvioiden kanssa kiinteähintaisen tuoton arvion laskentaan.

Projektitapahtumien kirjanpitoperiaatteet määritetään projektin kustannus- ja tuottoprofiileissa. Järjestelmä määrittää kullekin projektitapahtumalle asianmukaisen projektin kustannus- ja tuottoprofiilin käyttämällä määritettyjä projektin kustannus- ja tuottoprofiilien sääntöjä.

## <a name="define-project-cost-and-revenue-profiles"></a>Projektin kustannus- ja myyntivoittoprofiilien määrittäminen 

Projektin kustannus- ja tuottoprofiileissa määritetään projektitapahtumien kirjanpitosäännöt. Nämä profiilit on määritetty kohdassa Projektinhallinta ja kirjanpito. 

Luo uusi projektin kustannus- ja tuottoprofiili tekemällä seuraavat toimet. 

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Asetukset** > **Kirjaaminen** > **Projektin kustannus- ja tuottoprofiilit**. 
2. Valitse **Uusi**, jos haluat luoda uuden projektin kustannus- ja tuottoprofiilin.
3. Kirjoita **Nimi**-kenttään profiilin nimi ja lyhyt kuvaus.
4. Valitse **Laskutustapa**-kentässä **Aika ja materiaali** tai **Kiinteä hinta**.
5. Laajenna **Kirjanpito**-pikavälilehti. Tämän välilehden kentissä määritetään kirjanpitoperiaatteet, joita käytetään, kun projektitapahtumia kirjataan käyttämällä Project Operationsin integrointikirjauskansiota ja laskutetaan sitten kohdassa Projektin laskuehdotus.
6. Valitse asianmukaiset tiedot seuraaviin kenttiin **Kirjanpito**-pikavälilehdessä:

    - **Kulujen kirjaaminen – tunti**:

       - *Ei kirjanpitoon*: aikatapahtumien kustannusta ei kirjata kirjanpitoon, kun Project Operationsin integrointikirjauskansioon kirjataan. Kirjanpitäjä voi kuitenkin kirjata kustannukset käyttämällä Kirjaa kustannukset -toimintoa myöhemmin.
       - **Saldo**: Aikatapahtumien kustannukset veloitetaan Kirjanpito-tilityypin, *KET – kustannusarvo* -tilille ja hyvitetään *Palkanlaskennan kohdistustilille* kirjanpidon kirjausasetuksissa. Kirjanpitäjä käyttää Kirjaa kustannukset -toimintoa, jotta tämä kustannus voidaan siirtää saldotililtä Voitto ja tappio -tilille säännöllisin väliajoin.
       - **Voitto ja tappio**: Kun Project Operations integrointikirjauskansio kirjataan, aikatapahtuman kustannus veloitetaan kirjanpitotilityyppiin *Kustannus* ja hyvitetään *Palkanlaskennan kohdistustilille*, joka on määritetty **Kirjanpidon kirjausasetukset**-sivun (**Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Kirjaaminen** \> **Kirjanpidon kirjausasetukset**) **Kustannukset**-välilehdessä. Tämä on yleisin aika- ja materiaalitapahtumien määritys.
        - *Ei koskaan kirjanpitoon*: Aikatapahtumien kustannusta ei koskaan kirjata kirjanpitoon.

    - **Kirjaa kustannukset – kulu**:

         - **Saldo**: Kun Project Operationsin integrointikirjauskansiota kirjataan, kulutapahtuman kustannus veloitetaan **Kirjanpidon kirjausasetukset** -sivun **Kustannus**-välilehdessä määritetyltä kirjanpidon tilityypistä *KET – kustannusarvo* ja hyvitetään kirjauskansiorivin vastatilille. Kulun oletusvastatilit määritetään kohdassa **Projektinhallinta ja kirjanpito** > **Asetukset** \> **Kirjaaminen** \> **Kulujen oletusvastatili**. Kirjanpitäjä käyttää **Kirjaa kustannukset** -toimintoa, jotta tämä kustannus voidaan siirtää saldotililtä Voitto ja tappio -tilille säännöllisin väliajoin.
        - **Voitto ja tappio**: Kun Project Operationsin integrointikirjauskansiota kirjataan, kulutapahtuman kustannus veloitetaan **Kirjanpidon kirjausasetukset** -sivun **Kustannus**-välilehdessä määritetyltä kirjanpidon tilityypistä *Kustannus* ja hyvitetään kirjauskansiorivin vastatilille. Kulun oletusvastatilit määritetään kohdassa **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Kirjaaminen** \> **Kulujen oletusvastatili**.
      
    - **Kirjaa kustannukset – nimike**:

         - **Saldo**: Project Operationsin integrointikirjauskansion kirjauksen yhteydessä nimikkeen tapahtumakustannukset veloitetaan kirjanpidon tilin tyypiltä *KET kustannuksen arvo - nimike*, kuten on määritelty **Kustannus**-välilehdellä **Kirjanpidon kirjauksen määritykset** -sivulla ja hyvitetään seuraaville:
    
              - Asiakirjatyypille käyttö: **Kustannus - nimike** -tilille kohteessa **Kirjanpidon kirjausten määritykset**.  
              - Asiakirjatyypille osto: **Hankintojen integraatiotili** kohteessa **Projektinhallinta ja kirjanpitoparametrit**.
           Kirjanpitäjä käyttää **Kirjaa kustannukset** -toimintoa, jotta tämä kustannus voidaan siirtää saldotililtä Voitto ja tappio -tilille säännöllisin väliajoin.
        - **Tuloslaskelma**: Project Operationsin integrointikirjauskansion kirjauksen yhteydessä nimikkeen tapahtumakustannukset veloitetaan kirjanpidon tilin tyypiltä *Kustannus*, kuten on määritelty **Kustannus**-välilehdellä **Kirjanpidon kirjauksen määritykset** -sivulla ja hyvitetään seuraaville:
         
             - Asiakirjatyypille käyttö: **Kustannus - nimike** -tilille kohteessa **Kirjanpidon kirjausten määritykset**.  
             - Asiakirjatyypille osto: **Hankintojen integraatiotili** kohteessa **Projektinhallinta ja kirjanpitoparametrit**.
       
    - **Tilillä-laskutus**:

        - **Saldo**: Kun kirjaat projektin laskuehdotuksen, tilillä-tapahtuma (laskutuksen välitavoite) hyvitetään **Kirjanpidon kirjausasetukset** -sivun **Tuotto**-välilehdessä määritettyyn kirjanpidon tilityyppiin *Laskutettu KET – tilillä* ja veloitetaan asiakkaan saldotililtä.
         - **Voitto ja tappio**: Kun kirjaat projektin laskuehdotuksen, tilillä-tapahtuma (laskutuksen välitavoite) hyvitetään **Kirjanpidon kirjausasetukset** -sivun **Tuotto**-välilehdessä määritettyyn kirjanpidon tilityyppiin *Laskutettu tuotto – tilillä* ja veloitetaan asiakkaan saldotililtä. Asiakkaan saldotilit määritetään kohdassa **Myyntireskontra** \> **Asetukset** \> **Asiakkaan kirjausprofiilit**.

   Kun määrität aika- ja materiaalilaskutustavan kirjausprofiileita, voit kerryttää myyntituottoa tapahtumatyyppiä (tuntia, kulua, nimikettä ja maksua) kohden. Jos **Jaksota tuotto** -asetukseksi on määritetty **Kyllä**, laskuttamattomat myyntitapahtumat Project Operationsin integrointikirjauskansiossa kirjataan pääkirjaan. Myyntiarvo veloitetaan **KET – myyntiarvotililtä** ja hyvitetään **Kerrytetty tuotto - myyntiarvo** -tilille, joka määritettiin **Kirjanpidon kirjausasetukset** -sivun **Tuotto**-välilehdellä. 
  
  > [!NOTE]
  > Vaihtoehto **Jaksota tuotto** on käytettävissä vain silloin, kun vastaavan tapahtumatyypin **Kustannus** kirjataan tulostilille.
    
7. Laajenna **Arvio**-pikavälilehti. Tämän välilehden kentissä määritetään kiinteähintaisten tuottojen arvioiden laskenta-asetukset. Tämän välilehden kentät koskevat vain projektin kustannus- ja tuottoprofiileita, joiden laskutusmenetelmä on **Kiinteähintainen**.
8. Valitse asianmukaiset tiedot seuraaviin kenttiin **Arvio**-pikavälilehdessä:

    - **Projektin valmistumislaskelmissa käytettävä periaate**:

        - **Valmis sopimus**: Kustannusten vastaavuutta ja tuoton kirjausta ei tapahdu ennen projektin loppua. Kustannukset kuvastavat KET-töitä saldossa, kunnes projekti on valmis.
        - **Valmistumisprosentti**: Jaksotettu tuotto lasketaan ja kirjataan kirjanpitoon joka jaksossa projektin valmistumisprosentin perusteella. Valmistumisprosentin laskemiseksi on käytettävissä useita menetelmiä. Nämä menetelmät voidaan määrittää automaattisesti määritysten perusteella tai manuaalisesti.
        - **Ei KET-töitä**: Tätä asetusta käytetään kiinteähintaisissa projekteissa, joiden aikaväli on lyhyt ja joissa lasku ja kustannukset tapahtuvat samana ajanjaksona. Tässä tapauksessa **Kirjanpito**-pikavälilehden **Tilillä-laskutus**-kentän arvoksi määritetään automaattisesti **Voitto ja tappio**, jotta varmistetaan tuoton kirjaaminen laskutuksessa. Tuoton arviointiprosessia ei käytetä tässä projektin kustannus- ja tuottoprofiilissa.

    - **Täsmäytysperiaate**: Tässä kentässä määritetään, miten laskettu myyntiarvo (jaksotettu tuotto) kirjataan kirjanpitoon.

        - Kun **Myyntiarvo**-periaatetta käytetään, järjestelmä laskee myyntiarvon täsmäyttämällä kustannukset ja tuoton ja kirjaamalla sen sitten yhtenä summana.
        - **Tuotanto ja tuotto** -periaatteen avulla järjestelmä jakaa myyntiarvon toteutuneille kustannuksille ja lasketulle tuotolle. Nämä kirjataan erikseen.

    - **Kustannusmallit**: Salli projektitapahtumien ryhmittely tapahtumatyypin ja projektiluokan perusteella ja määritä näiden ryhmien valmistumisprosentin laskentasäännöt.
    - **Jaksokoodit**: Määritä, miten usein tuottoarviot lasketaan tietylle projektin kustannus- ja tuottoprofiilille.
    - **Arvioluokat**: Käytetään myyntiarvon (jaksotetun tuoton) kirjaamiseen projektitapahtumiin. Määritä ensin **Maksu**-tapahtumatyypille oma projektiluokka ja määritä sitten lmerkintä **Arvio** tälle projektiluokalle. Valitse seuraavaksi valitun täsmäytysperiaatteen mukaan tämä projektiluokka **Myyntiarvo**- tai **Tuotto** kentästä projektin kustannus- ja tuottoprofiilissa.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Projektin kustannus- ja tuottoprofiilien näytekokoonpanot

Aika ja materiaali – ei KET-töitä

![Kustannus- ja tuottoprofiili: Aika ja materiaali – ei KET-töitä.](media/time-material-no-wip.png)

Aika ja materiaalit – KET (tuotto)

![Kustannus- ja tuottoprofiili: Aika ja materiaali – KET.](media/time-material-with-wip.png)

Kiinteä hinta – ei KET-töitä

![Kustannus- ja tuottoprofiili: Kiinteä hinta – ei KET-töitä.](media/fixed-price-no-wip.png)

Kiinteä hinta – valmis sopimus

![Kustannus- ja tuottoprofiili: Kiinteä hinta – valmis sopimus.](media/fixed-price-completed-contract.png)

Kiinteä hinta – valmistumisprosentti

![Kustannus- ja tuottoprofiili: Kiinteä hinta – valmistumisprosentti.](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Projektin kustannus- ja tuottoprofiilien näytteen kirjanpitotapahtumaesimerkit.

| Kirjanpitotapahtuma                  | Aika ja materiaalit – ei KET-töitä                       | Aika ja materiaalit – KET                                                                                           | Kiinteä hinta – ei KET-töitä                                            | Kiinteä hinta – valmis sopimus                                                                            | Kiinteä hinta – valmistumisprosentti                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Aikatapahtumien kirjaaminen    | Debet – kustannus <br>Kredit – palkanlaskennan kohdistus          | Debet – kustannus <br>Kredit – palkanlaskennan kohdistus <br>Debet – KET-myyntiarvo <br>Kredit – jaksotetun tuoton myyntiarvo                | Debet – kustannus <br>Kredit – palkanlaskennan kohdistus                         | Debet – kustannus <br>Kredit – palkanlaskennan kohdistus                                                                    | Debet – kustannus <br>Kredit – palkanlaskennan kohdistus                       |
| Kulutapahtumien kirjaaminen | Debet – kustannus <br>Kredit – kulun vastatili | Debet – kustannus <br>Kredit – kulun vastatili <br>Debet – KET-myyntiarvo <br>Kredit – jaksotetun tuoton myyntiarvo      | Debet – kustannus <br>Kredit – kulun vastatili                 | Debet – kustannus<br> Kredit – kulun vastatili                                                            | Debet – kustannus <br>Kredit – kulun vastatili               |
| Laskutusasiakas                | Debet – asiakkaan saldo <br>Kredit – laskutettu tuotto | Debet – asiakkaan saldo <br>Kredit – laskutettu tuotto <br>Kredit – KET-myyntiarvo, Debet – jaksotetun tuoton myyntiarvo | Debet – asiakkaan saldo <br>Kredit – laskutettu tuotto – tilillä | Debet – asiakkaan saldo <br>Kredit – KET – laskutettu tilillä                                                  | Debet – asiakkaan saldo <br>Kredit – KET – laskutettu tilillä    |
| Kirjaa tuottoarvio             | Ei käytettävissä                                   | Ei käytettävissä                                                                                                    | Ei käytettävissä                                                  | Debet – KET-kustannusarvo <br>Kredit – kustannus                                                                         | Debet – KET – myyntiarvo <br>Kredit – jaksotetun tuoton myyntiarvo |
| Poista                         | Ei käytettävissä                                   | Ei käytettävissä                                                                                                    | Ei käytettävissä                                                  | Kredit – KET-kustannusarvo <br>Debet – kustannus <br>Kredit – jaksotetun tuoton myyntiarvo <br>Debet – KET – laskutettu tilillä | Debet – KET – laskutettu tilillä <br>Kredit – KET-myyntiarvo     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Projektin kustannus- ja myyntivoittoprofiilisääntöjen määrittäminen

Projektin kustannus- ja tuottoprofiilisäännöt määrittävät projektin kustannus- ja tuottoprofiilin, jota on käytettävä käsiteltäessä mitä tahansa laskutettavia projektitapahtumia. Määritä säännöt valitsemalla siirtymällä kohtaan **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Kirjaaminen** \> **Projektin kustannus- ja tuottoprofiilisäännöt**.

Säännöt voidaan määrittää projektisopimuksessa, projektiryhmässä tai tietyssä projektissa. Järjestelmä valitsee aina ensin suurimman rakeisuuden säännön.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
