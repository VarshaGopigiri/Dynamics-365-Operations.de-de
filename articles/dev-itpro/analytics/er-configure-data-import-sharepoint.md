---
title: Datenimport aus SharePoint konfigurieren
description: "In diesem Thema wird erläutert, wie Sie Daten aus Microsoft SharePoint importieren."
author: NickSelin
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 4285db9c71208bce45d64933e692a25ef3f46b26
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2018

---
# <a name="configure-data-import-from-sharepoint"></a>Datenimport aus SharePoint konfigurieren

[!include[banner](../includes/banner.md)]

Um Daten aus einer eingehenden Datei mit Hilfe des Framework für elektronische Berichterstellung zu importieren, müssen Sie ein ER-Format konfigurieren, das den Import unterstützt und dann eine Modellzuordnung des Typs **Bis Ziel** ausführen, der dieses Format als Datenquelle verwendet. Um Daten zu importieren, müssen Sie zu der Datei navigieren, die Sie importieren möchten. Die eingehende Datei kann vom Benutzer manuell ausgewählt werden. Mit der neuen ER-Funktion zum Importieren von Daten aus Microsoft SharePoint kann dieser Prozess als unbeaufsichtigter Prozess konfiguriert werden. Sie können ER-Konfigurationen verwenden, um Daten aus Dateien zu importieren, die in Microsoft SharePoint-Ordnern gespeichert sind. In diesem Thema wird erläutert, wie Sie den Import von SharePoint nach Microsoft Dynamics 365 for Finance and Operations abschließen. Die Beispiele verwenden Kreditorenbuchungen als Geschäftsdaten.

## <a name="prerequisites"></a>Erforderliche Komponenten
Um die Beispiele in diesem Thema abzuschließen, müssen Sie den folgenden Zugriff haben:

- Zugriff auf Finance and Operations für eine der folgenden Rollen:

    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

- Zugriff auf die Instanz von Microsoft SharePoint Server, die für die Verwendung mit Finance and Operations konfiguriert ist.
- ER-Format und Modellkonfigurationen für US 1099-Steuerzahlungen

### <a name="create-required-er-configurations"></a>Erforderliche ER-Konfigurationen erstellen
Spielen Sie die **ER Importieren von Daten aus einer Microsoft Excel Datei** Aufgabenleitfäden ab, die Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)** Geschäftsprozess sind. Diese Aufgabenleitfäden führen Sie durch den Prozess des Entwurfs und die Verwendung von ER-Konfigurationen zum interaktiven Importieren von Kreditorenbuchungen aus externen Microsoft Excel-Dateien. Weitere Informationen finden Sie unter [Eingehende Dokumente in Microsoft Excel analysieren](parse-incoming-documents-excel.md). Und schließlich haben Sie:

- ER-Konfigurationen:

    - ER-Modell-Konfiguration, **US 1099-Steuerzahlungsmodell**
    - Konfiguration des ER-Formats, **Format für den Import von Kreditorenbuchungen aus Excel**

[![Er-Konfigurationen zum Importieren von Daten von SharePoint](./media/GERImportFromSharePoint-01-Configurations.PNG)](./media/GERImportFromSharePoint-01-Configurations.PNG)

- Beispiel der eingehenden Datei für das Importieren von Daten:

    - Excel-Datei **1099import-data.xlsx** mit Kreditorenbuchungen, die in Finance and Operations importiert werden sollen.

[![Microsoft Excel-Beispieldatei zum Importieren aus SharePoint](./media/GERImportFromSharePoint-02-Excel.PNG)](./media/GERImportFromSharePoint-02-Excel.PNG)

> [!NOTE]
> Das Format für den Import von Kreditorenbuchungen wird als Standardmodellzuordnung ausgewählt. Wenn Sie also eine Modellzuordnung des Typs **US 1099-Steuerzahlungsmodell** ausführen und diese Modellzuordnung vom Typ **Bis Ziel** ist, führt die Modellzuordnung dieses Format aus, um Daten aus externen Dateien zu importieren. Diese Daten werden dann zur Aktualisierung der Anwendungstabellen verwendet.

## <a name="configure-document-management-parameters"></a>Parameter für Dokumentverwaltung konfigurieren
1. Konfigurieren Sie auf der Seite **Parameter für Dokumentverwaltung** den Zugriff auf die SharePoint Server-Instanz, die von dem Unternehmen verwendet wird, bei dem Sie angemeldet sind. In diesem Beispiel ist das Unternehmen USMF.
2. Testen Sie die Verbindung zur SharePoint Server-Instanz, um sicherzustellen, dass Ihnen der Zugriff gewährt wurde.

