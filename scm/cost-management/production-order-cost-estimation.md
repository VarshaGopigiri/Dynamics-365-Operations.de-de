---
title: "Vorkalkulation für Produktionsauftrag"
description: "Dieser Artikel enthält Informationen zur Produktvorkalkulation. Die Produktvorkalkulation stellt die voraussichtlichen Material- und Kapazitätsverbrauchskosten für die Produktion eines Artikels in der geplanten Produktionsauftragsmenge bereit."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3d43b186335b42fd5b7b6c84456d012f51b26799
ms.lasthandoff: 03/31/2017


---

# <a name="production-order-cost-estimation"></a>Vorkalkulation für Produktionsauftrag

Dieser Artikel enthält Informationen zur Produktvorkalkulation. Die Produktvorkalkulation stellt die voraussichtlichen Material- und Kapazitätsverbrauchskosten für die Produktion eines Artikels in der geplanten Produktionsauftragsmenge bereit. 

Nachdem Sie einen Produktionsauftrag erstellt haben, müssen Sie die Produktionskosten kalkulieren. Zweck ist es, den Artikel und den Arbeitsverbrauch für den Produktionsprozess zu schätzen, da diese Werte die Grundlage für die nachfolgenden Planungs- und Produktionsprozesse bilden.

## <a name="production-cost-estimation"></a>Produktionskosten vorkalkulieren
Die Vorkalkulation für die Produktionskosten basiert auf den folgenden Informationen:

-   Die Menge auf dem Produktionsauftrag
-   Die Komponenten in den Produktionsstücklisten (BOMs)
-   Der Routingbetrieb im Produktionsplan
-   Die indirekten Kosten, die auf die Komponenten sowie die Arbeitsgänge gelten
-   Die Daten der aktiven Kosten ab dem Berechnungsdatum

Befindet sich ein Phantompositionsartikel in der Produktionsstückliste, werden in den Berechnungen die Komponenten sowie die Arbeitsgänge des Arbeitsplans für das Phantom berücksichtigt. Mithilfe der Vorkalkulationsaufgabe können Sie vorkalkulierte Kosten unter Verwendung aktualisierter Informationen neu berechnen. Bei diesen aktualisierten Informationen kann es sich beispielsweise um eine Änderung der Produktionsauftragsmenge, der Komponenten in den Produktionsstücklisten, der Arbeitsgänge des Produktionsarbeitsplans, der indirekten Kosten für diese Komponenten/Arbeitsgänge oder der Daten für aktive Kosten zum Datum der Neuberechnung handeln. Anhand der Berechnung der vorkalkulierten Kosten wird auf Basis eines Kosten-plus-Aufschlag-Ansatzes auch ein Verkaufspreisvorschlag für den Produktionsartikel erstellt. Die Berechnung der vorkalkulierten Kosten kann optional auch für Referenzaufträge verwendet werden, bei denen es sich um mit dem Produktionsauftrag verknüpfte Produktionsaufträge handelt.

## <a name="view-the-estimated-costs"></a>Die vorkalkulierten Kosten anzeigen
Nach Ausführung der Vorkalkulation, können Sie die Ergebnisse auf der Seite **Preiskalkulation** anzeigen. Bei der Vorkalkulation werden die folgenden Werte berechnet:

-   **Produktionskosten** – Dies ist die oberste Position der Vorkalkulation. Es werden die Gesamtkosten der Ausführung des Produktionsauftrags und der Gesamtverkaufspreis für die Produktion angezeigt. Dies ist die Summe aller Kostenpositionen in der Vorkalkulation.
-   **Arbeitsplan- oder Ressourcenkosten** - Arbeitsplan- oder Ressourcenkosten sind die Kosten für die Produktionsaufträge. Die enthalten die Kosten von Elementen wie Rüstzeit, Bearbeitungszeit und Gemeinkosten.
-   **Materialkosten** – Dies sind die Kosten und Preise der BOM-Komponenten, die erforderlich sind, um den Artikel zu produzieren. Diese Kosten wurden zuvor erstellt und in das System eingegeben.

## <a name="other-uses-of-cost-estimation"></a>Sonstige Verwendung einer Kostenvorkalkulation
Eine Vorkalkulation stellt auch die folgenden Informationen bereit:

-   Aussagekräftige Preisangebote
-   Vorkalkulation der Rentabilität des Auftrags
-   Vorkalkulation des Rohmaterialverbrauchs
-   Vergleiche von Kosteninformationen aus vorherigen Produktionen
-   Budget- und Planungsinformationen
-   Vorkalkulation der zur Verwaltung bestimmter Kosten erforderlichen Produktionsgröße


