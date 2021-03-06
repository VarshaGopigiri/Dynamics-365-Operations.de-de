---
title: Beheben von Abweichungen beim Abgleich von Rechnungssummen
description: "Mit dem Rechnungssummenabgleich können Sie sicherstellen, dass die Abweichung der Gesamtbeträge in Rechnungen von den erwarteten Beträgen in einem akzeptablen Rahmen bleibt."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 18250a735d0421daa90b923504aeb94b5003a6a7
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Beheben von Abweichungen beim Abgleich von Rechnungssummen

[!include [banner](../includes/banner.md)]

Ein Typ der Rechnungsabgleichüberprüfung ist der Rechnungssummenabgleich. Um anzugeben, dass das System einen Rechnungssummenabgleich ausführen soll, legen Sie auf der Seite **Kreditorenkontenparameter** auf der Registerkarte **Rechnungsprüfung** die **Rechnungssummen abgleichen**-Option auf **Ja** fest. 

Mit dem Rechnungssummenabgleich können Sie sicherstellen, dass die Abweichung der Gesamtbeträge in Rechnungen von den erwarteten Beträgen in einem akzeptablen Rahmen bleibt. Sechs Summen werden auf der Seite **Detailabgleich für Rechnungssummen** verglichen. Weicht irgendeine der Summen von der erwarteten entsprechenden Bestellungssumme ab, wird eine Abgleichsabweichung markiert. 

Um die Rechnung zu prüfen, die die Summenabgleichsabweichungen aufweist, klicken Sie im Arbeitsbereich, **Kreditorenrechnungseintrag** auf die Kachel **Ausstehende Rechnungen**. Klicken Sie dann im Aktivitätsbereich auf der Registerkarte **Prüfen** auf **Detailabgleich**. Wenn Abgleichsabweichungen erfasst wurden, werden Warnsymbole neben dem Rechnungsbetrag angezeigt. Sie können weitere Details zu den Summen anzeigen, indem Sie den Detailabgleich für Rechnungssummen anzeigen. 

Sollten Sie nach Erkennung der Abweichung der Meinung sein, die Abweichung sei auf fehlerhafte Rechnungsinformationen zurückzuführen, müssen Sie sich möglicherweise mit dem Kreditor in Verbindung setzen. Abhängig von der Einigung mit dem Kreditor stehen folgende Möglichkeiten zur Verfügung:

-   Akzeptieren der Preisabweichung und Buchen der Rechnung mit den Abgleichsabweichungen Ihr System kann auch so eingerichtet werden, dass eine Genehmigung vor dem Buchen erforderlich ist, wenn es Abgleichsabweichungen gibt. In diesem Fall müssen Sie die Abgleichsabweichung genehmigen und können einen Genehmigungskommentar optional eingeben. Sie können dann die Buchung der Rechnung auswählen.
-   Ändern des Rechnungsbetrags auf den erwarteten Betrag und Buchen der Rechnung
-   Anfordern einer Gutschrift über den vollen Betrag sowie einer neuen korrigierten Rechnung des Kreditors

Weitere Informationen finden Sie unter [Erforschen oder Beheben von Ausnahmen](tasks/research-resolve-exceptions.md).



