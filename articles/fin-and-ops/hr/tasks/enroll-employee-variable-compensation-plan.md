--- 
title: "Registrieren eines Mitarbeiters in einem Plan für variable Vergütung"
description: "Der Leiter für Vergütungen/Bezüge kann Mitarbeiter in einem Plan für variable Vergütung registrieren, um Bargeld- und bargeldlose Prämien für Mitarbeiter zu berechnen."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c6108b11366f615be12e9a9f79ecf84728ee265f
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a>Registrieren eines Mitarbeiters in einem Plan für variable Vergütung

[!include[task guide banner](../../includes/task-guide-banner.md)]

Der Leiter für Vergütungen/Bezüge kann Mitarbeiter in einem Plan für variable Vergütung registrieren, um Bargeld- und bargeldlose Prämien für Mitarbeiter zu berechnen. Für dieses Verfahren wird vorausgesetzt, dass ein Plan für variable Vergütung mit dem Feld "Registrierung aktivieren" auf "Ja" festgelegt wurde und dass Berechtigungsregeln für diesen Plan für variable Vergütung erstellt wurden. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Um das Verfahren zu starten, gehen Sie zu "Personalverwaltung" > "Arbeitskräfte" > "Mitarbeiter" > "Vergütung" > "Variabler Plan registrieren".

1. Klicken Sie auf "Neu".
2. Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Plansuche wird gefiltert, um nur die Pläne für variable Vergütung anzuzeigen, für die der Mitarbeiter auf Grundlage der Berechtigungsregeln freigegeben wurde.  
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Schalten Sie die Erweiterung des Abschnitts "Allgemein" ein/aus.
5. Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.
6. Klicken Sie auf "Speichern".
7. Schalten Sie die Erweiterung des Abschnitts "Überschreibungen" ein/aus.
    * Optional kann ein Einstellungsregeldatum festgelegt werden, um das Einstellungsdatum für einen Mitarbeiter zu überschreiben, wenn die Einstellungsregel für den ausgewählten variablen Plan "Prozent" ist.  
    * Wenn der variable Plan ein prozentualer Anteil des Basisplans ist, kann der Prämienprozentsatz für den Mitarbeiter überschrieben werden. Wenn der variable Vergütungsplan ein Einheitenanzahlsplan ist, kann die Anzahl der Einheiten für den Mitarbeiter überschrieben werden.  
    * Wenn dem Mitarbeiter als Pauschalbetrag für seine Zulage gezahlt wird, kann der Betrag hier festgelegt werden.  
8. Schalten Sie die Erweiterung des Abschnitts "Überschreibungen in Organisation" ein/aus.
    * Wenn die Leistung des Mitarbeiters, die Leistung unterschiedlicher Abteilungen oder einer anderen als die der Position des Mitarbeiters zugewiesene Abteilung berücksichtigt werden soll, kann die Abteilung überschrieben werden. Die Spalte "Prozent" sollte sich auf 100 summieren.  