[![Einstellung der Dokumentenverwaltung - SharePoint-Server](./media/GERImportFromSharePoint-03-SharePointSetup.png)](./media/GERImportFromSharePoint-03-SharePointSetup.png)

3. Öffnen Sie die konfigurierte SharePoint-Website und erstellen Sie die folgenden Ordner, in denen die eingehenden Dateien gespeichert werden können:

    - Datei-Importquelle (primär)
    - Datei-Importquelle (alternativ)

[![Einstellung der Dokumentenverwaltung - SharePoint-Server](./media/GERImportFromSharePoint-04-SharePointFolder1.png)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

[![Einstellung der Dokumentenverwaltung - SharePoint-Server](./media/GERImportFromSharePoint-05-SharePointFolder2.png)](./media/GERImportFromSharePoint-05-SharePointFolder2.png)

4. Erstellen Sie in Finance and Operations auf der Seite **Dokumenttypen** die folgenden Dokumenttypen, die für den Zugriff auf die soeben erstellten SharePoint-Ordner verwendet werden:

    - SP-Haupt
    - SP Alternativ

5. Für angelegte Dokumentarten geben Sie im Feld **Gruppe** **Datei** und im Feld **Ort** **SharePoint** ein. Geben Sie dann die Adresse des SharePoint-Ordners ein:

    - Für die Dokumentart **SP Haupt**: Datei-Importquelle (Haupt)
    - Für die Dokumentart **SP Alternativ**: Datei-Importquelle (Alternativ)

[![SharePoint-Einstellung - neuer Dokumententyp](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>ER-Quellen für das ER-Format konfigurieren
1. Klicken Sie auf **Organisationsverwaltung** > **Elektronische Berichterstellung** > **Elektronische Berichtsquelle**.
2. Auf der Seite **Elektronische Berichtsquelle** konfigurieren Sie die Quelldateien für den Datenimport in dem konfigurierten ER-Format.
3. Definieren Sie eine Dateinamenmaske, sodass nur Dateien mit der .xlsx-Erweiterung importiert werden. Die Dateinamenmaske ist optional und wird nur verwendet, wenn sie definiert wurde. Sie können für jedes ER-Format nur eine Maske definieren.
4. Wählen Sie beide SharePoint-Ordner aus, die Sie zuvor erstellt haben.

[![ER-Dateien Quelleneinstellung](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
>Die ER *Quelle* wird für jedes Anwendungsunternehmen einzeln definiert. Im Gegensatz dazu werden ER *Konfigurationen* unternehmensübergreifend genutzt.

> [!NOTE]
> Wenn Sie eine ER-Quelleneinstellung für ein ER-Format löschen, werden auch alle angeschlossenen Dateizustände (siehe unten) gelöscht.

## <a name="review-the-files-states-for-the-er-format"></a>Überprüfen der Dateizustände für das ER-Format
1. Auf der Seite **Elektronische Berichtsquelle** wählen Sie **Dateistatus für die Quellen**, um den Inhalt der konfigurierten Dateiquellen für das aktuelle ER-Format zu überprüfen.
2. Überprüfen Sie im Abschnitt **Dateien** die Liste der Dateien. Diese Liste stellt Folgendes dar:

    - Quelldateien, die auf der Grundlage der Dateinamensmaske (falls eine Dateinamensmaske definiert ist) anwendbar und für den Datenimport bereit sind. Für diese Dateien ist der Bereich **Quellprotokoll für das Importformat** leer.
    - Zuvor importierte Dateien. Für jede dieser Dateien können Sie im Protokoll **Quellprotokoll für das Importformat**, den Verlauf des Imports dieser Datei einsehen.

Sie können auch die Seite **Dateistatus für die Quellen** öffnen, indem Sie **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Dateistatus für die Quellen** auswählen. In diesem Fall enthält die Seite Informationen über Dateiquellen für alle ER-Formate, für die die Dateiquellen in dem Unternehmen konfiguriert wurden, in dem Sie derzeit angemeldet sind.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Importieren von Daten aus Excel-Dateien, die sich in einem SharePoint-Ordner befinden.
1. Laden Sie in SharePoint die Microsoft-Excel-Datei **1099import-data.xlsx**, die Kreditorenbuchungen enthält, in den SharePoint-Ordner **Datei-Importquelle (primär)** hoch, den Sie zuvor erstellt haben.

[![SharePoint-Inhalt - Microsoft Excel-Datei zum Importieren](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Wählen Sie in Finance and Operations auf der Seite **Dateistatus für die Quellen** **Aktualisieren**, um die Seite zu aktualisieren. Beachten Sie, dass die Excel-Datei, die in SharePoint hochgeladen wurde, in dieser Form mit dem Status **Bereit** erscheint. Die folgenden Status werden derzeit unterstützt:

    - **Bereit** - Wird automatisch für jede neue Datei in einem SharePoint-Ordner zugewiesen. Dieser Status bedeutet, dass die Datei für den Import bereit ist.
    - **Importieren** - Wird automatisch von einem ER-Bericht zugewiesen, wenn die Datei durch den Importprozess gesperrt wird, um ihre Verwendung durch andere Prozesse zu verhindern (wenn viele von ihnen gleichzeitig laufen).
    - **Importiert** - Wird automatisch von einem ER-Bericht zugewiesen, wenn der Datei-Import erfolgreich abgeschlossen wurde. Dieser Status bedeutet, dass die importierte Datei aus der konfigurierten Dateiquelle (SharePoint-Ordner) gelöscht wurde .
    - **Fehlgeschlagen** - Wird automatisch von einem ER-Report zugewiesen, wenn der Dateiimport mit Fehlern oder Ausnahmen abgeschlossen wurde.
    - **Gesperrt** - Wird vom Benutzer in diesem Formular manuell vergeben. Dieser Status bedeutet, dass die Datei vorerst nicht importiert wird. Dieser Status kann verwendet werden, um das Importieren einiger Dateien zu verschieben.

[![ER-Datei-Statusseite für die ausgewählten Quellen](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Daten aus SharePoint-Dateien importieren
1. Öffnen Sie den ER-Konfigurationsstruktur, wählen Sie das **US 1099-Steuerzahlungsmodell** und erweitern Sie die Liste der ER-Modellkomponenten.
2. Wählen Sie den Namen der Modellzuordnung, um die Liste der Modellzuordnungen der ausgewählten ER-Modellkonfiguration zu öffnen.

[![ER-Datei-Statusseite für die ausgewählten Quellen](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Wählen Sie **Ausführen** aus, um die ausgewählte Modellzuordnung auszuführen. Da Sie die Dateiquellen für das ER-Format konfiguriert haben, können Sie die Einstellung der Option **Dateiquelle** beliebig ändern. Wenn Sie die Einstellung dieser Option beibehalten, werden die XSLX-Dateien aus den konfigurierten Quellen (in diesem Beispiel die SharePoint-Ordner) importiert.

    In diesem Beispiel importieren Sie nur eine Datei. Wenn jedoch mehrere Dateien vorhanden sind, werden sie in der Reihenfolge, in der sie dem SharePoint-Ordner hinzugefügt wurden, für den Import ausgewählt. Jede Ausführung eines ER-Formats importiert eine einzelne ausgewählte Datei.

[![ER-Modellzuordnung ausführen](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Die Modellzuordnung kann unbeaufsichtigt im Stapelverarbeitungsmodus ausgeführt werden. In diesem Fall wird jedes Mal, wenn eine Stapelverarbeitung dieses ER-Format ausführt, eine einzelne Datei aus den konfigurierten Dateiquellen importiert. Verwenden Sie den folgenden Code, um diese Stapelverarbeitungsausführung zu implementieren.

    ```
    ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId().run()
    ```

    Wenn eine Datei erfolgreich aus dem SharePoint-Ordner importiert wurde, wird sie aus diesem Ordner gelöscht.

5. Geben Sie die Belegkennung, z. B. **V-00001** ein, und wählen Sie dann **OK** aus.

[![ER-Modellzuordnung ausführen](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Wählen Sie auf der Seite **Dateistatus für die Quellen** **Aktualisieren**, um die Seite zu aktualisieren.

[![ER-Datei-Statusseite für die ausgewählten Quellen](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. Überprüfen Sie im Abschnitt **Dateien** die Liste der Dateien. Der Abschnitt **Quellenprotokoll für das Importformat** liefert den Verlauf des Excel-Dateiimports. Da diese Datei erfolgreich importiert wurde, wird sie im SharePoint-Ordner als **gelöscht** markiert.
8. Überprüfen Sie den SharePoint-Ordner **Datei-Importquelle (primär)** . Die erfolgreich importierten Excel-Dateien wurden aus diesem Ordner gelöscht.
9. Wählen Sie in Finance and Operations **Kreditorenkonten** \> **Periodische Aufgaben** \> **Steuererklärung (US 1099)** \> **Kreditorenausgleich für Steuerformulare (US 1099)** aus.
10. Geben Sie in den Feldern **Startdatum** und **Enddatum** entsprechende Werte ein. Wählen Sie dann **Manuelle US 1099-Buchungen** aus.

    Die Kreditorenbuchungen, die aus den Excel-Dateien auf SharePoint für Beleg **V-00001** importiert wurden, werden auf der Seite dargestellt.

[![US 1099-Kreditorenbuchungsseite](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Vorbereitung einer Excel-Datei für den Import
1. Öffnen Sie die zuvor verwendete Excel-Datei. Fügen Sie in Zeile 3 Spalte 1 einen Kreditorencode hinzu, der in der Anwendung nicht vorhanden ist. Fügen Sie der Zeile zusätzliche falsche Kreditoreninformationen hinzu.

[![Microsoft Excel-Beispieldatei zum Importieren aus SharePoint](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Laden Sie die aktualisierte Excel-Datei mit den Kreditorenbuchungen in den SharePoint-Ordner **Datei-Importquelle (primär)** hoch.
3. Öffnen Sie in Finance and Operations die ER-Konfigurationsstruktur, wählen Sie das **US 1099-Steuerzahlungsmodell** und erweitern Sie die Liste der ER-Modellkomponenten.
4. Wählen Sie den Namen der Modellzuordnung, um die Modellzuordnung zu aktualisieren, so dass der falsche Kreditorencode beim Datenimport als Fehler angesehen wird.
5. Wählen Sie **Designer** aus.
6. Auf der Registerkarte **Prüfungen** müssen Sie die Nach-Validierungs-Aktivität für die Validierungsregel ändern, die konfiguriert wurde, um auszuwerten, ob das importierte Kreditorenkonto in der Anwendung existiert. Aktualisieren Sie den Wert des Felds **Nach-Validierungs-Aktivität** auf **Ausführung beenden**, speichern Sie die Änderungen und schließen Sie die Seite.

[![ER-Modellzuordnungsdesigner](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Speichern Sie Ihre Änderungen und schließen Sie den ER-Modellzuordnungsdesigner.
8. Wählen Sie **Ausführen** aus, um die geänderte Modellzuordnung auszuführen.
9. Geben Sie die Belegkennung, z. B. **V-00002** ein, und wählen Sie dann **OK** aus.

    Beachten Sie, dass das Infolog die Benachrichtigung enthält, dass sich in der SharePoint-Ordnerdatei ein falsches Kreditorenkonto befindet und nicht importiert werden kann.

[![ER-Modellzuordnung ausführen](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Auf der Seite **Dateistatus für die Quellen** wählen Sie **Aktualisieren** und überprüfen Sie dann im Abschnitt **Dateien** die Liste der Dateien.

[![ER-Datei-Statusseite für die ausgewählten Quellen](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

Das Protokoll **Quellprotokoll für das Importformat** zeigt an, dass der Importvorgang fehlgeschlagen ist und sich die Datei noch im SharePoint-Ordner befindet (das Kontrollkästchen **Ist gelöscht** ist nicht markiert). Wenn Sie diese Datei auf SharePoint korrigieren, indem Sie den richtigen Kreditorencode hinzufügen und dann den Status der Datei von **Fehlgeschlagen** auf **Bereit** im **Abschnitt Quellprotokoll für das Importformat** ändern, können Sie die Datei erneut importieren.

11. Überprüfen Sie den SharePoint-Ordner **Datei-Importquelle (primär)** . Beachten Sie, dass sich die nicht importierte Excel-Datei immer noch in diesem Ordner befindet.
12. Wählen Sie in Finance and Operations **Kreditorenkonten** \> **Periodische Aufgaben** \> **Steuererklärung (US 1099)** \> **Kreditorenausgleich für Steuerformulare (US 1099)** aus, geben Sie die entsprechenden Werte in die Felder **Startdatum** und **Enddatum** ein, und wählen Sie dann **Manuelle US 1099-Buchungen** aus.

    Nur Transaktionen für Beleg V-00001 sind verfügbar. Es sind keine Transaktionen für den Beleg V-00002 verfügbar, obwohl der Fehler für die zuletzt importierte Transaktion in der Excel-Datei gefunden wurde.

