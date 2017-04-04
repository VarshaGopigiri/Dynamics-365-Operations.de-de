---
title: Und
description: "In diesem Thema wird erläutert, wie die eingerichtet, sodass Sie Intergesellschaftserfassungen für Finanzerfassungen, wie und Sachkonto-Zuweisungen Tageserfassungen, Kreditorenrechnungserfassungen und Zahlungserfassungen verwenden können."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5fd279327013f26230146be38e23e9955c6f12c7
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-accounting-setup"></a>Und

In diesem Thema wird erläutert, wie die eingerichtet, sodass Sie Intergesellschaftserfassungen für Finanzerfassungen, wie und Sachkonto-Zuweisungen Tageserfassungen, Kreditorenrechnungserfassungen und Zahlungserfassungen verwenden können.

Intergesellschaftserfassungen können in unterschiedlichen Szenarios, wie täglich, Kreditorenrechnungserfassungen für Erfassungen, Sachkonto-Zuweisungen und zentralisierte Zahlungen erstellt werden. Um diese Szenarien zu ermöglichen, müssen Sie die Verrechnung einrichten.

## <a name="define-main-accounts"></a>Definieren Sie Hauptkonten
Zunächst müssen Sie die Intercompany-Hauptkonten anlegen, die für die Buchhaltungseinträge "Fällig an" und "Fällig von" verwendet werden. Es wird empfohlen, eindeutige Hauptkonten für jedes Unternehmen zu verwenden, um die Abstimmung und die Löschung von Intercompany-Verrechnungseinträgen zu vereinfachen. Wenn Sie eine Äquivalentsdimension Handelspartner oder verwenden, um die Intergesellschaftspartei erkennen, können Sie diese als Dimension feste Dimension im Hauptkonto definieren, das bei der Verrechnung definiert wird. Wenn Sie die Hauptkonten einrichten, sollten Sie das ** Hauptkontotyp ** Feld auf setzen ** Bilanz ** ** ** Hauptkonten auf der Seite.

## <a name="define-journal-names"></a>Definieren von Journalen
Anschließend müssen Sie einen Erfassungsnamen definieren. Legt das ** Erfassungstyp ** Feld auf ** täglich ** ** ** Journale auf der Seite aus. Es wird empfohlen, einen spezifischen Erfassungsnamen für die Verrechnung zu verwenden.

## <a name="define-intercompany-accounting-setup"></a>Definieren Sie Verrechnungseinstellungen
** Verrechnung ** Die Seite wird verwendet, um die Paare von juristischen Personen erstellen, mit die einander abwickeln können. Die wird Verrechnungseinstellungen freigegeben, um die Einstellungen aus allen juristischen Personen angezeigt. Wenn Sie ein neues Paar der juristische Person erstellen, stellen Sie sicher, dass Sie berücksichtigen, welche juristische Person als das ursprüngliche Unternehmen für das Zielunternehmen definiert wird. Wenn Sie Intercompany-Buchungen eingibt, bestimmt die Buchung, der juristischen Person ist, initiierend Zeilencode oder die Buchung. Beispielsweise wird die Verrechnung für USMF (Ursprungslagerort) und USSI (Ziel) eingerichtet. Wenn ein Benutzer in USSI aktiv ist und eine Buchung mit den USMF eingibt, wird die Buchung nicht, da die Verrechnung nur für USMF definiert, wird das der Ersteller gesendet. Wenn jedem Unternehmen eine Buchung auslösen kann, müssen Sie ein zweites Paar der juristischen Person für die gegenseitige Einstellungen erstellen. 

Wählen Sie (Sollkonto ** Fällig von) ** aus und ** (Habenkonto) wegen ** für den Ursprungslagerort und konsolidierte juristische Person enthält. Definieren Sie, Journal ** ** die verwendet wird, wenn die Buchung im Zielunternehmen erstellt wird. Die Erfassung für das ursprüngliche Unternehmen bereits bekannt, da vom Benutzer festgelegt, sofern die Intercompany-Buchung erstellt hat. 

Schließlich wählen Sie, welche juristische Person die unterstützenden erklärenden Beträge erhält, z Skonto oder realisierte Gewinne/Verluste für zentralisierte Zahlungen aus. 

Eine Beziehung gegenseitige kann für die Verrechnung ** ** Seite einfacher eingerichtet werden, indem die verwendet ** Erstellen gegenseitige Beziehung ** Schaltfläche, nachdem das erste Paar der juristischen Person erstellt wurde. Wenn das gegenseitige Paar erstellt wird, werden die Angaben für das Zielunternehmen zum ursprünglichen Unternehmen und umgekehrt kopiert. Die Erfassung, die für das Zielunternehmen definiert wird, bleibt. Die meisten Organisationen verwendet dieselbe Benennungskonvention für ihre Journale, damit das Journal das gleich ist. Wenn das Journal unterscheidet, wird eine Warnung in dem Feld, die Sie darüber informiert werden, dass die Erfassung nicht vorhanden ist und eine andere Erfassung ausgewählt werden kann.

