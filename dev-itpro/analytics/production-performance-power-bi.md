---
title: "Power BI-Inhalt – Produktionsleistung"
description: "In diesem Thema wird beschrieben, was im Warehouse Performance Power Bl Inhalt enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen."
author: sericks
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 915ff93edff0f68f52a536ad169c8f0f917ac9b2
ms.contentlocale: de-de
ms.lasthandoff: 06/20/2017

---

# <a name="production-performance-power-bi-content"></a>Power BI-Inhalt – Produktionsleistung

[!include[banner](../includes/banner.md)]

In diesem Thema wird beschrieben, was im **Produktionsleistung** Microsoft Power Bl Inhalt enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

## <a name="overview"></a>Überblick

Der **Produktionsfluss** ist für Power BI Inhalt für Produktions-Managers oder Personen in der Organisation, die für Produktionssteuerung zuständig sind.

Die Berichte, die in Power BI Inhalt eingeschlossen sind, um die Leistung von Produktionsvorgängen hinsichtlich der fristgerechten Ausführung, der Qualität und der Kosten zu überwachen. Die Berichte verwenden Transaktionsdaten von Produktionsaufträgen sowie von Chargenaufträgen und bieten eine gesamte wertberichtigte, unternehmensweite Produktionsmetrik und eine Aufschlüsselung der Metrik nach Produkt und Ressource an.

Der Power BI Inhalt hebt die Möglichkeit der Organisation hervor, die Produktion pünktlich und vollständig abzuschließen. Zukünftige Leistung wird auf Basis der projektiert Produktionspläne geplant. Verständliche Berichte enthalten detaillierte Einblicke in Produktfehler, die während der Produktion anfallen, und zeigt auch die Defektsätze für Ressourcen und Arbeitsgänge.

Mit diesem Power BI Inhalt können Sie Produktionsabweichungen analysieren. Die Produktionsabweichung wird als Differenz zwischen aktiven Kosten und realisierten Kosten berechnet. Die Berechnung von Produktionsabweichungen erfolgt, wenn Produktionsaufträge oder Chargenaufträge den Status **Beendet** erreichen.

Der **Produktionsfluss** Power BI Inhalt umfasst Daten, die aus Produktionsaufträgen und Chargenaufträgen stammen. Die Berichte enthalten keine Daten, die den Kanbanproduktionen zugeordnet sind.

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt
Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, Juli 2017 verwenden, wird der Power PB Inhalt **Produktionsleistung** auf der Seite **Produktionsleistung** **Produktionsverwaltung** > **Abfragen und Berichte** > **Produktionsleistungsanalyse** > **Produktionsleistung** angezeigt. 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrik, die im Power BI Inhalt enthalten ist

Der **Produktionsfluss** Power BI Inhalt enthält einen Satz Berichtsseiten. Jede Seite enthält einen Satz Metriken, die als Diagramme, Kacheln und Tabellen visuell dargestellt werden.

Die folgende Tabelle enthält eine Übersicht der Visualisierungen im Inhaltspaket.

