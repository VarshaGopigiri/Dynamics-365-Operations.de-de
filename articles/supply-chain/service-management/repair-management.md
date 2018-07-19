---
title: Reparaturverwaltung
description: "Für die Reparaturverwaltung können Probleme systematisch gruppiert werden. Dadurch können Lösungsvorschläge gemacht werden, die bereits in der Vergangenheit funktioniert haben."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
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
ms.openlocfilehash: 937571968c6956ce3dba1427082b298983540f59
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="repair-management"></a><span data-ttu-id="71818-103">Reparaturverwaltung</span><span class="sxs-lookup"><span data-stu-id="71818-103">Repair management</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="71818-104">Für die Reparaturverwaltung können Probleme systematisch gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="71818-104">For repair management you can group problems systematically.</span></span> <span data-ttu-id="71818-105">Dadurch können Lösungsvorschläge gemacht werden, die bereits in der Vergangenheit funktioniert haben.</span><span class="sxs-lookup"><span data-stu-id="71818-105">This is to help with the suggestion of solutions that have been successful in the past.</span></span>

<span data-ttu-id="71818-106">Zu diesem Zweck werden Einstellungen für Symptome, Diagnose und Lösung eingerichtet,</span><span class="sxs-lookup"><span data-stu-id="71818-106">You set up symptoms, diagnosis, and resolution settings.</span></span> <span data-ttu-id="71818-107">die dann später bei der Reparatur ähnlicher Artikel angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="71818-107">All these can later be applied when you receive a similar item for repair.</span></span> <span data-ttu-id="71818-108">Zum Nachverfolgen des Status einer Reparatur können auch Reparaturphasen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="71818-108">You can also set up repair stages that can follow the progress of a repair issue.</span></span>

## <a name="setting-up-repair-management"></a><span data-ttu-id="71818-109">Einrichten der Reparaturverwaltung</span><span class="sxs-lookup"><span data-stu-id="71818-109">Setting up repair management</span></span>

<span data-ttu-id="71818-110">Verwenden Sie die folgenden Einrichtungsformulare, um Informationen über Symptome, Diagnose und Lösung in Bezug auf die Reparatur einzugeben.</span><span class="sxs-lookup"><span data-stu-id="71818-110">Use the following setup forms to enter information that will be used to specify the symptoms, the diagnosis, and the resolution, of the repair.</span></span>

1.  <span data-ttu-id="71818-111">Klicken Sie auf **Serviceverwaltung** \> **Einrichten** \> **Reparatur** \> **Bedingungen**.</span><span class="sxs-lookup"><span data-stu-id="71818-111">Click **Service management** \> **Setup** \> **Repair** \> **Conditions**.</span></span>

2.  <span data-ttu-id="71818-112">Klicken Sie auf **Serviceverwaltung** \> **Einrichten** \> **Reparatur** \> **Symptombereiche**.</span><span class="sxs-lookup"><span data-stu-id="71818-112">Click **Service management** \> **Setup** \> **Repair** \> **Symptom areas**.</span></span>

3.  <span data-ttu-id="71818-113">Klicken Sie auf **Serviceverwaltung** \> **Einrichten** \> **Reparatur** \> **Diagnosebereiche**.</span><span class="sxs-lookup"><span data-stu-id="71818-113">Click **Service management** \> **Setup** \> **Repair** \> **Diagnosis areas**.</span></span>

4.  <span data-ttu-id="71818-114">Klicken Sie auf **Serviceverwaltung** \> **Einrichten** \> **Reparatur** \> **Lösungen**.</span><span class="sxs-lookup"><span data-stu-id="71818-114">Click **Service management** \> **Setup** \> **Repair** \> **Resolutions**.</span></span>

5.  <span data-ttu-id="71818-115">Klicken Sie auf **Serviceverwaltung** \> **Einrichten** \> **Reparatur** \> **Reparaturphasen**.</span><span class="sxs-lookup"><span data-stu-id="71818-115">Click **Service management** \> **Setup** \> **Repair** \> **Repair stages**.</span></span>

## <a name="symptoms-and-conditions"></a><span data-ttu-id="71818-116">Symptome und Bedingungen</span><span class="sxs-lookup"><span data-stu-id="71818-116">Symptoms and conditions</span></span>

