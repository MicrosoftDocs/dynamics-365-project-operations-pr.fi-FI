---
title: Projektiaikataulun ohjelmointirajapintojen käyttäminen Power Automaten kanssa
description: Tässä artikkelissa on näytetyönkulku, joka käyttää projektiaikataulun ohjelmointirajapintoja.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404396"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Projektiaikataulun ohjelmointirajapintojen käyttäminen Power Automaten kanssa

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Tässä artikkelissa käsitellään esimerkkityönkulkua, joka näyttää, miten täydellinen projektisuunnitelma luodaan käyttämällä Microsoft Power Automatea, miten toimintojoukko luodaan ja miten entiteetti päivitetään. Tässä esimerkissä näytetään, miten luodaan projekti, projektiryhmän jäsen, toimintojoukot, projektitehtävät ja resurssimääritykset. Tässä artikkelissa on myös tietoja entiteetin päivittämisestä ja toimintojoukon suorittamisesta.

Seuraavassa on täydellinen luettelo vaiheista, jotka on dokumentoitu tämän artikkelin esimerkkityönkulussa:

1. [PowerApps-käynnistimen luominen](#1)
2. [Luo projekti](#2)
3. [Ryhmän jäsenen muuttujan alustaminen](#3)
4. [Yleisen ryhmän jäsenen luonti](#4)
5. [Toimintojoukon luominen](#5)
6. [Luo projektisäilö](#6)
7. [Linkin tilan muuttujan alustaminen](#7)
8. [Tehtävien määrän muuttujan alustaminen](#8)
9. [Projektitehtävän tunnuksen muuttujan alustaminen](#9)
10. [Tee kunnes](#10)
11. [Määritä projektitehtävä](#11)
12. [Luo projektitehtävä](#12)
13. [Luo resurssimääritys](#13)
14. [Pienennä muuttujaa](#14)
15. [Nimeä projektitehtävä uudelleen](#15)
16. [Toimintojoukon suorittaminen](#16)

## <a name="assumptions"></a>Oletustiedot

Tässä artikkelissa oletetaan, että käytössä on perustiedot Dataverse-alustasta, pilvityönkuluista ja projektiaikataulun ohjelmointirajapinnasta. Lisätietoja on myöhemmin tässä artikkelissa kohdassa [Viitteet](#references).

## <a name="create-a-flow"></a>Luo työnkulku

### <a name="select-an-environment"></a>Ympäristön valinta

Voit luoda Power Automate -työnkulun ympäristössäsi.

1. Siirry osoitteeseen <https://flow.microsoft.com> ja kirjaudu sisään järjestelmänvalvojan tunnistetiedoilla.
2. Valitse **Ympäristöt** oikeassa yläkulmassa.
3. Valitse luettelosta ympäristö, johon Dynamics 365 Project Operations on asennettu.

### <a name="create-a-solution"></a>Ratkaisun luominen

Voit luoda [ratkaisun huomioon ottavan työnkulun](/power-automate/overview-solution-flows) seuraavasti. Luomalla ratkaisulle tietoisia työnkulkuja voit viedä työnkulun helpommin myöhemmin käytettäväksi.

1. Valitse siirtymisruudussa **Ratkaisut**.
2. Valitse **Ratkaisut**-sivulla **Uusi ratkaisu**.
3. Määritä **Uusi ratkaisu** -valintaikkunassa pakolliset kentät ja valitse sitten **Luo**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Vaihe 1: PowerApps -käynnistimen luominen

1. Valitse **Ratkaisut**-sivulla luomasi ratkaisu ja valitse sitten **Uusi**.
2. Valitse vasemmanpuoleisesta ruudusta **Pilvityönkulut** \> **Automaatio** \> **Pilvityönkulku** \> **Välitön**.
3. Kirjoita **Työnkulun nimi** -kenttään **Schedule API Demo Flow**.
4. Valitse **Valitse , miten työnkulku käynnistyy** -luettelossa **Power Apps**. Kun luot Power Apps -käynnistimen, logiikka on tekijän vastuulla. Tässä artikkelissa syöteparametrit jätetään tyhjäksi testausta varten.
5. Valitse **Luo**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Vaihe 2: Luo projekti

Luo esimerkkiprojekti seuraavien vaiheiden mukaisesti.

1. Valitse luomassasi työnkulussa **Uusi vaihe**.

    ![Uuden vaiheen lisääminen.](media/newstep.png)

2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **suorita ei-sidottu toiminto**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.

    ![Toiminnon valitseminen.](media/chooseactiontab.png)

3. Valitse uudessa vaiheessa kolme pistettä (**...**) ja valitse sitten **Nimeä uudelleen**.

![Vaiheen nimeäminen uudelleen.](media/renamestep.png)

4. Nimeä uudelleen vaihe: **Luo projekti**.
5. Valitse **Toiminnon nimi** -kentässä **msdyn\_CreateProjectV1**.
6. Valitse **msdyn\_subject** -kentässä **Lisää dynaaminen sisältö**.
7. Kirjoita **Lauseke**-välilehden toimintokenttään **Projektin nimi - utcNow()**.
8. Valitse **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Vaihe 3: Ryhmän jäsenen muuttujan alustaminen

1. Valitse työnkulussa **Uusi vaihe**.
2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **alusta muuttuja**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.
3. Valitse uudessa vaiheessa kolme pistettä (**...**) ja valitse sitten **Nimeä uudelleen**.
4. Nimeä uudelleen vaihe: **Alusta ryhmän jäsen**.
5. Anna **Nimi**-kentässä **TeamMemberAction**.
6. Kirjoita **Tyyppi**-kenttään **Merkkijono**.
7. Syötä **Arvo**-kenttään **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Vaihe 4: Luo yleinen ryhmän jäsen.

1. Valitse työnkulussa **Uusi vaihe**.
2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **suorita ei-sidottu toiminto**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.
3. Valitse uudessa vaiheessa kolme pistettä (**...**) ja valitse sitten **Nimeä uudelleen**.
4. Nimeä uudelleen vaihe: **Luo ryhmän jäsen**.
5. Valitse **Toiminnon nimi** -kentässä **Dynaamisen sisältö** valintaikkunassa **TeamMemberAction**.
6. Kirjoita **Toimintoparametrit**-kenttään seuraavat parametritiedot.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Seuraavassa on selitetty parametrit:

    - **\@\@odata.type** – Entiteetin nimi. Kirjoita esimerkiksi **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – projektitiimin tunnuksen perusavain. Arvo on GUID-lauseke.   Tunnus luodaan Lauseke-välilehdestä.

    - **msdyn\_project\@odata.bind** – omistavan projektin tunnus. Arvo on dynaaminen sisältö, joka tulee Luo projekti -vaiheen vastauksesta. Varmista, että syötät koko polun ja lisäät dynaamisen sisällön sulkeiden väliin. Lainausmerkit ovat pakollisia. Kirjoita esimerkiksi **"/msdyn\_projects(LISÄÄ DYNAAMINEN SISÄLTÖ)"**.
    - **msdyn\_name** – ryhmän jäsenen nimi. Kirjoita esimerkiksi **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Vaihe 5: Toimintojoukon luominen

1. Valitse työnkulussa **Uusi vaihe**.
2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **suorita ei-sidottu toiminto**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.
3. Valitse uudessa vaiheessa kolme pistettä (**...**) ja valitse sitten **Nimeä uudelleen**.
4. Nimeä uudelleen vaihe: **Luo toimintojoukko**.
5. Valitse **Toiminnon nimi** -kentässä mukautettu Dataverse-toiminto **msdyn\_CreateOperationSetV1**.
6. Syötä **Kuvaus**-kenttään **ScheduleAPIDemoOperationSet**.
7. Anna **Projekti**-kenttään **/msdyn\_projects(**.
8. Valitse **Dynaaminen sisältö** -valintaikkunassa **msdyn\_CreateProjectV1Response ProjectId**.
9. Kirjoita **Projekti**-kenttään **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Vaihe 6: Luo projektisäilö

1. Valitse työnkulussa **Uusi vaihe**.
2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **lisää uusi rivi**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.
3. Valitse uudessa vaiheessa kolme pistettä (**...**) ja valitse sitten **Nimeä uudelleen**.
4. Nimeä uudelleen vaihe: **Luo säilö**.
5. Valitse **Taulukon nimi** -kentässä **Projektisäilöt**.
6. Anna **Nimi**-kentässä **ScheduleAPIDemoBucket1**.
7. Valitse **Projekti**-kentälle **Dynaaminen sisältö** -valintaikkunassa **msdyn\_CreateProjectV1Response ProjectId**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Vaihe 7: Linkin tilan muuttujan alustaminen

1. Valitse työnkulussa **Uusi vaihe**.
2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **alusta muuttuja**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.
3. Valitse uudessa vaiheessa kolme pistettä (**...**) ja valitse sitten **Nimeä uudelleen**.
4. Nimeä uudelleen vaihe **Alusta linkin tila**.
5. Anna **Nimi**-kentässä **linkstatus**.
6. Kirjoita **Tyyppi**-kenttään **Kokonaisluku**.
7. Anna **Arvo**-kentässä **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Vaihe 8: Tehtävien määrän muuttujan alustaminen

1. Valitse työnkulussa **Uusi vaihe**.
2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **alusta muuttuja**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.
3. Valitse uudessa vaiheessa kolme pistettä (**...**) ja valitse sitten **Nimeä uudelleen**.
4. Nimeä uudelleen vaihe: **Alusta tehtävien määrä**.
5. Anna **Nimi**-kentässä **tehtävien määrä**.
6. Kirjoita **Tyyppi**-kenttään **Kokonaisluku**.
7. Anna **Arvo**-kentässä **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Vaihe 9: Projektitehtävän tunnuksen muuttujan alustaminen

1. Valitse työnkulussa **Uusi vaihe**.
2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **alusta muuttuja**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.
3. Valitse uudessa vaiheessa kolme pistettä (**...**) ja valitse sitten **Nimeä uudelleen**.
4. Nimeä uudelleen vaihe: **Alusta ProjectTaskID**.
5. Anna **Nimi**-kentässä **tehtävien määrä**.
6. Kirjoita **Tyyppi**-kenttään **Merkkijono**.
7. Kirjoita **Arvo**-kenttään lausekkeen muodostimessa **guid()**.

## <a name="step-10-do-until"></a><a id="10"></a>Vaihe 10: Tee kunnes

1. Valitse työnkulussa **Uusi vaihe**.
2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **tee kunnes**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.
3. Määritä ehdollisen lauseen ensimmäinen arvo **dynaamisen sisällön** valintaikkunassa **tehtävien määrän** muuttujalle.
4. Määritä ehdoksi **pienempi tai yhtä suuri kuin**.
5. Aseta ehdollisen lausekkeen toisen arvon arvoksi **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Vaihe 11: Määritä projektitehtävä

1. Valitse työnkulussa **Uusi vaihe**.
2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **määritä muuttuja**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.
3. Valitse uudessa vaiheessa kolme pistettä (**...**) ja valitse sitten **Nimeä uudelleen**.
4. Nimeä uudelleen vaihe: **Määritä projektitehtävä**.
5. Valitse **Nimi**-kentässä **msdyn\_projecttaskid**.
6. Kirjoita **Arvo**-kenttään lausekkeen muodostimessa **guid()**.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Vaihe 12: Luo projektitehtävä

Seuraavien vaiheiden mukaisesti voit luoda projektitehtävän, jolla on nykyiseen projektiin ja luomaasi projektisäilöön kuuluva yksilöllinen tunnus.

1. Valitse työnkulussa **Uusi vaihe**.
2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **suorita ei-sidottu toiminto**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.
3. Valitse vaiheessa kolme pistettä (**...**) ja valitse sitten **Nimeä uudelleen**.
4. Nimeä uudelleen vaihe: **Luo projektitehtävä**.
5. Valitse **Toiminnon nimi** -kentässä **msdyn\_PssCreateV1**.
6. Kirjoita **Entiteetti**-kenttään seuraavat parametritiedot.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Seuraavassa on selitetty parametrit:

    - **\@\@odata.type** – Entiteetin nimi. Kirjoita esimerkiksi **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – tehtävän yksilöllinen tunnus. Arvoksi on määritettävä dynaaminen muuttuja, joka on peräisin kohteesta **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – omistavan projektin tunnus. Arvo on dynaaminen sisältö, joka tulee Luo projekti -vaiheen vastauksesta. Varmista, että syötät koko polun ja lisäät dynaamisen sisällön sulkeiden väliin. Lainausmerkit ovat pakollisia. Kirjoita esimerkiksi **"/msdyn\_projects(LISÄÄ DYNAAMINEN SISÄLTÖ)"**.
    - **msdyn\_subject** – mikä tahansa tehtävän nimi.
    - **msdyn\_projectbucket\@odata.bind** – projektisäilö, joka sisältää tehtävät. Arvo on dynaaminen sisältö, joka tulee Luo projektisäilö -vaiheen vastauksesta. Varmista, että syötät koko polun ja lisäät dynaamisen sisällön sulkeiden väliin. Lainausmerkit ovat pakollisia. Kirjoita esimerkiksi **"/msdyn\_projectbuckets(LISÄÄ DYNAAMINEN SISÄLTÖ)"**.
    - **msdyn\_start** – alkamispäivän dynaaminen sisältö. Esimerkiksi huominen näkyy muodossa **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – suunniteltu aloituspäivä. Esimerkiksi huominen näkyy muodossa **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – aikataulutettu päättymispäivä. Valitse tuleva päivämäärä. Määritä esimerkiksi **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – Linkin tila. Kirjoita esimerkiksi **"192350000"**.

7. Valitse **OperationSetId**-kentälle **Dynaaminen sisältö** -valintaikkunassa **msdyn\_CreateOperationSetV1Response**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Vaihe 13: Resurssimäärityksen luominen

1. Valitse työnkulussa **Uusi vaihe**.
2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **suorita ei-sidottu toiminto**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.
3. Valitse vaiheessa kolme pistettä (**...**) ja valitse sitten **Nimeä uudelleen**.
4. Nimeä uudelleen vaihe: **Luo määritys**.
5. Valitse **Toiminnon nimi** -kentässä **msdyn\_PssCreateV1**.
6. Kirjoita **Entiteetti**-kenttään seuraavat parametritiedot.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Valitse **OperationSetId**-kentälle **Dynaaminen sisältö** -valintaikkunassa **msdyn\_CreateOperationSetV1Response**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Vaihe 14: Pienennä muuttujaa

1. Valitse työnkulussa **Uusi vaihe**.
2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **pienennä muuttujaa**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.
3. Valitse **Nimi**-kentässä **tehtävien määrä**.
4. Anna **Arvo**-kentässä **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Vaihe 15: Nimeä projektitehtävä uudelleen

1. Valitse työnkulussa **Uusi vaihe**.
2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **suorita ei-sidottu toiminto**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.
3. Valitse vaiheessa kolme pistettä (**...**) ja valitse sitten **Nimeä uudelleen**.
4. Nimeä uudelleen vaihe: **Nimeä projektitehtävä uudelleen**.
5. Valitse **Toiminnon nimi** -kentässä **msdyn\_PssUpdateV1**.
6. Kirjoita **Entiteetti**-kenttään seuraavat parametritiedot.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Valitse **OperationSetId**-kentälle **Dynaaminen sisältö** -valintaikkunassa **msdyn\_CreateOperationSetV1Response**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Vaihe 16: Toimintojoukon suorittaminen

1. Valitse työnkulussa **Uusi vaihe**.
2. Kirjoita **Valitse toiminto** - valintaikkunan hakukenttään **suorita ei-sidottu toiminto**. Valitse sitten **Toiminnot**-välilehden tulosluettelosta toiminto.
3. Valitse vaiheessa kolme pistettä (**...**) ja valitse sitten **Nimeä uudelleen**.
4. Nimeä uudelleen vaihe: **Suorita toimintojoukko**.
5. Valitse **Toiminnon nimi** -kentässä **msdyn\_ExecuteOperationSetV1**.
6. Valitse **OperationSetId**-kentälle **Dynaaminen sisältö** -valintaikkunassa **msdyn\_CreateOperationSetV1Response OperationSetId**.

## <a name="references"></a>Viitteet

- [Työnkulkujen ja Dataversen integroimisen yleiskuvaus – Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Projektiaikataulun ohjelmointirajapintojen käyttö toimintojen suorittamiseen aikataulutusentiteeteillä](schedule-api-preview.md)
- [Yleiskatsaus pilvityönkuluista – Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Yleistä ratkaisutietoisista työnkuluista – Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
