---
title: "Überblick über die positive Zahlung"
description: "In diesem Artikel finden Sie Informationen über positive Zahlungen, die zur Generierung einer elektronischen Liste mit Schecks verwendet werden, die für die Bank bereitgestellt wird."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 13a7a842e7b4522b508a34fdf86bb3bf58a0845f
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="positive-pay-overview"></a>Überblick über die positive Zahlung

[!include [banner](../includes/banner.md)]

In diesem Artikel finden Sie Informationen über positive Zahlungen, die zur Generierung einer elektronischen Liste mit Schecks verwendet werden, die für die Bank bereitgestellt wird. 

Positive Zahlungen werden zur Generierung einer elektronischen Liste mit Schecks verwendet, die für die Bank bereitgestellt wird. Positive Lohndateien können Scheckbetrug verhindern. Sie richten positiven Zahlungen ein, um eine elektronische Liste mit Schecks zu generieren, wenn Schecks gedruckt werden. Wenn der Scheck der Bank präsentiert wird, vergleicht die Bank den Scheck mit der Liste der Schecks, die zuvor eingereicht gesendet wurden. Wenn der Originalscheck mit einem Scheck in der Liste übereinstimmt, löscht die Bank den Scheck. Wenn der Scheck mit keinem Scheck iin der Liste übereinstimmt, hält die Bank den Scheck zur Prüfung zurück.

Positiver Lohn wird auch als SafePay bezeichnet. 

Positive Lohndateien können vertrauliche Informationen zu Zahlungsempfänger und Scheckbeträgen enthalten. Daher stellen Sie sicher, dass Sie entsprechende Sicherheitspraktiken ab dem Zeitpunkt verwenden, an dem die Dateien generiert werden, bis sie von der Bank empfangen werden. Dateien für positive Zahlungen werden gemäß den Downloadanweisungen für den Webbrowser heruntergeladen. 

Dateien für positive Zahlungen werden über Datenentitäten erstellt. Bevor Sie eine Datei für positive Zahlungen generieren, müssen Sie die Transformationsformate für das XML einrichten, das die Daten in ein Format übersetzt, das die Bank verarbeiten kann. 

Jedem Bankkonto, für das Sie positive Erfassung von Lohndaten generieren möchten, müssen Sie das positive Lohnformat zuweisen. Nach der Generierung der Zahlungen können Sie eine positive Lohndatei für eine einzelne juristische Person und ein einzelnes Bankkonto generieren. Alternativ können Sie Dateien für positive Zahlungen für mehrere juristische Personen und Bankkonten gleichzeitig generieren. 

Nachdem die Schecks, die in einer positiven Lohndatei aufgeführt sind, bezahlt wurden, erhalten Sie eine Bestätigungsnummer von der Bank. Sie können anschließend die Positive Pay-Datei in Microsoft Dynamics 365 for Finance and Operations bestätigen. 

Wenn Sie eine Datei für positive Zahlungen ändern müssen, können Sie diese erneut aufrufen. Für jeden Scheck in der positiven Lohndatei zeigt das Feld an, ob der Scheck in einer positiven Lohndatei zurückgesetzt wurde.

Weitere Informationen finden Sie unter [Einrichten und Generieren von Dateien für positive Zahlungen](set-up-generate-positive-pay-files.md).




