---
title: "Erstellen Sie ein Budget für Buchungs- und Summenkonten"
description: "Dieser Artikel gibt einen Überblick über den Prozess für das Erstellen von Budgets basierend auf Summenkonten. Er erläutert auch, wie die Budgetsteuerung für Summenkonten aktiviert wird, wenn die Budgetsteuerung erforderlich ist."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3e3c86bd32a05a392fcb82a86f2c461cc3abfb03
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>Erstellen Sie ein Budget für Buchungs- und Summenkonten

[!include [banner](../includes/banner.md)]

Dieser Artikel gibt einen Überblick über den Prozess für das Erstellen von Budgets basierend auf Summenkonten. Er erläutert auch, wie die Budgetsteuerung für Summenkonten aktiviert wird, wenn die Budgetsteuerung erforderlich ist.

Sowohl mit Haushaltsplan- als auch mit Budgetregistereintragsdokumenten können Hauptkonten budgetiert werden, deren Hauptkontotyp **Summe** lautet. Istwerte können nur den buchungsbezogenen Hauptkonten gebucht werden. 

Für den periodischen Prozess zum **Generieren eines Budgetplans aus dem Hauptbuch** auf der Registerkarte **Quelle** können Sie den Hauptkontotyp **Summe** als Kriterium angeben. In diesem Fall ist jedes Gesamthauptkonto im Ziel-Haushaltsplan einbezogen, und der Betrag entspricht dem Gesamtbetrag des Bereichs der ausgewählten Hauptkonten. 

Sie können die Budgetsteuerung für Hauptkonten vom **Summe**-Typ aktivieren. Diese Funktionalität wird durch die Verwendung von Budgetgruppen unterstützt. Für jedes Hauptkonto muss das gesamte Budget, für das eine Budgetgruppe gesteuert werden soll, auf der Seite ** Budgetsteuerungskonfiguration ** erstellt werden. Die Kriterien, die Sie angeben, müssen das gesamte Hauptkonto und den Bereich der Konten umfassen. Um den Prozess der Erstellung von Budgetgruppen zu beschleunigen, können Sie die Datenentität Budgetsteuerungsgruppen nutzen. 

Wenn ein Budget für die Berichterstellung, also beispielsweise in einer Finanzaufstellung, verwendet wird, setzt sich die Budgetsumme für das Summenkonto wie folgt zusammen:

-   Aus den Budgets, die auf jedem Buchungssachkonto innerhalb des Intervalls des Summenkontos erstellt werden.
-   Aus dem Budgetbetrag, der direkt auf dem Summenkonto gebucht wird

Auf diese Weise können also separate Budgets für die wichtigsten Buchungskonten im Intervall des Summenkontos erstellt und kann der verbleibende Budgetbetrag dem Summenkonto hinzugefügt werden.




