---
title: "Buchen der Wareneingangserfassung für zurückgelieferte Produkte"
description: "Buchen der Wareneingangserfassung für zurückgelieferte Produkte."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverview
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
ms.openlocfilehash: cbe60846f0a16b5061349d9960c49bb5310bd6f9
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---


# <a name="post-arrival-journal-for-returned-products"></a>Buchen der Wareneingangserfassung für zurückgelieferte Produkte 

[!include [banner](../includes/banner.md)]


Prüfen Sie zum Verarbeiten einer Rücklieferung zuerst die Rückgabemenge, und aktualisieren Sie das Mengenfeld in der Wareneingangserfassung. Wählen Sie anschließend einen Dispositionscode aus, oder geben Sie an, dass die zurückgelieferten Artikel geprüft werden müssen. Nach Ausführung dieser Schritte kann die Wareneingangserfassung für die Rücklieferung gebucht werden.

1.  Klicken Sie auf **Lagerverwaltung** \> **Periodisch** \> **Wareneingangsübersicht**.

2.  Im **Setupname** Filter wählen Sie **Rücklieferung** aus.

3.  Wenn die Liste der Zugänge lang ist, schränken Sie die Liste mithilfe der Felder im Bereich **Bereich** ein.

4.  Suchen Sie die Position der Rücklieferung, die gebucht werden soll, aktivieren Sie das entsprechende Feld **Für Wareneingang auswählen**, und klicken Sie dann auf **Wareneingang starten**.

5.  Klicken Sie **Erfassungen** \> **Wareneingänge aus Zugängen anzeigen**, um das Formular **Lagerplatzerfassung** zu öffnen.
    

    > [!TIP]
    > <P>Wählen Sie eine Erfassung aus, und klicken Sie auf <STRONG>Positionen</STRONG>, um detaillierte Informationen anzuzeigen.</P>


6.  Nehmen Sie erforderliche Aktualisierungen vor, und klicken Sie anschließend auf **Buchen**.

Nach der Buchung der Erfassung werden die zurückgelieferten Artikel im Lagerbestand erfasst, und im Formular **Rücksendungen** wird angezeigt, dass die Artikel am Lagerort eingegangen sind.

## <a name="see-also"></a>Siehe auch

[Formular "Lagerplatzerfassung"](https://technet.microsoft.com/en-us/library/aa584822\(v=ax.60\))

  



