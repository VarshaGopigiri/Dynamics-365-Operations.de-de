---
title: Planen von Ladungen mit der Hubkonsolidierung
description: Dieser Artikel beschreibt die Funktion zur Konsolidierung von Lieferungen in einem Hub bei der Lieferung von Waren aus unterschiedlichen Lagerorten an einen Kunden oder bei der Lieferung von mehreren Kreditoren an einen Lagerort.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 475fa9b73deeddd0f9118b0062e834a053fcb919
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="plan-loads-using-hub-consolidation"></a>Planen von Ladungen mit der Hubkonsolidierung

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Funktion zur Konsolidierung von Lieferungen in einem Hub bei der Lieferung von Waren aus unterschiedlichen Lagerorten an einen Kunden oder bei der Lieferung von mehreren Kreditoren an einen Lagerort.

Die Konsolidierung von Lieferungen in einem Hub kann bei der Lieferung von Waren aus unterschiedlichen Lagerorten an einen Kunden oder bei der Lieferung von mehreren Kreditoren an einen Lagerort hilfreich sein.

## <a name="building-loads"></a>Erstellen von Ladungen
Bevor Sie die Hub-Konsolidierung verwenden können, müssen Sie die Option **In Transitplanung** auf der Seite **Transportverwaltungsparameter** aktivieren. Außerdem müssen Sie die Hubs für die Konsolidierung erstellen. Das folgende Diagramm zeigt ein Beispiel für die Hub-Konsolidierung. In diesem Fall gehen die Aufträge von verschiedenen Lagerorten an denselben Debitor. Die grundlegenden Ladungen werden ganz normal auf Basis von Aufträgen erstellt (über die Seite **Ladungsplanungsworkbench**). Um zwei Ladungen vor der Auslieferung in einem Hub zu konsolidieren, wählen Sie auf der Seite **Ladungsplanungsworkbench** im Feld **Transport** die Option **Hub-Konsolidierung**. Bei der Auswahl des richtigen Hubs für jede Ladung nutzen die Ladungen den Hub als "Abladeziel". Im Abschnitt **Beschaffung und Bedarf** auf der Seite **Ladungsplanungsworkbench** gibt es außerdem zwei "Transportanforderungspositionen". Sie können diese zwei Positionen dann zu einer neuen Ladung hinzufügen. Die neue Ladung umfasst beide Auftragspositionen und den Hub als "Aufladeadresse" sowie Kunde A als "Abladeziel". Die drei Ladungen können dann wie jede andere Ladung geroutet werden. Sie können jeden Spediteur auswählen, den das System für eine Ladung vorschlägt. [![Hub-Konsolidierung](./media/hubconsol.jpg)](./media/hubconsol.jpg) Die gleiche Methode können sie auch zur Konsolidierung von Ladungen für mehrere Umlagerungsauftrag nutzen. In diesem Fall ist Kunde A im obigen Diagramm ein Lagerort. Alternativ können Sie Ladungen für mehrere Aufträge, in denen Ladungen von unterschiedlichen Kreditoren an den selben Lagerort geliefert werden, konsolidieren. Sie können mehrere Konsolidierungs-Hubs nutzen und in mehreren Hubs für mehrere Ladungen aus verschiedenen Lagerorten konsolidieren. Nachdem Sie die grundlegenden Ladungen erstellt und die Option zur Hub-Konsolidierung verwendet haben, erstellen Sie über die konsolidierten Transportanforderungsposition neue Ladungen. Dann routen Sie die Ladungen.




