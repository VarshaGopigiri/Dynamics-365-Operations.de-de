---
title: Vordatierte Schecks
description: "Dieser Artikel wird Unterstützung Informationen zu für vordatierte Schecks in Microsoft Dynamics 365 für Arbeitsgänge festgelegt. Vordatierte Schecks sind Schecks, die ausgestellt werden, um Zahlungen zu einem späteren Datum leisten oder erhalten zu können. Daher kann der Scheck nicht bis zum angegebene Datum eingewechselt werden."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 7349771b7f9a1ad4cd5b239f1d10bd3229d2d0df
ms.lasthandoff: 03/31/2017


---

# <a name="postdated-checks"></a>Vordatierte Schecks

Dieser Artikel wird Unterstützung Informationen zu für vordatierte Schecks in Microsoft Dynamics 365 für Arbeitsgänge festgelegt. Vordatierte Schecks sind Schecks, die ausgestellt werden, um Zahlungen zu einem späteren Datum leisten oder erhalten zu können. Daher kann der Scheck nicht bis zum angegebene Datum eingewechselt werden.

Microsoft Dynamics 365 für Arbeitsgänge unterstützt den vollständigen Verwaltungszyklus für vordatierte Schecks in "Debitoren" und " Kreditor, wie in der folgenden Tabelle dargestellt.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Szenario</th>
<th>Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Einrichten von vordatierten Schecks</td>
<td>Sie müssen eine neue Zahlungsmethode einrichten und definieren die Zahlungsroutine für das Vorbereiten für ausgegebene Schecks, Erhaltene Schecks und Quellensteuer.</td>
</tr>
<tr class="even">
<td>Erfassen und Buchen eines vordatierten Schecks für einen Kreditor</td>
<td>Erfassung eines vordatierten Schecks, bevor der Scheck an einen Kreditor ausgestellt wird. Beim Buchen wird, die die Verbindlichkeiten dem Kreditor gegenüber werden erkannt, doch das Bankkonto ist noch keine Gutschrift. Stattdessen wird ein Verrechnungskonto für diesen Zweck verwendet.</td>
</tr>
<tr class="odd">
<td>Erfassen und Buchen eines vordatierten Schecks von einem Debitor</td>
<td>Sie können die Details eines vordatierten Schecks erfassen, den Sie von einem Debitor erhalten haben. Beim Buchen wird, ist die Debitorenforderung Haben, aber das Bankkonto ist noch Sollbuchung. Stattdessen wird ein Verrechnungskonto für diesen Zweck verwendet.</td>
</tr>
<tr class="even">
<td>Erfassen und Buchen eines vordatierten Ersatzschecks für einen Debitor oder einen Kreditor</td>
<td>
Wenn Ihr Originalscheck an einen Händler oder von einem Kunden verloren ging oder beschädigt wird, können Sie für den Kreditor einen vordatierten Ersatzscheck ausstellen. Geben Sie beim Erfassen der Scheckdetails einen Verweis auf den Originalscheck an, und weisen Sie darauf hin, dass der neue Scheck als Ersatz für das Original gilt. Sie können den Ersatzscheck auch buchen.</td>
</tr>
<tr class="odd">
<td>Übertragen eines vordatierten Debitorenschecks an einen Kreditor</td>
<td>Wenn Sie von einem Kunden einen vordatierten Scheck erhalten, können Sie diesen Scheck als Zahlung an einen Kreditor übermitteln.</td>
</tr>
<tr class="even">
<td>Ausgleichen eines vordatierten Schecks für einen Kreditor</td>
<td>Verwenden Sie das Formular , um einen rückdatierten Scheck auszugleichen, der für einen Debitor oder Kreditor auf ein Transferkonto gebucht wurde. Wenn der Scheck ausgeglichen wird, ist die Bank schließlich Soll oder Haben für das Verrechnungskonto, das zuvor verwendet wurde.</td>
</tr>
<tr class="odd">
<td>Stornieren eines vordatierten Schecks für einen Kreditor</td>
<td>Sie können einen vordatierten Scheck in diesen Fällen stornieren: - Die Bank verweigert die Annahme des Schecks.
- Der Scheck wurde auf eine falsche Rechnung angewendet.
- Eine Barzahlung des Schecks wird vorgenommen.
</td>
</tr>
<tr class="even">
<td>Zahlungsstop für einen vordatierten Schecks</td>
<td>Sie können die Zahlung für einen vordatierten Scheck stoppen, der für einen Kreditor ausgestellt wurde. Gründe dafür können eine mangelnde Deckung, eine Änderung der vertraglichen Vereinbarungen mit dem Kreditor, die Lieferung fehlerhafter Waren durch den Kreditor oder die Rückgabe von Waren an den Kreditor sein. Sie können Zahlungen nur für Schecks stoppen, die noch nicht verrechnet wurden.</td>
</tr>
</tbody>
</table>




