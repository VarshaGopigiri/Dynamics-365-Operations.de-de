---
title: Bestandsnachverfolgungsinformationen korrigieren
description: "Diese Prozedur führt Sie durch den einzelnen Schritte der Erstellung und des Buchens einer Umlagerungserfassung, um Lagerbestandsnachverfolgungsinformationen zu korrigieren."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: caf8c67d315666edfffe86e459bc7a4478697f07
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="correct-inventory-tracking-information"></a>Bestandsnachverfolgungsinformationen korrigieren

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur führt Sie durch den einzelnen Schritte der Erstellung und des Buchens einer Umlagerungserfassung, um Lagerbestandsnachverfolgungsinformationen zu korrigieren. In diesem Beispiel aktualisieren wir die Informationen für eine durch einen Artikel gesteuerte Charge, indem wir eine falsch erfassten Charge mit einer anderen Charge ersetzen. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USPI durchführen oder können Ihre eigenen Daten verwenden. Wenn Sie eigene Daten verwenden, müssen Sie einen Artikel haben, der für Chargen aktiviert ist. Er darf nicht über den Lagerplatz gesteuert werden. Sie müssen außerdem einen Namen der Lagererfassungen für die Umlagerungen haben. Diese Aufgaben werden normalerweise von einem Lagerortmitarbeiter ausgeführt.


## <a name="create-an-inventory-transfer-journal"></a>Lagerumlagerungserfassung erstellen
1. Wechseln Sie zu "Umlagerung".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.
4. Klicken Sie auf "OK".

## <a name="create-journal-lines"></a>Erfassungspositionen erstellen
1. Klicken Sie auf "Neu".
2. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie USPI verwenden, wählten Sie Artikel M5003 aus.  
3. Geben Sie im Feld "Menge" eine Zahl ein.
4. Klicken Sie auf die Registerkarte "Lagerungsdimension".
5. Geben Sie im Feld "Chargennummer" einen Wert ein oder wählen Sie einen Wert aus.
6. Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.
7. Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.
8. Geben Sie im Feld "Chargennummer" einen Wert ein oder wählen Sie einen Wert aus.

## <a name="post-the-journal"></a>Erfassung buchen
1. Klicken Sie auf "Buchen".
2. Klicken Sie auf "OK".

## <a name="check-tracing-information"></a>Prüfen von Verfolgungsinformationen
1. Klicken Sie auf Lager.
2. Klicken Sie auf "Verfolgen".
3. Klicken Sie auf "OK".
    * Bei Verwendung dieser Nachverfolgungsinformationen können Sie nachverfolgen, über welche Charge Sie den Bestand korrigieren.  Sie können die Seite "Artikelverfolgung" verwenden, um diese Informationen anzuzeigen.  
4. Schließen Sie die Seite.

## <a name="check-inventory-transactions"></a>Prüfen von Lagerbuchungen
1. Klicken Sie auf Lager.
2. Klicken Sie auf "Transaktionen".
    * Hier können Sie die Transaktionen anzeigen, die erstellt wurden, als Sie Ihre Erfassung gebucht haben.   
