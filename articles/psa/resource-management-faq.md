---
title: Resurssienhallinta UKK
description: Tässä aiheessa on vastauksia usein kysyttyihin kysymyksiin resurssienhallinnasta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075559"
---
# <a name="resource-management-faq"></a>Resurssienhallinta UKK

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Mitä eroa on ryhmän jäsenellä ja resurssitarpeella?

Projektiryhmän jäsen voidaan kohdentaa tehtäviin, varata tai ylivarata ja määrittää hyväksyjäksi. Resurssivaatimus voi olla olemassa ilman projektiryhmän jäsentä alustavana kysyntähuomautuksena. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Mitä eroa on ehdotetuilla ja alustavasti varatuilla tunneilla?

Ehdotetut tunnit ja alustavasti varatut tunnit eroavat näkyvyydessä. Ehdotetut tunnit näkyvät vain resurssi -ja projektipäällikköille, jotka ovat luoneen kysynnän resurssipyynnön avulla. Alustavasti varatut tunnit näkyvät kaikille, joilla on pääsy aikataulutaulukkoon.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Miten voin nähdä ryhmän resurssien alustavasti varatut tunnit?

Alustavia varauksia voidaan tehdä resurssitarvetta varattaessa. Resurssit, jotka on alustavasti varattu projektiryhmään, näkyvät ryhmän jäseninä, joilla on alustavasti varattuja tunteja. Ne näkyvät myös aikataulutaulukossa.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Kuinka voin muuttaa vaaditut tunnit ja aloitus- ja lopetuspäivämäärät resurssille (yleiselle tai nimetylle), jonka varasin?

Kun resurssit on varattu, valitse **Ylläpidä varauksia** tehdäksesi tarvittavat muutokset.

## <a name="what-resources-types-does-project-service-automation-support"></a>Mitä resurssityyppejä Project Service Automation tukee?

**Käyttäjä** ja **Yhteyshenkilö** ovat ainoita resurssityyppejä, joita tuetaan ohjelmassa Dynamics 365 Project Service Automation. Vaikka onkin mahdollista luoda muuntyyppisiä resursseja (esimerkiksi **Välineitä** ja **Ryhmiä** ), niitä varten ei tueta mitään päästä päähän -käyttötapauksia.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Mitä eroa on kohdennuksella ja varauksella?

Kohdennukset ovat resurssien kohdennuksia projektitehtäviin projektiaikataulussa. Resurssit voivat olla joko todellisia tai yleisiä resursseja. Varaukset ovat resurssien sitovia tai alustavia jakoja projekteihin. Sitovat varaukset kuluttavat resurssin kapasiteettia. Ihannetapauksessa todellisille resursseilla varausten ja kohdennusten tulisi olla ristiriidattomia, koska niissä ei ole eroja. PSA ei kuitenkaan pakota tähän yhteensopivuuteen. Täsmäytysnäkymä näyttää projektipäällikölle kohteet, joissa resurssin varaukset ja kohdennukset eivät täsmää.
