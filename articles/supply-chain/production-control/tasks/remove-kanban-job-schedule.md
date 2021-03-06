--- 
title: Einen Kanban-Einzelvorgang aus der Planung entfernen
description: "Der Schwerpunkt dieser Prozedur liegt auf dem Entfernen eines geplanten Kanban-Bearbeitungseinzelvorgang aus der Planung durch das Zurücksetzen des Einzelvorgangsstatus zu \"Nicht geplant\"."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9a0f246bfe42dde0befdf5c4f01d2ad1e1200b12
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="remove-a-kanban-job-from-the-schedule"></a>Einen Kanban-Einzelvorgang aus der Planung entfernen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Der Schwerpunkt dieser Prozedur liegt auf dem Entfernen eines geplanten Kanban-Bearbeitungseinzelvorgang aus der Planung durch das Zurücksetzen des Einzelvorgangsstatus zu "Nicht geplant". Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Dieses Verfahren ist für Fertigungsbereichsvorgesetzte und Produktionsplaner vorgesehen.


## <a name="find-a-planned-kanban-job"></a>Geplanten Kanban-Einzelvorgang suchen
1. Wechseln Sie zu "Produktionssteuerung" > "Kanban" > "Kanban-Einzelvorgangsplanung".
2. Klicken Sie im Feld "Arbeitsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie die Arbeitsgruppe 1250 aus.  
4. Klicken Sie auf Auswählen.
5. Wählen Sie im Feld "Einzelvorgangsstatus anzeigen" "Geplant" aus.

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a>Entfernen des geplanten Kanban-Einzelvorgangs aus der Planung
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie einen Einzelvorgang aus, der den Statuts "Geplant" hat, beispielsweise einen Einzelvorgang vom 19. Dezember 2012.  
2. Klicken Sie im Aktivitätsbereich auf "Plan".
3. Klicken Sie auf "Einzelvorgangsstatus zurücksetzen".
4. Klicken Sie auf "OK".
    * Dadurch wird der aktuelle Status von "Geplant" zu "Nicht geplant" geändert und aus der Prozessübersicht entfernt.   


