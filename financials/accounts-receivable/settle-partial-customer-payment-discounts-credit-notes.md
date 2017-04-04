---
title: "Ausgleichen einer teilweise Debitorenzahlung, Rabatte für Gutschriften verfügt"
description: "Dieser Artikel führt Sie durch ein Szenario, in dem ein Skonto in eine Gutschrift übernommen wird, wenn die Originalrechnung auch ein Skonto beinhaltet."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: e43bcea67d9c408c93258f9b64565560b59fbb88
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Ausgleichen einer teilweise Debitorenzahlung, Rabatte für Gutschriften verfügt

Dieser Artikel führt Sie durch ein Szenario, in dem ein Skonto in eine Gutschrift übernommen wird, wenn die Originalrechnung auch ein Skonto beinhaltet. 

Fabrikam ermöglicht Debitoren, Skonti auf Teilzahlungen und auf Gutschriften. Ein Skonto kann für eine Gutschrift in Anspruch genommen werden, wenn die Gutschrift für eine Rechnung ausgegeben wird, für die der Debitor ein Skonto angenommen hat. Anstatt einen Habenbetrag für den Gesamtbetrag bereitzustellen, können Sie den Saldo des Debitors für einen Betrag gutschreiben, der das Skontoprozent des Debitors ausschließt. Die Ausgleichsparameter sind ** ** Debitorenparameter auf der Seite.

## <a name="invoice-and-credit-note"></a>Rechnung und Gutschrift
Debitor 4035 enthält eine Rechnung über 1.000,00 und eine Gutschrift für 100,00. Jedes Dokument hat einen 1-Prozent-Rabatt, wenn es in 14 Tagen beglichen wird. Auf der Seite** Debitorenbuchungen** können Sie diese Information anzeigen.

| Beleg    | Transaktionstyp | Datum      | Rechnung  | Geschuldeter Betrag in Buchungswährung | Gutschriftsbetrag in Buchungswährung | Gesamtbetrag  | Währung |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | Rechnung          | 6/28/2015 | 10050    | 1.000,00                             |                                       | 1.000,00 | USD      |
| CCRN-10050 | Gutschrift      | 6/28/2015 | CR-10050 |                                      | 100,00                                | -100,00  | USD      |

## <a name="settle-a-credit-note-with-an-invoice"></a>Eine Gutschrift mit einer Rechnung ausgleichen
Über die Seite **Debitorenbuchungen** öffnen Sie die Seite **Bankbuchungen**. Sie kann die Seite **Buchungen ausgleichen** verwendet werden, um die Rechnung und Gutschrift auszugleichen. Als Teil des Ausgleichsprozesses zeigt er die Skontodatumsangaben der Beträge an. Er markiert die zwei Dokumente und klickt anschließend auf **Buchen**, um die Buchungen auszugleichen. Es gibt einen Rabatt von -1,00 in der Gutschrift, da Fabrikam Rabatte für Gutschriften zulässt.

| Markieren     | Skonto verwenden | Beleg    | Konto | Datum      | Fälligkeitsdatum  | Rechnung  | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Ausgewählt | Normal            | FTI-10050  | 4035    | 6/28/2015 | 7/28/2015 | 10050    | 1.000,00                       | USD      | 990,00           |
| Ausgewählt | Normal            | CCRN-10050 | 4035    | 6/28/2015 | 7/28/2015 | CR-10050 | -100,00                        | USD      | -99,00           |

Rabattinformationen werden am unteren Rand der Seite **Buchungen ausgleichen** angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 7/12/2015 |
| Skontobetrag         | -1,00     |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | -1,00     |

Der Ausgleich ist 100,00 und umfasst eine Zahlung von 99,00 und einen Rabatt von 1,00.