<span data-ttu-id="71818-117">Bei den Symptomen handelt es sich um die Problembeschreibung des Kunden.</span><span class="sxs-lookup"><span data-stu-id="71818-117">Symptoms are how the customer characterizes the problem.</span></span> <span data-ttu-id="71818-118">Hierzu zählen auch die Informationen des Kunden zum Grund für die Reparatur.</span><span class="sxs-lookup"><span data-stu-id="71818-118">Symptoms include the customer observations that indicate the need for repair.</span></span>

<span data-ttu-id="71818-119">Für Symptome können Symptombereiche und -codes sowie Bedingungen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="71818-119">You can set up symptom areas, symptom codes, and conditions.</span></span> <span data-ttu-id="71818-120">Der Symptombereich enthält den Bereich der Fehlerfunktion, und der Symptomcode steht für das Symptom der Fehlerfunktion.</span><span class="sxs-lookup"><span data-stu-id="71818-120">The symptom area covers the area of malfunction, and the symptom code covers the malfunction symptom.</span></span> <span data-ttu-id="71818-121">Die Bedingung beschreibt die Situation oder Umgebung, in der das Problem auftritt.</span><span class="sxs-lookup"><span data-stu-id="71818-121">The condition describes the situation or environment that is present when the problem occurs.</span></span>

<span data-ttu-id="71818-122">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="71818-122">**Example**</span></span>

<span data-ttu-id="71818-123">Ein Kunde bringt einen Computer zur Reparatur, da die Festplatte nach längerer Computernutzung ausfällt.</span><span class="sxs-lookup"><span data-stu-id="71818-123">A computer is brought in for repair because the hard drive fails after an extended period of use.</span></span> <span data-ttu-id="71818-124">Der Festplattenausfall verursacht einen Bluescreen-Fehler.</span><span class="sxs-lookup"><span data-stu-id="71818-124">The hard drive failure causes a blue screen error.</span></span> <span data-ttu-id="71818-125">Der Techniker, der den Computer empfängt, gibt folgende Symptome und Bedingungen ein:</span><span class="sxs-lookup"><span data-stu-id="71818-125">The technician who receives the computer enters the following symptoms and conditions:</span></span>

1.  <span data-ttu-id="71818-126">Der Symptombereich ist die Festplatte.</span><span class="sxs-lookup"><span data-stu-id="71818-126">The symptom area is the hard drive</span></span>

2.  <span data-ttu-id="71818-127">Der Symptomcode ist der Bluescreen-Fehler.</span><span class="sxs-lookup"><span data-stu-id="71818-127">The symptom code is the blue screen error</span></span>

3.  <span data-ttu-id="71818-128">Die Bedingung ist, dass die Festplatte nach längerer Computernutzung ausfällt.</span><span class="sxs-lookup"><span data-stu-id="71818-128">The condition is that the hard drive fails after extended use</span></span>

## <a name="diagnosis-and-resolutions"></a><span data-ttu-id="71818-129">Diagnose und Lösungen</span><span class="sxs-lookup"><span data-stu-id="71818-129">Diagnosis and resolutions</span></span>

<span data-ttu-id="71818-130">Die Felder für die Diagnose und die Lösung enthalten Informationen zur Reparatur.</span><span class="sxs-lookup"><span data-stu-id="71818-130">The diagnosis and resolution fields are statements from the repair perspective.</span></span> <span data-ttu-id="71818-131">Hierbei handelt es sich um die Schritte, die von einem Techniker zum Ergründen des Problems ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="71818-131">These are the steps that a technician went through to investigate the problem.</span></span>

