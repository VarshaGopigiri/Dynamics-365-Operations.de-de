---
title: "Erstellen einer Vorlagenstückliste"
description: "Eine Vorlagenstückliste kann auf viele Arten erstellt werden."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
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
ms.openlocfilehash: a80cf596a3e7c7f08d493a0fb7350fad62d38c3e
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="create-a-template-bom"></a><span data-ttu-id="99b35-103">Erstellen einer Vorlagenstückliste</span><span class="sxs-lookup"><span data-stu-id="99b35-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="99b35-104">Eine Vorlagenstückliste kann auf folgende Arten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="99b35-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="99b35-105">Bei allen Verfahren gilt: Die Felder **Von Datum** und **Bis datum** sind optional und nur zu Informationszwecken vorhanden.</span><span class="sxs-lookup"><span data-stu-id="99b35-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="99b35-106">Manuelles Erstellen einer Vorlagenstückliste</span><span class="sxs-lookup"><span data-stu-id="99b35-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="99b35-107">Klicken Sie auf **Serviceverwaltung** \> **Einstellungen** \> **Serviceobjekte** \> **Vorlagenstücklisten**.</span><span class="sxs-lookup"><span data-stu-id="99b35-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="99b35-108">Drücken Sie STRG+N, um das Formular **Vorlagenstückliste erstellen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="99b35-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="99b35-109">Wählen Sie unter **Stücklistenpositionen aus Referenz kopieren** die Option **Manuell** aus.</span><span class="sxs-lookup"><span data-stu-id="99b35-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="99b35-110">Geben Sie im Feld **Artikelnummer** einen Artikel des Typs **Stückliste** ein.</span><span class="sxs-lookup"><span data-stu-id="99b35-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="99b35-111">Geben Sie im Feld **Name** einen Namen für die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="99b35-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="99b35-112">Geben Sie mithilfe der Felder **Von Datum** und **Bis Datum** ein Datumsintervall an, in dem die Vorlagenstückliste aktiv sein soll.</span><span class="sxs-lookup"><span data-stu-id="99b35-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="99b35-113">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="99b35-113">Click **OK**.</span></span>

<span data-ttu-id="99b35-114">Eine neue leere Vorlagenstückliste wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="99b35-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="99b35-115">Erstellen einer Vorlagenstückliste auf Basis einer anderen Vorlagenstückliste</span><span class="sxs-lookup"><span data-stu-id="99b35-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="99b35-116">Klicken Sie auf **Serviceverwaltung** \> **Einstellungen** \> **Serviceobjekte** \> **Vorlagenstücklisten**.</span><span class="sxs-lookup"><span data-stu-id="99b35-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="99b35-117">Drücken Sie STRG+N, um das Formular **Vorlagenstückliste erstellen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="99b35-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="99b35-118">Wählen Sie unter **Stücklistenpositionen aus Referenz kopieren** die Option **Vorlagenstückliste** aus.</span><span class="sxs-lookup"><span data-stu-id="99b35-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="99b35-119">Wählen Sie im Feld **Referenznummer** eine vorhandene Vorlagenstückliste aus, die in die neue Vorlagenstückliste kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="99b35-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="99b35-120">Geben Sie im Feld **Name** einen Namen für die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="99b35-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="99b35-121">Geben Sie mithilfe der Felder **Von Datum** und **Bis Datum** ein Datumsintervall an, in dem die Vorlagenstückliste aktiv sein soll.</span><span class="sxs-lookup"><span data-stu-id="99b35-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="99b35-122">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="99b35-122">Click **OK**.</span></span>

<span data-ttu-id="99b35-123">Eine neue Vorlagenstückliste wird erstellt. Diese enthält die gleichen Positionen wie die ursprüngliche Vorlagenstückliste.</span><span class="sxs-lookup"><span data-stu-id="99b35-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="99b35-124">Erstellen einer Vorlagenstückliste auf Basis einer Artikelstückliste</span><span class="sxs-lookup"><span data-stu-id="99b35-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="99b35-125">Klicken Sie auf **Serviceverwaltung** \> **Einstellungen** \> **Serviceobjekte** \> **Vorlagenstücklisten**.</span><span class="sxs-lookup"><span data-stu-id="99b35-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="99b35-126">Drücken Sie STRG+N, um das Formular **Vorlagenstückliste erstellen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="99b35-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="99b35-127">Wählen Sie unter die **Stücklistenpositionen aus Referenz kopieren** **Stückliste** aus.</span><span class="sxs-lookup"><span data-stu-id="99b35-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="99b35-128">Wählen Sie im Feld **Referenznummer** eine Stücklistenversion wählen Sie aus.</span><span class="sxs-lookup"><span data-stu-id="99b35-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="99b35-129">Ein Artikel vom Typ "Stückliste" wird in das Feld **Artikelnummer** kopiert.</span><span class="sxs-lookup"><span data-stu-id="99b35-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="99b35-130">Geben Sie im Feld **Name** einen Namen für die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="99b35-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="99b35-131">Geben Sie mithilfe der Felder **Von Datum** und **Bis Datum** ein Datumsintervall an, in dem die Vorlagenstückliste aktiv sein soll.</span><span class="sxs-lookup"><span data-stu-id="99b35-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="99b35-132">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="99b35-132">Click **OK**.</span></span>

<span data-ttu-id="99b35-133">Eine neue Vorlagenstückliste erstellt. Diese enthält die gleichen Positionen, die auch in der unter **Stücklisten** aufgeführten Stückliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="99b35-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="99b35-134">Erstellen einer Vorlagenstückliste auf Basis einer Produktionsstückliste</span><span class="sxs-lookup"><span data-stu-id="99b35-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="99b35-135">Klicken Sie auf **Serviceverwaltung** \> **Einstellungen** \> **Serviceobjekte** \> **Vorlagenstücklisten**.</span><span class="sxs-lookup"><span data-stu-id="99b35-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="99b35-136">Drücken Sie STRG+N, um das Formular **Vorlagenstückliste erstellen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="99b35-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="99b35-137">Wählen Sie unter die **Stücklistenpositionen aus Referenz kopieren** **Produktion** aus.</span><span class="sxs-lookup"><span data-stu-id="99b35-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="99b35-138">Wählen Sie im Feld **Referenznummer** eine Produktions-Stücklistenversion aus.</span><span class="sxs-lookup"><span data-stu-id="99b35-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="99b35-139">Geben Sie im Feld **Name** einen Namen für die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="99b35-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="99b35-140">Geben Sie mithilfe der Felder **Von Datum** und **Bis Datum** ein Datumsintervall an, in dem die Vorlagenstückliste aktiv sein soll.</span><span class="sxs-lookup"><span data-stu-id="99b35-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="99b35-141">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="99b35-141">Click **OK**.</span></span>

<span data-ttu-id="99b35-142">Eine neue Vorlagenstückliste erstellt. Diese enthält die gleichen Positionen, die auch in der unter **Stückliste** aufgeführten Stückliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="99b35-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="99b35-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99b35-143">See also</span></span>

[<span data-ttu-id="99b35-144">Vorlagenstücklisten</span><span class="sxs-lookup"><span data-stu-id="99b35-144">Template BOMs</span></span>](template-boms.md)

  


