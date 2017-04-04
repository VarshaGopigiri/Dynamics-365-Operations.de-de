---
title: Mischplanung - Hiermit werden einzelne, Prozess und schlanke Bevorratung
description: "Dieser Artikel enthält Informationen zum gemischten Planungsmodus. In im gemischten Planungsmodus können Sie Ihre Lieferkette basierend auf dem Materialfluss modellieren. Microsoft Dynamics 365 für Arbeitsgänge wird sichergestellt, dass der Materialfluss Ihren Modellen folgt, unabhängig von der Lieferungsrichtlinie, die ausgewählt wird &quot; Kanbans, Produktionsaufträge, Bestellungen, Umlagerungsaufträge Chargenaufträgen oder)."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d635421112f6d1e79a47090de3ffc4178b36b132
ms.lasthandoff: 03/31/2017


---

# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Mischplanung - Hiermit werden einzelne, Prozess und schlanke Bevorratung

Dieser Artikel enthält Informationen zum gemischten Planungsmodus. In im gemischten Planungsmodus können Sie Ihre Lieferkette basierend auf dem Materialfluss modellieren. Microsoft Dynamics 365 für Arbeitsgänge wird sichergestellt, dass der Materialfluss Ihren Modellen folgt, unabhängig von der Lieferungsrichtlinie, die ausgewählt wird " Kanbans, Produktionsaufträge, Bestellungen, Umlagerungsaufträge Chargenaufträgen oder). 

Sie können die allgemeine Strategie für das Beschaffen eines Produkts unabhängig von der Produktstruktur auswählen.  

So können Sie Kanbansteuerelemente in der Assembly haben, in der Materialien für den Montagebereich nach Produktionsaufträgen, Kanbans, Übertragungen, Stapelverarbeitungsaufträgen beschafft werden, oder eine beliebige Kombination, die für die Merkmale der Lieferkette geeignet ist, Sie jedoch die volle Übersicht über die Bereitstellung haben. Diese Funktion führt zu optimierten Lieferkettenprozessen und erweiterter Sichtbarkeit in der Lieferkette.  

Die Granularität der Lieferrichtlinien die im Produktprogrammplanungslauf verwendet werden, hängt von den Lagerdimensionen ab, die als Deckungsdimensionen aktiviert werden. Um den Produktprogrammplanungslauf zu aktivieren, um die Auffüllung und Bereitstellung von unterschiedlichen Arten der Lagerplätze zu steuern (beispielsweise durch das Trennen der Produktion für verschiedene Produktionseinheiten, oder durch Trennen unterschiedlicher Arten von Material- und Endproduktlagerorten), sollten Sie Standort und Lagerort als Deckungsdimensionen aktivieren. Alternativ kann der Lagerort als Deckungsdimension ausgelassen werden. In diesem Fall, wenn Sie erweiterte Lagerortverwaltung verwenden, werden alle Bewegungen innerhalb eines Lagerorts nach Lagerortarbeit gesteuert, während alle Bewegungen innerhalb von Lagerorten nach Entnahme-Kanbans gesteuert werden können.

## <a name="supply-policies"></a>Lieferrichtlinien
Dynamics 365 für Arbeitsgangsmischplanungskontrollen, beispielsweise ein Produkt beschafft wird und, basierend die Lieferung, z abgeleitete Anforderungen " Verbrauch von Artikeln aus einer Stückliste Stücklisten \[\]\[ausgegeben\]. Basierend auf dem Auftragstyp beschafft das System Materialien automatisch nach den Anforderungen.  

Lieferrichtlinien können auf der Produktebene oder einer beliebigen Granularität definiert werden, die Ihre Anforderungen unterstützt. Sie definieren die Granularität von Lieferrichtlinien auf der **Standardauftragseinstellungen**-Seite.  

Lieferrichtlinien können gesteuert werden nach Produkt, Artikeldimensionen (Konfiguration, Farbe und Größe), Standort und Lagerort. Diese Einstellung wird auf der Seite **Artikeldeckung **ausgeführt.  

Der standardmäßige Auftragstyp steuert das, was der Auftragsproduktprogrammplan generiert.  

Unabhängig davon, wie die Lieferkette modelliert wird, unterstützt Dynamics 365 für die Arbeitsgänge Lieferungspolitischen Mischung von Richtlinien. Sie können Produktionsaufträge haben, die von Kanbans beschafft werden. Alternativ können Sie einen Chargenauftrag haben, der ein Produkt benötigt, das nach Übertragungen oder nach Kanbans beschafft wird.  

Dynamics 365 für Arbeitsgänge wird sichergestellt, dass der Materialfluss das Modell folgt.  

Der Lagerort für die Entnahme des Materials wird dynamisch zur Laufzeit zugewiesen, nachdem die Lieferrichtlinie definiert wurde.  

In der Regel werden Kanbans nicht für zukünftige Zeiträume erstellt, da ein Kanban eine Kurzlebigkeit hat. Um vollständig Sichtbarkeit in der Lieferkette zu verwalten, haben wir das neue Planungskonzept eines "geplanten Kanbans" eingeführt, das verwendet wird, um abgeleitete Anforderungen zu berechnen, und hilft sicherzustellen, dass die Anforderungen auf der gleichen Logik basierend beschafft werden, die verwendet wird, wenn das tatsächliche Kanban erstellt wird.  

Die gleiche Logik ist daher für alle anderen Lieferrichtlinientypen vorhanden. Daher basiert die langfristige Materialplanung auf der gleichen Logik, von der Sie erwarten, dass sie mit dem tatsächlichen Aufträgen ausgeführt werden, nachdem die Produktion und Lieferung genehmigt wird.

## <a name="materials-allocation-crosssupply-policy--resource-consumption-on-boms"></a>Richtlinie der Material-Zuweisung – crosssupply Ressourcenverbrauch auf Stücklisten
Ressourcenverbrauch ist wichtige Funktionen. Ressourcenverbrauch ermöglicht, dass ein Lagerort für die Entnahme von Materialien dynamisch ausgewählt werden kann, basierend auf der Lieferrichtlinie (Auftragstyp), und erleichtert auch die Verwaltung von den Stammdaten.  

Ressourcenverbrauch erfordert, dass der Lagerort, von dem Material entnommen wird, auf Grundlage der Methode, wie das Produkt beschafft wird, zugewiesen wird. Das bedeutet, zur Laufzeit sucht das System die Ressourcen, die für das Herstellen verwendet werden sollen. Auf Grundlage dieser Ressourcen sucht das System dann den Entnahmelagerort.  

Für Arbeit, die unabhängig von einer Lieferrichtlinie ist, müssen Sie nicht Informationen zur Stückliste ändern, wenn die Lieferung geändert wird. Bei Änderungen auch unabhängig hoc wird sichergestellt Dynamics 365 für Arbeitsgänge, dass Materialien aus dem rechten Lagerort Ursprungs sind.

## <a name="process-manufacturing--the-production-type"></a>Prozessfertigung – Der Produktionstyp
Für vollständige Flexibilität im gemischten Modus, empfiehlt es sich, Produktionstyp Stücklisten für alle Produkte verwenden. Sie können Kanbans, Produktionsaufträge, Umlagerungsaufträge oder Bestellungen Anschließend können, ein Produkt zu liefern. Für Fertigungsverarbeitung muss der Produktionstyp **Formel**, **Kuppelprodukt**, **Nebenprodukt** oder **Planungsartikel** verwendet werden. Kanbans und Produktionsaufträge können nicht für diese Produktionstypen verwendet werden.

