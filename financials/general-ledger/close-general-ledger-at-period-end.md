---
title: Abschluss des Hauptbuchs am Ende der Periode
description: "In diesem Thema werden die Aufgaben beschrieben, die in der Regel ausgeführt werden, wenn ein Periodenabschluss für Hauptbuch ausgeführt wird."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 54bd0296d2569c38fccd0ff13a2316cb18466675
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="close-the-general-ledger-at-period-end"></a>Abschluss des Hauptbuchs am Ende der Periode

[!include[banner](../includes/banner.md)]


In diesem Thema werden die Aufgaben beschrieben, die in der Regel ausgeführt werden, wenn ein Periodenabschluss für Hauptbuch ausgeführt wird. 

Im Hauptbuch können Sie Abschlussprozeduren für eine Periode oder ein Jahr ausführen. Abschlussvorgänge bereiten das System auf eine neue Periode vor. Um das System auf ein neues Jahr vorzubereiten, müssen Sie den Jahresabschlussprozess ausführen. Jede Organisation hat unterschiedliche Verfahren und Schritte, die für das Ende einer Periode ausgeführt werden. Nachfolgend sind einige Schritte für optionale Periodenenden beschrieben:

-   Schließen Sie alle Aufgaben für alle anderen Module ab, z. B. Debitoren, Kreditoren und Bestand.
-   Überprüfen Sie, ob alle Erfassungen gebucht werden.
-   Führen Sie die Neubewertung der Fremdwährung aus, um alle unrealisierten Gewinn- oder Verlustbeträge zu generieren.
-   Gleichen Sie Buchungen für jedes Sachkonto aus.
-   Verarbeiten Sie alle erforderlichen Zuteilungen.
-   Buchen Sie manuelle Regulierungen für das Ende der Periode.
-   Journalisieren Sie Transaktionen und überprüfen Sie den **Sachkontoerfassungs** Bericht.
-   Führen Sie eine Konsolidierung aus, indem Sie ein Konsolidierungsunternehmen oder eine Finanzberichterstellung verwenden.
-   Generieren Sie Finanzaufstellungen zum Periodenende, indem Sie Finanzberichterstellung verwenden.
-   Legen Sie Sachkontoperioden auf **Gesperrt** fest, damit keine weitere Buchung stattfindet. Sie können für bessere Kontrolle eine Periode auf eine bestimmte Benutzergruppe begrenzen, wenn Aktivitäten zum Periodenende auftreten. Es ist nicht sinnvoll, Perioden auf **Ständig Geschlossen** festzulegen, da eine geschlossene Periode nicht erneut geöffnet werden kann.

Der Arbeitsbereich Finanzperioden schließen kann verwendet werden, um die Aufgaben, die für verschiedene Periodenendenprozesse erforderlich sind, zu organisieren und nachzuverfolgen. Siehe [Arbeitsbereich Finanzperioden schließen](financial-period-close-workspace.md) und [Jahresabschluss](Year-end-close.md) für weitere Informationen. 





