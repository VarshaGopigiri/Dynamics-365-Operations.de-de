---
title: "Reservieren derselben Charge für einen Auftrag"
description: "In diesem Artikel wird beschrieben, wie ein Produkt eingerichtet wird, um Bestandreservationen für eine einzelne Bestandcharge zu ermöglichen."
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: aef3a52f4cb2d5af47a8c25a67e6c2076fa1ff03
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="reserve-the-same-batch-for-a-sales-order"></a>Reservieren derselben Charge für einen Auftrag

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie ein Produkt eingerichtet wird, um Bestandreservationen für eine einzelne Bestandcharge zu ermöglichen.

Mit der Reservierung derselben Charge können Sie Bestand für eine Auftragsposition aus einer einzelnen Lagercharge reservieren. Zum Beispiel kann ein Debitor, der Tapete bestellt, fordern, dass der gesamte Auftrag aus derselben Charge oder demselben Los stammt, damit Unterschiede zwischen den Rollen vermieden werden. Damit ein Produkt die Reservierung derselben Charge verwendet, müssen die folgenden Einstellungen in den Artikelmodellgruppen, der Rückverfolgungsangabengruppe und der Lagerdimensionsgruppe, die alle dem Produkt zugewiesen werden, aktiviert sein:

-   **Artikelmodellgruppen** – Für die Artikelmodellgruppe müssen die Felder **Auswahl derselben Charge** und **Bedarf konsolidieren** in der Feldgruppe **Reservierung** für Bestandsrichtlinien aktiviert werden.
-   **Rückverfolgungsangabengruppen** – Für die Rückverfolgungsangabengruppe muss das Feld **Disposition nach Dimensionen** für die Chargennummer aktiviert werden.
-   **Lagerdimensionsgruppen** – Für die Lagerdimensionsgruppe muss das Feld **Disposition nach Dimensionen** für **Standort** und **Lagerort** aktiviert werden.

Beim Reservieren von Bestand für ein Produkt in einer Auftragsposition, die für die Auswahl derselben Charge eingerichtet ist, versucht Microsoft Dynamics 365 for Finance and Operations, die aus einer einzelnen Lagercharge bestellte Menge zu reservieren. Dabei werden auch bestimmte Chargenattributanforderungen berücksichtigt. Kann die Menge nicht durch eine Charge abgedeckt werden kann, wird die Seite **Reservierungskonflikt aufgrund identischer Charge** angezeigt. Diese Seite beschreibt die Probleme und auch die Aktivitäten, die Sie ausführen können, um mit der Reservierung fortzufahren. Die folgenden Umstände könnten verhindern, dass die Charge reserviert werden kann:

-   Im Chargendispositionscode ist die Einstellung **Reservierung sperren** für Verkäufe mit dem Status **Gesperrt** gekennzeichnet.
-   Die Charge ist abgelaufen (unter Berücksichtigung des Ablaufdatums und aller zutreffenden Verkaufstage für Debitoren). Der Artikel kann nach wie vor für die Reservierung berücksichtigt werden, wenn die Lagermodellgruppe für den Artikel First Expiry First Out (FEFO)-datumsgesteuert ist und Mindesthaltbarkeitsdatum als Kommissionierungskriterium ausgewählt wird.
-   Die verbleibende Haltbarkeitsdauer der Charge ist unzureichend (dabei werden das Ablauf- bzw. Mindesthaltbarkeitsdatum sowie alle Verkaufstage für Debitoren berücksichtigt).





