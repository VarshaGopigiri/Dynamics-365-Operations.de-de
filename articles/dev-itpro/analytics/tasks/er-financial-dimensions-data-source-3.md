--- 
title: "Entwerfen eines Berichts zum Verwenden von Finanzdimensionen als Datenquelle für elektronische Berichterstellung"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c67bf235f3514a19893bcefcaae6e3bb11bbb151
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-report-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Entwerfen eines Berichts zum Verwenden von Finanzdimensionen als Datenquelle für elektronische Berichterstellung

[!include [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann. Diese Schritte können in jedem Unternehmen ausgeführt werden.

Um diese Schritte auszuführen, müssen Sie erst die Schritte im Verfahren "ER - Finanzdimensionen als Datenquelle nutzen (Teil 2: Modellzuordnung)" ausführen.


## <a name="design-a-report-to-present-financial-dimensions"></a>Entwerfen eines Berichts zur Darstellung von Finanzdimensionen
1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell".
3. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
4. Geben Sie im Feld "Neu" "Format basierend auf Finandimensions-Beispieldatenmodell" ein.
    * Verwenden Sie das Modell, die im Voraus als Datenquelle für den neuen Bericht erstellt wurde.  
5. Geben Sie im Feld "Name" "Sachkontoerfassungbericht" ein.
6. Wählen Sie im Feld "Datenmodelldefinition" "Erfassung" aus.
7. Klicken Sie auf Konfiguration erstellen.
8. Klicken Sie auf Designer.
9. Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.
10. Wählen Sie in der Struktur den Knoten 'XML\Element'.
11. Geben Sie im Feld Name "Root" ein.
12. Klicken Sie auf "OK".
13. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
14. Wählen Sie in der Struktur 'XML\Attribute' aus.
15. Geben Sie im Feld Name "Firma" ein.
16. Klicken Sie auf "OK".
17. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
18. Wählen Sie in der Struktur den Knoten 'XML\Element'.
19. Geben Sie im Feld "Name" "Journal" ein.
20. Klicken Sie auf "OK".
21. Wählen Sie in der Strukturdarstellung "Root: XML Element\Journal: XML Element".
22. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
23. Wählen Sie in der Struktur 'XML\Attribute' aus.
24. Geben Sie im Feld "Name" "Charge" ein.
25. Klicken Sie auf "OK".
26. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
27. Wählen Sie in der Struktur den Knoten 'XML\Element'.
28. Geben Sie im Feld "Name" "Buchung" ein.
29. Klicken Sie auf "OK".
30. Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element'.
31. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
32. Wählen Sie in der Struktur 'XML\Attribute' aus.
33. Geben Sie im Feld "Name" "Beleg" ein.
34. Klicken Sie auf "OK".
35. Klicken Sie auf "Attribut hinzufügen".
36. Geben Sie im Feld "Name" "Datum" ein.
37. Klicken Sie auf "OK".
38. Klicken Sie auf "Attribut hinzufügen".
39. Geben Sie im Feld "Name" 'Währung' ein.
40. Klicken Sie auf "OK".
41. Klicken Sie auf "Attribut hinzufügen".
42. Geben Sie im Feld Name "Dt" ein.
43. Klicken Sie auf "OK".
44. Klicken Sie auf "Attribut hinzufügen".
45. Geben Sie im Feld Name "Ct" ein.
46. Klicken Sie auf "OK".
47. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
48. Wählen Sie in der Struktur den Knoten 'XML\Element'.
49. Geben Sie im Feld "Name" "Dimensionen" ein.
50. Klicken Sie auf "OK".
51. Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element'.
52. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
53. Wählen Sie in der Struktur 'XML\Attribute' aus.
54. Geben Sie im Feld "Name" "Code" ein.
55. Klicken Sie auf "OK".
56. Klicken Sie auf "Attribut hinzufügen".
57. Geben Sie im Feld 'Name' "Wert" ein.
58. Klicken Sie auf "OK".
59. Klicken Sie auf "Attribut hinzufügen".
60. Geben Sie im Feld Name "Desc" ein.
61. Klicken Sie auf "OK".

## <a name="map-report-elements-to-data-sources"></a>Zuweisen von Berichtselementen zu Datenquellen
1. Klicken Sie auf die Registerkarte Zuordnung.
2. In der Struktur erweitern Sie "Modell: Datenmodell-Finanzdimensionsbeispielmodell".
3. In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste'.
4. In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste'.
5. In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste'.
6. Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML-Attribut'.
7. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Beschreibung: String'.
8. Klicken Sie auf Binden.
9. Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Wert: XML-Attribut'.
10. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Code: String'.
11. Klicken Sie auf Binden.
12. Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML-Attribut'.
13. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Name: String'.
14. Klicken Sie auf Binden.
15. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste'.
16. Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dimensions: XML Element'.
17. Klicken Sie auf Binden.
18. Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Ct: XML-Attribut'.
19. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Haben: Gleitkommazahl'.
20. Klicken Sie auf Binden.
21. Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Dt: XML-Attribut'.
22. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Soll: Gleitkommazahl'.
23. Klicken Sie auf Binden.
24. Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Währung: XML-Attribut'.
25. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Währung: String'.
26. Klicken Sie auf Binden.
27. Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Datum: XML-Attribut'.
28. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Datum: Datum'.
29. Klicken Sie auf Binden.
30. Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element\Beleg: XML-Attribut'.
31. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Beleg: String'.
32. Klicken Sie auf Binden.
33. Wählen Sie in der Strukturdarstellung 'Root: XML Element\Transaction: XML Element'.
34. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste'.
35. Klicken Sie auf Binden.
36. Wählen Sie in der Strukturdarstellung 'Root: XML Element\Charge: XML Attribut'.
37. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste\Charge: String'.
38. Klicken Sie auf Binden.
39. Wählen Sie in der Strukturdarstellung "Root: XML Element\Journal: XML Element".
40. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste'.
41. Klicken Sie auf Binden.
42. Wählen Sie in der Strukturdarstellung "Root: XML Element\Unternehmen: XML-Attribut".
43. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Unternehmen: String'.
44. Klicken Sie auf Binden.
45. Klicken Sie auf "Speichern".
46. Schließen Sie die Seite.


