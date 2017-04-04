---
title: "Nehmen Sie ein Skonto außerhalb des Skontoabzinsungszeitraums"
description: "Dieser Artikel beschreibt zwei Szenarien, die zeigen, wie ein Skonto übernommen werden kann, wenn die Zahlung außerhalb der Skontoperiode erfolgt."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: bea9565f488c01e5e6aede8cabe73ac13b75dacb
ms.lasthandoff: 03/31/2017


---

# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>Nehmen Sie ein Skonto außerhalb des Skontoabzinsungszeitraums

Dieser Artikel beschreibt zwei Szenarien, die zeigen, wie ein Skonto übernommen werden kann, wenn die Zahlung außerhalb der Skontoperiode erfolgt.

Am 28. Juni erstellt April eine Rechnung in Höhe von 2.000,00 für den Kreditor " 3052. Für die Rechnung wird ein Skonto von 1 %, wenn die Rechnung innerhalb von 14 Tagen bezahlt wird.

## <a name="use-cash-discount-option--always"></a>Option "Skonto verwenden" = "Immer"
April erstellt eine Zahlung am 1. Juli, was nach dem Skontodatum ist. April öffnet die Seite **Transaktionen ausgleichen**, um die Transaktionen anzuzeigen, die ausgeglichen werden können. 

April markiert die Rechnung zur Zahlung. Kein Skonto wird genommen, da die Zahlung nach dem Skontodatum ist. Hat jedoch der Kreditor April-Genehmigung angegeben, um das Skonto dennoch zu nehmen. Daher ändert April den Wert im Feld Verwendungsskonto ** ** ** immer **.

| Markieren     | Skonto verwenden | Beleg   | Konto | Skontodatum | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Immer            | Inv-10030 | 3052    | 6/28/2015          | 7/12/2015 | 10030   | -2,000,00                      | USD      | -1.980,00        |

Rabattinformationen werden am unteren Rand der Seite **Buchungen ausgleichen** angezeigt.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 7/12/2015 |
| Skontobetrag         | -20,00    |
| Skonto verwenden            | Immer    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | -20,00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>Für die Berechnung von Rabatten zu verwendendes Datum = Ausgewähltes Datum
Wenn sowohl die Rechnung als auch die Zahlung gebucht wurden, kann das Skonto immer noch in Anspruch genommen werden, wenn die Transaktionen auf der Seite **Transaktionen ausgleichen** ausgeglichen werden. April ändert den Wert im Feld **Für die Berechnung von Rabatten zu verwendendes Datum** auf **Ausgewähltes Datum**. Sie gibt das Datum 28. Juni ein, das in der Skontoperiode für die Rechnung liegt. Dieses Datum wird verwendet, um ein Skonto für die Buchung zu berechnen. Auf der Seite **Offene Transaktionen ausgleichen** sieht April, dass standardmäßig der vollständige Rabatt von 20,00 angezeigt wird. Die Rechnungsposition zeigt, dass der auszugleichende Betrag 1.980,00 ist.

| Markieren                     | Skonto verwenden | Beleg   | Konto | Skontodatum | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|--------------------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt und hervorgehoben | Normal            | Inv-10030 | 3052    | 6/28/2015          | 7/12/2015 | 10030   | -2,000,00                      | USD      | -1.980,00        |
| Ausgewählt                 | Normal            | APP-10030 | 3052    | 7/15/2015          | 7/15/2015 |         | 500,00                         | USD      | 500,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt. Der angewendete Rabattbetrag ist 20,00, da der auszugleichende Betrag für die Rechnung der Standardbetrag ist, 1.980,00.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 7/12/2015 |
| Skontobetrag         | -20,00    |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | -20,00    |

April aktualisiert den Wert im Feld **Auszugleichender Betrag** auf **500,00**. Der Wert im Feld **Anzuwendender Skontobetrag** wird als **5,05** berechnet.

| Markieren                     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt und hervorgehoben | Normal            | Inv-10030 | 3052    | 6/28/2015 | 7/12/2015 | 10030   | 2.000,00                       | USD      | -500,00          |
| Ausgewählt                 | Normal            | APP-10030 | 3052    | 7/15/2015 | 7/15/2015 |         | 500,00                         | USD      | 500,00           |

Rabattinformationen werden am unteren Rand der Seite **Offene Buchungen ausgleichen** angezeigt. Der Wert im Feld **Anzuwendender Skontobetrag** ist **5,05**, da der auszugleichende Betrag für die Rechnung zu dem Zahlungsbetrag 500,00 geändert wurde.

|                              |           |
|------------------------------|-----------|
| Skontodatum           | 7/12/2015 |
| Skontobetrag         | -20,00    |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | -5,05     |



