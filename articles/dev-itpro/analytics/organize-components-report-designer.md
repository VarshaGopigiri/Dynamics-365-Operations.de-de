---
title: Organisieren von Berichtskomponenten im Berichtsdesigner
description: "Nachdem Sie Bausteine und generierte Berichte entworfen haben, ist es hilfreich, diese Objekte zu organisieren, sodass sie vom Benutzer leichter gefunden werden können. Dieser Artikel erläutert, wie vorhandene Berichte, Bausteine und Objekte im Berichts-Designer organisiert werden."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7207febc58dbab1df5551ae0f74ad74d9ced8e56
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="organize-report-components-in-report-designer"></a>Organisieren von Berichtskomponenten im Berichtsdesigner

[!include [banner](../includes/banner.md)]

Nachdem Sie Bausteine und generierte Berichte entworfen haben, ist es hilfreich, diese Objekte zu organisieren, sodass sie vom Benutzer leichter gefunden werden können. Dieser Artikel erläutert, wie vorhandene Berichte, Bausteine und Objekte im Berichts-Designer organisiert werden.

Sie können Ordner, Berichte, Bausteine und andere Objekte im Berichtsdesigner umbenennen, um Ihre Dateien besser zu organisieren. Je nach Art des Objekts, das Sie umbenennen, müssen Sie möglicherweise Zuordnungen für das Objekt aktualisieren.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Umbenennen eines Ordner oder Bausteins im Berichts-Designer
Im Berichts-Designer können Sie Ordner, Berichtsdefinitionen, Zeilendefinitionen, Spaltendefinitionen und Berichtsbaumstruktur-Definitionen umbenennen. **Hinweis:** Beim Umbenennen eines Bausteins müssen Sie alle Berichtsdefinitionen, die in dem Baustein verwendet werden, aktualisieren. Andernfalls kann kein neuer Bericht generiert werden.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Umbenennen eines Ordner oder Bausteins im Berichts-Designer

1.  Im Berichts-Designer verwenden Sie den Navigationsbereich, um den Ordner oder das Objekt zu suchen, den bzw. das Sie umbenennen möchten.
2.  Klicken Sie mit der rechten Maustaste auf den Ordner oder das Objekt, und klicken Sie dann auf **Umbenennen**. Das Feld **Name** im Navigationsbereich ist nun verfügbar.
3.  Geben Sie einen neuen Namen ein, und drücken Sie die Eingabetaste.
4.  Wenn der Baustein eine Zeilendefinition, eine Spaltendefinition oder eine Berichtstruktur-Definition ist, müssen Sie weitere Bausteine, die dem Artikel zugeordnet sind, aktualisieren. Klicken Sie mit der rechten Maustaste auf den Baustein, den Sie in Schritt 3 umbenannt haben, wählen Sie **Zuordnungen**, und wählen Sie dann den Artikel in der Liste, um ihn zu aktualisieren.
5.  Wiederholen Sie Schritt 4, bis alle zugeordneten Artikel aktualisiert wurden.

## <a name="create-and-manage-report-groups"></a>Erstellen und Verwalten von Berichtsgruppen
Sie können Berichtsdefinitionen gruppieren, um mehrere Berichte gleichzeitig zu generieren. Zum Erstellen, Ändern, Löschen und Generieren von Berichtsgruppen müssen Sie die Designer- oder Administrator-Rolle haben. Benutzer mit der Generator-Rolle können Berichtsgruppen generieren und anzeigen und die Benutzerberichtsdefinitions-Einstellungen für Berichtsgruppen ändern.

### <a name="create-a-report-group"></a>Erstellen einer Berichtsgruppe