<span data-ttu-id="71818-132">Im Diagnosebereich wird der Arbeitsgang angegeben, der zum Beheben des Problems ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="71818-132">The diagnosis area covers the operation that must occur to solve the issue.</span></span> <span data-ttu-id="71818-133">Der Diagnosecode gibt Aufschluss darüber, wie das Problem behandelt wurde. Für die Lösung kann beispielsweise angegeben werden, dass der Artikel repariert oder ausgetauscht wurde oder dass der Kunde den Auftrag storniert hat.</span><span class="sxs-lookup"><span data-stu-id="71818-133">The diagnosis code is how the problem was handled, and the resolution could be that the item was repaired, replaced, or the order was canceled by the customer.</span></span> <span data-ttu-id="71818-134">Für den reparierten Computer können beispielsweise folgende Informationen angegeben werden: Diagnosebereich: "Teil defekt", Diagnosecode: "Einbau einer neuen Grafikkarte", Lösung: "Ausgetauscht".</span><span class="sxs-lookup"><span data-stu-id="71818-134">For example, if the computer is repaired, the diagnosis area could be "defective part," the diagnosis code could be "new video card installed," and the resolution could be "replaced."</span></span>

## <a name="repair-stages"></a><span data-ttu-id="71818-135">Reparaturphasen</span><span class="sxs-lookup"><span data-stu-id="71818-135">Repair stages</span></span>

<span data-ttu-id="71818-136">Anhand von Reparaturphasen lässt sich der Status der Reparatur ablesen.</span><span class="sxs-lookup"><span data-stu-id="71818-136">Repair stages state the progress of the repair process.</span></span> <span data-ttu-id="71818-137">Die Reparaturphase verfügt über den Abzeichnungsparameter **Abgeschlossen**, mit dem angegeben wird, dass die Reparaturposition abgeschlossen ist und Enddatum sowie -zeit erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="71818-137">The repair stage has a **Finished** sign-off parameter that indicates that the repair line has been completed, and the finishing date and time has been recorded.</span></span>

## <a name="applying-repair-management"></a><span data-ttu-id="71818-138">Verwenden der Reparaturverwaltung</span><span class="sxs-lookup"><span data-stu-id="71818-138">Applying repair management</span></span>

<span data-ttu-id="71818-139">Zum Verwenden der Reparaturverwaltung muss der entsprechende Artikel in einem Serviceauftrag mit einer Serviceobjektbeziehung versehen sein.</span><span class="sxs-lookup"><span data-stu-id="71818-139">To apply repair management to an item, the item must be set up with a service object relation on a service order.</span></span> <span data-ttu-id="71818-140">Im Serviceauftrag kann dann eine Reparaturposition mit Informationen zum vorliegenden Problem erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="71818-140">From the service order you can then create a repair line with information about the current issue.</span></span> <span data-ttu-id="71818-141">In der Reparaturposition werden das zu reparierende Serviceobjekt sowie Informationen zu Symptomen, Diagnose und Ausführung angegeben.</span><span class="sxs-lookup"><span data-stu-id="71818-141">On the repair line you define the service object that is in repair and information about symptoms, diagnosis, and execution.</span></span> <span data-ttu-id="71818-142">Darüber hinaus kann die Reparaturposition mit einem Hinweis versehen werden.</span><span class="sxs-lookup"><span data-stu-id="71818-142">You can also create a note for the repair line.</span></span>

<span data-ttu-id="71818-143">Reparaturpositionen können für jeden Schritt des Reparaturvorgangs erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="71818-143">You can create repair lines for each step in the repair process.</span></span>

## <a name="create-a-repair-line-on-a-service-order"></a><span data-ttu-id="71818-144">Erstellen einer Reparaturposition in einem Serviceauftrag</span><span class="sxs-lookup"><span data-stu-id="71818-144">Create a repair line on a service order</span></span>

1.  <span data-ttu-id="71818-145">Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.</span><span class="sxs-lookup"><span data-stu-id="71818-145">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="71818-146">Wählen Sie den Serviceauftrag mit dem zu reparierenden Serviceobjekt aus.</span><span class="sxs-lookup"><span data-stu-id="71818-146">Select the service order with the service object that needs repair.</span></span>

3.  <span data-ttu-id="71818-147">Klicken Sie **Reparatur** \> **Reparaturpositionen**, um das Formular **Reparaturpositionen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="71818-147">Click **Repair** \> **Repair lines** to open the **Repair lines** form.</span></span>

4.  <span data-ttu-id="71818-148">Erstellen Sie durch Drücken von Strg+N eine neue Position.</span><span class="sxs-lookup"><span data-stu-id="71818-148">Press CTRL+N to create a new line.</span></span>

