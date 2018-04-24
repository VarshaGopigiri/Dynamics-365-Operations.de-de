---
title: "Optimierungsratgeber – Überblick"
description: "In diesem Thema wird beschrieben, wie Sie Optimierungsratgeber verwenden können, um eine optimale Konfiguration von Microsoft Dynamics 365 Finance and Operations zu gewährleisten."
author: roxanadiaconu
manager: AnnBe
ms.date: 03/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core (Operations, Core)
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4eeb5802831f5a02408e1ac2a2b529a78761966b
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="optimization-advisor-overview"></a><span data-ttu-id="caa51-103">Optimierungsratgeber – Überblick</span><span class="sxs-lookup"><span data-stu-id="caa51-103">Optimization advisor overview</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="caa51-104">In diesem Thema wird beschrieben, wie Sie Optimierungsratgeber verwenden können, um eine optimale Konfiguration von Microsoft Dynamics 365 Finance and Operations zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="caa51-104">This topic describes how you can use Optimization advisor to help guarantee optimal configuration of Microsoft Dynamics 365 Finance and Operations.</span></span>

## <a name="overview"></a><span data-ttu-id="caa51-105">Überblick</span><span class="sxs-lookup"><span data-stu-id="caa51-105">Overview</span></span>

<span data-ttu-id="caa51-106">Falsche Konfiguration und Einstellung eines Moduls können die Verfügbarkeit von Funktionen im Bereich Finance and Operations, die Systemleistung und das reibungslose Funktionieren von Unternehmensabläufen beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="caa51-106">Incorrect configuration and setup of a module can adversely affect the availability of features in Finance and Operations, system performance, and the smooth operation of business processes.</span></span> <span data-ttu-id="caa51-107">Die Qualität von Geschäftsdaten (beispielsweise die Korrektheit, Vollständigkeit und Sauberkeit der Daten) wirkt sich auch auf die Systemleistung und beispielsweise die Entscheidungsfähigkeit oder Produktivität einer Organisation aus.</span><span class="sxs-lookup"><span data-stu-id="caa51-107">The quality of business data (for example, the correctness, completeness, and cleanliness of the data) also affects system performance, and an organization's decision-making capabilities, productivity, and so on.</span></span>

<span data-ttu-id="caa51-108">Der Arbeitsbereich **Optimierungsratgeber** ist ein Tool, mit dem durch Poweruser, Business Analysten, Funktionsberater und IT-Supportfunktionen Probleme in der Modulkonfiguration und in Geschäftsdaten identifiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="caa51-108">The **Optimization advisor** workspace is a tool that lets power users, business analysts, functional consultants, and IT support functions identify issues in module configuration and business data.</span></span> <span data-ttu-id="caa51-109">Optimierungsratgeber schlägt Verfahren für Modulkonfiguration vor und bezeichnet die Daten, die veraltet oder falsch sind.</span><span class="sxs-lookup"><span data-stu-id="caa51-109">Optimization advisor suggests best practices for module configuration and identifies business data that is obsolete or incorrect.</span></span>

<span data-ttu-id="caa51-110">Optimierungsratgeber führt in regelmäßigen Zeitabständen eine Gruppe von Regeln für bewährte Methoden aus.</span><span class="sxs-lookup"><span data-stu-id="caa51-110">Optimization advisor periodically runs a set of best practice rules.</span></span> <span data-ttu-id="caa51-111">Ein Standardsatz an Regeln wird zusammen mit Microsoft Dynamics 365 for Finance and Operations, Version 8.0 (April 2018) freigegeben.</span><span class="sxs-lookup"><span data-stu-id="caa51-111">A default set of rules is released together with Microsoft Dynamics 365 for Finance and Operations version 8.0 (April 2018).</span></span> <span data-ttu-id="caa51-112">Allerdings können auch Benutzer Regeln erstellen, die spezifisch auf die Anpassungen, Lösungen von den unabhängigen Softwareherstellern (ISVs) und Geschäftsdaten bestimmt sind.</span><span class="sxs-lookup"><span data-stu-id="caa51-112">However, users can also create rules that are specific to their customizations, solutions from independent software vendors (ISVs), and business data.</span></span> <span data-ttu-id="caa51-113">Weitere Informationen zum Erstellen von Regeln finden Sie unter [Erstellen neuer Regeln](./create-rules-optimization-advisor.md).</span><span class="sxs-lookup"><span data-stu-id="caa51-113">For more information about how to create rules, see [Create new rules](./create-rules-optimization-advisor.md).</span></span>

