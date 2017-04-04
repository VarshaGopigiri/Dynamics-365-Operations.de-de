---
title: "Einstellungen erweiterte die Funktionen für Cloud POS und MPOS"
description: "Dieses Wiki behandelt die Optionen für die Einrichtung der erweiterten Anmeldung für Cloud-POS und Retail Modern POS (MPOS)."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 0dc80784a5c9a7de6009826284cb68f1aee83f70
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a>Einstellungen erweiterte die Funktionen für Cloud POS und MPOS

Dieses Wiki behandelt die Optionen für die Einrichtung der erweiterten Anmeldung für Cloud-POS und Retail Modern POS (MPOS).

<a name="setting-up-extended-logon"></a>Einrichten der erweiterten Anmeldung
=========================

Sie können die Einstellung für Strichcodemasken ** Einzelhandel und Handel ** ** &gt; am richten Kanal suchen ** &gt; ** POS eingerichtet ** &gt; ** POS-Profile ** &gt; ** Funktionsprofile **. Das Inforegister **Funktionen** umfasst folgende Optionen, die der erweiterten Anmeldung zugeordnet sind.

### <a name="staff-bar-code-logon"></a>Personal-Strichcodeanmeldung

Wenn die Option **Personal-Strichcodeanmeldung** aktiviert ist, können Arbeitskräfte, deren POS-Anmeldeinformationen die erweiterte Anmeldung zugewiesen ist, sich mit einem Strichcode anmelden.

### <a name="staff-bar-code-logon-requires-password"></a>Personalanmeldung mit Strichcode erfordert Kennwort.

Wenn die Option **Personalanmeldung mit Strichcode erfordert Kennwort** aktiviert ist, wird bei der Personalanmeldung mit Strichode nur die Arbeitskraft ausgewählt, die der angegebenen erweiterten Anmeldung zugewiesen ist. Arbeitskräfte müssen noch eigene Kennwörter eingeben, wenn diese Option aktiviert ist.

### <a name="staff-card-logon"></a>Personalkartenanmeldung

Wenn die Option **Personalkartenanmeldung** aktiviert ist, können Arbeitskräfte, deren POS-Anmeldeinformationen die erweiterte Anmeldung zugewiesen ist, sich mit einem Magnetstreifen anmelden.

### <a name="staff-card-logon-requires-password"></a>Personalanmeldung mit Karte erfordert Kennwort.

Wenn die Option **Personalanmeldung mit Karte erfordert Kennwort** aktiviert ist, wird bei der Personalanmeldung mit Karte nur die Arbeitskraft ausgewählt, die der angegebenen erweiterten Anmeldung zugewiesen ist. Arbeitskräfte müssen noch eigene Kennwörter eingeben, wenn diese Option aktiviert ist.

<a name="assigning-an-extended-logon"></a>Zuweisen einer erweiterten Anmeldung
===========================

Standardmäßig können nur Manager die erweiterte Anmeldung den Arbeitskräften zuweisen. Damit erweiterte Anmeldung zuzuweisen, fahren Sie mit ** erweiterte Anmeldung ** in POS. Anschließend Suche nach einer Arbeitskraft nach Eingabe der Kennung oder Bediener in der Auswahlliste. Wählen Sie die Arbeitskraft aus, und klicken Sie anschließend auf **Zuweisen**. Auf der nächsten Seite ziehen Sie die Karte durch das Lesegerät oder scannen Sie die Karte, um der Arbeitskraft die erweiterte Anmeldung zuzuweisen. Wenn der Vorgang erfolgreich war, wird die Schaltfläche **OK **verfügbar. Klicken Sie auf **OK**, um die erweiterten Anmeldung für diese Arbeitskraft zu speichern.

<a name="deleting-an-extended-logon"></a>Löschen einer erweiterten Anmeldung
==========================

Um die erweiterte Anmeldung zu löschen, die einer Arbeitskraft zugewiesen wurde, suchen Sie die Arbeitskraft, indem Sie den Vorgang **Erweiterte Anmeldung** verwenden. Wählen Sie die Arbeitskraft aus, und klicken Sie anschließend auf **Zuweisung aufheben**. Alle erweiterten Anmeldeinformationen, die dieser Arbeitskraft zugeordnet sind, werden entfernt.

<a name="extending-extended-logon"></a>Erweitern der erweiterten Anmeldung
========================

Der Anmeldedienst kann erweitert werden, um zusätzliche Geräte für die erweiterte Anmeldung zu unterstützen, z.B. Handflächenscanner. Weitere Informationen finden Sie in der Dokumentation zur Erweiterbarkeit des POS.

<a name="using-extended-logon"></a>Verwenden der erweiterten Anmeldung
====================

Wenn die erweiterte Anmeldung konfiguriert ist und einer Arbeitskraft ein Strichcode oder ein Magnetstreifen zugewiesen wurde, muss die Arbeitskraft seine Karte nur Karte durch ein Lesegerät ziehen, wenn die POS-Anmeldeseite angezeigt wird. Wenn auch ein Kennwort erforderlich ist, damit die Anmeldung durchgeführt werden kann, wird die Arbeitskraft aufgefordert, das Kennwort einzugeben.

