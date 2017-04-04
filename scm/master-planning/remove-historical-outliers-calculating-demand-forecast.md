---
title: "Entfernen Sie Ausreißer aus den historischen Buchungsdaten, wenn Sie eine Bedarfsplanung berechnen."
description: "In diesem Artikel wird beschrieben, wie Ausreißer aus den historischen Daten ausgeschlossen werden, die verwendet werden, um eine Bedarfsplanung zu berechnen. Wenn Sie Ausreißer ausschließen, können Sie die Prognosegenauigkeit verbessern."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 6f44e1ce566781f1586203528d55b13b28001a2c
ms.lasthandoff: 03/31/2017


---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Entfernen Sie Ausreißer aus den historischen Buchungsdaten, wenn Sie eine Bedarfsplanung berechnen.

In diesem Artikel wird beschrieben, wie Ausreißer aus den historischen Daten ausgeschlossen werden, die verwendet werden, um eine Bedarfsplanung zu berechnen. Wenn Sie Ausreißer ausschließen, können Sie die Prognosegenauigkeit verbessern.

Sie können Ausreißer ausschließen, um Planungsrichtigkeit zu verbessern. Diese Aufgabe ist optional. Hier ein Überblick über den Prozess:

1.  ** Auf Produktprogrammplanung ** &gt; ** Einstellungen ** &gt; ** Bedarfsplanung ** &gt; ** Ausreißerentfernen ** die Ausreißerentfernen ** ** Seite öffnen, in der Sie eine Abfrage verwenden können, um die Transaktionen, um auszuschließen.
2.  Wählen Sie das Unternehmen, für das die Abfrage gilt, und geben Sie dann einen Namen und eine Beschreibung ein. Das **Abfragendatum** Feld wird automatisch auf das aktuelle Datum festgelegt.
3.  Aktivieren Sie das Kontrollkästchen **Aktiv**, um die Transaktionen, die von der Abfrage gefunden wurden, von den historischen Daten auszuschließen. Diese Einstellung tritt in Kraft, wenn Sie eine Basisprognose erstellen.
4.  Auf der Seite **Abfrage für Ausreißerentfernung** können Sie die Kriterien hinzufügen, entfernen und auswählen, welche festlegen, welche Transaktionen ausgeschlossen werden, wenn die Basisprognose berechnet wird. Beispielsweise wählen Sie einen bestimmten Artikel oder eine Auftragsbuchung aus, den bzw. die Sie ausschließen möchten.
5.  Klicken Sie auf **Transaktionen anzeigen**. Die Seite **Ausreißerbuchungen** enthält die Transaktionen, die den Kriterien entsprechen, die Sie in der Abfrage definiert haben und die aus den historischen Daten ausgeschlossen werden, wenn die Bedarfsplanung berechnet wird.

**Hinweis:** Sie können eine Abfrage auch erstellen, die auf einer vorhandenen Abfrage basiert. Wählen Sie die Abfrage aus, die kopiert werden soll, und klicken Sie dann auf **Duplizieren**. Das Feld **Abfragedatum** kennzeichnet die Version. Sie können die Abfrage verwenden, belassen, oder Sie können auf **Abfrage bearbeiten** klicken, um die Kriterien zu ändern. Sie können den Namen und die Beschreibung der neuen Abfrage optional ändern.

<a name="see-also"></a>Siehe auch
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

