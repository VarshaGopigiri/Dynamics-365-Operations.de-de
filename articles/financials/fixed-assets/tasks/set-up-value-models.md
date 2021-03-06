--- 
title: "Bücher einrichten"
description: Die folgende Prozedur zeigt, wie Sie ein neues Abschreibungsbuch erstellen und es einer Anlagengruppe zuordnen.
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a29cae6cdcd03903359a3a468243c6ad03c7adc6
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-books"></a>Bücher einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Die folgende Prozedur zeigt, wie Sie ein neues Abschreibungsbuch erstellen und es einer Anlagengruppe zuordnen. Dabei werden die Buchhalterrolle und die Demodaten für die juristische Person USMF verwendet.


## <a name="create-a-book"></a>Buch erstellen
1. Wechseln Sie zu "Anlagen" > "Einstellungen" > "Bücher".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld 'Buch' einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Wenn "Abschreibung berechnen" ausgewählt ist, werden die zugeordneten Anlagenbuch in die Abschreibungsvorschläge einbezogen. Wenn dies nicht ausgewählt ist, wird die Anlagebuch nicht automatisch abgeschrieben.  
5. Wählen Sie "Ja" im Feld "Ermittelte Abschreibung" aus.
6. Geben Sie im Feld 'Abschreibungsprofil' einen Wert ein, oder wählen Sie einen Wert aus.
    * Ein alternatives Abschreibungsprofil ist auch als eine Switchover-Methode der Abschreibung bekannt. Der Abschreibungsvorschlag schaltet auf dieses Profil um, wenn das alternative Profil einen Abschreibungsbetrag berechnet, der gleich oder größer ist, als das standardmäßiges "Abschreibungsprofil".  
    * Das "Außerordentliche Abschreibungsprofil" wird für die zusätzliche Abschreibung einer Anlage unter besonderen Umständen verwendet. Sie können dieses Profil z. B. verwenden, um eine Abschreibung in Folge einer Naturkatastrophe zu erfassen.  
    * Wenn die Option "Abschreibungsregulierungen mit Basisregulierungen erstellen" ausgewählt ist, werden Abschreibungsregulierungen automatisch erstellt, wenn der Wert einer Anlage aktualisiert wird. Wenn sie nicht ausgewählt ist, wird der aktualisierte Anlagewert sich nur auf die Abschreibungsberechnungen ausgehend vom heutigen Datum auswirken.  
7. Wählen Sie "Ja" im Feld "Abschreibungsregulierungen mit Basisregulierungen erstellen".
    * Standardmäßig werden Anlagenbuchtransaktionen im Hauptbuch gebucht. Sie können Buchungen im Hauptbuch für das Buch deaktivieren, indem Sie das Feld "Ins Hauptbuch buchen" auf Nein festlegen. Bücher, die nicht im Hauptbuch buchen, werden in der Regel für die Steuererklärung verwendet. Dies bietet zusätzliche Flexibilität zur Löschung von historischen Buchungen für das Anlagenbuch, da sie nicht im Hauptbuch eingerichtet wurden.  
    * Die Buchungsebene wird standardmäßig auf die aktuellen Ebene festgelegt, wenn das Buch im Hauptbuch bucht, und auf "Keine", wenn es nicht im Hauptbuch bucht. Aktualisieren Sie die "Buchungsebene", wenn Sie benötigen, dass Transaktionen für dieses Buch zu einer anderen Ebene gebucht werden.  
8. Geben Sie im Feld "Kalender" einen Wert ein oder wählen Sie einen Wert aus.
    * Abgeleitete Bücher buchen Translationen für verschiedene Bücher gleichzeitig. Sie erstellen die Buchungen mit dem primären Buch und während der Buchung wird eine genaue Kopie der Buchung im abgeleiteten Abschreibungsbuch gebucht. Es gibt keine Neuberechnung bei den Transaktionen im abgeleiteten Buch. Sie sollten diese nicht für Abschreibungsbuchungen verwenden.  

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Buch einer Anlagengruppe zuordnen
1. Klicken Sie auf "Anlagengruppen".
2. Geben Sie im Feld "Anlagengruppe" einen Wert ein oder wählen Sie einen Wert aus.
3. Geben Sie im Feld "Nutzungsdauer" eine Zahl ein.
    * Beachten Sie, dass Abschreibungszeiträume nach der Festlegung der Nutzungsdauer berechnet wird.  
    * Sie können die Abschreibungskonvention für Steuerzwecke bei Bedarf festlegen.  


