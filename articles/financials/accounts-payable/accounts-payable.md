---
title: "Startseite für Kreditorenkonten"
description: "Dieses Thema enthält eine Übersicht über die Kreditorenkonten."
author: twheeloc
manager: AnnBe
ms.date: 08/18/2017
ms.topic: index-page
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 21901
ms.assetid: 1e4c2ac4-077b-4678-8733-5cec8f6ff659
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7bc09cbd108949b37ea1b2207fc3e0c6961abf4b
ms.contentlocale: de-de
ms.lasthandoff: 02/07/2018

---

# <a name="accounts-payable-home-page"></a>Startseite für Kreditorenkonten

[!include [banner](../includes/banner.md)]

Dieses Thema enthält eine Übersicht über die Kreditorenkonten. 

Sie können Kreditorenrechnungen manuell eingeben oder elektronisch über eine Datenentität empfangen. Nachdem Rechnungen eingegeben oder empfangen wurden, können sie mithilfe einer Rechnungsgenehmigungserfassung oder über die Seite **Kreditorenrechnung** geprüft und genehmigt werden. Sie können den Prüfungsprozess mit einem Rechnungsabgleich, Kreditorenrechnungsrichtlinien und Workflows automatisieren, sodass bestimmten Kriterien entsprechende Rechnungen automatisch genehmigt und die übrigen Rechnungen zur Prüfung durch einen autorisierten Benutzer markiert werden.

**Geschäftsprozesse**

[![Geschäftsprozess](./media/AP-process.PNG)](./media/AP-process.PNG)

## <a name="set-up-accounts-payable"></a>Einrichten von Kreditorenkonten

Richten Sie Kreditorengruppen, Kreditoren, Buchungsprofile, verschiedene Zahlungsoptionen sowie Parameter zu Kreditoren, Gebühren, Lieferungen und Ziele, Solawechsel und andere Typen von Kreditorenkontendaten ein. 

[Kreditorenkonten konfigurieren](accounts-payable-overview.md)

[Buchhaltungsverteilungen und Erfassungseinträge im untergeordneten Sachkonto für Kreditorenrechnungen](accounting-distributions-subledger-journal-entries-vendor-invoices.md) 

[Neubewertung der Fremdwährung für Kreditorenkonten und Debitoren](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md)

## <a name="configure-vendor-invoices"></a>Kreditorenrechnungen konfigurieren

Verwenden Sie Kreditorenkonten, um Rechnungen und Aufwendungen an Kreditoren zu verfolgen.

[Kreditorenkonten-Rechnungsabgleich](accounts-payable-invoice-matching.md)

[Kreditorenbuchungsprofile](vendor-posting-profiles.md)

[Überprüfung des Kreditorenkonten-Rechnungsabgleichs einrichten](tasks/set-up-accounts-payable-invoice-matching-validation.md)

[Dreiseitige Abgleichsrichtlinien](three-way-matching-policies.md)

[Rechnungsabgleich sowie Intercompany-Bestellungen](invoice-matching-intercompany-purchase-orders.md)

[Beheben von Abweichungen beim Abgleich von Rechnungssummen](resolve-invoice-totals-invoice-matching-discrepancies.md)

[Standardgegenkonten für Kreditorenrechnungserfassungen und Rechnungsgenehmigungserfassungen](default-offset-accounts-vendor-invoice-journals.md)

[Mobile Rechnungsgenehmigungen](mobile-invoice-approvals.md)

[Arbeitsbereich für Kreditorkooperationsrechnungen](vendor-portal-invoicing-workspace.md)

[Kreditorenrechnungsautomatisierung](vendor-invoice-automation.md)

## <a name="configure-vendor-payments"></a>Kreditorenzahlungen konfigurieren 

Sie können jeder beliebigen benutzerdefinierten Zahlungsmethode einen vom System definierten Zahlungstyp zuweisen, wie Scheck, elektronischer Zahlungsverkehr oder Solawechsel. Zahlungstypen sind optional. Sie sind jedoch hilfreich, wenn Sie elektronische Zahlungen überprüfen und sie schnell feststellen möchten, welcher Zahlungstyp bei einer Zahlung verwendet wird. 

[Arbeitsbereich für Kreditorenzahlungen](vendor-payments-workspace.md)

[Gebühren für Kreditorenzahlung definieren](tasks/define-vendor-payment-fees.md)

