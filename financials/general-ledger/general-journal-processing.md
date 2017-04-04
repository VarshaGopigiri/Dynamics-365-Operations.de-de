---
title: Allgemeine Erfassungsverarbeitung
description: "Diese bezeichnet Artikel Funktionen in Microsoft Dynamics 365 für Arbeitsgänge, die von Marketingkanälen, Verarbeiten der allgemeinen Erfassung zu vereinfachen und außerdem von Marketingkanälen Feld, um sicherzustellen, den, korrekten Daten Kostengruppe dennoch und internen Kontrollen nicht beeinträchtigt wird."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 50cd203025be8857de943e458fc32315e494fb7a
ms.lasthandoff: 03/31/2017


---

# <a name="general-journal-processing"></a>Allgemeine Erfassungsverarbeitung

Dieser Artikel beschreibt die Funktionen in Microsoft Dynamics AX, mit denen die allgemeine Erfassung einfacher wird und die auch helfen sicherzustellen, dass die korrekten Daten erfasst und die internen Kontrollen nicht beeinträchtigt werden.  

Journale

Einer der wichtigsten Bereiche einrichten ist Journale. Es empfiehlt sich, bestimmte Journale für jeden Zweck, wie Abgrenzungsregulierung Fehlerkorrektur Intercompany, und zu definieren. Sie können jedes Journal anpassen, mit deren Hilfe, Dateneingabe für jeden Zweck einfach und sicherstellen zu machen. 

Auf der Seite **Journale** können Sie folgende Elemente einrichten:

-   **Workflowgenehmigung** - Definieren Sie Journal-Workflows, die basierend auf Kriterien wie „Gesamt“ oder „Betrag“ Wesentlichkeitsgrenzen für Überprüfung- und Genehmigungsschritte festlegen, um die interne Kontrolle zu erhöhen. Sie richten für Workflow die allgemeinen Erfassungen auf der Seite. ** ** Hauptbuchworkflows
-   **Standardwerte** – Wählen Sie Standardwerte für Gegenkonten, Währung und Finanzdimensionen aus.
-   **Erfassungssteuerung** – Richten Sie Einschränkungen für den Unternehmens- und Kontotyp und die Segmentwerte ein. 

**Beispiele**

Ein Journal kann nur für Regulierungen verwendet werden. In diesem Fall können Sie angeben, dass nur die **Sachkonto**-Kontenart für alle Unternehmen gültig ist. ![Erfassungssteuerungskontenart( [] . /media/journal-control-account-types1.png)]". /media/journal-control-account-types1.png)

Ein Journal kann nur für ein bestimmtes Segment oder für einen Bereich für Hauptkonten verwendet werden. ![Erfassungssteuerungssegment( [] . /media/journal-control-segment1.png)]". /media/journal-control-segment1.png)

Die Option **Automatische Rückbuchung** ist nur in allgemeinen Erfassungen verfügbar. Beispiel: Sie haben eine Abgrenzungsregulierung, in der das eigentliche Dokument noch nicht verarbeitet wurde, wie in der folgenden Abbildung dargestellt.
[Rückbuchungen] (![allgemeine Erfassung. /media/general-journal-reversing1.png)]". /media/general-journal-reversing1.png) 

Das Microsoft Excel-Add-In für Erfassungseintrag enthält einen zusätzlichen Automatisierungsgrad vornimmt Dateneingabe und einfacher. Die **Positionen in Excel öffnen**-Aktivität ist auf den Seiten **Allgemeine Erfassung** und **Alle Journale** verfügbar. 

Auf der Seite **Periodische Erfassungen** können Sie wiederholende Erfassungen einrichten, um die Erfassungsverarbeitung zu automatisieren. 

Belegvorlagen können jederzeit verwenden. ** Auf der allgemeine Erfassungen ** Seite, ** Speichern ** ** Belegvorlage und wählen Sie aus ** Aktivitäten auf werden der Erfassungsbeleg ** ** Seite, unter ** Funktionen ** für Belegpositionen die gesucht.

## <a name="related-setup"></a>Verwandte Einstellung
Die folgende Einstellung ist für allgemeine Erfassungen nicht spezifisch, sorgt aber dafür, dass die Dateneingabe richtig und einfach ist.

### <a name="main-account"></a>Hauptkonto

Die Hauptkontoeinstellung stellt viele Optionen zum Verarbeiten der allgemeinen Erfassung bereit:

-   **SOLL/HABEN-Anforderung** - Verwenden Sie diese Option, wenn ein Hauptkonto auf Soll- oder Habenbuchungen beschränkt ist. Die Einstellung wird überprüft, wenn eine Erfassung geprüft oder gebucht wird.
-   **Standardgegenkonto**
-   **Unterbrochen** – Aussetzen eines Hauptkontos für die Dateneingabe für alle Unternehmen oder für ein bestimmtes Unternehmen bzw. bestimmte juristische Personen
-   **Keine manuellen Eingaben zulassen** – Verhindert, dass Benutzer in Erfassungen manuell einen Wert für dieses Konto eingeben
-   **Standard-Währung/Währung prüfen**
-   **Juristische Person überschreibt** - Diese Einstellung ist spezifisch für das definierte Unternehmen/die definierte juristische Person:
    -   **Standard-MwSt/MwSt prüfen**
    -   **Standarddimension** – **Nicht fixiert** oder **Fester Wert** **Fester Wert** unterstützt, dass alle Buchungen für dieses Hauptkonto immer einen beliebigen Dimensionswert verwenden, der als **Fest** eingerichtet ist.
-   **Buchungsprüfung**
    -   **Benutzervalidierung** - Diese Option regelt, welche Benutzer auf ein Hauptkonto buchen dürfen.
    -   **Überprüfung des Buchungstyps** – Diese Option regelt, welche Buchungsarten für ein Hauptkonto zulässig sind.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Buchhaltungsstrukturen und Strukturen für erweiterte Regeln

Buchhaltungsstrukturen und Strukturen für erweiterte Regeln sind sehr wichtig, um sicherzustellen, dass die Daten, die für die Finanzberichterstellung und die Leistungsnachverfolgung erforderlich sind, während der allgemeinen Erfassungsverarbeitung und in allen Dokumentationen erfasst werden. Mit Buchhaltungsstrukturen und Strukturen für erweiterten Regeln können Sie die Dateneingabeerfahrung anpassen. Sie können die Dateneingabe nur für Finanzdimensionen zulassen, die in jeder Situation relevant sind. Sie können auch die Anforderung erzwingen, dass erforderliche und korrekte Daten immer erfasst werden.

Weitere Informationen finden Sie unter: [Planung Kontenplan (plan-chart-of-accounts.md]). 