1.  Klicken Sie im Navigationsbereich des Berichts-Designers auf **Berichtsgruppen**.
2.  Klicken Sie im Menü **Datei** auf **Neu** &gt; **Berichtsgruppe**, um eine neue Berichtsgruppe im Viewer-Fenster öffnen. Klicken Sie alternativ auf die **Berichtsgruppe** -Schaltfläche ![Berichtsgruppe](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Berichtsgruppe") auf der Symbolleiste.
3.  Klicken Sie auf die Registerkarte **Gruppen-Bericht**. Um die Informationen zu den einzelnen Berichtsdefinitionen für die Generierung dieses Berichts zu überschreiben, aktivieren Sie das Kontrollkästchen **Überschreiben von Unternehmen**, Details und Datumseinstellungen von einzelnen Berichtsdefinitionen. Die Felder Unternehmensname, Detailebene, vorläufige Einstellungen und Datumsinformationen werden automatisch ausgefüllt, aber Sie können Aktualisierungen vornehmen.
4.  Um mehrere Berichte zu generieren, die die Berichtswährung anzeigen, aktivieren Sie das Kontrollkästchen **Alle Berichtswährungen einschließen**. Es sind mehrere Ansichten verfügbar, wenn Sie den Bericht anzeigen und auf die Schaltfläche **Währung** im Web-Viewer klicken.
5.  Klicken Sie im Feld **Berichte in Gruppe** auf **Hinzufügen**, um die Berichte zu wählen, die in die Berichtsgruppe einbezogen werden sollen. Um mehrere Berichte im Dialogfeld **Hinzufügen** auszuwählen, halten Sie STRG-Taste gedrückt, während Sie Berichte auswählen. Wenn Sie die Berichtsauswahl abgeschlossen haben, klicken Sie auf **OK**.
6.  Klicken Sie auf **Datei** &gt; **Speichern**, um die neue Berichtsgruppe zu speichern.

### <a name="modify-a-report-group"></a>Ändern einer Berichtsgruppe

1.  Klicken Sie im Navigationsbereich des Berichts-Designers auf **Berichtsgruppen**.
2.  Doppelklicken Sie auf die zu ändernde Berichtsgruppe.
3.  Nehmen Sie auf der Registerkarte **Berichtsgruppe** die gewünschten Änderungen vor.
4.  Klicken Sie im Menü **Datei** auf **Speichern**, um die geänderte Berichtsgruppe zu speichern. Alternativ klicken Sie auf die **Speichern**-Schaltfläche ![Speichern](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Speichern") in der Symbolleiste.

**Hinweis:** Wenn Sie geplant haben, Berichte in Zeitabständen zu erstellen, können Sie diese Einstellungen überschreiben und einen Bericht sofort generieren.

### <a name="generate-a-report-group-report"></a>Generieren eines Berichtsgruppenberichts

1.  Klicken Sie im Navigationsbereich des Berichts-Designers auf **Berichtsgruppen**.
2.  Öffnen Sie die zu generierende Berichtsgruppe.
3.  Klicken Sie auf die **Bericht generieren** -Schaltfläche ![Bericht generieren](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Bericht generieren") zum Generieren von Berichten.

### <a name="delete-a-report-group"></a>Löschen einer Berichtsgruppe

1.  Klicken Sie im Navigationsbereich des Berichts-Designers auf **Berichtsgruppen**.
2.  Zum Löschen klicken Sie im Navigationsbereich mit der rechten Maustaste auf die Berichtsgruppe, und wählen Sie dann **Löschen** aus.
3.  Wenn eine Bestätigungsmeldung angezeigt wird, klicken Sie auf **Ja**.

## <a name="report-group-tab-controls"></a>Berichtsgruppen-Registerkartensteuerelement
In der folgenden Tabelle werden die Steuerelemente der Registerkarte **Berichtsgruppen** beschrieben.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Steuerung</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Überschreiben von Unternehmen, Details und Datumseinstellungen von einzelnen Berichtsdefinitionen</td>
<td>Aktivieren Sie dieses Kontrollkästchen, um einzelne Berichtsdefinitionen der Berichte in dieser Berichtsgruppe für die Generierung dieser Berichte zu überschreiben.</td>
</tr>
<tr class="even">
<td>Unternehmensname</td>
<td>Wählen Sie das Unternehmen für die Berichte aus.</td>
</tr>
<tr class="odd">
<td>Detailebene</td>
<td>Spezifizieren Sie die für den Bericht gewünschte Detailstufe.
<ul>
<li><strong>Financial</strong> − Ein übergeordneter Zusammenfassungsbericht. Sie können keine Detailinformationen zu Konten und Dimensionen anzeigen, ausgenommen derer, die über die Berichtsstruktur hinzugefügt wurden.</li>
<li><strong>Finanzen &amp; Konto</strong> − Ein Bericht, der eine übergeordnete Zusammenfassung und Kontodetails enthält.</li>
<li><strong>Finanzen, Konto &amp; Buchung</strong> − Ein Bericht, der eine übergeordnete Zusammenfassung und Buchungsdetails enthält.</li>
</ul></td>
</tr>
<tr class="even">
<td>Vorläufig</td>
<td>Spezifizieren Sie die für den Bericht gewünschten Aktivitätstypen.
<ul>
<li><strong>Nur gebuchte Aktivität</strong> − Enthält nur die Buchungen und Salden, die in den Finanzdaten gebucht wurden.</li>
<li><strong>Gebuchte und nicht gebuchte Aktivität</strong> − Enthält alle Buchungen und Salden, die in den Finanzdaten eingegeben und gebucht wurden.</li>
<li><strong>Nur nicht gebuchte Aktivität</strong> − Enthält nur Buchungen, die in die Finanzdaten eingegeben, aber noch nicht gebucht wurden.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Alle Berichtswährungen einschließen</td>
<td>Alle zusätzlichen Berichtswährungen, die in Ihrem Microsoft Dynamics ERP-System konfiguriert sind, werden hier aufgeführt. Wählen Sie dieses Kontrollkästchen aus, um zusätzliche Berichte in den angegebenen Währungen zu generieren. Sie können dann im Web-Viewer angezeigt werden, indem Sie auf die Schaltfläche <strong>Währung</strong> klicken und eine Währung auswählen.</td>
</tr>
<tr class="even">
<td>Nicht mit Berichtsdefinition gespeicherte Datumsinformationen</td>
<td><ul>
<li>Basisperiode</li>
<li>Basisjahr</li>
<li>Berücksichtigter Zeitraum</li>
</ul>
Nur Einstellungen zum Standardbasiszeitraum werden mit der Berichtsdefinition gespeichert.</td>
</tr>
<tr class="odd">
<td>Mit Berichtsdefinition gespeicherte Datumsinformationen</td>
<td><ul>
<li>Berichtsdatum</li>
<li>Standardbasiszeitraum</li>
</ul></td>
</tr>
<tr class="even">
<td>Berichte in Gruppe</td>
<td>Fügen Sie Berichte in der Berichtsgruppe hinzu, entfernen Sie sie aus dieser oder sortieren Sie sie neu.
<ul>
<li>Doppelklicken Sie zum Hinzufügen von Berichtsdefinitionen zur Berichtsgruppe auf die Berichtsgruppe, um sie zu öffnen, und klicken Sie dann auf <strong>Hinzufügen</strong>. Wählen Sie die Berichte aus, die in die Berichtsgruppe eingefügt werden sollen, und klicken Sie dann auf <strong>OK</strong>.</li>
<li>Wählen Sie zum Entfernen eines Berichts aus der Berichtsgruppe den Bericht aus, und klicken Sie dann auf <strong>Entfernen</strong>.</li>
<li>Um die Reihenfolge zu ändern, in der die Berichte generiert werden, wählen Sie einen Bericht in der Liste aus, und klicken anschließend auf <strong>Nach oben verschieben</strong> oder <strong>Nach unten verschieben</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Finanzberichterstellung](financial-reporting-intro.md)




