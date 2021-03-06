---
title: Buchhaltungsquellen-Explorer
description: "Dieser Artikel enthält Informationen zum Buchhaltungsquellexplorer, den Sie für die detaillierte Analyse der Quellinformationen hinter den Hauptbuchbuchhaltungseinträgen verwenden können."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cb5a674472936a52b624c548fd37079d57eb6cb7
ms.openlocfilehash: d21f214ef8a29c19f0af1d4a2bdfc3264987f0b8
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---

# <a name="accounting-source-explorer"></a>Buchhaltungsquellen-Explorer

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zum Buchhaltungsquellexplorer, den Sie für die detaillierte Analyse der Quellinformationen hinter den Hauptbuchbuchhaltungseinträgen verwenden können.

Der Buchhaltungsquellen-Explorer ist eine neue Seite, die Quellinformationen anzeigt. Sie können den Buchhaltungsquellexplorer entweder als eigenständiges Tool verwenden oder die Details nach Hauptbuchbuchhaltungseinträgen analysieren. So können Sie Buchhaltungsquellexplorer verwenden, um die aktuellesten Detailquellinformationen für einen Saldo in der Probebeilanz oder für eine Belegbuchungen abzurufen. Sie können dann die Funktion "Nach Microsoft Excel exportieren" verwenden, um die Informationen in Microsoft Excel weiter aufzuteilen (beispielsweise in einer Pivottabelle oder einem PivotTable-Bericht).

Der Buchhaltungsquellen-Explorer zeigt stets denselben Gesamtbetrag pro Sachkonto wie das Hauptbuch an (beispielsweise in der Zwischenbilanz). Wie in der Zwischenbilanz können Sie Segmente in unterschiedlichen Spalten anzeigen. Wählen Sie einfach den entsprechenden Finanzdimensionssatz aus. 

Sie können Parameter verwenden, um ein Datumsintervall für die Analyse zu definieren. Diese Funktion ähnelt der Funktion in der Zwischenbilanz.

Für alle Dokumente, die das Quelldokumentframework verwenden, zeigt das Gegenkonto Quellexplorer zusätzliche Informationen, basierende auf der Buchhaltungsverteilungen und ggf. der  Projektbuchhaltungsverteilungen. Diese Informationen enthalten den Geldbetrag Typ, Projekt, Kategorie, Projektvorgang und Abrechnungscode. Nachfolgend finden Sie einige Analysebeispiele:

-   Abweichungen zwischen Bestellungen und Kreditorenrechnungen, da jede Abweichung durch einen Geldbetragstyp dargestellt wird (z. B. Abweichung der Belastung)
-   Differenz zwischen berechenbaren Stunden und nicht-berechenbaren Stunden und Ausgaben pro Projekt, Unternehmenseinheit und Hauptkonto

Für Quelldokumente, die das Konzept der Quelldokument-Referenzidentitäten verwenden, zeigt der Buchhaltungsquellen-Explorer noch weitere Details an, z. B. Debitor, Kreditor, Arbeitskraft, Produkt, Menge, Einheitentext und Beschreibungen. Nachfolgend finden Sie einige Analysebeispiele:

-   Hotelkosten pro Unternehmenseinheit und Hotelmarke für einen Finanzzeitraum auf der Grundlage von Spesenabrechnungen
-   Rabatte nach Kreditor, Produkt, Abteilung

Für diese Dokumente können Sie vom Buchhaltungsquellen-Explorer aus auch zum ursprünglichen Quelldokument navigieren.




