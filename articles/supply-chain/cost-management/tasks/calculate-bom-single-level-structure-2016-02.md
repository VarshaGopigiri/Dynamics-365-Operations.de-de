--- 
title: "Berechnen einer Stückliste mithilfe einer Struktur mit einer Ebene (nur Februar 2016)"
description: "Diese Prozedur zeigt, wie die Kosten eines fertigen Produkts berechnet werden, indem eine Auflösung mit einer einzelnen Ebene verwendet wird, die auf dem Nachkalkulationsbogen beruht."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0e6829238b244cc01b070fde6acdf37bdaeb9670
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016-only"></a>Berechnen einer Stückliste mithilfe einer Struktur mit einer Ebene (nur Februar 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie die Kosten eines fertigen Produkts berechnet werden, indem eine Auflösung mit einer einzelnen Ebene verwendet wird, die auf dem Nachkalkulationsbogen beruht. Dies ist die sechste Aufgabe in der Stücklistenberechnungsserie. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.

1. Wechseln Sie zu "Freigegebene Produkte".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Produkt-BOM_1 auswählen.  
3. Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".
4. Klicken Sie auf „Artikelpreis”.
5. Klicken Sie auf „Artikelkosten berechnen”.
    * Sie müssen möglicherweise auf die Auslassungspunkte (...) klicken, um diese Option im Hauptmenü anzuzeigen.  
6. Klicken Sie im Feld „Nachkalkulationsversion” auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie für diese Demo 10 aus. Dies ist die gleiche Nachkalkulationsversion, die zum Hinzufügen des Einstandspreis zu den Komponenten verwendet wird.  
7. Klicken Sie auf "OK".
8. Klicken Sie auf Berechnungsdetails anzeigen
    * Sie müssen möglicherweise auf die Auslassungspunkte (...) klicken, um diese Option im Hauptmenü anzuzeigen.    Hier ist die Zusammenstellung der Kosten:   •    10 ist von ARTIKEL_A, 10 % von ARTIKEL_B, 10 % von BOM_2 berechnet. In diesem Fall gibt es keine Details für BOM_2, da sie als Standardkosten von 10 eingegeben wurde, aber es erfolgte nicht durch Berechnung.  •  7 ist von der Rüstzeit abgeleitet, welche konstante Kosten sind und zusätzliche 7 sind vom Laufzeitvorgang (Prozess) abgeleitet.  •   Es gibt auch andere Beträge, die den indirekten Kosten entsprechen.  
9. @SysTaskRecorder:_RequestClose