| Berichtsseiten                                | Diagramme                                               | Kacheln |
|--------------------------------------------|------------------------------------------------------|-------|
| Produktionsleistung                     | <ul><li>Anzahl der Produktionsauftragspositionen nach Datum</li><li>Anzahl der Produktionen nach Produkt und Artikelgruppe</li><li>Anzahl der geplanten Produktionsaufträge nach Datum</li><li>10 tiefsten Produkte nach Pünktlichkeit und Vollständigkeit</li></ul> | <ul><li>Gesamtbestellung</li><li>Rechtzeitig und vollständig in Prozent</li><li>Unvollständig in %</li><li>Vorzeitig in %</li><li>verspätet in %</li></ul> |
| Defekte nach Produkt                         | <ul><li>Fehlerhafter Satz (PPM) nach Datum</li><li>Fehlerhafte Rate nach Produkt (PPM) und Artikelgruppe</li><li>Jährlich produzierte Menge nach Datum</li><li>Top 10 Produkte nach gültigem Preis</li></ul> | <ul><li>Fehlerhafter Satz (PPM)</li><li>Fehlerhafte Menge</li><li>Gesamtmenge</li></ul> |
| Defekter Trend nach Produkt                   | Defekter Satz (PPM) nach produzierter Menge | Fehlerrate (ppm) |
| Defekte nach Ressource                        | <ul><li>Fehlerhafter Satz (PPM) nach Datum</li><li>Fehlerhafter Satz (PPM) nach Ressource und Standort</li><li>Fehlerhafter Satz (PPM) nach Betrieb</li><li>Top 10 Ressourcen nach Defektsatz</li></ul> | Fehlerhafte Menge |
| Defekter Trend nach Ressource                  | Defekter Satz (PPM) nach produzierter Menge | |
| Produktionsabweichungen für eine Auftragskalkulation | <ul><li>Produktionsabweichung von Datums- und Kostengruppentyp</li><li>Produktionsabweichung nach Standort und Kostengruppentyp</li><li>Top 10 Produkte mit ungünstiger Produktionsabweichung</li><li>Top 10 Produkte mit ungünstiger Produktionsabweichung nach Ressource</li></ul> | <ul><li>Realisierte Kosten</li><li>Produktionsabweichung</li><li>Produktionsabweichung in %</li></ul> |

## <a name="extending-the-power-bi-content"></a>Erweitern des Power BI-Inhalts
Wenn Sie die Inhaltspakete verwenden, die in Microsoft Dynamics Lifecycle Services (LCS) verfügbar sind, können Sie großartige Analysen für Person bereitstellen, die sich nicht in Microsoft Dynamics 365 anmelden. Sie können diese Inhaltspakete so ändern, dass sie andere Berichte oder grafische Elemente umfassen, und die Inhaltspakete dann für die Analyse auf Ihrem Power BI.com-Mandanten veröffentlichen.

Sie finden die **Produktionsleistung**-Power BI Inhalt in der freigegebenen Anlagenbibliothek in LCS. Weitere Informationen dazu, wie Sie Power BI-Inhalte herunterladen und in Ihrer Organisation implementieren, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md). Um eine Vorführung anzusehen, die zeigt, wie der Power BI-Inhalt impementiert wird, zeigen Sie den Office Mix [Power BI-Inhalt von Microsoft und Ihren Partnern in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) an.

Stellen Sie sicher, dass Sie den **Produktionstleistungs**-Inhalt herunterladen, der der von Ihnen verwendeten Dynamics 365-Version entspricht.

> [!NOTE]
> Wenn Sie Microsoft Dynamics 365 for Operations, Version 1611, verwenden, ist KB 4011327 eine Voraussetzung für diesen Power BI-Inhalt. Nachdem Sie sich bei LCS angemeldet haben, können Sie unter https://fix.lcs.dynamics.com/issue/results/?q=kb4011327 auf KB zugreifen.

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

Die folgenden Daten werden verwendet, um die Berichtsseiten im Power BI-Inhalt **Produktionsleistung** auszufüllen. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden. Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die zwecks Analyse optimiert ist. Weitere Informationen zu den Entitätsshop finden Sie unter [Power BI-Integration mit Entitäts-Shop](power-bi-integration-entity-store.md).

Die folgenden aggregierten Messungen der Rechnungspositionsentität werden als Grundlage des Power BI Inhalts verwendet.

| Entität                   | Zentrale aggregierte Messungen  | Datenquelle für Finance and Operations | Feld              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

Die folgende Tabelle zeigt, wie die zentralen aggregierten Messungen verwendet werden, um mehrere berechnete Kennzahlen im Dataset des Inhalts zu erstellen.

