---
title: "Ausgeglichene Erfassungen für einheitenübergreifende Buchhaltung"
description: "Dieser Artikel zeigt, wie eine Erfassung automatisch ausgeglichen wird, wenn eine ausgleichende Finanzdimension auf der Sachkontoseite ausgewählt ist."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 9b509e6561f017c71c5c9614af6f22c682ec89e3
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="balanced-journals-for-interunit-accounting"></a>Ausgeglichene Erfassungen für einheitenübergreifende Buchhaltung

[!include[banner](../includes/banner.md)]


Dieser Artikel zeigt, wie eine Erfassung automatisch ausgeglichen wird, wenn eine ausgleichende Finanzdimension auf der Sachkontoseite ausgewählt ist. 

Wenn Buchhaltungseinträge nicht auf der Ebene der Finanzdimensionswerte ausgeglichen sind, werden zusätzliche Kontoeinträge automatisch erstellt, um die Erfassung auszugleichen. Diese Kontoeinträge verwenden **Einheitenbezogen - Soll**- und **Einheitenbezogen - Haben**-Buchungstypen auf der Seite **Konten für automatische Buchungen**, um das Hauptkonto zu bestimmen. Beispielsweise wird Verzweigung, die das zweite Segment des Sachkontos darstellt, als Ausgleichsfinanzdimension ausgewählt, und die folgenden Buchhaltungseinträge werden anschließend erstellt.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100,00 DR |
| 6100 – NY – OU\_249  | 100,00 DR |
| 2100 – MSP – OU\_256 | 200,00 CR |

In diesem Fall werden die folgenden Salden bestimmt:

-   Für Verzweigung MSP = 100.00 HABEN
-   Für Verzweigung NY = 100.00 SOLL

Die folgenden Buchhaltungseinträge werden daher automatisch erstellt, damit die Erfassung auf der Ebene der Finanzdimensionswerte ausgeglichen ist.

|                                   |           |
|-----------------------------------|-----------|
| (Einheitenbezogen Soll) – MSP  – OU\_256 | 100,00 DR |
| (Einheitenbezogen Haben) – NY – OU\_249 | 100,00 CR |





