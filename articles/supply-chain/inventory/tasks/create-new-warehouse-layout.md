---
title: Ein neues Lagerortlayout erstellen
description: "Diese Prozedur zeigt Ihnen an, wie die Informationen zu den Lagerplätzen in einem Lagerort eingerichtet werden."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 253440d81edd6f71b52ae349398e3c6a895bf05c
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-new-warehouse-layout"></a>Ein neues Lagerortlayout erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt Ihnen an, wie die Informationen zu den Lagerplätzen in einem Lagerort eingerichtet werden. Dies gilt nur für Lagerorte, die mithilfe von die mithilfe der "Standardlagerung" im Modul "Lagerverwaltung" erstellt wurden, nicht für Lagerorte, die im Modul "Lagerortverwaltung" erstellt werden. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.


## <a name="set-the-default-location-capacity"></a>Die Standardlagerplatzkapazität festlegen
1. Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Lager- und Lagerortverwaltungsparameter".
2. Klicken Sie auf die Registerkarte "Lagerplätze".
3. Geben Sie im Feld "Standardbreite" eine Zahl ein.
4. Geben Sie im Feld "Standardtiefe" eine Zahl ein.
5. Geben Sie im Feld "Standardhöhe" eine Zahl ein.
6. Klicken Sie auf "Speichern".
7. Schließen Sie die Seite.

## <a name="define-the-location-name-format"></a>Das Format des Lagerplatznamens definieren
1. Wechseln Sie zu Bestandsverwaltung > Einstellungen > Lageraufschlüsselung > Lagerorte.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Lagerort" einen Wert ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Schalten Sie die Erweiterung des Abschnitts "Lagerplatznamen" ein/aus.
    * Die Optionen in diesem Abschnitt definieren das Standardformat für Lagerplatznamen. In unserem Beispiel schließen wir die Gangnummer, Regalnummer und Regelbodennummer ein.  
8. Legen Sie die Option "Gang einschließen" auf "Ja" fest.
9. Legen Sie die Option "Regal einschließen" auf "Ja" fest.
10. Geben Sie im Feld "Format" für das Regal einen Wert ein.
    * Beispiel: -##  
11. Legen Sie die Option "Regalboden einschließen" auf "Ja" fest.
12. Geben Sie im Feld "Format" für den Regalboden einen Wert ein.
    * Beispiel: -##  

## <a name="define-warehouse-locations"></a>Lagerort-Lagerplätze definieren
1. Klicken Sie im Aktivitätsbereich auf "Lagerort".
2. Klicken Sie auf den Lagerplatz-Assistent.
3. Klicken Sie auf Weiter.
4. Heben Sie die Auswahl für die Option "Ausgangsrampen" auf.
5. Heben Sie die Auswahl für die Option "Sammellagerplätze" auf.
6. Klicken Sie auf Weiter.
7. Klicken Sie auf Weiter.
8. Klicken Sie auf Weiter.
9. Klicken Sie auf Weiter.
10. Klicken Sie auf Weiter.
11. Klicken Sie auf Weiter.
12. Klicken Sie auf Weiter.
    * Beachten Sie, dass die physischen Dimensionen, die auf dieser Seite angezeigt werden, die sind, die Sie zu Beginn dieser Prozedur festgelegt haben.  
13. Klicken Sie auf Weiter.
14. Klicken Sie auf Fertig stellen.
15. Schließen Sie die Seite.
16. Aktualisieren Sie die Seite.

