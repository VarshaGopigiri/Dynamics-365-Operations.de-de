---
title: "Produktprogrammpläne"
description: "Zur Unterstützung der täglichen Arbeitsabläufe Ihres Unternehmens, zum Simulieren unterschiedlicher Planungsstrategien, die überwacht werden sollen, und zum Implementieren einer Unternehmensrichtlinie, z. B. eine Richtlinie für die interne Leistung oder die Kundenzufriedenheit, können Sie verschiedene Produktprogrammpläne einrichten und verwenden."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: bf73ae6653cf5100e70d3ca9891c81f1a24e3574
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="master-plans"></a>Produktprogrammpläne

[!include[banner](../includes/banner.md)]


Zur Unterstützung der täglichen Arbeitsabläufe Ihres Unternehmens, zum Simulieren unterschiedlicher Planungsstrategien, die überwacht werden sollen, und zum Implementieren einer Unternehmensrichtlinie, z. B. eine Richtlinie für die interne Leistung oder die Kundenzufriedenheit, können Sie verschiedene Produktprogrammpläne einrichten und verwenden. 

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

[Taktische und Betriebsplanung für den Produktprogrammplanungslauf trennen](http://blogs.msdn.com/b/axmfg/archive/2012/10/12/separating-tactical-and-operative-planning-for-master-scheduling.aspx)

[Produktprogrammplanung: Verwenden eines statischen und dynamischen Produktprogrammplan oder verwenden Sie einen Plan?](https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)