<span data-ttu-id="caa51-114">Wenn ein Verstoß einer Regel erkannt wird, wird eine Optimierungsverkaufschance generiert und wird im Arbeitsbereich **Optimierungsratgeber** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="caa51-114">When a violation of a rule is detected, an optimization opportunity is generated and appears in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="caa51-115">Ein Benutzer kann entsprechenden Korrektur-Aktivitäten direkt im Formular **Optimierungsratgeber** ausführen.</span><span class="sxs-lookup"><span data-stu-id="caa51-115">A user can take appropriate corrective action directly from the **Optimization advisor** workspace.</span></span>

<span data-ttu-id="caa51-116">Verkaufschancen können abhängig vom Typ der Rüstzeit und Daten oder unternehmensübergreifend unternehmensspezifisch sein, die geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="caa51-116">Opportunities can be company-specific or cross-company, depending on the type of setup and data that is being validated.</span></span> <span data-ttu-id="caa51-117">Unternehmensübergreifende Verkaufschancen können alle Unternehmen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="caa51-117">Cross-company opportunities can be viewed from all companies.</span></span> <span data-ttu-id="caa51-118">Um die Verkaufschancen für ein bestimmtes Unternehmen anzuzeigen, müssen Sie zuerst das Unternehmen auswählen.</span><span class="sxs-lookup"><span data-stu-id="caa51-118">To view the opportunities for a specific company, you must first select the company.</span></span>

<span data-ttu-id="caa51-119">Standardsicherheits-Richtlinien gelten für Optimierungsverkaufschancen.</span><span class="sxs-lookup"><span data-stu-id="caa51-119">Standard security policies apply to optimization opportunities.</span></span> <span data-ttu-id="caa51-120">Beispielsweise sind die Optimierungsverkaufschancen, die der Variante des **Lagerortverwaltung** zugeordnet sind, nur für Benutzer sichtbar, die den Zugriff zur Lagerortverwaltung haben und die Einstellung ändern.</span><span class="sxs-lookup"><span data-stu-id="caa51-120">For example, the optimization opportunities that are related to configuration of the **Warehouse management** module are visible only to users who have access to Warehouse management and can change its setup.</span></span>

<span data-ttu-id="caa51-121">Wenn Sie für manche Optimierungsverkaufschancen Maßnahmen ergreifen, berechnet das System die Auswirkungen der Verkaufschance in Bezug auf die Verringerung in der Laufzeit von Geschäftsprozessen.</span><span class="sxs-lookup"><span data-stu-id="caa51-121">When you take action on some optimization opportunities, the system calculates the impact of the opportunity in terms of the reduction in the runtime of business processes.</span></span> <span data-ttu-id="caa51-122">Leider ist diese Funktion nicht für alle Optimierungsverkaufschancen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="caa51-122">Unfortunately, this feature isn't available for all optimization opportunities.</span></span>

<span data-ttu-id="caa51-123">Um weitere Informationen zu Optimierungsratgeber zu erhalten, sehen Sie sich den kurzen Video [Optimierungsratgeber in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ) an.</span><span class="sxs-lookup"><span data-stu-id="caa51-123">To learn more about Optimization advisor, watch the short [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ) video.</span></span>