| Kennzahl                  | Wie die festgelegte Kennzahl berechnet wird |
|--------------------------|-------------------------------|
| Produktionsabweichung in %   | SUMME ("Produktionsabweichungs" Produktionsabweichung[])/ (SUMME "Produktionsabweichung "[ vorkalkulierte Kosten)] |
| Alle Bestellvorschläge       | COUNTROWS (Geplanter Produktionsauftrag) |
| Vorzeitig                    | COUNTROWS(FILTER('Geplanter Produktionsauftrag', 'Geplanter Produktionsauftrag'[Geplantes Enddatum] \< 'Geplanter Produktionsauftrag'[Anforderungsdatum])) |
| Verspätet                     | COUNTROWS(FILTER('Geplanter Produktionsauftrag', 'Geplanter Produktionsauftrag'[Geplantes Enddatum] \> 'Geplanter Produktionsauftrag'[Anforderungsdatum])) |
| Termingerecht                  | COUNTROWS(FILTER('Geplanter Produktionsauftrag', 'Geplanter Produktionsauftrag'[Geplantes Enddatum] = 'Geplanter Produktionsauftrag'[Anforderungsdatum])) |
| Termingerecht %                | IF ("geplanter Produktionsauftrag" [] Einschaltzeit \<\> 0, "Einschaltzeit geplanter Produktionsauftrag" [], IF ("geplanter Produktionsauftrag" [alle Bestellvorschläge] \<\> 0, 0, LEER()))/"geplanter Produktionsauftrag" [alle Bestellvorschläge] |
| Abgeschl.                | COUNTROWS (FILTER ("Produktionsauftrag", "Produktionsauftrag" [], ist RAF'ed TRUE)) = |
| Fehlerhafter Satz (PPM)     | IF ("Produktionsauftrag" [Gesamtmenge] = 0, BLANK(), (SUMME(Produktionsauftrag[Ausschussmenge]) / Produktionsauftrag[Gesamtmenge]\* 1000000) |
| Verzögerte Produktionsrate  | "Produktionsauftrag [Spät \#]/Produktionsauftrag abgeschlossen [Abgeschlossen] |
| Vorzeitig und vollständig          | COUNTROWS(FILTER('Produktionsauftrag', 'Produktionsauftrag'[Vollständig] = TRUE && 'Produktionsauftrag'[Vorzeitig] = TRUE)) |
| Vorzeitig \#                 | COUNTROWS (FILTER ("Produktionsauftrag", "Produktionsauftrag" [ist vorzeitig] = TRUE)) |
| Vorzeitig in %                  | IFERROR( IF('Produktionsauftrag'[Vorzeitig \#] \<\> 0, 'Produktiosnauftrag'[Vorzeitig \#], IF('Produktionsauftrag'[Gesamtauftrag] = 0, BLANK(), 0)) / 'Produktionsauftrag'[Gesamtauftrag], BLANK()) |
| Unvollständig               | COUNTROWS(FILTER('Produktionsauftrag', 'Produktionsauftrag'[Vollständig] = FALSE && 'Produktionsauftrag'[Is RAF'ed] = TRUE)) |
| Unvollständig in %             | IFERROR( IF('Produktionsauftrag'[Unvollständig] \<\> 0, 'Produktionsauftrag'[Unvollständig], IF('Produktionsauftrag'[Gesamtauftrag] = 0, BLANK(), 0)) / 'Produktionsauftrag'[Gesamtauftrag], BLANK()) |
| verzögert               | 'Produktionsauftrag'[Is RAF'ed] = TRUE && 'Produktionsauftrag'[Verzögerter Wert] = 1 |
| Ist früh                 | 'Produktionsauftrag'[Is RAF'ed] = TRUE && 'Produktionsauftrag'[Tage verzögert] \<0 |
| Vollständig               | "Produktionsauftrag" [] Gute Menge \>= "Produktionsauftrag" [Planmenge] |
| Ist RAF'ed                | "Produktionsauftrag" [Produktionsstatuswert] = 5\ |\| "Produktionsauftrag" [Produktionsstatuswert] = 7\ |
| Spät und vollständig           | COUNTROWS(FILTER('Produktionsauftrag', 'Produktionsauftrag'[Vollständig] = TRUE && 'Produktionsauftrag'[Verspätet] = TRUE)) |
| verspätet \#                  | COUNTROWS (FILTER ("Produktionsauftrag", "Produktionsauftrag" [ist voerspätet] = TRUE)) |
| verspätet in %                   | IFERROR( IF('Produktionsauftrag'[Spät \#] \<\> 0, 'Produktiosnauftrag'[Spät \#], IF('Produktionsauftrag'[Gesamtauftrag] = 0, BLANK(), 0)) / 'Produktionsauftrag'[Gesamtauftrag], BLANK()) |
| Rechtzeitig und vollständig        | COUNTROWS(FILTER('Produktionsauftrag', 'Produktionsauftrag'[vollständig] = TRUE && 'Produktionsauftrag'[verspätete] = FALSE && 'Produktionsauftrag'[Vorzeitig] = FALSE)) |
| Rechtzeitig und vollständig in Prozent      | IFERROR( IF('Produktionsauftrag'[Unvollständig] \<\> 0, 'Produktionsauftrag'[Rechtzeitig und vollständig], IF('Produktionsauftrag'[abgeschlossen] = 0, BLANK(), 0)) / 'Produktionsauftrag'[abgeschlossen], BLANK()) |
| Gesamtbestellung             | COUNTROWS (Produktionsauftrag) |
| Gesamtmenge           | SUMME('Produktionsauftrag'[Gute Menge]) + SUMME('Produktionsauftrag'[Fehlerhafte Menge]) |
| Fehlerrate (ppm)        | IF( 'Routentransaktion'[Verarbeitete Menge] = 0, BLANK(), (SUMME('Routentransaktion '[Fehlerhafte Menge]) / 'Routentransaktion'[Verarbeitete Menge]) \* 1000000) |
| Fehlerverhältnis (ppm) | IF( 'Routentransaktion'[Gesamte gemischte Menge] = 0, BLANK(), (SUMME('Routentransaktion '[Fehlerhafte Menge]) / 'Routentransaktion'[Gesamte gemischte Menge]) \* 1000000) |
| Verarbeitungsmenge       | SUMME (Arbeitsplanbuchungen [Gute Menge]) + SUMME (Arbeitsplanbuchung[Ausschussmenge]) |
| Gesamte gemischte Menge     | SUM('Produktionsauftrag'[Gute Menge]) + SUM('Routentransaktion'[Fehlerhafte Menge]) |

Die folgenden wichtigen Dimensionen im Verkaufscube werden als Filter verwendet, um die aggregierten Messungen zu teilen, um eine größere Granularität zu erreichen und tiefere und analytische Einblicke bereitzustellen.

| Entität                    | Beispiele für Attribute                                        |
|---------------------------|---------------------------------------------------------------|
| Datum der Fertigmeldung | Abschlussdatum (Fertigmeldung), Monat und Jahr                 |
| Enddatum                | Beendetes Monatsgegenkonto und Monat                                  |
| Bedarfsdatum          | Bedarfsdatummonat Bedarfsdatum und Gegenkonto            |
| Arbeitsplan-Buchungsdatum    | Arbeitsplanbuchungsmonat Gegenkonto und Datum                       |
| Standorte                     | Standorte-Kennung, Standortsname, Bundesland und Ort                          |
| Entitäten                  | Benutzerkennung und Name                                                   |
| Ressourcen                 | Ressourcen-ID, Ressourcenname, Ressourcentyp und Ressourcengruppe |
| Produkte                  | Produktnummer, Produktname, Artikelgruppenname und Artikel-ID         |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

- [Datenentitäten](https://ax.help.dynamics.com/en/wiki/data-entities/)
- [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](http://ax.help.dynamics.com/en/wiki/configuring-powerbi-integration/)
