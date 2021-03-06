---
title: Affordable Care Act-Berichte erstellen
description: "Funktion ist verfügbar, um Arbeitgeber zu unterstützten, die Informationen erfassen müssen, die auf den Formularen 1095-B und 1095-C aufgrund des Abschnitts \"Employer Mandate \" im Affordable Care Act gemeldet wurden. Hinweis: Diese Funktionalität ist nur für juristische Personen in den USA aktiviert."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 1994edc5d6c932be3a285f9bb328a05504c90f07
ms.contentlocale: de-de
ms.lasthandoff: 03/07/2018

---
# <a name="generate-affordable-care-act-reports"></a>Affordable Care Act-Berichte erstellen

[!include [banner](includes/banner.md)]

Funktion ist verfügbar, um Arbeitgeber zu unterstützten, die Informationen erfassen müssen, die auf den Formularen 1095-B und 1095-C aufgrund des Abschnitts **Employer Mandate** im Affordable Care Act gemeldet wurden. Hinweis: Diese Funktionalität ist nur für juristische Personen in den USA aktiviert.

## <a name="getting-started"></a>Erste Schritte
Wenn die auf den Formularen 1095-B und 1095-C zu meldende Informationen erstmalig nachverfolgt werden, müssen Sie zunächst eine oder mehrere Dispositionssteuerungsgruppen für Affordable Care Act erstellen. Diese Affordable Care-Dispositionssteuerungsgruppen werden verwendet, um das Angebot der Disponierung, das einem Mitarbeiter unterbreitet wurde, die günstigste Monatsprämie des Mitarbeiters (falls die Kosten über der Bundesarmutsgrenze liegen) sowie der vom Mitarbeiter verwendete Safe Harbor, sofern anwendbar, verwendet. Die Verwendung von Affordable Care Act-Gruppen ermöglicht es Ihnen, die Informationen für diese Felder zu verwalten, ohne alle Mitarbeiterdatensätze mit gleichen Bedingungen anfassen zu müssen. Darüber hinaus können Affordable Care-Dispositionssteuerungsgruppen mit der Massenzuweisungsfunktion auf der Seite leicht einem oder mehreren Mitarbeitern zugewiesen werden.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Mehrere Versionen einer Dispositionssteuerungsgruppe aufrecht halten
Sie können mehrere Versionen einer Dispositionssteuerungsgruppe wahren, und dadurch Änderungen vornehmen, damit die Informationen der Gruppe aktuell sind, ohne eine neue Gruppe zu erstellen und Mitarbeiter neu zuordnen zu müssen, wenn sich in der Organisation oder in der angebotenen Leistung etwas ändert. 

Nachdem Sie die Affordable Care-Dispositionssteuerungsgruppen erstellt haben, die Sie benötigen, können Sie die Gruppen mit der **Massen-Zuweisung**-Funktion auf der Seite Mitarbeitern zuweisen, oder Sie können bei jedem Mitarbeiter angeben, ob ACA-Informationen verfolgt und für diesen Mitarbeiter gemeldet werden müssen. Außerdem können Sie den Mitarbeiter einer Affordable Care-Dispositionssteuerungsgruppe zuweisen.

Wenn Affordable Care-Dispositionsinformationen für einen Mitarbeiter nicht nachverfolgt oder gemeldet werden müssen, beispielsweise beim einem Teilzeitbeschäftigten, kann das Feld **Berichtsdisposition** auf "Nein" festgelegt werden. Obwohl jeder Mitarbeiter, für den ACA-Information nachverfolgt werden müssen, einer Affordable Care-Dispositionssteuerungsgruppe zugewiesen werden muss, können Sie die Optionen **Abdeckungsangebot**, **Mitarbeiteranteil an den Kosten** und **Safe Harbor** für einen Monat (oder Monate), bei denen andere Werte als bei der Affordable Care -Dispositionssteuerungsgruppe eingegeben werden müssen, ändern.

Um Ausnahmen für Affordable Care-Dispositionssteuerungsgruppenwerte einzugeben, klicken Sie auf den Link "Affordable Care-Disposition" auf der Seite "Details zur Arbeitskraft", unter dem Abschnitt " Zusätzliche Informationen" auf der Registerkarte "Mitarbeiter".

## <a name="reporting-health-care-coverage"></a>Melden von Gesundheitsvorsorgeabdeckung
Neben der Nachverfolgung, ob einem Vollzeitmitarbeiter Krankenversicherungsschutz angeboten wird, ob der Arbeitgeber eine vom Arbeitgeber geförderten selbstversicherten Krankenversicherungsschutz, für den der Mitarbeiter registriert ist, (unabhängig davon, ob sie Vollzeit- oder Teilzeitbeschäftigt sind) anbietet, müssen Zusatzinformationen im 1095-C gemeldet werden. Jeder Mitarbeiter (einschließlich abhängiger), die von Arbeitgeber-geförderten Vorteilspläne abgedeckt sind, muss in dem Bericht für die Monate einbezogen werden, die sie abgedeckt waren. 

