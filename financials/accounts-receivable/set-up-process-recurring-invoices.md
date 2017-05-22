---
title: Einrichten und Verarbeiten von Serienrechnungen
description: "In diesem Artikel wird beschrieben, wie Serienrechnungen eingerichtet und verarbeitet werden. Sie können Serienrechnungen verwenden, wenn Sie Debitoren regelmäßig für den gleichen Betrag eine Rechnung stellen müssen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d37531eb746324c6ddb9ca363f2bde1dfd84a197
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-and-process-recurring-invoices"></a>Einrichten und Verarbeiten von Serienrechnungen

[!include[banner](../includes/banner.md)]


In diesem Artikel wird beschrieben, wie Serienrechnungen eingerichtet und verarbeitet werden. Sie können Serienrechnungen verwenden, wenn Sie Debitoren regelmäßig für den gleichen Betrag eine Rechnung stellen müssen.

<a name="create-a-recurring-free-text-invoice-template"></a>Erstellen einer Vorlage für Freitext-Serienrechnungen
---------------------------------------------

Um Debitoren regelmäßig dieselben Dienstleistungen in Rechnung zu stellen, müssen Sie eine Freitext-Rechnungsvorlage definieren, die immer wieder zum Ausstellen der Rechnungen verwendet werden kann. Diese Vorlage enthält folgende Informationen:

-   Kopfzeileninformationen, wie Steuergruppen, Zahlungsbedingungen und Zahlungsmethode
-   Positionsinformationen, wie eine Beschreibung der Dienstleistung, Umsatzerlöskonten, Preis je Einheit und Rechnungsbetrag
-   Zuschläge für Versand- oder Bearbeitungskosten
-   Buchhaltungsverteilungen zusammen mit Finanzdimensionsinformationen, wie Kostenstellen und Unternehmenseinheiten

Im Prinzip erstellen Sie eine komplette Rechnung und speichern diese als Vorlage. Sie können die Vorlagen unter Verwendung der Seite **Serienrechnungen** einrichten.

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a>Zuweisen einer Freitextrechnungsvorlage zu einem Debitor und Eingabe von Seriendetails
Nachdem die Vorlage erstellt wurde, müssen Sie die Vorlage den Debitoren zuordnen, für die Rechnungen erstellt werden sollen. Darüber hinaus müssen Sie angeben, wann und wie häufig die Rechnung verwendet wird. Sie können die Vorlagen auf der Registerkarte **Rechnung** der Seite **Debitoren** zuweisen. Fügen Sie die Vorlage der Liste hinzu, und aktualisieren Sie die folgenden Informationen:

-   Das Startdatum und (optional) das Enddatum für die Serienrechnung
-   Die Häufigkeit der Serienrechnung (beispielsweise täglich oder einmal im Monat)
-   Den maximalen Abrechnungsbetrag (wenn diese Angabe erforderlich ist)

Für einen Debitor können mehrere Vorlagen mit unterschiedlichen Zahlungshäufigkeiten erstellt werden.

## <a name="generate-the-recurring-invoices"></a>Generieren der Serienrechnungen
Auf der Seite **Serienrechnungen**gibt es eine Aufgabe zum Verarbeiten von Serienrechnungsvorlagen. Sie geben das Rechnungsdatum und die Vorlage zum Generieren der Rechnungen an. Die Rechnungen werden generiert, und jeder Gruppe von verarbeiteten Rechnungen wird eine individuelle Serienkennung zugewiesen.
Buchen von Freitext-Serienrechnungen
---------------------------------

Nachdem Serienrechnungen generiert wurden, werden die Serienkennungen in einer Buchungsaufgabe auf der Seite **Serienrechnungen**angezeigt. Sie können alle Rechnungen für eine Serienkennung anzeigen, indem Sie auf den Link klicken. Beim Überprüfen der Rechnungen für eine Serienkennung können Sie einzelne Rechnungen löschen. Die Wiederholungseinstellungen für den Debitor werden für diese Vorlage zurückgesetzt und können später neu generiert werden. Sie können eine, mehrere oder alle Rechnungen für eine Serienkennung buchen. Wenn Workflows aktiviert sind, müssen Sie auf **Senden** klicken, bevor Sie die Rechnungen buchen können.
Drucken von Freitext-Serienrechnungen
----------------------------------

Nach dem Buchen von Serienrechnungen können Sie die Rechnungen auf der Seite mit der Liste mit Freitextrechnungen drucken. Sie können die ausgewählten Rechnungen drucken oder einen Bereich von Rechnungen auswählen und drucken.