> [!Video https://www.youtube.com/embed/MRsAzgFCUSQ]

## <a name="optimization-rules"></a><span data-ttu-id="caa51-124">Optimierungsregeln</span><span class="sxs-lookup"><span data-stu-id="caa51-124">Optimization rules</span></span>

<span data-ttu-id="caa51-125">Um die vollständige Liste der Optimierungsratgeberregeln anzuzeigen und zu sehen, wie oft die Regeln bewertet werden, wechseln Sie zu **Systemverwaltung** &gt; **Periodische Aufgaben** &gt; **Diagnoseüberprüfungsregeln verwalten**.</span><span class="sxs-lookup"><span data-stu-id="caa51-125">To view the complete list of Optimization advisor rules and to see how often the rules are evaluated, go to **System administration** &gt; **Periodic tasks** &gt; **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="caa51-126">Nur Regeln, die den Status **Aktiv** besitzen, werden ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="caa51-126">Only rules that have a status of **Active** are evaluated.</span></span> <span data-ttu-id="caa51-127">Die Bewertungshäufigkeit kann auf **Täglich**, **Wöchentlich**, **Monatlich** oder **Ungeplant** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="caa51-127">The evaluation frequency can be set to **Daily**, **Weekly**, **Monthly**, or **Unscheduled**.</span></span>

<span data-ttu-id="caa51-128">Um die Bewertung von ungeplanten Regeln auszulösen, oder um periodische Regeln außerhalb des vordefinierten Zeitplans neu zu bewerten, wechseln Sie zu **Systemverwaltung** &gt; **Periodische Aufgaben** &gt; **Diagnoseüberprüfungsregel planen**.</span><span class="sxs-lookup"><span data-stu-id="caa51-128">To trigger the evaluation of unscheduled rules, or to reevaluate periodic rules outside their predefined schedule, go to **System administration** &gt; **Periodic tasks** &gt; **Schedule diagnostics validation rule**.</span></span> <span data-ttu-id="caa51-129">Im Dialogfeld **Diagnoseregelprüfung** wählen Sie eine Bewertungshäufigkeit aus.</span><span class="sxs-lookup"><span data-stu-id="caa51-129">Then, in the **Diagnostic rule validation** dialog box, select an evaluation frequency.</span></span> <span data-ttu-id="caa51-130">Alle Regeln, die die angegebenen Häufigkeit haben, werden neu bewertet.</span><span class="sxs-lookup"><span data-stu-id="caa51-130">All rules that have the specified frequency will be reevaluated.</span></span>

<span data-ttu-id="caa51-131">Der aktuelle Satz von Optimierungsregeln kann in die folgenden Kategorien unterteilt werden.</span><span class="sxs-lookup"><span data-stu-id="caa51-131">The current set of optimization rules can be divided into the following categories.</span></span>

### <a name="module-configuration-and-setup"></a><span data-ttu-id="caa51-132">Modul-Einrichtung und -Konfiguration</span><span class="sxs-lookup"><span data-stu-id="caa51-132">Module configuration and setup</span></span>

<span data-ttu-id="caa51-133">Die Einrichtung der Lagerortverwaltung ist ein komplizierter Prozess.</span><span class="sxs-lookup"><span data-stu-id="caa51-133">The setup of Warehouse management is a complicated process.</span></span> <span data-ttu-id="caa51-134">Um den Prozess zu vereinfachen, sind einige Regeln eingeführt worden, um die Korrektheit der Einstellungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="caa51-134">To make the process easier, some rules have been introduced to help validate the correctness of the setup.</span></span> <span data-ttu-id="caa51-135">Beispielsweise prüft eine Regel die Einstellung von Lagerortlagerplatzdirektiven für feste Produktvariantenlagerplätze für Aufträge und Umlagerungsaufträge.</span><span class="sxs-lookup"><span data-stu-id="caa51-135">For example, one rule validates the setup of warehouse location directives for fixed product variant locations for sales orders and transfer orders.</span></span>

<span data-ttu-id="caa51-136">Darüber hinaus überprüfen einige Regeln, ob mehrere Regeln-Funktionen, die ausgeführt wurden, geplant werden.</span><span class="sxs-lookup"><span data-stu-id="caa51-136">Additionally, some rules check whether features that have been enabled are actually used.</span></span> <span data-ttu-id="caa51-137">Beispielsweise bestimmt eine Regel, ob Sie das Modul **Produktprogrammplanung** verwenden.</span><span class="sxs-lookup"><span data-stu-id="caa51-137">For example, one rule determines whether you're using the **Master planning** module.</span></span> <span data-ttu-id="caa51-138">Wenn die Regel festlegt, dass Sie das Modul nicht verwenden, wird eine Optimierungsverkaufschance  generiert, dass Sie die Planungsprozesse deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="caa51-138">If the rule determines that you aren't using the module, an optimization opportunity is generated to suggest that you turn off the planning processes.</span></span>

### <a name="system-configuration"></a><span data-ttu-id="caa51-139">Systemkonfiguration</span><span class="sxs-lookup"><span data-stu-id="caa51-139">System configuration</span></span>

<span data-ttu-id="caa51-140">Wenn bestimmte Funktionen, die durch einen Konfigurationsschlüssel gesteuert wird, nicht verwendet werden, wird ein Optimierungsverkaufschancen-Bericht generiert, um vorzuschlagen, dass Sie den Variantenschlüssel deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="caa51-140">If specific functionality that is controlled by a configuration key isn't used, an optimization opportunity is generated to suggest that you disable the configuration key.</span></span> <span data-ttu-id="caa51-141">Beispiele von Konfiguration sind **Artikelgewicht**, **Budgetplanung**, **Projekt** und **Liste der genehmigten Kreditoren**.</span><span class="sxs-lookup"><span data-stu-id="caa51-141">Examples of configuration keys include **Catch weight**, **Budget planning**, **Project**, and **Approved vendor list**.</span></span>

### <a name="business-data-consistency-and-cleanup"></a><span data-ttu-id="caa51-142">Datenkonsistenz und -Bereinigung</span><span class="sxs-lookup"><span data-stu-id="caa51-142">Business data consistency and cleanup</span></span>

<span data-ttu-id="caa51-143">Wenn Masterdaten nicht korrekt sind (beispielsweise, wenn Sie Maßeinheitsumrechnungen für Einheiten aufweisen, die noch nicht definiert wurden, oder wenn Sie Maßeinheitsumrechnungen haben, die durch eine Division 0 haben \[Null\]), wird ein Optimierungsverkaufschancen-Bericht generiert, so dass Sie die Daten korrigieren.</span><span class="sxs-lookup"><span data-stu-id="caa51-143">If master data isn't correct (for example, if you have unit of measure conversions for units that haven't been defined, or if you have unit of measure conversions that have a division by 0 \[zero\]), an optimization opportunity is generated to suggest that you correct the data.</span></span> 