5.  <span data-ttu-id="71818-149">Wählen Sie ein Serviceobjekt aus.</span><span class="sxs-lookup"><span data-stu-id="71818-149">Select a service object.</span></span> <span data-ttu-id="71818-150">Sie können jedes beliebige Serviceobjekt auswählen, für das im Serviceauftrag eine Objektbeziehung eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="71818-150">You can select any service object that has been set up with an object relation on the service order.</span></span>

6.  <span data-ttu-id="71818-151">Wählen Sie in der Reparaturposition die zutreffenden Werte für Symptome, Diagnose und Ausführung aus, und klicken Sie ggf. zum Erstellen eines Hinweises für die Reparaturposition auf die Registerkarte **Hinweis**.</span><span class="sxs-lookup"><span data-stu-id="71818-151">Select any of the preset symptoms, diagnosis, and execution values that are relevant in the repair line and then click the **Note** tab to create a note on the repair line, if needed.</span></span>

7.  <span data-ttu-id="71818-152">Drücken Sie zum Speichern der neuen Reparaturposition die Tastenkombination STRG+S.</span><span class="sxs-lookup"><span data-stu-id="71818-152">Press CTRL+S to save the new repair line.</span></span> <span data-ttu-id="71818-153">Das Feld **Erstellungsdatum und -uhrzeit** auf der Registerkarte **Allgemein** des Formulars **Reparaturpositionen** wird mit dem Zeitpunkt des Speichervorgangs aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="71818-153">The **Created date and time** field in the **General** tab of the **Repair lines** form is updated with the time of saving.</span></span>

## <a name="tracking-progress-and-resolving-a-repair-issue"></a><span data-ttu-id="71818-154">Nachverfolgen des Status und Beheben eines Reparaturproblems</span><span class="sxs-lookup"><span data-stu-id="71818-154">Tracking progress and resolving a repair issue</span></span>

<span data-ttu-id="71818-155">Mithilfe der Reparaturphasen einer Reparaturposition lässt sich der Status der Reparatur nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="71818-155">You can set the repair stages of a repair line to track the progress of the repair.</span></span>

<span data-ttu-id="71818-156">Nach erfolgter Reparatur kann die Reparaturposition abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="71818-156">When a repair issue is resolved, you can close the repair line.</span></span> <span data-ttu-id="71818-157">Hierzu muss als Reparaturphase eine Phase gewählt werden, bei der die Eigenschaft **Abschlossen** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="71818-157">Set the repair stage to a stage with a **Finished** property enabled.</span></span> <span data-ttu-id="71818-158">Daraufhin werden in der Position das aktuelle Datum sowie die aktuelle Uhrzeit als Abschlusszeit erfasst.</span><span class="sxs-lookup"><span data-stu-id="71818-158">The current date and time is registered as the finish time on the line.</span></span>

## <a name="close-a-repair-line-for-a-resolved-issue"></a><span data-ttu-id="71818-159">Abschließen der Reparaturposition eines behobenen Problems</span><span class="sxs-lookup"><span data-stu-id="71818-159">Close a repair line for a resolved issue</span></span>

1.  <span data-ttu-id="71818-160">Formular für **Reparaturpositionen**öffnen.</span><span class="sxs-lookup"><span data-stu-id="71818-160">Open the **Repair lines** form.</span></span> <span data-ttu-id="71818-161">Führen Sie die Schritte zum Erstellen einer Reparaturposition durch, die weiter oben in diesem Thema aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="71818-161">Follow the procedure earlier in this topic to create a repair line.</span></span>

2.  <span data-ttu-id="71818-162">Wählen Sie die Reparaturposition mit der abzuschließenden Reparatur aus.</span><span class="sxs-lookup"><span data-stu-id="71818-162">Select the repair line with the repair issue that you want to close.</span></span>

3.  <span data-ttu-id="71818-163">Wählen Sie im Feld **Reparaturphase** eine Phase aus, bei der die Eigenschaft **Abgeschlossen** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="71818-163">In the **Repair stage** field, select a stage with the **Finished** property enabled.</span></span>

  


