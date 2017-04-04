---
title: Planen Sie den Kontenplan
description: "Dieser Artikel enthält Informationen, die Ihnen helfen, Kontenpläne für Ihre Organisation zu planen."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 34425ecd4b78a134c92a2282576d0d7967d870b3
ms.lasthandoff: 03/31/2017


---

# <a name="plan-your-chart-of-accounts"></a>Planen Sie den Kontenplan

Dieser Artikel enthält Informationen, die Ihnen helfen, Kontenpläne für Ihre Organisation zu planen.

Um Finanzdaten in einer Organisation zu verfolgen und zu verwalten, können Sie einen Kontenplan einrichten. Ein Kontenplan ist eine Reihe von Konten, die ein finanziellen Rahmen definieren. Sie können Segmente hinzufügen, so genannte Finanzdimensionen, damit die Buchungen in diesen Konten noch weiter verfolgt werden können. Beispielsweise kann ein Ausgabenkonto Finanzdimensionen mit der Bezeichnung "Abteilung", "Kostenstelle" und "Kostenträger" enthalten. Mit benutzerdefinierten Regeln (Kontostrukturen und erweiterte Regeln genannt) wird bestimmt, wie diese Finanzdimensionen den Hauptkonten und anderen Finanzdimensionen angefügt werden und wie Buchungen eingegeben werden. 

Der Kontenplan ist eine strukturierte Liste der Hauptbuchkonten einer juristischen Person. Diese Liste wird verwendet, um Finanzberichte für Behörden und Eigentümer vorzubereiten. Die Konten sind nach Kontenarten gruppiert und wiederum in übergeordneten Kategorien zusammengefasst. Auf der allgemeinsten Ebene sind die Konten in Umsatzerlöse und Kosten (Betriebskonten) sowie Aktiva und Passiva (Bilanzkonten) unterteilt. 

Ein Kontenplan kann freigegeben und von jeder juristischen Person in einer Organisation verwendet werden. Der Kontenplan, der von einer juristischen Person verwendet wird, wird auf der Seite ** Sachkonto ** definiert. 

Hier einige der Faktoren, die Sie bei der Strukturierung des Kontenplans für Ihre Organisation berücksichtigen müssen:

-   Die Meldeanforderungen für das Land bzw. die Region, in der die Organisation ihren Sitz hat.
-   Die Meldeanforderungen für Ihre juristische Person
-   Der erforderliche Spezifikationsgrad, sowohl für externe Organisationen als auch für Ihre Organisation

Erstellen Sie den Kontenplan auf der Seite **Kontenplan**. Hauptkonten können über die Seite **Kontenplan** oder aus der Seite **Hauptkonten** erstellt werden. Ihre Hauptkonten dürfen keine Sonderzeichen verwenden, die als Trennzeichen für Kontenplan verwendet werden. Wenn Sie ein Sonderzeichen haben, das das gleiche wie das Trennzeichen für Kontenplan ist, könnte Instabilität die Folge sein, oder dass Sie immer nachschlagen oder das Flyout nutzen müssen, wenn Sie Kombinationen aus Konten und Dimensionen eingeben. 

Es wird empfohlen, die Hauptkonten mit Hauptkontokategorien verknüpfen, sodass Sie die standardmäßige Finanzberichte nutzen können, ohne Änderungen vornehmen zu müssen. Daher können Sie Berichte schneller und einfacher entwerfen und verwalten. 

Verwenden Sie die Seite **Kontostrukturen konfigurieren**, um Kontostrukturen zu erstellen. Kontostrukturen definieren zulässige Kombinationen. Diese Kombinationen bilden zusammen mit den Hauptkonten einen Kontenplan. 

**Legal entity overrides** 

Nicht alle Hauptkonten sind für alle juristischen Personen gültig und andere werden möglicherweise nur für eine bestimmte Zeitperiode relevant. In diesem kann der Abschnitt "Überschreibungen der juristischen Person" dazu verwendet werden, um festzulegen, für welche Unternehmen das Hauptkonto ausgesetzt werden soll, wer der Besitzer ist und die Zeitperiode, während der die Dimension aktiv ist. Die Überschreibungen auf der freigegebenen Ebene können nicht einschränkender als die Überschreibungen auf der Ebene der juristischen Person sein.

Weitere Informationen finden Sie financial-dimensions.md Finanzdimensionen [] ().