<span data-ttu-id="caa51-144">Wenn Sie zu viele Stapelverarbeitungsauftragsverlaufinträge haben, werden veraltete Artikel, geschlossene verfügbare Einträge für Lagerort aktivierte Artikel, usw. haben oder wenn diese Einträge und Artikel zu alt sind, werden Optimierungsverkaufschancen generiert, aus der Sie Daten bereinigen.</span><span class="sxs-lookup"><span data-stu-id="caa51-144">If you have too many batch job history entries, obsolete items, closed on-hand entries for warehouse enabled items, and so on, or if those entries and items are too old, optimization opportunities are generated to suggest that you clean up the data.</span></span> <span data-ttu-id="caa51-145">Wenn Sie Ihre Daten führen, bereinigen Sie, Sie kann festgestellt, zur Verbesserung gesamte Systemleistung.</span><span class="sxs-lookup"><span data-stu-id="caa51-145">By keeping your data clean, you can help improve overall system performance.</span></span>

### <a name="best-practices"></a><span data-ttu-id="caa51-146">Optimale Verfahren</span><span class="sxs-lookup"><span data-stu-id="caa51-146">Best practices</span></span>

<span data-ttu-id="caa51-147">Wenn Sie mehrere Verfahren nicht entsprechend den Geschäftsprozessen ausführen (beispielsweise, wenn Sie Bestandsvorabschluss ausführen, bevor der Bestand geschlossen ist, oder wenn Sie die geplanten Charge für die Erfassung im untergeordneten Sachkontos-Chargen-Übertragung), informieren Optimierungsverkaufschancen Sie die Abfrage und Verfahren, dass Sie ihn folgen.</span><span class="sxs-lookup"><span data-stu-id="caa51-147">If you aren't running some business processes according to best practices (for example, if you run inventory pre-closing before the inventory is closed, or if you use the scheduled batch for subledger journal batch transfer), optimization opportunities inform you about the best practice and ask that you follow it.</span></span>

