---
title: Einrichten eines bevorzugten Technikers
description: "Sie können eine beliebige Arbeitskraft als bevorzugten Techniker für eine Servicevereinbarung oder einen Serviceauftrag auswählen."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 390e436b63fdfe82e0b743e7f286cae3bb29be55
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---


# <a name="set-up-a-preferred-technician"></a>Einrichten eines bevorzugten Technikers 

[!include [banner](../includes/banner.md)]


Sie können eine beliebige Arbeitskraft als bevorzugten Techniker für eine Servicevereinbarung oder einen Serviceauftrag auswählen. Es empfiehlt sich allerdings, die Arbeitskraft dem entsprechenden Einsatzteam zuzuordnen, damit sie im Modul **Einsatzplanung** berücksichtigt wird.

## <a name="assign-employee-to-a-dispatch-team"></a>Zuweisen eines Mitarbeiters zu einem Einsatzteam

1.  Klicken Sie auf **Personalverwaltung** \> **Allgemein** \> **Arbeitskräfte** \> **Arbeitskräfte**. Doppelklicken Sie auf eine Arbeitskraft, um die Seite "Details zur Arbeitskraft" zu öffnen. Klicken im **Aktivitätsbereich** auf **Einstellungen** \>**Einsatzteam**, um das Formular **Arbeitskräfte disponieren** zu öffnen.

2.  Wählen Sie im Feld **Einsatzteam** das Team aus, dem die Arbeitskraft zugewiesen werden soll.

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a>Zuweisen eines bevorzugten Technikers zu einer Servicevereinbarung

1.  Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**. Doppelklicken Sie auf eine Servicevereinbarung, um das Detailformular zu öffnen.

2.  Aktivieren Sie auf der Registerkarte **Allgemein** das Kontrollkästchen **Bevorzugter Techniker**, und wählen Sie anschließend ein Mitglied des entsprechenden Einsatzteams als bevorzugten Techniker für die Servicevereinbarung aus.

## <a name="assign-a-preferred-technician-to-a-service-order"></a>Zuweisen eines bevorzugten Technikers zu einem Serviceauftrag

1.  Klicken Sie auf **Serviceverwaltung** \> **Periodisch** \> **Einsatzplanung**.
    

    > [!NOTE]
    > <P>Geben Sie im Formular <STRONG>Einsatzplanung</STRONG> einen Datumsbereich für die anzuzeigenden Einsatzaktivitäten an. Geben Sie außerdem an, ob abgeschlossene Aktivitäten angezeigt werden sollen und ob die Liste mit den Einsatzaktivitäten auf die Teams beschränkt werden soll, denen Sie selbst angehören oder die Sie selbst überwachen. Klicken Sie auf <STRONG>OK</STRONG>, um das Formular <STRONG>Einsatzplanung</STRONG> zu öffnen.</P>



2.  Wählen Sie die Position der Serviceaktivität aus, die Sie ändern möchten.

3.  Weisen Sie auf der  **Registerkarte** mithilfe der Liste **Arbeitskraft** ein Mitglied des entsprechenden Einsatzteams als bevorzugten Techniker für den Serviceeinsatz zu.

## <a name="see-also"></a>Siehe auch

[Servicevereinbarungen](service-agreements.md)

[Manuelles Erstellen von Serviceaufträgen](create-service-orders-manually.md)

[Formular "Servicevereinbarungen"](https://technet.microsoft.com/en-us/library/aa617823\(v=ax.60\))
  



