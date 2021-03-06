---
title: "Minderungstage – Beispiel"
description: "Minderungstage – Beispiel."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 69e4b1b0fe100b17e5b2c59be81604019347956f
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---


# <a name="reduction-days-example"></a>Minderungstage – Beispiel 

[!include [banner](../includes/banner.md)]


Sie haben eine Dauerauftragsbuchung für den Wartungsdauerauftrag eines Debitors erstellt und dabei die in der folgenden Tabelle aufgeführten Werte verwendet:

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Von Datum</p></th>
<th><p>Bis Datum</p></th>
<th><p>Dauerauftrag</p></th>
<th><p>Dauerauftragstyp</p></th>
<th><p>Projekt</p></th>
<th><p>Kategorie</p></th>
<th><p>Verkaufswährung</p></th>
<th><p>Verkaufspreis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>01. März 2011</p></td>
<td><p>31. März 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Regelmäßig</strong></p></td>
<td><p>9013</p></td>
<td><p>UnterKat2</p></td>
<td><p>EUR</p></td>
<td><p>200,00</p></td>
</tr>
</tbody>
</table>


Der Debitor teilt Ihnen mit, dass er an zwei Tagen (10. und 11. März) keine Dienstleistungen in Anspruch nehmen will. Sie vereinbaren, den Dauerauftrag um diese beiden Tage zu verkürzen.

Sie erstellen eine neue Buchung vom Typ **Minderungstage** gemäß der folgenden Tabelle:

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Anfangsdatum</p></th>
<th><p>Enddatum</p></th>
<th><p>Dauerauftrag</p></th>
<th><p>Dauerauftragstyp</p></th>
<th><p>Projekt</p></th>
<th><p>Kategorie</p></th>
<th><p>Verkaufswährung</p></th>
<th><p>Verkaufspreis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10. März 2011</p></td>
<td><p>11. März 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Minderungstage</strong></p></td>
<td><p>9013</p></td>
<td><p>UnterKat2</p></td>
<td><p>EUR</p></td>
<td><p>-12,90</p></td>
</tr>
</tbody>
</table>


Bei der Fakturierung der Buchungen für März 2011 wird der Verkaufspreis von EUR 200 um EUR 12,90 verringert. Der fakturierbare Betrag für die Dauerauftragsbuchung beträgt somit EUR 187,10, und es werden zwei Buchungen mit einem Gesamtwert von EUR 187,10 fakturiert.

## <a name="see-also"></a>Siehe auch

[Verringern der Tage für Dauerauftragsgebühren](reduce-the-days-on-subscription-fees.md)

  



