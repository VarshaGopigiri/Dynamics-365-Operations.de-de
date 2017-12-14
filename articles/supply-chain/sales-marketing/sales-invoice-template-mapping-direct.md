---
title: Verkaufsrechnungskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren
description: "Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e9d7e756c56932372ed931620016973c794fb3fc
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="fb417-103">Verkaufsrechnungskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="fb417-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fb417-104">Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="fb417-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="fb417-105">Datenfluss in Interessent nach Bargeld</span><span class="sxs-lookup"><span data-stu-id="fb417-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="fb417-106">Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Finance and Operations und Sales hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="fb417-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="fb417-107">Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Finance and Operations und Sales.</span><span class="sxs-lookup"><span data-stu-id="fb417-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="fb417-108">Die folgende Abbildung zeigt, wie Daten zwischen Finance and Operations und Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="fb417-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="fb417-109">[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="fb417-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="fb417-110">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="fb417-110">Templates and tasks</span></span>

<span data-ttu-id="fb417-111">Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [PowerApps-Administrator-Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="fb417-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="fb417-112">Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="fb417-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="fb417-113">Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Rechnungskopfzeilen und -positionen von Finance and Operations mit Sales zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="fb417-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="fb417-114">**Name der Vorlage in der Datenintegration:** Verkaufsrechnungen (Finance and Operations zu Sales) - direkt</span><span class="sxs-lookup"><span data-stu-id="fb417-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="fb417-115">**Namen der Aufgaben im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="fb417-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="fb417-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="fb417-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="fb417-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="fb417-117">SalesInvoiceLine</span></span>

<span data-ttu-id="fb417-118">Die folgenden Synchronisierungsaufgaben sind erforderlich, bevor die Synchronisierung von Rechnungskopfzeilen und -positionen erfolgen kann:</span><span class="sxs-lookup"><span data-stu-id="fb417-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="fb417-119">Produkte (Finance and Operations nach Sales) - Direkt</span><span class="sxs-lookup"><span data-stu-id="fb417-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="fb417-120">Konten (Sales nach Finance and Operations) - Direkt (wenn verwendet)</span><span class="sxs-lookup"><span data-stu-id="fb417-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="fb417-121">Kontakte (Sales nach Finance and Operations) - Direkt (wenn verwendet)</span><span class="sxs-lookup"><span data-stu-id="fb417-121">Contacts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="fb417-122">Auftragskopf und -positionen (Finance and Operations nach Sales) - Direkt</span><span class="sxs-lookup"><span data-stu-id="fb417-122">Sales order header and lines (Fin and Ops to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="fb417-123">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="fb417-123">Entity set</span></span>

| <span data-ttu-id="fb417-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fb417-124">Finance and Operations</span></span>                               | <span data-ttu-id="fb417-125">Vertrieb</span><span class="sxs-lookup"><span data-stu-id="fb417-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="fb417-126">Extern gepflegte Debitorenverkaufsrechnungs-Kopfzeilen</span><span class="sxs-lookup"><span data-stu-id="fb417-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="fb417-127">Rechnungen</span><span class="sxs-lookup"><span data-stu-id="fb417-127">Invoices</span></span>       |
| <span data-ttu-id="fb417-128">Extern gepflegte Debitorenverkaufsrechnungs-Positionen</span><span class="sxs-lookup"><span data-stu-id="fb417-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="fb417-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="fb417-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="fb417-130">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="fb417-130">Entity flow</span></span>

<span data-ttu-id="fb417-131">Verkaufsrechnungen werden in Finance and Operations erstellt und mit Sales synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="fb417-131">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="fb417-132">Die Steuer für Belastungen auf dem Verkaufsrechnungskopf ist derzeit nicht in der Synchronisierung von Finance and Operations mit Sales enthalten.</span><span class="sxs-lookup"><span data-stu-id="fb417-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="fb417-133">Sales unterstützt keine Steuerinformationen auf Kopfebene.</span><span class="sxs-lookup"><span data-stu-id="fb417-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="fb417-134">Allerdings sind Steuern, die den Belastungen auf Positionsebene zugeordnet sind, in die Synchronisierung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="fb417-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="fb417-135">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="fb417-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="fb417-136">Ein Feld **Rechnungsnummer** wurde zur Entität **Rechnung** hinzugefügt und wird auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fb417-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="fb417-137">Die Schaltfläche **Rechnung erstellen** auf der Seite **Auftrag** ist ausgeblendet, da Rechnungen in Finance and Operations erstellt und mit Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="fb417-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="fb417-138">Die Seite **Rechnung** kann nicht geändert werden, da Rechnungen über Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="fb417-138">The **Invoice** page can't be edited, because invoices will be synchronized from Finance and Operations.</span></span>
- <span data-ttu-id="fb417-139">Der **Auftragsstatus**-Wert wird automatisch in **Fakturiert** geändert, wenn die zugehörige Rechnung aus Finance and Operations mit Sales synchronisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="fb417-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Finance and Operations has been synchronized to Sales.</span></span> <span data-ttu-id="fb417-140">Darüber hinaus wird der Eigentümer des Auftrags, aufgrund dessen die Rechnung erstellt wurde, als Eigentümer der Rechnung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="fb417-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="fb417-141">Daher kann der Besitzer des Auftrags die Rechnung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="fb417-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="fb417-142">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="fb417-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="fb417-143">Vor dem Synchronisieren von Rechnungen müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:</span><span class="sxs-lookup"><span data-stu-id="fb417-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="fb417-144">Einrichtung in Sales</span><span class="sxs-lookup"><span data-stu-id="fb417-144">Setup in Sales</span></span>

<span data-ttu-id="fb417-145">Gehen Sie zu **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Sales**, und überprüfen Sie, ob die folgenden Einstellungen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="fb417-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="fb417-146">Die Option **Systempreisberechnungssystem verwenden** wird auf **Ja** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fb417-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="fb417-147">Das Feld **Rabattberechnungsmethode** wird auf **Positionsartikel** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fb417-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="fb417-148">Einrichtung im Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="fb417-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="fb417-149">SalesInvoiceHeader-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="fb417-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="fb417-150">Vergewissern Sie sich, dass die erforderliche Zuordnung für **InvoiceCountryRegionId** zu **BillingAddress\_Country** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fb417-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="fb417-151">Der Vorlagenwert ist eine Wertzuordnung, in der verschiedene Länder/Regionen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fb417-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="fb417-152">Preisliste ist erforderlich, um Rechnungen in Sales zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb417-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="fb417-153">Aktualisieren Sie die Wertzuordnung für **pricelevelid.name \[Price list name\]** auf die Preisliste, die in Sales pro Währung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fb417-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="fb417-154">Sie können die Standardpreisliste für eine einzelne Währung verwenden.</span><span class="sxs-lookup"><span data-stu-id="fb417-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="fb417-155">Alternativ können Sie, wenn Sie Preislisten in mehreren Währungen haben, eine Zuordnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="fb417-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="fb417-156">Der Vorlagenwert für **pricelevelid.name \[Price list name\]** ist ein Wertzuordnung, die auf Währung mit USD = CRM Service USA (Beispiel) basiert.</span><span class="sxs-lookup"><span data-stu-id="fb417-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="fb417-157">SalesInvoiceLine-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="fb417-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="fb417-158">Vergewissern Sie sich, dass die erforderliche Zuordnung für **Maßeinheit** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fb417-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="fb417-159">tellen Sie sicher, dass die erforderliche Wertzuordnung für **SalesUnitSymbol** in Finance and Operations vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fb417-159">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="fb417-160">Ein Vorlagenwert, der eine Wertzuordnung hat, wird für **SalesUnitSymbol** als **Quantity\_UOM** definiert.</span><span class="sxs-lookup"><span data-stu-id="fb417-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="fb417-161">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="fb417-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="fb417-162">Die Felder **Zahlungsbedingungen**, **Frachtbedingungen**, **Lieferbedingungen**, **Liefermethode** und **Bereitstellungsmodus** sind nicht in den Standardzuordnungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="fb417-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="fb417-163">Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="fb417-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="fb417-164">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="fb417-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="fb417-165">Die Zuordnung zeigt, welche Feldinformationen von Sales zu Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="fb417-165">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="fb417-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="fb417-166">SalesInvoiceHeader</span></span>

![Vorlagenzuordnung in Datenintegration](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="fb417-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="fb417-168">SalesInvoiceLine</span></span>

![Vorlagenzuordnung in Datenintegration](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="fb417-170">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="fb417-170">Related topics</span></span>

[<span data-ttu-id="fb417-171">Interessent zu Bargeld</span><span class="sxs-lookup"><span data-stu-id="fb417-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="fb417-172">Konten von Sales direkt mit Debitoren in Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="fb417-172">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="fb417-173">Produkte direkt von Finance and Operations mit Produkten in Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="fb417-173">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="fb417-174">Kontakte direkt von Sales mit Kontakten oder Debitoren in Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="fb417-174">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="fb417-175">Auftragskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="fb417-175">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)






