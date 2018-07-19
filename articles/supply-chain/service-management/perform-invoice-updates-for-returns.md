---
title: "Ausführen von Rechnungsaktualisierungen für Rücklieferungen"
description: "Diese Funktion unterstützt die Geschäftsprozesse von Organisationen, in denen Rücklieferungen und Aufträge gleichzeitig und von der gleichen Person fakturiert werden sollen."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
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
ms.openlocfilehash: 53ae1c3bda06d07a0ca633981ddd46092eae507e
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---


# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="77e94-103">Ausführen von Rechnungsaktualisierungen für Rücklieferungen</span><span class="sxs-lookup"><span data-stu-id="77e94-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="77e94-104">Eine Rücklieferung ist ein Typ eines Auftrags, der als zurückgegebener Auftrag markiert ist.</span><span class="sxs-lookup"><span data-stu-id="77e94-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="77e94-105">**Daher wird die Listenseite** zum Erzeugen von Rechnungen für Rücklieferungen anstelle des Formulars **Rücklieferungen** verwendet.</span><span class="sxs-lookup"><span data-stu-id="77e94-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="77e94-106">Diese Funktion unterstützt die Geschäftsprozesse von Organisationen, in denen Rücklieferungen und Aufträge gleichzeitig und von der gleichen Person fakturiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="77e94-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="77e94-107">Da die Rechnung für einen zurückgelieferten Artikel einen negativen Betrag ausweist, wird sie als Gutschrift bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="77e94-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="77e94-108">Beim Einrichten der Rechnungsaktualisierung für die Stapelverarbeitung muss für den Auftrag vom Typ **Rücklieferung** der Status der Rückgabeposition **Eingegangen** lauten, womit angezeigt wird, dass der Lieferschein des Auftrags aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="77e94-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="77e94-109">Buchen einer Rechnung für eine Rücklieferung</span><span class="sxs-lookup"><span data-stu-id="77e94-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="77e94-110">Klicken auf **Debitorenkonten** \> **Allgemein** \> **Aufträge** \> **Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="77e94-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="77e94-111">Wählen Sie einen Auftrag aus, für den **rückstendungen** im Feld **Auftragstyp** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="77e94-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="77e94-112">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** auf **Rechnung**.</span><span class="sxs-lookup"><span data-stu-id="77e94-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="77e94-113">Wählen Sie auf der Registerkarte **Parameter** das Kontrollkästchen **Buchung** aus.</span><span class="sxs-lookup"><span data-stu-id="77e94-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="77e94-114">Prüfen Sie die Informationen im Formular, und nehmen Sie ggf. erforderliche Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="77e94-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="77e94-115">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="77e94-115">Click **OK**.</span></span> <span data-ttu-id="77e94-116">Die Gutschrift wird gebucht.</span><span class="sxs-lookup"><span data-stu-id="77e94-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="77e94-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77e94-117">See also</span></span>

[<span data-ttu-id="77e94-118">Lieferscheinaktualisierungen für Rücklieferungen</span><span class="sxs-lookup"><span data-stu-id="77e94-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  


