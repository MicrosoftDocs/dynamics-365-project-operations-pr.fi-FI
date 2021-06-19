---
title: Sisäisten projektien kirjanpidon määrittäminen
description: Tässä ohjeaiheessa on tietoja siitä, miten projektitoimintojen sisäisten projektien kirjanpitokäytäntöjä määritetään.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012852"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="7f02e-103">Sisäisten projektien kirjanpidon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7f02e-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="7f02e-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="7f02e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7f02e-105">Sisäiset projektit mahdollistavat sen, että yritykset voivat seurata aktiviteetteihin liittyviä kustannuksia, joita ei laskuteta asiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="7f02e-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="7f02e-106">Sisäisiä projekteja ovat esimerkiksi seuraavat:</span><span class="sxs-lookup"><span data-stu-id="7f02e-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="7f02e-107">Tuotteen, kuten mobiilisovelluksen, kehittäminen ja kehitykseen liittyvien kustannusten seuraaminen.</span><span class="sxs-lookup"><span data-stu-id="7f02e-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="7f02e-108">Ennakkomyyntiajan ja -kulujen hallinta.</span><span class="sxs-lookup"><span data-stu-id="7f02e-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="7f02e-109">Tämä ennakkomyynnin sisäinen projekti voidaan muuntaa myöhemmin laskutettavaksi projektiksi, jos tarjous on voitettu.</span><span class="sxs-lookup"><span data-stu-id="7f02e-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="7f02e-110">Projekteja, jotka eivät liity sopimukseen Dynamics 365 Project Operationsissa, käsitellään sisäisinä.</span><span class="sxs-lookup"><span data-stu-id="7f02e-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="7f02e-111">Projektin kustannus- ja tuottoprofiileita ei käytetä määrittämään projektin kirjanpitosääntöjä.</span><span class="sxs-lookup"><span data-stu-id="7f02e-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="7f02e-112">Sisäiset projektikustannukset kirjataan aina käyttämällä voiton ja tappion periaatteita.</span><span class="sxs-lookup"><span data-stu-id="7f02e-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="7f02e-113">Tapahtumarekisterin kirjanpitotilit määritetään **Tapahtumarekisterin kirjauksen asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="7f02e-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="7f02e-114">Aikatapahtumat kirjataan veloittamalla **Kustannus**-tiliä ja hyvittämällä **Palkanlaskennan kohdistus** -tiliä.</span><span class="sxs-lookup"><span data-stu-id="7f02e-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="7f02e-115">Kulutapahtumat kirjataan veloittamalla **Kustannus**-tiliä ja hyvittämällä **Kulujen vastatili** -tiliä.</span><span class="sxs-lookup"><span data-stu-id="7f02e-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="7f02e-116">Nimiketapahtumat kirjataan veloittamalla **Kustannus** -tiliä ja hyvittämällä **Kustannus - nimike** -tilille.</span><span class="sxs-lookup"><span data-stu-id="7f02e-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="7f02e-117">Kun tapahtumat on kirjattu projektiin ja projekti on liitetty projektisopimukseen, järjestelmä peruuttaa kaikki kertyneet tapahtumat ja luo uudet laskutettavat tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="7f02e-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="7f02e-118">Laskutettavat tapahtumat noudattavat kunkin projektin kustannus- ja tuottoprofiilissa määritettyjä kirjanpitosääntöjä.</span><span class="sxs-lookup"><span data-stu-id="7f02e-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