## <a name="optimization-opportunities"></a><span data-ttu-id="caa51-148">Optimierungsmöglichkeiten</span><span class="sxs-lookup"><span data-stu-id="caa51-148">Optimization opportunities</span></span>

<span data-ttu-id="caa51-149">Um die Optimierungsverkaufschancen anzuzeigen, die während der Bewertung der Optimierungsregeln generiert werden, öffnen Sie den Arbeitsbereich **Optimierungsberater**.</span><span class="sxs-lookup"><span data-stu-id="caa51-149">To view the optimization opportunities that are generated during the evaluation of optimization rules, open the **Optimization advisor** workspace.</span></span>

<span data-ttu-id="caa51-150">In diesem Arbeitsbereich können Sie weitere Informationen zu einer Verkaufschance anzeigen, indem Sie **Weitere Informationen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="caa51-150">In this workspace, you can view more information about an opportunity by selecting **More information**.</span></span> <span data-ttu-id="caa51-151">Wenn Sie möchten, dass das System Aktivitäten ausführt und die Einstellung korrigiert. müssen Sie die entsprechenden Seiten nicht öffnen, wählen Sie **Aktion ausführen**.</span><span class="sxs-lookup"><span data-stu-id="caa51-151">If you want the system to take action and correct the setup, clean the data, and so on, so that you don't have to open the corresponding pages yourself, select **Take action**.</span></span>

<span data-ttu-id="caa51-152">Es gibt keinen Workflow für Optimierungsverkaufschancen.</span><span class="sxs-lookup"><span data-stu-id="caa51-152">There is no workflow for optimization opportunities.</span></span> <span data-ttu-id="caa51-153">Nachdem Sie **Aktionen ausführen** augewählt haben oder einen Navigationspfad verwenden, der im Dialogfeld **Weitere Informationen** angegeben wird, verschwindet die Optimierungsverkaufschance aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="caa51-153">After you select **Take action** or use a navigation path that is provided in the **More information** dialog box, the optimization opportunity disappears from the list.</span></span> <span data-ttu-id="caa51-154">Wenn die Korrektur nicht vollständig ein Problem löst, wird die Verkaufschance erneut das nächste Mal generiert, an der die Regel ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="caa51-154">If the corrective action doesn't completely resolve an issue, the opportunity will be generated again the next time that the rule is evaluated.</span></span>

<span data-ttu-id="caa51-155">Wenn eine Verkaufschance nicht für Ihre Rolle gilt, können Sie **Kontrollkästchen von meiner Liste** auswählen.</span><span class="sxs-lookup"><span data-stu-id="caa51-155">If an opportunity doesn't apply to your role, you can select **Hide from my list**.</span></span> <span data-ttu-id="caa51-156">Auch wenn die Regel nach dieser Verkaufschance erneut später ausgelöst wurde, finden Sie die Verkaufschance nicht in der Liste.</span><span class="sxs-lookup"><span data-stu-id="caa51-156">Even if the rule behind this opportunity is triggered again later, you won't see the opportunity in your list.</span></span>

<span data-ttu-id="caa51-157">Um die Bewertung bestimmter Regeln zu deaktivieren, wählen Sie die Verkaufschance aus, die durch die Regel generiert wurde, und wählen dann **Analyse deaktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="caa51-157">To deactivate the evaluation of specific rules, select the opportunity that was generated by the rule, and then select **Deactivate analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="caa51-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="caa51-158">See also</span></span>

[<span data-ttu-id="caa51-159">Erstellen neuer Regeln</span><span class="sxs-lookup"><span data-stu-id="caa51-159">Create new rules</span></span>](./create-rules-optimization-advisor.md)

[<span data-ttu-id="caa51-160">Optimierungsberater in Dynamics 365 for Finance and Operations, (Video)</span><span class="sxs-lookup"><span data-stu-id="caa51-160">Optimization advisor in Dynamics 365 for Finance and Operations (Video)</span></span>](https://www.youtube.com/watch?v=MRsAzgFCUSQ)
