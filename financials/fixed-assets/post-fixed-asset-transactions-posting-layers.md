---
title: Beitragsanlagenbuchungen Buchungsebenen
description: "Dieser Artikel gibt eine Übersicht über das Buchen von Ebenenfunktionen für Anlagenbuchungen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 4b112eee303604149c7609972a60c2014d4be423
ms.lasthandoff: 03/31/2017


---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Beitragsanlagenbuchungen Buchungsebenen

Dieser Artikel gibt eine Übersicht über das Buchen von Ebenenfunktionen für Anlagenbuchungen.

Eine Anlage wird für unterschiedliche Zwecke häufig mit unterschiedlichen Methoden abgeschrieben. Die Abschreibung zu steuerlichen Zwecken wird anhand der aktuellen Steuerregeln berechnet, um die höchstmögliche Abschreibung vor Steuern zu erreichen, wohingegen die Abschreibung zu Berichtszwecken entsprechend den Buchhaltungsgesetzen und -standards berechnet wird. Die unterschiedlichen Abschreibungsarten werden auf den Buchungsebenen separat berechnet und aufgezeichnet.

Jedes Buch, das einer Anlage zugeordnet ist, wird für eine bestimmte Buchungsebene eingerichtet, die ein übergeordnetes Abschreibungsziel aufweist. Es gibt zehn Buchungsebenen: Aktuelle, Vorgänge, Steuern und sieben benutzerdefinierte Ebenen. Sie können Buchungen im Hauptbuch für das Buch deaktivieren, indem Sie das Feld Ins Hauptbuch buchen auf Nein festlegen. Das Feld Buchungsebene wird dann automatisch auf Keine gesetzt. In der Regel werden Bücher, die nicht im Hauptbuch zu buchen, die Steuererklärung verwendet. Durch diesen Ansatz können Sie erkennen die zusätzliche Flexibilität, historische Buchungen zum Anlagenbuch zu löschen, da sie nicht im Hauptbuch eingerichtet wurden.

Anlagenerfassungen definieren sich durch die Nutzung der Seite  Journalnamen unter Hauptbuch > Journaleinrichtung > Journalnamen. Jede Erfassung, in der Sie Abschreibungen buchen können, wird anhand des Erfassungsnamens (Journal) für eine einzelne Buchungsebene definiert. Die Buchungsebene kann im Journal nicht geändert werden. Diese Einschränkung hilft sicherzustellen, dass Buchungen für die einzelnen Buchungsebenen getrennt gehalten werden. Für jede Buchungsebene muss mindestens ein Journal angelegt werden. Wenn Sie Bücher arbeiten, die nicht auf das Sachkonto buchen, müssen Sie eine Erfassung auch erstellen, in der die Buchungsebene in nicht festgelegt wird.

Sie können Sachkonten für Anlagenbuchungen auf der Seite Anlagenbuchungsprofile festlegen. Sie müssen für jedes Buchungsprofil die relevante Buchungsart und das Buch auswählen und können dann die Sachkonten angeben. Einrichten eines Buchungsprofildatensatz für jedes Buch, das im Hauptbuch gebucht wird.

> [!NOTE] 
> Wenn Sie abgeleitete Bücher verwenden, können Sie Buchungen auf unterschiedlichen Buchungsebenen gleichzeitig gebucht werden. Sie erstellen die Buchungen des primären Buchs in einem Journal mit der Buchungsebene, die der Buchungsebene des Wertmodells entspricht. Beim Buchen werden die Buchungen der abgeleiteten Buchtransaktionen dann auf den entsprechenden Buchungsebenen gebucht.

Weitere Informationen finden Sie, Bücher abgeleitete [] () derived-books.md und [Buchen mit abgeleiteten Büchern] (post-derived-value-models.md).

