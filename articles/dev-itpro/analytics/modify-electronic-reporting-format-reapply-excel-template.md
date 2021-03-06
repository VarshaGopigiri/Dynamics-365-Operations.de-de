---
title: "Ein elektronisches Berichterstellungsformat ändern, indem eine Microsoft Excel-Vorlage erneut angewendet wird"
description: "Dieses Thema enthält Informationen darüber, wie Sie das elektronische Meldung (ER)- Format ändern können, das verwendet wird, um Geschäftsdokumente zu generieren, indem eine geänderte Tabelle erneut angewendet wird."
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: fca7fb75b965886c2ebc06b12940434f2ffc2543
ms.contentlocale: de-de
ms.lasthandoff: 02/27/2018

---
# <a name="modify-an-electronic-reporting-format-by-reapplying-a-microsoft-excel-template"></a>Ein elektronisches Berichterstellungsformat ändern, indem eine Microsoft Excel-Vorlage erneut angewendet wird

[!include [banner](../includes/banner.md)]

Das elektronische Meldung (ER)- Tool wird verwendet, um Geschäftsdokumente in einem elektronischen Format zu generieren. Um ein Geschäftsdokument zu generieren, müssen Sie ein ER-Format erstellen und verwenden dann den ER-Designe, um das Layout des Geschäftsdokuments zu definieren und die Daten anzugeben, die im Modul implementierten einbezogen werden sollen. Sie können das ER-Format anschließend ausführen, um das Geschäftsdokument zu generieren.

Das ER-Tool kann verwendet werden, um Geschäftsdokumente als Microsoft Excel-Dateien zu generieren. Sie können ein Excel-Dokument als Vorlage für diese Dokumente verwenden. Um das Dokumentlayout im ER-Designer zu definieren, können Sie den Inhalt des Excel-Dokuments importieren das als Vorlage für das festgelegte ER-Format verwenden möchten. Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Design einer Konfiguration zur Generierung von Berichten im OPENXML-WORD-Format** (Teil des 7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)-Geschäftsprozesses) wieder.

Wenn Sie das Excel-Dokument bearbeiten, das als Vorlage für ein Geschäftsdokument verwendet wird, wenn neue ER-Funktionen Sie die aktualisierte Vorlage für den ER-Format erneut verwenden. Das ER-Format wird dann aktualisiert, damit sie die aktualisierte Vorlage verwendet werden soll. Weitere Informationen zu diesen Funktionen, siehe Aufgabenleitfaden **Ein elektronisches Berichterstellungsformat ändern, indem eine Microsoft Excel-Vorlage erneut angewendet wird** (Gehört zum 7.5.5.3 Acquire/Develop IT service/solution components (10683) Geschäftsprozess). Als Teil des Schritts für das Importieren einer aktualisierten Vorlage im Aufgabenleitfaden, verwenden Sie die geänderte Vorlage des Zahlungsberichts SampleVendPaymWsReport2-Excel-Datei als Vorlage.

