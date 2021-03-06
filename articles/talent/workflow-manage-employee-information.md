---
title: Mit Workflows Mitarbeiterinformationen verwalten
description: "In diesem Thema wird erläutert, wie die Sie Workflowfunktion für die Personalverwaltung verwenden können, um Mitarbeiterdaten zu verwalten. So können Sie beispielsweise einen Workflow einer Position zuordnen und einen Genehmigungsworkflow konfigurieren, der gestartet wird, wenn Mitarbeiter Ihren Datensatz ändern."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: abc52192848649672cbcb8c770d74ba2aef139be
ms.openlocfilehash: cf2200057053f5a6d4754d37111ebe34849bb99d
ms.contentlocale: de-de
ms.lasthandoff: 02/14/2018

---

# <a name="use-workflows-to-manage-employee-information"></a>Mit Workflows Mitarbeiterinformationen verwalten

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie die Sie Workflowfunktion für die Personalverwaltung verwenden können, um Mitarbeiterdaten zu verwalten. So können Sie beispielsweise einen Workflow einer Position zuordnen und einen Genehmigungsworkflow konfigurieren, der gestartet wird, wenn Mitarbeiter Ihren Datensatz ändern.

Die Workflowfunktion für die Personalverwaltung beinhaltet zahlreiche Workflows zur Verwaltung von Personalverwaltungsaktivitäten. Darüber hinaus stehen zahlreiche Optionen zur Verfügung. So können Sie bestimmte Workflows ändern und einer Berichterstellungshierarchie zuordnen. Workflows sind verfügbar, um die Verwaltung von Änderungen an mehreren Standardtypen der Mitarbeiterdaten zu unterstützten. Sie können einen Workflow einer Position zuordnen. Wenn Mitarbeiter dann ihren Datensatz ändern, wird ein Workflow gestartet, der eine Genehmigung erfordert, bevor die neuen Informationen gespeichert werden. Workflows sind für die folgenden Informationsarten vordefiniert, damit Sie Änderungen effizient verwalten können und Ihre Mitarbeiterdaten immer korrekt sind.

-   Kennnummern
-   Kurse
-   Ausbildung
-   Bild
-   Ausgeliehene Artikel
-   Berufserfahrung
-   Projekterfahrung
-   Qualifikationen
-   Vertrauensposition
-   Personalverwaltungsaktivitäten
-   Kursregistrierung

Wenn Mitarbeiter eingestellt oder übertragen werden oder das Beschäftigungsverhältnis beendet wird, kann der Workflow einen Prüfprozess enthalten. Auf diese Weise kann ein Dokument überarbeitet oder die Bedingungen für eine Aktivität als Teil des Workflows definiert werden. Nach Abschluss des Prüfprozesses wird das Dokument oder die Aktivität abgeschlossen. Der Workflow wird dann zum Schritt der abschließenden Genehmigung verschoben.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Zuordnen eines Workflows zu einer Positionshierarchie
Sie können einen Workflow einer beliebigen Hierarchie zuordnen, die Sie konfigurieren. Wird beispielsweise eine Position einer Matrixberichterstellungshierarchie zugeordnet, können Sie einen Workflow konfigurieren, der Ausgaben für ein bestimmtes Projekt an den Projektleiter weiterleitet und nicht an den Vorgesetzten des Mitarbeiters, der dieser Position zugeordnet ist. Zum Erstellen oder Ändern eines vorhandenen Workflows klicken Sie auf der Seite **Personalverwaltungsworkflow** auf **Neu**. Wählen Sie einen Workflow in der Liste aus, um den Workflowdesigner zu starten. Sie können den Designer verwenden, um einen neuen Workflow zu erstellen oder die Schritte in einem vorhandenen Workflow zu ändern. Wenn Sie einen vorhandenen Workflow ändern, werden die Änderungen als neue Version gespeichert. Daher können Sie immer wieder zu einer früheren Version wechseln, falls notwendig.

## <a name="configure-a-human-resources-workflow"></a>Konfigurieren eines Personalverwaltungsworkflows
Um einen grundlegenden Workflow zu konfigurieren, der startet, wenn Mitarbeiter Änderungen an ihrer persönlichen Kennung fordern, führen Sie die folgenden Schritte aus:

1.  Klicken Sie auf der Seite **Personalverwaltungsworkflows** auf **Neu**.
2.  Wählen Sie in der Liste der verfügbaren Workflows **Kennnummern** aus.
3.  Klicken Sie auf **Ausführen**, um den Workflowdesigner zu starten, und geben Sie nach Aufforderung Ihren Benutzernamen und Ihr Kennwort ein.
4.  Verschieben Sie das **Kennungsnummer genehmigen**-Element von der Liste der Workflowelemente in die Designercanvas.
5.  Verbinden Sie das Genehmigungselement mit **Start** und **Fertig stellen**.
6.  Doppelklicken Sie auf die Option für **Element genehmigen**, klicken Sie dann mit der rechten Maustaste, und wählen Sie **Eigenschaften** aus.
7.  Gehen Sie folgendermaßen vor, um Anweisungen für die Arbeitsaufgabe hinzuzufügen:
    1.  Wählen Sie **Zuweisung** und anschließend **Hierarchie** unter dem Zuweisungstyp aus.
    2.  Wählen Sie unter der **Hierarchie**-Auswahl die Option **Konfigurierbare Hierarchie** aus.
    3.  Fügen Sie eine Beendigungsbedingung hinzu, und schließen Sie die Seite.

8.  Führen Sie alle zusätzlichen Anweisungen zu Ende aus (es sollten keine zusätzlichen Warnungen vorhanden sein).
9.  Klicken Sie auf **Speichern und schließen**. Aktivieren Sie den neuen Workflow, wenn das Dialogfeld geöffnet wird, und wählen Sie **Als aktiv festlegen** aus.
10. Wechseln Sie zu **Personalverwaltung** &gt; **Positionen** &gt; **Hierarchietypen für die Position**.
11. Wählen Sie **Matrix** aus.
12. Fügen Sie den **Arbeitskraft-Kennungsnummer**-Workflow zur Liste hinzu.





