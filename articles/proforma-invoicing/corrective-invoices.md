---
title: Korjatut laskut
description: Tässä aiheessa on tietoja korjatuista laskuista.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122384"
---
# <a name="corrected-invoices"></a><span data-ttu-id="807e0-103">Korjatut laskut</span><span class="sxs-lookup"><span data-stu-id="807e0-103">Corrected invoices</span></span>

<span data-ttu-id="807e0-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="807e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="807e0-105">Vahvistettuja laskuja voidaan muokata.</span><span class="sxs-lookup"><span data-stu-id="807e0-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="807e0-106">Kun muokkaat vahvistettua laskua, korjatusta laskusta luodaan luonnos.</span><span class="sxs-lookup"><span data-stu-id="807e0-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="807e0-107">Koska oletuksena on, että haluat kumota kaikki alkuperäisen laskun tapahtumat ja määrät, tämä korjattu lasku sisältää kaikki alkuperäisen laskun tapahtumat ja kaikki siinä olevat määrät ovat nollia (0).</span><span class="sxs-lookup"><span data-stu-id="807e0-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="807e0-108">Jos jotkin tapahtumat eivät vaadi korjausta, voit poistaa ne korjaavasta laskuluonnoksesta.</span><span class="sxs-lookup"><span data-stu-id="807e0-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="807e0-109">Jos haluat kumota tai palauttaa vain osamäärän, voit muokata rivin tietojen Määrä-kenttää.</span><span class="sxs-lookup"><span data-stu-id="807e0-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="807e0-110">Voit tarkastella alkuperäisen laskun määrää avaamalla laskurivin tiedot.</span><span class="sxs-lookup"><span data-stu-id="807e0-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="807e0-111">Tämän jälkeen voit muokata nykyisen laskun määrää siten, että se ylittää tai alittaa alkuperäisen laskun määrän.</span><span class="sxs-lookup"><span data-stu-id="807e0-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="807e0-112">Kun vahvistat korjaavan laskun, alkuperäinen laskutetun myynnin todellinen arvo kumotaan ja uusi laskutetun myynnin todellinen arvo luodaan.</span><span class="sxs-lookup"><span data-stu-id="807e0-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="807e0-113">Jos määrää vähennettiin, ero aiheuttaa myös uuden laskuttamattoman myynnin todellisen arvon luomiseen.</span><span class="sxs-lookup"><span data-stu-id="807e0-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="807e0-114">Jos alkuperäinen laskutettu myynti esimerkiksi oli kahdeksan tuntia ja korjattujen laskurivien tietojen määrä on vain kuusi tuntia, alkuperäisen laskutetun myynnin rivi peruutetaan ja seuraavat kaksi uutta todellista arvoa luodaan:</span><span class="sxs-lookup"><span data-stu-id="807e0-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="807e0-115">Laskutetun myynnin todellisen arvon kuudelle tunnille.</span><span class="sxs-lookup"><span data-stu-id="807e0-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="807e0-116">Laskuttamattoman myynnin todellisen arvon kahdelle jäljelle jääneelle tunnille.</span><span class="sxs-lookup"><span data-stu-id="807e0-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="807e0-117">Tämä tapahtuma voidaan joko laskuttaa myöhemmin tai merkitä ei-veloitettavaksi riippuen siitä, mitä asiakkaan kanssa sovitaan.</span><span class="sxs-lookup"><span data-stu-id="807e0-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
