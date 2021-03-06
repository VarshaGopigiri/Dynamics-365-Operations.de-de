--- 
title: Wellenverarbeitung konfigurieren
description: "In diesem Leitfaden wird beschrieben, wie die Kriterien eingerichtet werden, die bestimmen, welche Arbeit für einen Lagerort generiert wird, wenn eine Wellen verarbeitet wird und ob Wellen manuell oder automatisch verarbeitet werden."
author: YuyuScheller
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f7a6db585468c235e07c4a0117a83995ec93f4b0
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="configure-wave-processing"></a>Wellenverarbeitung konfigurieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Leitfaden wird beschrieben, wie die Kriterien eingerichtet werden, die bestimmen, welche Arbeit für einen Lagerort generiert wird, wenn eine Wellen verarbeitet wird und ob Wellen manuell oder automatisch verarbeitet werden. Sie geben die Kriterien an, indem Sie Wellenvorlagen und Abfragen einrichten, die mit einer Welle mit freigegebenen Positionen in Aufträgen, Produktionsaufträgen oder in Kanban-Aufträgen übereinstimmen. Die Wellenverarbeitung wird an Lagerorten verwendet, die die Funktionen im Modul für "Lagerortverwaltung" verwenden, und nicht an denen, die die Funktionen im Modul für "Bestandsverwaltung" verwenden. Sie können diese Prozedur im Demodatunternehmen USMF ausführen.

1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Wellen" > "Wellenvorlagen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Wellenvorlage" einen Wert ein.
    * Wenn Sie eine Wellenvorlage einrichten, geben Sie die Reihenfolge an, in der die Vorlagen mit freigegebenen Positionen in Aufträgen, Produktionsaufträge oder Kanbans abgeglichen werden. Wenn eine Position für einen Lagerort oder für die Produktion freigegeben wird, verwendet sie die erste Wellenvorlage, für die sie die Kriterien erfüllt. Es wird empfohlen, dass Sie die Vorlagen mit den spezifischsten Kriterien an den Anfang der Liste platzieren. Je breiter die Kriterien, desto wahrscheinlicher ist es, dass eine Position die Kriterien erfüllt, und dass könnte dazu führen, dass Positionen der falschen Welle zugewiesen werden.  
4. Geben Sie im Feld "Wellenvorlagenbeschreibung" einen Wert ein.
5. Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie "Standort 2" auswählen.  
6. Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie Lagerort 24 auswählen.  
7. Legen Sie das Feld "Wellenerstellung automatisieren" auf "Ja" fest.
    * Aktivieren Sie diese Option, um eine Welle automatisch zu erstellen, wenn ein Auftrag, ein Produktionsauftrag oder ein Kanban für den Lagerort freigegeben wird.  
8. Legen Sie die Option "Welle bei Freigabe für Lagerort verarbeiten" auf "Ja" fest. 
    * Aktivieren Sie diese Option, um die Welle automatisch zu verarbeiten und Arbeit zu erstellen, wenn eine Position an den Lagerort freigegeben wird.  
9. Legen Sie die Option "Wellenfreigabe automatisieren" auf "Ja" fest. 
    * Aktivieren Sie diese Option, um die Welle automatisch freizugeben. Die Entnahmearbeit wird auf mobilen Geräten erstellt und bereitgestellt.  
10. Legen Sie die Option "Offenen Wellen zuweisen" auf "Ja" fest. 
    * Positionen werden Wellen basierend auf den Abfragefilter für die Wellenvorlage zugewiesen.  
11. Legen Sie die Option "Welle bei Schwelle automatisch verarbeiten" auf "Ja" fest. 
    * Aktivieren Sie diese Option, um die Welle automatisch zu verarbeiten, wenn die Werte die Schwellenwerte für Gewicht, Lieferung und die Positionen erreichen, die in der Feldgruppe angegeben sind. Diese Option steht nur zur Verfügung, wenn im Feld Vorlagentypwellen das Feld Versand ausgewählt wurde.  
12. Legen Sie die Option "Auffüllungsarbeitsfreigabe automatisieren" auf "Ja" fest. 
    * Aktivieren Sie diese Option, um bedarfbasierte Wiederbeschaffungsarbeit zu erstellen und diese automatisch freizugeben. Sie müssen die Wiederbeschaffungswellenmethode der Wellenvorlage hinzufügen und eine Auffüllungsvorlage vom Typ Wellenbedarf erstellen.  
13. Erweitern Sie den Abschnitt "Methoden".
    * Wellenvorlagenmethoden ermöglichen es Ihnen, die Reihenfolge der Aktivitäten zu steuern, die jede Welle durchläuft, wenn sie verarbeitet wird. Beispielsweise haben Sie möglicherweise eine Methode für die Wellenauffüllung. Wenn Sie eine Methode hinzufügen, wird diese automatisch im geeigneten Speicherort in der Reihenfolge der Schritte aufgeführt. Wenn Sie die Option "Auffüllungsarbeitsfreigabe automatisieren" auf "Ja" festgelegt haben, müssen Sie die Auffüllungsmethode hier hinzufügen.  
    * Wellenattribute fungieren als Filter, um die Art von Artikeln zu beschränken, die die Welle verwenden können. Sie könnten beispielsweise eine Artikelgruppe angeben.  
14. Klicken Sie auf "Speichern".
15. Schließen Sie die Seite.
16. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Lagerortverwaltungsparameter".
17. Erweitern Sie den Abschnitt "Wellenverarbeitung".
18. Geben Sie im Feld "Wellenverarbeitungs-Stapelverarbeitungsgruppe" einen Wert ein, oder wählen Sie einen Wert aus.
19. Legen Sie die Prozesswellen in der Option "Charge" auf "Ja" fest.
20. Geben Sie im Feld "Auf Sperre (ms) warten" eine Zahl ein.
    * Geben Sie die Uhrzeit ein, in Millisekunden, die ein Zuteilungsschritt auf eine Systemressource wartet, die von einem anderen Zuteilungsschritt gesperrt ist. Bei Überschreitung dieser Zeit wird, wird die Welle nicht verarbeitet und eine Fehlermeldung wird angezeigt.  
21. Klicken Sie auf "Speichern".
22. Schließen Sie die Seite.
23. Wechseln Sie zu "Produktionssteuerung" > "Einstellungen" > "Produktionssteuerungsparameter".
24. Wählen Sie im Feld "Für Lagerort freigeben" eine Option aus.
    * Bei Aufträgen und Kanbanaufträgen muss Lagerbestand reserviert werden, bevor der Auftrag an den Lagerort freigegeben wird. Andernfalls können die Artikel oder der Verteilungspositionen nicht in einer Welle verarbeitet werden. Bei Produktionsaufträgen haben Sie auch die Option, "Teilweise Reservierung zulassen" auszuwählen. Beispielsweise ist dies hilfreich, wenn Sie die Materialien haben, die Sie zum Starten der Produktion benötigen, und dann warten können, bis die zusätzlicher Materialien verfügbar werden, um den Prozess abzuschließen. Wenn Sie diese Option auswählen, müssen Sie den Prozess der Freigabe für den Lagerort manuell wiederholen, wenn die zusätzlichen Materialien verfügbar werden.  
25. Schließen Sie die Seite.


