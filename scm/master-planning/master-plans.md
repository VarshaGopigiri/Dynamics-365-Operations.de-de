---
title: "Produktprogrammpläne"
description: "Verwenden Sie verschiedene Produktprogrammpläne, die täglichen Arbeitsabläufe Ihres Unternehmens, zum Simulieren Sie unterschiedlicher Planungsstrategien, die überwacht werden sollen, und Ausführen einer Unternehmensrichtlinie, z eine Richtlinie für interne Leistung oder Kundenzufriedenheit durch."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqParameters, ReqPlanSched
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7911
ms.assetid: a116b7de-3d6d-4321-87ba-5a5d99c2f64e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 29bb560c11e63938bea73ed8471c27563b546f8f
ms.lasthandoff: 03/31/2017


---

# <a name="master-plans"></a>Produktprogrammpläne

Verwenden Sie verschiedene Produktprogrammpläne, die täglichen Arbeitsabläufe Ihres Unternehmens, zum Simulieren Sie unterschiedlicher Planungsstrategien, die überwacht werden sollen, und Ausführen einer Unternehmensrichtlinie, z eine Richtlinie für interne Leistung oder Kundenzufriedenheit durch. 

Sie können Produktprogrammpläne auf der Seite **Produktprogrammpläne** konfigurieren.

Es gibt zwei Arten von Plänen:
-   **Statischer Produktprogrammplan** – Bei der Kalkulation im Produktprogrammplanungslauf werden die aktuellen Daten zum Generieren von Bedarfsverlaufsplänen verwendet. Dieser Plan bleibt bis zur nächsten Ausführung eines Produktprogrammplanungslaufs unverändert. Es handelt sich um einen Betriebsablaufplan, den verschiedene Mitarbeiter wie Einkäufer oder Produktionsplaner verwenden können, um informierte Entscheidungen zu treffen und um ihre täglichen Aufgaben und Aktivitäten auszuführen.
-   **Dynamischer Produktprogrammplan** – Dieser Plan setzt auf dem gleichen Bedarfsverlaufsplan auf, der im Produktprogrammplanungslauf generiert wurde. Der dynamische Plan kann allerdings jederzeit aktualisiert werden, wenn sich die Stammdaten ändern. Dieser Fall könnte z. B. eintreten, wenn ein neuer Auftrag erstellt wird. Hiermit sind Sie in der Lage, das sich ändernde Auftragsnetzwerk und die Artikelverfügbarkeit zu überwachen, ohne den statischen Plan zu stören, den andere Personen für ihre Arbeitsprozesse benötigen.

Ein Unternehmen kann nur mit einem dynamischen Produktprogrammplan oder mit statischen und dynamischen Plänen arbeiten. Darüber hinaus kann jeder Produktprogrammplan so konfiguriert werden, dass er eine bestimmte Strategie oder ein Problem berücksichtigt. Beispiele:
-   Legen Sie höhere Lagerbestände fest, um Fehlbestände zu verhindern.
-   Legen Sie höhere Sicherheitszuschläge fest, um sich gegen unzuverlässige Lieferanten abzusichern.

Der anfängliche dynamische Produktprogrammplan kann auch so eingerichtet werden, dass er bei jedem Produktprogrammplanungslauf mit dem neuen Bedarfsverlaufsplan aktualisiert wird. Sie können diese Einstellungen auf der Seite **Produktprogrammplanungsparameter** angeben.



<a name="see-also"></a>Siehe auch
--------

[Dispositionseinstellungen](coverage-settings.md)

[Taktische und Betriebsplanung für den Produktprogrammplanungslauf trennend( http://blogs.msdn.com/b/axmfg/archive/2012/10/12/separating-tactical-and-operative-planning-for-master-scheduling.aspx)]

[Produktprogrammplanung: Verwenden eines statischen und dynamischen Produktprogrammplan oder verwenden Sie einen Plan?] (https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)

