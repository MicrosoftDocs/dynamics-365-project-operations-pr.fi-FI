---
title: Projektien aikataulutuslokit
description: Tässä artikkelissa on tietoja ja esimerkkejä, joiden avulla voidaan seurata projektin aikataulutuslokien avulla projektin aikataulutuspalvelun ja projektin aikataulutuksen ohjelmointirajapintoihin liittyviä virheitä.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923691"
---
# <a name="project-scheduling-logs"></a>Projektien aikataulutuslokit

_**Koskee seuraavaa:** Project Operations resursseihin/ei-varastoitaviin perustuville skenaarioille, lite-käyttöönotto - tarjouksesta proformalaskutukseen_, _Project for the web_

Microsoft Dynamics 365 Project Operations käyttää [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) -sovellusta ensisijaisena aikataulutusmoduulina. Project Operations ei käytä vakiomuotoisia Microsoft Dataverse -WWW-sovellusten ohjelmointirajapintoja vaan uusien projektien aikataulutuksen ohjelmointirajapintoja projektitehtävien, resurssin määritysten, tehtävien riippuvuuksien, projektipäälliköiden ja projektiryhmien jäsenten luomiseen, päivittämiseen ja poistamiseen. Virheitä voi kuitenkin ilmetä, kun luonti-, päivitys- tai poistotoimintoja suoritetaan ohjelmallisesti työrakenteen entiteeteille. Jotta näitä virheitä ja toimintojen historiaa voidaan seurata, on otettu käyttöön kaksi uutta hallintalokia: **Operation Set** ja **Project Scheduling Service (PSS)**. Jos haluat käyttää näitä lokeja, siirry kohtaan **Asetukset** \> **aikataulutuksen integrointi**.

Seuraavassa kuvassa on projektiaikataulutuslokin tietomalli.

