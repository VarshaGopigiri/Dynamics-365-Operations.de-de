--- 
title: "Zahlungsnachlässe verarbeiten"
description: "Diese Verfahren zeigt, wie genehmigte und verarbeiteten Debitorenrückvergütungen zu den Gutschriften konvertiert."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 791ec304b9ea7c49fbea506d73c4daffd4478739
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="process-rebates-for-payment"></a>Zahlungsnachlässe verarbeiten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Verfahren zeigt, wie genehmigte und verarbeiteten Debitorenrückvergütungen zu den Gutschriften konvertiert. Sie können diese Anleitung im Demodatenunternehmen USMF ausführen. Die Vorbedingung für dieses Handbuch ist, eine oder mehrere Rückvergütungsansprüche zu haben, die einen Status der Markierung haben. Wenn Sie USMF verwenden, sollten Sie das "generieren und verarbeiten Kundenrabatt" Handbuch ausführen, bevor Sie dieses Handbuch starten.


## <a name="convert-rebate-claims-to-credit-note"></a>Konvertieren Sie Rückvergütungsansprüche zur Gutschrift
1. Dient zum Zusammenführen aller Debitoren.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie im Aktivitätsbereich auf "Sammeln".
5. Klicken Sie auf Transaktionen ausgleichen.
6. Klicken Sie auf Funktionen.
7. Einrichten des Rückvergütungsprogramms
    * Die Rückvergütungsseite werden die Rückvergütungsansprüche aufgeführt, die im Kundenrabattwerktisch verarbeitet haben und die in Status Markieren sind.    
8. Klicken Sie auf "Bearbeiten".
    * Legen Sie Häkchen im Markengebiet für die Ansprüche fest, die Sie in Gutschrift einbezogen werden sollen.   
9. Klicken Sie auf Funktionen.
10. Klicken Sie, um die Gutschrift zu erstellen.
    * Eine Meldung, Sie zu informieren, dass eine Erfassung gebucht wurde (dies ist die Debitoren-Verbrauchserfassung, wie in der Debitorenparameterseite angegeben). Dies führt dazu den tatsächlichen Betrag der Passivposten (Haben), auf den Debitorensaldo verschoben werden. Auf dieser Stufe ist das Nachlassabgrenzungskonto belastet worden, und dem Nachlassausgabenkonto ist gutgeschrieben worden.  
11. Schließen Sie die Seite.
12. Klicken Sie auf "Abbrechen".
    * Dieses aktualisiert die Seite, um die Aktualisierungen finden können.  
13. Klicken Sie im Aktivitätsbereich auf "Sammeln".
14. Klicken Sie auf Transaktionen ausgleichen.
    * Beachten Sie, dass eine Buchung für einen negativen Betrag, der gesamte Nachlassbetrag, ohne Rechnungsreferenz darstellend zum Debitorensaldo hinzugefügt wurde.   
15. Klicken Sie auf "Abbrechen".


