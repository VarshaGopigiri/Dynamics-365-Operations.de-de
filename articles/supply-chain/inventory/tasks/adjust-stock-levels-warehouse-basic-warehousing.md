---
title: Bestandswerte im Lagerort anpassen (grundlegendes Warehousing)
description: "Diese Prozedur führt Sie durch die einzelnen Schritte der Erstellung und des Buchens einer Lagerregulierungserfassung, um Bestandswerte von Produkten im Lagerort anzupassen."
author: MarkusFogelberg
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
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9ca5841fe857990cae8d9551ccf79c3c0fd490ae
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>Bestandswerte im Lagerort anpassen (grundlegendes Warehousing)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur führt Sie durch die einzelnen Schritte der Erstellung und des Buchens einer Lagerregulierungserfassung, um Bestandswerte von Produkten im Lagerort anzupassen. Sie müssen einen Lagererfassungnamen für die Bestandsregulierungen haben, bevor Sie diese starten. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden. Diese Aufgaben werden normalerweise von einem Lagerortmitarbeiter ausgeführt.


## <a name="create-an-inventory-adjustment-journal"></a>Lagerregulierungserfassung erstellen
1. Wechseln Sie zu Lagerverwaltung > Journaleinträge > Artikel > Lagerregulierung.
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Klicken Sie in der Liste auf den Lageregulierungserfassungsnamen, den Sie verwenden möchten.
    * Einige andere Felder werden basierend auf den Einstellungen der Lagerregulierungserfassung ausgefüllt, die Sie auswählen.  
5. Klicken Sie auf "OK".

## <a name="create-journal-lines"></a>Erfassungspositionen erstellen
1. Klicken Sie auf "Neu".
2. Markieren Sie das Feld "Artikelnummer" in der Liste.
3. Wählen Sie im Feld "Artikelnummer" einen Artikel aus. Wenn Sie das Demodatunternehmen USMF verwenden, geben Sie " D0001" ein.
4. Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Wählen Sie in der Liste einen Lagerplatz aus.
6. Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Wählen Sie in der Liste einen Lagerort aus.
    * Wenn Sie einen Artikel mit Lagerplatz als obligatorische Dimension ausgewählt haben, müssen Sie den Lagerplatz hier festlegen.  
8. Geben Sie im Feld "Menge" eine Zahl ein.
    * Der Einstandspreis legt die Kosten pro Einheit für Lagerzugänge fest. Wenn keine Kosten für die Artikelnummer angegeben sind oder diese manuell geändert werden sollen, geben Sie sie hier ein.  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a>Lagerregulierungserfassung prüfen und buchen
1. Klicken Sie auf "Überprüfen".
2. Klicken Sie auf "OK".
3. Klicken Sie auf "Buchen".
    * Beim Buchen dieser Art von Erfassung wird ein Lagerzugang oder -abgang gebucht, der Lagerbestand und der Lagerwert werden geändert, und Sachkontobuchungen werden generiert.  
4. Klicken Sie auf "OK".
5. Schließt das Formular.
6. Schließen Sie die Seite.

