---
title: "Empfangen von Teillieferungen zurückgelieferter Artikel"
description: "Teillieferungen werden in Bezug auf Rücklieferungspositionen und nicht Rücklieferungen definiert."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f9f596d31f2438a353b02bf939786b284937db86
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="36fe7-103">Empfangen von Teillieferungen zurückgelieferter Artikel</span><span class="sxs-lookup"><span data-stu-id="36fe7-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="36fe7-104">Teillieferungen werden in Bezug auf Rücklieferungspositionen und nicht Rücklieferungen definiert.</span><span class="sxs-lookup"><span data-stu-id="36fe7-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="36fe7-105">Dies bedeutet, wenn die in einer Rücklieferungsposition angegebene volle Menge eingeht, jedoch kein Artikel aus den anderen Positionen in der Rücklieferung, dann ist die Lieferung keine Teillieferung.</span><span class="sxs-lookup"><span data-stu-id="36fe7-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="36fe7-106">Um eine Teillieferung handelt es sich dagegen, wenn z. B. laut einer Rücklieferungsposition zehn Einheiten eines bestimmten Artikels zurückgeliefert werden sollen, jedoch nur vier Einheiten eingehen.</span><span class="sxs-lookup"><span data-stu-id="36fe7-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="36fe7-107">Wenn eine Rücklieferung weniger als die volle Menge einer Rücklieferungsposition enthält, können Sie die Lieferung ruhen lassen und auf den Eingang der restlichen zurückgelieferten Menge warten oder die Teillieferung erfassen und buchen.</span><span class="sxs-lookup"><span data-stu-id="36fe7-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="36fe7-108">Erfassen und Buchen einer Teilmenge</span><span class="sxs-lookup"><span data-stu-id="36fe7-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="36fe7-109">Nachdem Sie eine Rücklieferung für den Eingang im Formular **Wareneingangsübersicht - Lagerort: %1: Rampe %2, Erfassungsname: %3** ausgewählt haben, klicken Sie **Wareneingang starten**, um die Wareneingangserfassung zu erstellen, und klicken Sie anschließend **Erfassungen** \> **Wareneingänge aus Zugängen anzeigen**, um das Formular **Lagerplatzerfassung** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="36fe7-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="36fe7-110">Wählen Sie die zu verwendende Erfassungsposition aus, und klicken Sie dann auf **Positionen**, um das Formular **Erfassungspositionen, Lagerplätze** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="36fe7-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="36fe7-111">Wählen Sie die Position der Artikelnummer aus, für die nur eine Teilmenge eingegangen ist, und klicken Sie dann auf  **Funktionen** \> **Teilen**, um das Formular **Teilen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="36fe7-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="36fe7-112"> **Geben Sie im Feld** die Menge für die Gesamtzahl der eingegangenen Artikel ein, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="36fe7-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="36fe7-113">**Wählen Sie im Formular** die Position für die eingegangene Artikelmenge aus, und klicken Sie auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="36fe7-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="36fe7-114">Die Position für die zusätzliche Menge kann nach Eingang der Artikel gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="36fe7-114">You can post the line for the additional quantity after the items have arrived.</span></span>




