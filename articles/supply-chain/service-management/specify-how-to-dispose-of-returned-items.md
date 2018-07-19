---
title: "Angeben zur Entsorgung zurückgelieferter Artikel"
description: "Angeben zur Entsorgung zurückgelieferter Artikel."
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventQuarantineOrder
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
ms.openlocfilehash: d25a53ac58b0ab44605af253f174ba2ec7b74174
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="f9770-103">Angeben zur Entsorgung zurückgelieferter Artikel</span><span class="sxs-lookup"><span data-stu-id="f9770-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f9770-104">Wenn Sie eine Rücklieferung verarbeiten, muss mittels eines Ursachencodes angegeben werden warum das Produkt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f9770-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="f9770-105">Sie müssen auch einen Dispositionscode und eine Dispositionsaktivität angeben, um zu bestimmen, wie mit dem zurückgelieferten Produkt verfahren werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9770-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="f9770-106">Ein Dispositionscode kann beim Erstellen der Rücklieferung, beim Erfassen des Wareneingangs oder beim Ausführen einer Lieferscheinaktualisierung eines Wareneingangs sowie beim Beenden eines Quarantäneauftrags angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9770-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="f9770-107">Sie haben die Möglichkeit zum Erstellen beliebiger Dispositionscodes, die für die verwendeten Geschäftsprozesse benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="f9770-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="f9770-108">In der folgenden Tabelle finden Sie eine Reihe häufig verwendeter Codes für die Disposition zurückgelieferter Artikel:</span><span class="sxs-lookup"><span data-stu-id="f9770-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9770-109">Dispositionstyp</span><span class="sxs-lookup"><span data-stu-id="f9770-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="f9770-110">Allgemeiner Code</span><span class="sxs-lookup"><span data-stu-id="f9770-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="f9770-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9770-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9770-112">Abgang</span><span class="sxs-lookup"><span data-stu-id="f9770-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="f9770-113">AV</span><span class="sxs-lookup"><span data-stu-id="f9770-113">SC</span></span></p></td>
<td><p><span data-ttu-id="f9770-114">Ausschuss/Vernichtung</span><span class="sxs-lookup"><span data-stu-id="f9770-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9770-115">Abgang</span><span class="sxs-lookup"><span data-stu-id="f9770-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="f9770-116">WZ</span><span class="sxs-lookup"><span data-stu-id="f9770-116">DC</span></span></p></td>
<td><p><span data-ttu-id="f9770-117">Spende für wohltätige Zwecke</span><span class="sxs-lookup"><span data-stu-id="f9770-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9770-118">Abgang</span><span class="sxs-lookup"><span data-stu-id="f9770-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="f9770-119">ED</span><span class="sxs-lookup"><span data-stu-id="f9770-119">TD</span></span></p></td>
<td><p><span data-ttu-id="f9770-120">Entsorgung durch Dritte</span><span class="sxs-lookup"><span data-stu-id="f9770-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9770-121">Abgang</span><span class="sxs-lookup"><span data-stu-id="f9770-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="f9770-122">AM</span><span class="sxs-lookup"><span data-stu-id="f9770-122">SL</span></span></p></td>
<td><p><span data-ttu-id="f9770-123">Altmaterial</span><span class="sxs-lookup"><span data-stu-id="f9770-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9770-124">Abgang</span><span class="sxs-lookup"><span data-stu-id="f9770-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="f9770-125">VD</span><span class="sxs-lookup"><span data-stu-id="f9770-125">TS</span></span></p></td>
<td><p><span data-ttu-id="f9770-126">Verkauf durch Dritte (Sekundärmärkte)</span><span class="sxs-lookup"><span data-stu-id="f9770-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9770-127">Reparatur/Abänderung</span><span class="sxs-lookup"><span data-stu-id="f9770-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="f9770-128">NB</span><span class="sxs-lookup"><span data-stu-id="f9770-128">RW</span></span></p></td>
<td><p><span data-ttu-id="f9770-129">Nachbesserung</span><span class="sxs-lookup"><span data-stu-id="f9770-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9770-130">Reparatur/Abänderung</span><span class="sxs-lookup"><span data-stu-id="f9770-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="f9770-131">AÜ</span><span class="sxs-lookup"><span data-stu-id="f9770-131">RF</span></span></p></td>
<td><p><span data-ttu-id="f9770-132">Aufbereitung/Überholung</span><span class="sxs-lookup"><span data-stu-id="f9770-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9770-133">Reparatur/Abänderung</span><span class="sxs-lookup"><span data-stu-id="f9770-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="f9770-134">AÄ</span><span class="sxs-lookup"><span data-stu-id="f9770-134">MD</span></span></p></td>
<td><p><span data-ttu-id="f9770-135">Abänderung</span><span class="sxs-lookup"><span data-stu-id="f9770-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9770-136">Reparatur/Abänderung</span><span class="sxs-lookup"><span data-stu-id="f9770-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="f9770-137">RP</span><span class="sxs-lookup"><span data-stu-id="f9770-137">RP</span></span></p></td>
<td><p><span data-ttu-id="f9770-138">Reparatur</span><span class="sxs-lookup"><span data-stu-id="f9770-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9770-139">Reparatur/Abänderung</span><span class="sxs-lookup"><span data-stu-id="f9770-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="f9770-140">RK</span><span class="sxs-lookup"><span data-stu-id="f9770-140">RV</span></span></p></td>
<td><p><span data-ttu-id="f9770-141">Rücklieferung an Kreditor</span><span class="sxs-lookup"><span data-stu-id="f9770-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9770-142">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="f9770-142">Other</span></span></p></td>
<td><p><span data-ttu-id="f9770-143">KÄ</span><span class="sxs-lookup"><span data-stu-id="f9770-143">AI</span></span></p></td>
<td><p><span data-ttu-id="f9770-144">Keine Änderung</span><span class="sxs-lookup"><span data-stu-id="f9770-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9770-145">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="f9770-145">Other</span></span></p></td>
<td><p><span data-ttu-id="f9770-146">WV</span><span class="sxs-lookup"><span data-stu-id="f9770-146">RS</span></span></p></td>
<td><p><span data-ttu-id="f9770-147">Wiederverkauf</span><span class="sxs-lookup"><span data-stu-id="f9770-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9770-148">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="f9770-148">Other</span></span></p></td>
<td><p><span data-ttu-id="f9770-149">AT</span><span class="sxs-lookup"><span data-stu-id="f9770-149">EX</span></span></p></td>
<td><p><span data-ttu-id="f9770-150">Austausch</span><span class="sxs-lookup"><span data-stu-id="f9770-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9770-151">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="f9770-151">Other</span></span></p></td>
<td><p><span data-ttu-id="f9770-152">SO</span><span class="sxs-lookup"><span data-stu-id="f9770-152">MS</span></span></p></td>
<td><p><span data-ttu-id="f9770-153">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="f9770-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f9770-154">Für jeden Dispositionscode, den Sie definieren, müssen Sie eine Dispositionsaktivität auswählen.</span><span class="sxs-lookup"><span data-stu-id="f9770-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="f9770-155">Die Dispositionsaktivität bestimmt die physischen und die finanziellen Auswirkungen der Dispositionscodes.</span><span class="sxs-lookup"><span data-stu-id="f9770-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="f9770-156">Beispielsweise bestimmt die Dispositionsaktivität die physische Handhaben der zurückgelieferten Artikel, die finanziellen Auswirkungen des zurückgegebenen Artikels und wenn ein Ersetzungsartikel an den Debitor gesendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="f9770-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="f9770-157">Sie können eine unbegrenzte Anzahl Dispositionscodes gemäß Ihren Geschäftsanforderungen definieren, es bestehen jedoch nur sechs vordefinierte Dispositionsaktivitäten, von denen Sie auswählen können.</span><span class="sxs-lookup"><span data-stu-id="f9770-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="f9770-158">Die folgende Tabelle enthält die Dispositionsaktivitäten und deren Definitionen.</span><span class="sxs-lookup"><span data-stu-id="f9770-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9770-159">Dispositionsaktivität</span><span class="sxs-lookup"><span data-stu-id="f9770-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="f9770-160">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9770-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9770-161"><strong>Entlastung</strong></span><span class="sxs-lookup"><span data-stu-id="f9770-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="f9770-162">Den Artikel zum Lager zurücksenden und dem Debitor gutschreiben.</span><span class="sxs-lookup"><span data-stu-id="f9770-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9770-163"><strong>Nur gutschreiben</strong></span><span class="sxs-lookup"><span data-stu-id="f9770-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="f9770-164">Schreiben Sie den Artikel dem Debitor gut, ohne den Artikel einzufordern oder zu erwarten, dass er zurückgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="f9770-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9770-165"><strong>Ausschuss</strong></span><span class="sxs-lookup"><span data-stu-id="f9770-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="f9770-166">Verschrotten Sie den Artikel und schreiben Sie ihn dem Debitor gut.</span><span class="sxs-lookup"><span data-stu-id="f9770-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9770-167"><strong>Ersatz und Entlastung</strong></span><span class="sxs-lookup"><span data-stu-id="f9770-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="f9770-168">Geben Sie den Artikel dem Lager zurück, erstellen Sie einen Ersetzungsauftrag und schreiben Sie ihn dem Debitor gut.</span><span class="sxs-lookup"><span data-stu-id="f9770-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9770-169"><strong>Ersatz und Aussonderung</strong></span><span class="sxs-lookup"><span data-stu-id="f9770-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="f9770-170">Verschrotten Sie den Artikel, erstellen Sie einen Ersetzungsauftrag und schreiben Sie ihn dem Debitor gut.</span><span class="sxs-lookup"><span data-stu-id="f9770-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9770-171"><strong>Rückgabe an den Debitor</strong></span><span class="sxs-lookup"><span data-stu-id="f9770-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="f9770-172">Lehnen Sie den zurückgesendeten Artikel ab und senden Sie ihn dem Debitor zurück.</span><span class="sxs-lookup"><span data-stu-id="f9770-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="f9770-173">Auswählen eines Dispositionscodes für einen Quarantäneauftrag</span><span class="sxs-lookup"><span data-stu-id="f9770-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="f9770-174">Klicken Sie auf **Lagerverwaltung** \> **Periodisch** \> **Qualitätsmanagement** \> **Quarantäneaufträge**.</span><span class="sxs-lookup"><span data-stu-id="f9770-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="f9770-175">Wählen Sie für einen vorhandenen Quarantäneauftrag auf der Registerkarte **Übersicht** im Feld **Dispositionscode** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="f9770-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="f9770-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9770-176">See also</span></span>

<span data-ttu-id="f9770-177">[Formular "Quarantäneauftrag"](https://technet.microsoft.com/en-us/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="f9770-177">[Quarantine order (form)](https://technet.microsoft.com/en-us/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="f9770-178">[Dispositionscodes (Formular)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="f9770-178">[Disposition codes (form)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span></span>

  