![Projektin aikataulutuslokien tietomalli.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Toimintojen asetusloki

Toimintojoukkoloki seuraa sellaisen toimintojoukon suorittamista, jota käytetään yhden tai usean projektin luonti-, päivitys- tai poistotoimintojen suorittamiseen projekti-, projektitehtävä-, resurssimääritys-, tehtävien riippuvuus, projektisäilöjen tai projektiryhmän jäsenten erää varten. **Toiminto tilassa** -kentässä näkyy toimintojoukon yleinen tila. Toimintojoukon tietojen tiedot tallennetaan liittyviin toimintojoukon tietotietueisiin.

### <a name="operation-set"></a>Toimintojoukko

Seuraavassa taulukossa on kentät, jotka liittyvät **Toimintojoukko**-entiteetissä.

| Rakenteen nimi            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Päivämäärä/kellonaika, jona toimintojoukko on valmistunut tai epäonnistunut.                                                | CompletedOn            |
| msdyn_correlationid   | Pyynnön **correlationId**-arvo.                                                                  | CorrelationId          |
| msdyn_description     | Asetusjoukon kuvaus.                                                                        | Description            |
| msdyn_executedon      | Päivämäärä/aika, jolloin tietue suoritettiin.                                                                       | Suoritettu            |
| msdyn_operationsetId  | Entiteettiesiintymien yksilöllinen tunnus.                                                                   | OperationSet           |
| msdyn_Project         | Projekti, joka liittyy toimintojoukkoon.                                                            | Project                |
| msdyn_projectid       | Pyynnön **projectId**-arvo.                                                                      | ProjectId (vanhentunut) |
| msdyn_projectName     | Ei käytettävissä.                                                                                              | Ei käytettävissä         |
| msdyn_PSSErrorLog     | Toimintojoukkoon liittyvän projektiajoituspalvelun virhelokin yksilöllinen tunnus. | PSS-virheloki          |
| msdyn_PSSErrorLogName | Ei käytettävissä.                                                                                              | Ei käytettävissä         |
| msdyn_status          | Asetusjoukon tila.                                                                             | Status                 |
| msdyn_statusName      | Ei käytettävissä.                                                                                              | Ei käytettävissä         |
| msdyn_useraadid       | Sen käyttäjän Azure Active Directory (Azure AD) -objektin tunnus, jolle tämä pyyntö kuuluu.                     | UserAADID              |

### <a name="operation-set-detail"></a>Toimintojoukon tieto

Seuraavassa taulukossa on kentät, jotka liittyvät **Toimintojoukon tieto** -entiteetissä.

| Rakenteen nimi                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Sarjoitetut Dataverse-kentät pyyntöä varten.                                            | CdsPayload            |
| msdyn_entityname           | Entiteetin nimi pyyntöä varten.                                                     | EntityName            |
| msdyn_httpverb             | Pyyntömenetelmä.                                                                         | HTTP-verbi (vanhentunut) |
| msdyn_httpverbName         | Ei käytettävissä.                                                                             | Ei käytettävissä        |
| msdyn_operationset         | Sen toimintokohteen yksilöivä tunnus, johon tämä tietue kuuluu.                      | OperationSet          |
| msdyn_operationsetdetailId | Entiteettiesiintymien yksilöllinen tunnus.                                                  | OperationSet-kohteen tiedot   |
| msdyn_operationsetName     | Ei käytettävissä.                                                                             | Ei käytettävissä        |
| msdyn_operationtype        | Toimintojoukon tietojen toimintotyyppi.                                             | OperationType         |
| msdyn_operationtypeName    | Ei käytettävissä.                                                                             | Ei käytettävissä        |
| msdyn_psspayload           | Pyynnön sarjoitetut Projektin aikataulutuspalvelu -kentät.                           | PssPayload            |
| msdyn_recordid             | Pyyntötietueen tunniste.                                                       | Tietuetunnus             |
| msdyn_requestnumber        | Automaattisesti luotu numero, joka yksilöi järjestyksen, jossa pyynnöt vastaanotettiin. | Pyynnön numero        |

## <a name="project-scheduling-service-error-logs"></a>Projektin aikataulutuspalvelun virhelokit

Projektin aikataulutuspalvelun virhelokien avulla voidaan siepata virheitä, jotka ilmenevät, kun projektin aikataulutuspalvelu yrittää **tallentaa** tai **avata** toiminnon. Seuraavissa kolmessa tuetussa skenaariossa luodaan seuraavat lokit:

- Käyttäjän käynnistäneet toiminnot epäonnistuvat kriittisesti (esimerkiksi määritystä ei voi luoda puuttuvien oikeuksien vuoksi).
- Projektin aikataulutuspalvelu ei voi luoda, päivittää, poistaa tai suorittaa entiteetille mitään toista johdannaistoimintoa.
- Käyttäjällä on virheitä, kun tietueen avautuminen epäonnistuu (esimerkiksi projekti avataan tai ryhmän jäsenen tiedot päivitetään).

### <a name="project-scheduling-service-log"></a>Projektin aikataulutuspalveluloki

Seuraavassa taulukossa on kentät, jotka kuuluvat projektin aikataulutuspalvelulokiin.

| Rakenteen nimi          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Poikkeuksen kutsupino.                                               | Kutsupino     |
| msdyn_correlationid | Virheen korrelointitunnus.                                               | CorrelationId  |
| msdyn_errorcode     | Kenttä, jossa on Dataverse-virhekoodi tai HTTP-virhekoodi. | Virhekoodi     |
| msdyn_HelpLink      | Linkki julkiseen ohjedokumentaatioon.                                       | Ohjelinkki      |
| msdyn_log           | Projektin aikataulutuspalvelun loki.                                   | Loki            |
| msdyn_project       | Projekti, joka liittyy virhelokiin.                             | Project        |
| msdyn_projectName   | Projektin nimi, jos toimintojoukon tiedot säilyvät. | Ei käytettävissä |
| msdyn_psserrorlogId | Entiteettiesiintymien yksilöllinen tunnus.                                     | PSS-virheloki  |
| msdyn_SessionId     | Projektin istuntotunnus.                                                        | Istunnon tunnus     |

## <a name="error-log-cleanup"></a>Virhelokin tyhjennys

Sekä projektien aikataulutuspalvelun virhelokit että toimintojoukon lokit voidaan palauttaa 90 päivän välein. Kaikki yli 90 päivää vanhemmat tietueet poistetaan. Muuttamalla **Projektiparametrit**-sivun **msdyn_StateOperationSetAge**-kentän arvoa järjestelmänvalvojat voivat kuitenkin muuttaa puhdistusaluetta niin, että se on 1–120 päivää. Tämän arvon muuttamiseen on käytettävissä useita menetelmiä:

- Mukauta **Projektiparametri**-entiteetti luomalla mukautettu sivu ja lisäämällä **Vanhentuneiden projektien asetettu ikä** -kenttä.
- Käytä asiakaskoodia, joka käyttää [WebApi Software Development Kit (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord) -pakettia.
- Käytä Service SDK -koodia, joka käyttää Xrm SDK **updateRecord**-menetelmää (asiakasohjelmointirajapintaviitettä) mallipohjaisessa sovelluksissa. Power Apps sisältää **updateRecord**-menetelmän kuvauksen ja tuetut parametrit.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
