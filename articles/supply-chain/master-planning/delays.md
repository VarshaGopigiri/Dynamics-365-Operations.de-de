---
title: "Verzögerungen"
description: "Dieser Artikel enthält Informationen zu verzögerten Daten in der Masterplanung. Ein verzögertes Datum ist ein realistisches Fälligkeitsdatum, das eine Transaktion erhält, wenn das früheste Erfüllungsdatum, das die Masterplanung berechnet, später ist als das angeforderte Datum."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fed78a7eba16d286a81b1e9ad709142422298c91
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="delays"></a>Verzögerungen

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu verzögerten Daten in der Masterplanung. Ein verzögertes Datum ist ein realistisches Fälligkeitsdatum, das eine Transaktion erhält, wenn das früheste Erfüllungsdatum, das die Masterplanung berechnet, später ist als das angeforderte Datum.

Der Produktprogrammplan kann das früheste Erfüllungsdatum für eine Buchung, für den Lieferzeiten, Materialverfügbarkeit, Kapazitätsverfügbarkeit und verschiedene Planungsparameter berechnen. 

Wenn Produktprogrammplan ein Auftragsdatum berechnet, das vor dem aktuellen Datum liegt, kann der Auftrag nicht rechtzeitig erfüllt werden. Daher wird der Auftrag verzögert. In diesem Fall plant der Produktprogrammplan den Auftrag im Voraus, ausgehend vom aktuellen Datum und einschließlich Lieferzeiten. Diese Lieferzeiten beginnen mit Komponentenartikeln auf niedrigerer Ebene. Der Auftrag empfängt dann ein verzögertes Datum. Ein verzögertes Datum ist ein realistisches Fälligkeitsdatum basierend auf den aktuellen Daten. Produktprogrammplan berechnet auch die Anzahl der Verzögerungstagen. 

In bestimmten Situationen möchten Sie möglicherweise Verzögerungen nicht berechnen, z. B. wenn Benutzer wissen, dass sie Durchlaufzeiten beschleunigen können, indem sie Alternativmodi der Lieferung auswählen. 

Sie können konfigurieren, wie Verzögerungen für eine Dispositionssteuerungsgruppe berechnet werden. Sie können die Dispositionssteuerungsgruppe dann später einem Artikel zuordnen. 

Auf der Seite **Parameter für Produktprogrammplanung** können Sie die Startzeit für die Berechnung von Verzögerungen festlegen. Wenn ein Auftrag nach dieser Zeit erfüllt wird, addiert das System einen Tag Verzögerung zum Verzögerungsdatum des Auftrags hinzu. 

**Hinweis:** In früheren Versionen waren berechnete Verzögerungen als *Verfügbarkeitsmeldungen* bekannt, das verzögerte Datum als *Verfügbarkeitsdatum*, und eine verzögerte Buchung war als *eine Buchung mit Erfüllung in der Zukunft* bekannt.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Deckungseinstellungen](coverage-settings.md)




