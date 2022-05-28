---
title: Laskutusprosessin yleiskatsaus
description: Tässä aiheessa on tietoja laskutuksesta Project Operationsissa resurssi-/ei-varastoitavissa skenaarioissa.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 0328d5321909bcc17754da4e19d7652b77a665d5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582706"
---
# <a name="invoicing-process-overview"></a>Laskutusprosessin yleiskatsaus

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Project Operations resursseihin ja ei-varastoitaviin perustuvat skenaariot tarjoaa kattavat ominaisuudet, jotka on räätälöity projektipäällikön ja myyntireskontraa hoitavan sihteerin tai projektin kirjanpitäjän tarpeisiin. Laskutusta varten projektipäällikkö hallinnoi projektin keskeneräistä laskutusta ja myyntireskontraa hoitava sihteeri tai projektin kirjanpitäjä luo vaatimustenmukaisen ja tarkan asiakkaalle toimitettavan laskuasiakirjan.

![Laskutuksen vuokaavio.](./media/invoicing-flow.png)

Projektisopimusrivi määrittää liittyvien projektitapahtumien laskutustavan. Kun projektipäällikkö hyväksyy aika- ja kulutapahtumat, järjestelmä kirjaa tapahtumat **Projektin toteutuneet arvot** -kohteeseen ja lähettää tiedot Dynamics 365 Financen **Projektinhallinta ja kirjanpito** -moduuliin. Tämän jälkeen projektin kirjanpitäjä tarkistaa ja kirjaa tietueet käyttämällä [Project Operationsin integroinnin](../project-accounting/project-operations-integration-journal.md) kirjauskansiota. Tämä kirjauskansio sisältää projektin toteutuneiden arvojen tärkeät kirjanpitotiedot, kuten laskutuksen, arvonlisäveroryhmän, laskutusnimikkeen arvonlisäveroryhmän ja taloushallinnon dimensiot.

Projektipäällikkö voi tarkastella laskuttamattomia myyntitapahtumia käyttämällä ajan ja materiaalin laskutustapaa [Ajan ja materiaalien laskutuksen jonossa](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) ja kiinteän hinnan laskutusta [Kiinteän hinnan välitavoitteissa](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Näiden näkymien avulla voit suodattaa ja valita tapahtumat, jotka on sisällytettävä seuraavaan laskutusjaksoon, ja merkitä ne **valmiiksi laskuttamista varten**.

Voit luoda [proformalaskun manuaalisesti](../proforma-invoicing/create-manual-proforma-invoice.md) tai käyttää [kausittaista prosessia](../proforma-invoicing/configure-automated-invoice-creation.md). Projektipäällikkö voi [muokata proformalaskuluonnosta](../proforma-invoicing/manage-proforma-invoice.md) tarpeen mukaan ja vahvistaa sen.

Vahvistettu proformalasku lähetetään Financen **Projektinhallinta ja kirjanpito** -moduuliin. Projektin kirjanpitäjä muotoilee ja päivittää projektilaskuehdotuksen ja kirjaa ja tulostaa sitten asiakirjan. Kirjatit projektilaskut tallennetaan pääkirjaan sekä asiakkaan ja projektin alakirjanpitoon.


[!INCLUDE[footer-include](../includes/footer-banner.md)]