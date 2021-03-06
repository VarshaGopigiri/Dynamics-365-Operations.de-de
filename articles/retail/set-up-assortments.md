---
title: Einrichten von Sortimenten
description: In diesem Artikel wird beschrieben, was ein Sortiment ist, und es wird beschrieben, wie Sie Sortimente in Microsoft Dynamics 365 for Retail einrichten.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 91713a4492ad82520f7dde611c17a5ea168ed80d
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-assortments"></a>Sortimente einrichten

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, was ein Sortiment ist, und es wird beschrieben, wie Sie Sortimente in Microsoft Dynamics 365 for Retail einrichten.

Ein Sortiment ist eine Sammlung zugehörige Produkte, die einem Einzelhandelskanal, wie einem physischen Laden oder einem Onlineshop, zugewiesen werden. Sie verwenden Sortimente, um die Produkte zu erkennen, die in jedem Shop verfügbar sind. Ein Sortiment kann Produktgruppen enthalten. Daher werden alle Produkte, die einer bestimmten Kategorie zugeordnet sind, ins Sortiment eingeschlossen. Ein Sortiment kann außerdem bestimmte Produkte und bestimmte Varianten von Produkten enthalten. Wenn Sie ein Sortiment einrichten, können Sie Tausende von Produkten für Ihre Einzelhandelskanälen gleichzeitig zuweisen, in beliebigen Kombinationen, die Ihre Shops erfordern. Sie können so viele Sortimente einrichten, wie Sie benötigen. Jedes Produkt kann einem oder mehreren Sortimenten hinzugefügt werden, und jedes Sortiment kann zu einem oder mehreren Einzelhandelskanälen zugewiesen werden. Sie definieren z. B. ein Sortiment, das einen Basissatz an Produkten enthält. Alle Filialen erhalten dieses Sortiment. Sie können dann ein anderes Sortiment definieren, das nur große Sportausrüstung enthält. Nur die größeren Filialen erhalten dieses Sortiment. Das folgende Diagramm zeigt, wie Produkte Sortimenten zugewiesen werden können und wie diese Sortimente Einzelhandelskanälen zugewiesen werden können. ![Produktsortimentbeziehungen](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Erforderliche Komponenten
Bevor Sie ein Sortiment einrichten und dieses einem Einzelhandelskanal zuweisen können, müssen Sie die folgenden Aufgaben ausführen.

| Aufgabe                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Einrichten eines Einzelhandelskanals.          | Einzelhandelskanäle stellen einen physischen Laden, einen Onlineshop oder einen Onlinemarktplatz dar. Sie müssen mindestens einen Einzelhandelskanal festlegen und Optionen für die Filiale konfigurieren. Sortimente werden den Filialen zugewiesen, um die Produkte zu erkennen, die eine bestimmte Filiale führt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Dient zum Erstellen einer Organisationshierarchie. | Nachdem Sie die Einzelhandelskanäle für Ihre Organisation eingerichtet haben, müssen Sie eine Einzelhandels-Organisationshierarchie konfigurieren, die die Organisationsstruktur der Einzelhandelskanäle darstellt. Eine Organisationshierarchie kann für Sortimente, Auffüllung und Berichterstellung verwendet werden. Wenn Sie die Einzelhandelskanäle zu einer Organisationshierarchie hinzufügen, können Sie Sortimente den Gruppen von Filialen zuordnen. Anstatt das Sortiment zu jedem Shop einzeln zuzuordnen, weisen Sie das Sortiment dem allgemeinen Organisationsknoten zu. Wenn anschließend ein neuer Einzelhandelskanal dem allgemeinen Organisationsknoten hinzugefügt wird, werden diesem Einzelhandelskanal automatisch alle Sortimente zugewiesen, die dem Organisationsknoten höherer Ebene zugeordnet waren. Sie können Sortimente nur Einzelhandelskanälen zuweisen, die in einer Organisationshierarchie eingeschlossen sind, der der Kostenträger **Einzelhandelssortiment** zugewiesen ist. |
| Produkte definieren.                  | Bevor Sie Produkte einem Sortiment hinzufügen können, müssen Sie sie in Microsoft Dynamics 365 for Retail hinzufügen. Sie können auch Produkte manuell hinzufügen oder von einem Lieferanten importieren. Nachdem Sie die Produkte hinzufügen, müssen Sie diese einer juristischen Person freigeben. Nur Produkte, die für eine juristische Person freigegeben wurden, können den Einzelhandelskanälen verfügbar gemacht werden. Produkte, die noch nicht für eine juristische Person freigegeben wurden, können einem Sortiment hinzugefügt werden, und das Sortiment kann genehmigt werden. Bis jedoch die Produkte für eine juristische Person freigegeben wurden, können sie nicht den Einzelhandelskanälen verfügbar gemacht werden.                                                                                                                                                                                                                                                                                     |
| Einrichten einer Kategoriehierarchie.      | Wenn Sie Ihre Einzelhandelsprodukte erstellen, können Sie diese gruppieren und kategorisieren, indem Sie das Kategoriehierarchiefeature in verwenden. Sie können eine Kernhierarchie erstellen, um alle Produkte zu gruppieren und zu kategorisieren, die Sie über die Einzelhandelskanäle vertreiben. Sie können auch einzelnen, zusätzliche Kategoriehierarchien erstellen, um die Produkte zu bestimmten Kostenträgern, wie verkaufsfördernden Maßnahmen oder Sortimente, zu gruppieren oder kategorisieren. Wenn Sie Kategoriehierarchien verwenden, können Sie alle die Produkte in einer bestimmten Kategorie einem Sortiment zuweisen. Alle Produkte, die der Kategorie hinzugefügt werden, die im Sortiment enthalten ist, werden automatisch ins Sortiment einbezogen. Anschließend wird beim nächsten Ausführen des Einzelhandelssortimentplaners diese Produkte für die Einzelhandelskanäle verfügbar gemacht, denen das Sortiment zugeordnet ist.                                            |

## <a name="setting-up-an-assortment"></a>Einrichten eines Sortiments
Nachdem Sie die Voraussetzungen abgeschlossen haben, können Sie ein Sortiment erstellen und es den Einzelhandelskanälen zuweisen. Zum Einrichten eines Sortiments müssen folgende Aufgaben ausgeführt werden.

1.  Erstellen Sie ein neues Sortiment, oder kopieren Sie ein vorhandenes Sortiment.
2.  Wählen Sie die Einzelhandelskanäle oder die allgemeinen Gruppen von Einzelhandelskanälen aus, für die das Sortiment gilt.
3.  Fügen Sie Produktkategorien, Einzelprodukte oder Produktvarianten dem Sortiment hinzu. Sie können alle Produkte in einer bestimmten Kategorie einschließen oder Sie können bestimmte Produkte aus einer Kategorie ausschließen, die im Sortiment enthalten ist.
4.  Veröffentlichen Sie das Sortiment. Wenn Sie ein Sortiment veröffentlichen, wird der Einzelhandelssortimentplaner automatisch ausgeführt. Dieser Vorgang generiert die Liste der Produkte. Wenn dieser Prozess abgeschlossen ist, werden die Produkte für die Einzelhandelskanäle verfügbar gemacht, denen das Produktsortiment zugeordnet ist. Wenn Änderungen an einem Sortiment vorgenommen werden, das veröffentlicht wurde, oder am dem Einzelhandelskanälen, denen das Sortiment zugeordnet ist, muss das Sortiment aktualisiert werden. Um das Sortiment aktualisieren wenn Änderungen vorgenommen wurden, können Sie den Einzelhandelssortimentplaner Chargenauftrag ausführen.





