---
title: Grobterminierung
description: "Dieses Thema enthält allgemeine Informationen zur Grobterminierung. Diese Grobplanung wird häufig verwendet, wenn eine allgemeine Schätzung der Dauer des Produktionsprozesses benötigt wird."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 198073
ms.assetid: 12c28b11-80aa-4668-b15b-724cb24890bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 660d6b2dfb5fbed58a5c28b77aac3bb4604c7d8d
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="operations-scheduling"></a>Grobterminierung

[!include [banner](../includes/banner.md)]

Dieses Thema enthält allgemeine Informationen zur Grobterminierung. Diese Grobplanung wird häufig verwendet, wenn eine allgemeine Schätzung der Dauer des Produktionsprozesses benötigt wird.

Sie können die Produktion auf der Arbeitsgangsebene und auf der Einzelvorgangebene planen. Mit der Grobterminierung werden die Arbeitsgänge im Produktionsarbeitsplan nicht in Einzelvorgänge aufgelöst. Wenn Sie weitere Details in die Planung aufnehmen möchten, beispielsweise Informationen über die aktuelle Kapazität, können Sie die Feinterminierung nach der Grobterminierung ausführen. Sie können auch nur eine Feinterminierung ausführen. Die Feinterminierung wird normalerweise verwendet, um Einzelvorgänge im Fertigungsbereich für einen sofortigen oder kurzfristigen Zeitrahmen zu planen.

## <a name="components-of-operations-scheduling"></a>Komponenten der Grobterminierung
Die Hauptkomponenten der Grobterminierung sind die Planungsrichtung, die Ressourcenkapazität und die Materialoptimierung. Die Grobterminierung ermöglicht Folgendes:

-   Steuern der Planungsmethode durch Vorwärts- oder Rückwärtsplanung ab einem bestimmten Datum.
-   Optimieren der Ressourcennutzung durch Planen der Produktionen auf Basis der Ressourcenkapazität. Dies hilft auch zu erkennen, wann alternative Ressourcen verwendet müssen.
-   Optimieren der Materialverwendung durch Planen der Produktionen auf Basis der Verfügbarkeit der erforderlichen Materialien.
-   Planen und synchronisieren von Referenzproduktionen. Die Datumsangaben der Referenzproduktionen werden angepasst, wenn Änderungen am Zeitplan des Produktionsauftrags vorgenommen werden.

Sie müssen die Kosten eines Produktionsauftrags vorkalkulieren, bevor Sie die Grobterminierung ausführen können. Wenn Sie noch keine Vorkalkulation durchgeführt haben, wird sie automatisch ausgeführt, bevor der Grobterminierungsprozess eingeleitet wird. Eine Grobterminierung gibt folgende Informationen an:

-   Das Produkt, das für die Produktion geplant wird
-   Die Konfiguration des Produkts
-   Die in die Produktion eingesetzten Mengen
-   Das Start- und Enddatum der Produktion
-   Die Kapazitätsreservierungen für die Ressourcen, die die Produktionsaktivitäten ausführen

Die Rüstzeit, die Bearbeitungszeit und die Ausführungszeit werden für Arbeitsgänge in der Produktion festgelegt. Nach dem Ausführen der Grobterminierung hat der Produktionsauftrag den Status **Geplant**, und alle Arbeitsgänge werden in der Reihenfolge terminiert, die durch den Produktionsarbeitsplan angegeben ist. Es wird jedoch nur die Dauer des Arbeitsgangs berücksichtigt. Start- und Endzeiten werden nicht terminiert.

## <a name="scheduling-direction-and-date"></a>Planungsrichtung und -datum
Die Planungsrichtung ist eine Grundlage für den Planungsvorgang. Die Produktion kann je nach Zeit- und Planungsanforderungen ab einem beliebigen Datum vorwärts oder rückwärts geplant werden.

-   **Vorwärts ab Planungsdatum** – Die Produktion wird so geplant, dass sie so früh wie möglich beginnt. Die Produktion kann heute, morgen oder ab einem bestimmten Datum in der Zukunft geplant werden. Die Produktion wird in der Zeit vorwärts bis zum frühestmöglichen Enddatum geplant.
-   **Rückwärts ab Planungsdatum** – Die Produktion wird so geplant, dass sie so spät wie möglich beginnt. Die Rückwärtsplanung geht von dem Datum aus, an dem die Produktion abgeschlossen sein muss. Der Zeitplan wird rückwärts ab diesem Datum bis zum letzten möglichen Datum berechnet, an dem die Produktion gestartet und noch pünktlich abgeschlossen werden kann.