Sie können angeben, ob jeder Vorteilsplan angegeben werden muss, indem Sie das Kontrollkästchen **ACA meldepflichtig** aktivieren.

Wenn Mitarbeiter darüber hinaus ausgewählt haben, irgendwelche ihrer abhängigen Personen unter einer Leistung abdecken zu lassen, können Sie auf der Seite "Vergütungen verwalten" das Datum angeben, zu dem die Unterhaltsberechtigten für jeden Mitarbeiter abgedeckt wurden. Um anzugeben dass der Unterhaltsberechtigte unter der Vergütung abgedeckt wird, wählen Sie im Aktivitätsbereich des Inforegisters "Unterhaltsberechtigte" die Schaltfläche "Bearbeiten" aus.

Auf der Seite **Manager des Dispositionsdatums für Unterhaltsberechtigte** können Sie den Zeitraum angeben, zu dem der Unterhaltsberechtigte durch die Vergütung abgedeckt wurde. Das Eingeben von Daten auf dieser Seite aktiviert automatisch das Kontrollkästchen **Abgedeckt** auf der Seite **Vergütungen verwalten**.

## <a name="generate-1095b-and-1095c-forms"></a>1095B- und 1095C-Formulare generieren
Sie können Formulare 109-B und mit 1095-C im Produkt erstellen und sie an jeden der Mitarbeiter verteilen. Das System kann 1095-C und die entsprechenden 1094-C-Übertragungsdateien zum Senden an die IRS generieren.  

Wenn Sie das Formular 1095-C generieren, geben Sie das entsprechende Kalender- oder Geschäftsjahr ein und, ob Sie das zwei- oder dreiseitige Formular drucken möchten. Das dreiseitige Formular ist nur erforderlich, wenn der Arbeitgeber eigenversicherte Abdeckung bereitgestellt hat und ein Mitarbeiter mehr als sechs abgedeckte Unterhaltsberechtigte einschließlich sich selbst angibt. Wenn Sie das zweiseitige Formular generieren, erkennt das System automatisch, ob ein Mitarbeiter mehr als 6 abgedeckte Unterhaltsberechtigte hat und schließt den Mitarbeiter bei der Formulargenerierung aus. Wenn darüber hinaus das dreiseitige Formular generiert wird, schließt das System nur die Mitarbeiter ein, die mehr als sechs abgedeckte Unterhaltsberechtigte haben.

## <a name="viewing-information"></a>Informationen anzeigen
Sie können die Seite **Deckung für Affordable Care Act für Arbeitskraft** verwenden, um festzustellen, welche Mitarbeiter jeder Dispositionssteuerungsgruppe zugewiesen wurden, welche Mitarbeiter im Bericht nicht eingeschlossen werden müssen und welche Mitarbeiter nicht zugewiesen sind.

Wurden irgendwelche der Standardwerte der Affordable Care-Dispositionssteuerungsgruppe überschrieben, wird ein Sternchen neben dem geänderten Wert angezeigt. Wenn die Werte für alle 12 Monate identisch sind und nicht überschrieben wurden, wird der Wert in der Spalte **Alle 12 Monate** ausgegeben.

Sie können das Abfragefenster auch verwenden, um besser zu verstehen, welche Mitarbeiter markiert wurden, nicht ACA meldepflichtig zu sein. Das bedeutet, dass Sie nicht verfolgen müssen, ob ihnen Abdeckung angeboten wurde und dass Sie am Jahresende kein 1095-C für sie ausstellen müssen. Durch die Auswahl von **Nicht ACA meldepflichtig** im Feld **Filtern nach** können Sie eine Liste aller Mitarbeiter generieren, die markiert wurden, um 1095-C nicht zu erhalten.

Zusätzlich zur Anzeige einer Liste von Mitarbeiten, die nicht ACA meldepflichtig sind, können Sie auch alle Mitarbeiter anzeigen, die nicht zugewiesen sind (das Feld **ACA-Berichtsdisposition** ist leer) oder die einer Affordable Care-Dispositionssteuerungsgruppe zugewiesen wurden, die für das im Feld **Jahr** ausgewählte Jahr abgelaufen ist.

Sie können Mitarbeiterlisten exportieren, die mithilfe einer der Filteroptionen in Excel generiert wurden.

Wenn Sie abgedeckte Personen angegeben müssen, da Sie als Arbeitgeber eigenversicherte Disposition bereitstellen, können Sie auch alle Unterhaltsberechtigten anzeigen, die unter Vorteilsplänen gedeckt werden, die als **ACA meldepflichtig** markiert wurden. Wählen Sie dazu die Aktion "Abdeckung für Unterhaltsberechtigte anzeigen" auf der Aktivitätsbereichsleiste aus.

**Hinweis:** Nur Leistungen, deren Plan als **ACA meldepflichtig** markiert wurde, werden im Abfragefenster angezeigt.

