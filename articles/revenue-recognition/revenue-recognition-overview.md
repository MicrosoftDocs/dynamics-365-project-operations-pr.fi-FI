---
title: Tuoton kirjaamisen yleiskatsaus
description: Tässä artikkelissa on tietoja tuoton kirjaamisesta Project Operationsissa.
author: sigitac
ms.date: 11/16/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 22486693226256f765589b272e6df36aceaf9c1c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926266"
---
# <a name="revenue-recognition-overview"></a>Tuoton kirjaamisen yleiskatsaus

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Dynamics 365 Project Operationsissa tuoton kirjaamisperiaatteet vaihtelevat projektin tai projektin osan valitun laskutustavan mukaan. Tässä artikkelissa on tietoja tuoton kirjaamisesta Project Operationsissa.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Tapahtumat, joista pidetään kirjaa aika ja materiaalit -laskutustapaa käyttäen

- Kustannusten ja tuottojen kirjaaminen liittyvät toisiinsa. Tapahtumakustannukset ja laskuttamattomat myynnit kirjataan [Project Operationsin integrointikirjauskansion](../project-accounting/project-operations-integration-journal.md) avulla.
- Projektin kustannus- ja tuottoprofiili määrittää, kirjataanko laskuttamattomia myyntitapahtumia kirjanpitoon. Jos **Kerrytä tuottoa** on valittuna, järjestelmä käyttää **Käynnissä oleva arvo** - ja **Kerrytetty tuoton myyntiarvo** -tilejä kirjauksen aikana. Seuraava on esimerkki tästä menetelmästä.  

  | Tapahtumatyyppi | Debit/Credit | Summa |
  | --- | --- | --- |
  | Käynnissä oleva myynnin arvo | Debit | 100 |
  | Kerrytetyn tuoton myyntiarvo | Credit | 100 |

- Tuotto kirjataan laskutuksen aikana. Järjestelmä käyttää **Laskutettu tuotto** -tiliä kirjauksen aikana. Seuraava on esimerkki tästä menetelmästä.  

  | Tapahtumatyyppi | Debit/Credit | Summa |
  | --- | --- | --- |
  | Asiakkaan saldo | Debit | 120 |
  | Maksettava arvonlisävero | Credit | 20 |
  | Laskutettu tuotto | Credit | 100 |

- Jos tuottoa kerrytettiin, kun ei-laskutettu myynti kirjataan, järjestelmä peruuttaa kerrytetyn tuoton laskutuksen aikana.

  | Tapahtumatyyppi | Debit/Credit | Summa |
  | --- | --- | --- |
  | Käynnissä oleva myynnin arvo | Credit | 100 |
  | Kerrytetyn tuoton myyntiarvo | Debit | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Tapahtumat, joista pidetään kirjaa kiinteä hinta -laskutustapaa käyttäen

- Kustannusten ja tuottojen kirjaaminen ovat erillisiä. Tapahtumakustannukset kirjataan [Project Operationsin integrointikirjauskansion](../project-accounting/project-operations-integration-journal.md) avulla. Laskuttamattomia myyntitapahtumia ei luoda.
- Tuotto voidaan kirjata laskutuksen aikana, jos projektin kustannus- ja tuottoprofiilien **Projektin valmistumislaskelmiin käytetty periaate** on asetettu arvoksi **Ei käynnissä olevaa**. Käytä tätä menetelmää vain lyhytaikaisia ja yksinkertaisia projekteja varten.
- Tuotto voidaan kirjata käyttämällä kiinteähintaisia tuottoarvioita joko **Valmistunut sopimus** tai **Valmistumisprosenttiin perustuva tuoton kirjaaminen** -menetelmän avulla.

## <a name="additional-resources"></a>Lisäresurssit
[Laskutettavien projektien kirjanpidon määrittäminen -artikkeli](../project-accounting/configure-accounting-billable-projects.md)

[Kiinteähintaisen arvioidun myyntituoton projektit](rev-rec-percentage-completion-method.md)

[Myyntituottoarvioiden hallinta](rev-rec-completed-contract-method.md)

[Valmistumiskustannusmenetelmät](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]