## <a name="resource-scheduling"></a>Ressourcenplanung
Wenn Sie eine Grobterminierung durchführen, wird jeder Arbeitsgang im Produktionsarbeitsplan für die Ressource geplant, die für den Arbeitsgang angegeben wurde. Zusätzlich wird die Dauer der einzelnen Arbeitsgänge im Produktionsarbeitsplan aufgeführt. Wenn eine Ressourcengruppe für einen Arbeitsgang angegeben wird, reserviert die Planung Kapazitäten für die Gruppe. Im Unterschied zur Feinterminierung werden bei der Grobterminierung jedoch keine bestimmten Ressourcen in der Gruppe ausgewählt. Wenn Sie mit begrenzter Kapazität arbeiten, hängt die Planung von der Verfügbarkeit der Ressourcen ab, die zum Abschluss der Produktion erforderlich sind. Die Grobterminierung folgt der Folge von Arbeitsgängen, die im Produktionsarbeitsplan angegeben ist. Die Planung reserviert Kapazität für die Ressourcengruppen auf Grundlage der Arbeitszeiten, die für den Produktionsarbeitsplan definiert sind. Die Summe der verfügbaren Kapazität der beteiligten Ressourcen bestimmt die Kapazität der Ressourcengruppe. Kapazitätsreservierungen, die bereits für die Ressourcen vorhanden sind, werden als nicht verfügbare Kapazität betrachtet. Falls die verfügbare Kapazität für die Produktion nicht ausreichend ist, können die Produktionsaufträge verzögert oder auch angehalten werden. Sie können auch die Effizienz angeben, die Sie von den an der Produktion beteiligten Ressourcen erwarten. Sie geben die Effizienz als Prozentsatz der Ressource an. Der Effizienzprozentsatz passt den Durchsatz der Ressource an. Dies Regulierung wirkt sich auf die Zeit aus, die für die Ressource reserviert ist. Die Lieferzeiten für die Arbeitsgänge, die die Ressource verwenden, werden ebenfalls entsprechend angepasst.

## <a name="operations-scheduling-and-master-planning"></a>Grobterminierung und Produktprogrammplanungslauf
Durch die Grobterminierung wird auch der Master-Produktprogrammplan gesteuert, der alle Materialbedarfsberechnungen bestimmt. Bei der Grobterminierung wird Folgendes berücksichtigt:

-   **Bestandsproduktionen** – Geplante, freigegebene oder gestartete Produkte
-   **Materialverfügbarkeit** – Bestand, Unterproduktion, Lieferanten und Kreditoren
-   **Kapazitätsverfügbarkeit** – Ressourcen, die für die Produktion erforderlich sind

## <a name="cancellations"></a>Stornierungen
Wenn Sie die Grobterminierung ausführen, können Sie bestimmte Teile des Arbeitsplans stornieren. Dazu zählen die Wartezeit, die Rüstzeit, die Bearbeitungszeit, die Überschneidungszeit und die Transportzeiten.

## <a name="finite-materials"></a>Begrenztes Material
Wenn Sie mit begrenztem Material arbeiten, hängt die Planung auch von der Verfügbarkeit des Materials ab, das für die Produktion benötigt wird. Wenn die verfügbaren Komponenten für die Produktion nicht ausreichen, kann die Produktion verzögert werden. Sie können die Planung auf der Materialverwendung beruhen lassen, indem Sie das Material angeben, das für die Produktion verfügbar sein muss. Wenn Sie sowohl die Ressourcenkapazität als auch die Verfügbarkeit des Materials optimieren, wird die Produktion gemäß diesen Einschränkungen berechnet. Der Start eines Produktionsauftrag kann erst geplant werden, wenn Kapazität und Material gleichzeitig und in den erforderlichen Mengen verfügbar sind.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Optionen für die Grobterminierung](operation-scheduling-options.md)