[Kreditorenzahlungsbedingungen definieren](tasks/define-vendor-payment-terms.md)

[Überblick über die positive Zahlung](positive-pay-overview.md)

[Einrichten und Generieren von Dateien für positive Zahlungen](set-up-generate-positive-pay-files.md)

[Kreditorenzahlungen unter Verwendung eines Zahlungsvorschlags erstellen](create-vendor-payments-payment-proposal.md)

[Kreditorenzahlungen für einen Teilbetrag](vendor-payments-partial-amount.md)

[Einen Rabatt in Anspruch nehmen, der höher ist, als der berechnete Rabatt für eine Kreditorenzahlung](take-discount-more-calculated-discount-vendor-payment.md)

[Ein Skonto außerhalb der Skontoperiode in Anspruch nehmen](take-cash-discount-outside-cash-discount-timeframe.md)

[Elektronische Berichterstellung für Kreditorenschecks](electronic-reporting-sample-vendor-checks.md)

[Stornieren einer Kreditorenzahlung](reverse-vendor-payment.md)

[Überblick über Vorauszahlungsrechnungen und Vorauszahlungen](prepayments-invoices-vs-prepayments.md)

[Zentralisierte Zahlungen für Kreditorenkonten](centralized-payments-accounts-payable.md)

## <a name="settlements"></a>Ausgleiche

Unter den folgenden Themen finden Sie Informationen zum Verwalten von Ausgleichen. Ausgleich ist der Prozess für das Ausgleichen von Zahlungen mit Rechnungen. 

[Konfigurieren eines Ausgleichs](../cash-bank-management/configure-settlement.md)

[Ausgleich einer teilweisen Kreditorenzahlung vor dem Rabattdatum](settle-partial-vendor-payment-before-discount-or-final-payment-after.md)

[Ausgleich einer teilweisen Kreditorenzahlung, bei der es Rabatte auf Kreditorengutschriften gibt](settle-partial-vendor-payment-discounts-vendor-credit-notes.md)

[Ausgleichen einer teilweisen Kreditorenzahlung, die mehrere Rabattzeiträume hat](settle-partial-vendor-payment-multiple-discount-periods.md)

[Ausgleich einer teilweisen Kreditorenzahlung oder endgültigen Zahlung vor dem Rabatt](settle-partial-vendor-payment-or-final-payment-before-discount.md)

[Einzelner Beleg mit mehreren Debitoren- oder Kreditorendatensätzen](single-voucher-multiple-customer-vendor-records.md)



### <a name="additional-resources"></a>Zusätzliche Ressourcen

#### <a name="whats-new-and-in-development"></a>Neuigkeiten und Entwicklungen

Besuchen Sie [Microsoft Dynamics 365 – Produktplan](https://roadmap.dynamics.com/), um zu erfahren, welche neue Funktionen veröffentlicht wurden und welche neuen Funktionen gerade entwickelt werden. 

#### <a name="blogs"></a>Blogs

Meinungen, Neuigkeiten und weitere Informationen zu Kreditorenkonten und anderen Lösungen finden Sie im [Microsoft Dynamics 365-Blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).

Im [Microsoft Dynamics AX-Produktteamblog](https://blogs.msdn.microsoft.com/dax/) finden Sie viele Beiträge zu Kreditorenkonten. Auch wenn einige dieser Beiträge für die ältere Version von Kreditorenkonten verfasst wurden, gelten die gleichen Konzepte noch und die Prozeduren sind in der aktuellen Version ebenfalls vergleichbar.

Der [Microsoft Dynamics Operations-Partner-Community-Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) fasst alle Informationen zu Neuigkeiten und Trends bei MBS Operations für Microsoft Dynamics-Partner in einer einzigen Ressource zusammen.

#### <a name="task-guides"></a>Aufgabenleitfäden
Weitere Hilfe finden Sie als Aufgabenleitfäden innerhalb von Finance and Operations. Um auf Aufgabenleitfäden zuzugreifen, klicken Sie auf einer beliebigen Seite auf die Schaltfläche „Hilfe”.

#### <a name="videos"></a>Videos

Sehen Sie in den Videos zu Hilfe + Anleitungen nach, die jetzt im [YouTube-Kanal zu Microsoft Dynamics 365](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ) verfügbar sind.





