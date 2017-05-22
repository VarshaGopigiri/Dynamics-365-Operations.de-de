---
title: Navigationssuche
description: In diesem Artikel wird beschrieben, wie die die Suchfunktion verwendet wird, um zu den Seiten in Microsoft Dynamics 365 for Operations zu navigieren.
author: aneesmsft
manager: AnnBe
ms.date: 04/27/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 650c8b60ba8204e8990cf607c1c9901b8f0bb762
ms.openlocfilehash: 9f2cbafa3e21006f458067baf99ea5abaef8bb86
ms.contentlocale: de-de
ms.lasthandoff: 04/28/2017


---

# <a name="navigation-search"></a>Navigationssuche

[!include[banner](../includes/banner.md)]


In diesem Artikel wird beschrieben, wie die die Suchfunktion verwendet wird, um zu den Seiten in Microsoft Dynamics 365 for Operations zu navigieren.

Microsoft Dynamics 365 for Operations bietet Funktionen für eine große Auswahl an Branchen und Segmenten. Die Bewerbung beinhaltet mehrere Bereiche und Seiten, um Ihnen dabei zu unterstützten, verschiedene Funktionen auszuführen. Um die Seiten rasch zu finden, die Sie mit Ihren Aufgaben durchführen müssen, verwenden Sie die Navigations-Suchfunktion. 

Zur Verwendung dieser Funktion, klicken Sie auf das Symbol **Suche** um das Feld **Suchen** anzuzeigen. Sie können dann eines oder mehrere Wörter im Feld eingeben. Das Systems durchsucht sofort in der Anwendung nach entsprechenden Seiten, die den Begriffen entsprechen, die Sie eingegeben haben. So können Sie beispielsweise "Kreditorenrechnung" als Eingabe eingeben, und dann zeigt das System Ergebnisse an, die mit diese Eingabe übereinstimmen. 

**Hinweis:** Das Feld **Suchen** hilft Ihnen dabei, Seiten finden und zu navigieren. Es unterstützt Sie nicht dabei, bestimmte Daten oder Aktivitäten zu suchen. 

[![Suchfeld](media/navigation-search.png "Suchfeld") 

## <a name="quickly-navigate-to-a-particular-page"></a>Navigieren Sie schnell zu einer bestimmten Seite
Die Navigationssuchfunktion dient auch dazu, damit Sie schnell zu einer bestimmten Seite navigieren können. Wenn Sie beispielsweise Buchhalter für die Kreditorenkonten sind, der häufig die Seite **Zahlungserfassung verwendet**, können Sie " Zahlungserfassung" im **Suchfeld** eingeben. Da die Eingabe ein exaktes gleich wie der Seitentitel, wird die Seite oben der Suchergebnisse angezeigt, und Sie können sie schnell zu navigieren. 

Die Suchergebnisliste zeigt sowohl den Seitentitel als auch den Navigationspfad an. Dies zeigt die Position der Seite in der Anwendung an. Darüber hinaus hilft es dabei, zwischen zwei oder mehr ähnlichen Seiten in den Ergebnissen zu unterscheiden. 

Wenn Sie nach einer Seite suchen, wird die Eingabe mit dem Seitentitel sowie dem Navigationspfad abgeglichen. Wenn Sie zum Beispiel "Forderung" im **Such**feld eingeben, finden Sie Ergebnisse für die Seiten, die im Debitorenbereich verfügbar sind, obwohl der Seitentitel nicht das Wort "Forderung" enthält. 

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Navigieren Sie schnell zu einer Seite basierend auf dem technischen Formularnamen
Die Navigationssuchfunktionen enthalten außerdem eine vielgenutzte Funktion für Poweruser: die Möglichkeit, schnell zu einer Seite basierend auf dem technischen Formularname zu navigieren. Viele Benutzer sind mit dem System so vertraut, dass ihnen die genauen Formularnamen bekannt sind, mit denen sie arbeiten. Wenn Sie einer dieser Benutzer sind, können Sie **Formular:** eingeben, gefolgt vom Namen des Formulars nach dem Sie suchen. Wenn Sie beispielsweise **Formular: vendinvoice** eingeben, enthalten die Suchergebnisse alle Seiten, in denen die Formularnamen mit **vendinvoice** beginnen. 

## <a name="administration-and-security"></a>Administration und Sicherheit
Aus Sicht einer Verwaltungs- und Sicherheitsperspektive tauchen in den Navigationssuchenfunktionen nur zwei Ergebnisstypen auf:

-   Seiten, die in der aktuellen Konfiguration aktiviert sind (über Konfigurationsschlüssel).
-   Seiten, auf die der Benutzer aufgrund seiner Rolle Zugriff hat.

Die Liste von Suchergebnissen ist auf 10 Artikeln beschränkt. Wenn Sie nicht gefunden, wonach Sie in den Ergebnisse suchen, sollten Sie versuchen, die Eingabe zu verfeinern oder den Inhalt aktualisieren. 

## <a name="development"></a>Entwicklung 
Aus der Entwicklungsperspektive sind die Navigationssuchenfunktionen sehr einfach zu nutzen, da es virtuell keine Verzögerung zwischen der Bereitstellung von Menüelementen und deren Anzeige in den Suchergebnissen gibt. Solange die Menüelemente entweder mit dem Navigationsbereich oder dem Dashboard verknüpft sind, werden diese automatisch durchsuchbar. 
