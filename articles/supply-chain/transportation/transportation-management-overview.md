---
title: "Übersicht Transportverwaltungsaufgaben"
description: "Dieses Thema enthält eine Übersicht der Transportverwaltungsfunktionen in Microsoft Dynamics 365 for Finance and Operations."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f4dc2c15d35d93d1563c866b20ad7f2bbb5c8457
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="transportation-management-overview"></a>Übersicht Transportverwaltungsaufgaben

[!include [banner](../includes/banner.md)]

Dieses Thema enthält eine Übersicht der Transportverwaltungsfunktionen in Microsoft Dynamics 365 for Finance and Operations.

Mit der Transportverwaltung können Sie den Transport Ihres Unternehmens verwenden und Kreditor- und Routinglösungen für ein- und ausgehende Aufträge identifizieren. So können Sie beispielsweise die schnellste Route oder den günstigsten Satz für eine Lieferung identifizieren. In der folgenden Tabelle werden die wichtigsten Szenarien für die Nutzung der Transportverwaltung in Microsoft Dynamics 365 for Finance and Operations beschrieben.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Szenario</th>
<th>Nutzen der Transportverwaltung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nutzung externer Logistikanbieter für Transportaktivitäten.</td>
<td>Verwenden Sie die Transportverwaltung für den eingehenden und ausgehenden Transport.</td>
</tr>
<tr class="even">
<td>Die eigene Flotte des Unternehmens ist für Lieferung/Abholung verfügbar, und Zustellgebühren werden an an Debitoren weitergegeben.</td>
<td>Für ausgehende Prozesse können Sie die Transportverwaltung verwenden, um die Transportbelastungen festzulegen und sie an Debitoren weiterzuleiten. Allerdings ist der Spediteursrechnung-Abstimmungsprozess nicht erforderlich.</td>
</tr>
<tr class="odd">
<td>Die eigene Flotte des Unternehmens steht für Lieferung/Abholung zur Verfügung, aber Zustellgebühren werden nicht an Debitoren weitergegeben, da Produktpreise den Transport enthalten.</td>
<td>Viele Transportverwaltungsfunktionen sind nicht erforderlich. Sie können jedoch die Transportverwaltung verwenden, um die Transportsätze zu bestimmen und den Verkaufspreis entsprechend anzupassen.</td>
</tr>
<tr class="even">
<td>Logistikdienste werden von einer anderen juristischen Person im gleichen Unternehmen bereitgestellt.</td>
<td><ul>
<li>Sie können die Transportverwaltung nutzen, indem Sie die andere juristische Person wie jeden anderen Spediteur behandeln. Sie können die wirtschaftlichen Buchungen zwischen juristischen Personen nicht automatisieren. Daher müssen Sie diese Buchungen manuell behandeln (beispielsweise mithilfe einer Bestellung).</li>
<li>In der juristischen Person, die die Logistik zur Verfügung stellt, kann die Transportverwaltung verwendet werden, um zu bestimmen Transportsätze festzulegen.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a>Transport in Finance and Operations planen
In der Transportverwaltung kann die Transportplanung entweder auf Aufträgen oder auf Lieferungen basieren, die auf Basis dieser Aufträge erstellt werden. Die Lieferungen sind immer irgendwann vorhanden. Sie sind jedoch nicht zur Transportplanung erforderlich. Umlagerungsaufträge sind Teil des ausgehenden Szenarios und können zusammen mit Aufträgen geplant werden. 

![Auslastungabbildung](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Eingehender Transport
Wenn Sie Artikel von einem Kreditor zur Lieferung an Ihren Lagerort bestellen, möchten Sie den Transport der Artikel möglicherweise selbst organisieren. Sie können Finance and Operations nutzen, um den Transport und den Empfang einer eingehenden Ladung zu planen. Die folgende Abbildung zeigt den Geschäftsprozessablauf für die Planung des Transports einer eingehenen Auslastung. 

![Geschäftsprozessfluss für den Transport eingehender Auslastungen](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Ausgehender Transport
Sie können eine ausgehende Ladung planen und verarbeiten, um bestimmte Artikel aus dem Lagerort eines Unternehmens an einen Debitor zu versenden. Sie können Finance and Operations nutzen, um den Transport und den Versand einer azusgehenden Ladung zu planen. Die folgende Abbildung zeigt den Geschäftsprozessablauf für die Planung und Verarbeitung von ausgehenden Ladungen für den Versand. 

![Planung und Verarbeitung von ausgehenden Ladungen](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Ladungserstellung
Finance and Operations enthält eine Ladungserstellungsstrategie mit dem Namen "Volumenbasierte Ladungserstellungsstrategie". Mit dieser Strategie können Sie die Höchstwerte verwenden, die für Höhe und Gewicht in der Ladungsvorlage angegeben sind, oder die Einstellungen überschreiben, indem sie neuen Werte eingeben. Um diese Strategie zu verwenden, wählen Sie sie im Feld **Ladungserstellungsstrategie** im Inforegister **Einstellungen** auf der Seite **Ladungserstellungsworkbench** aus. Darüber hinaus können Sie eigene Ladungserstellungsstrategien hinzufügen, indem Sie eine neue Klasse in der Entwicklungsumgebung erstellen.




