---
title: Einrichten von Einzelhandelsprodukten
description: In diesem Artikel wird beschrieben, wie Einzelhandelsprodukte in Microsoft Dynamics 365 for Operations - Retail eingerichtet.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 4f565bd5563cbcf9079f3220dd855f41889f1d5e
ms.contentlocale: de-de
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-retail-products"></a>Einrichten von Einzelhandelsprodukten

[!include[banner](includes/banner.md)]


In diesem Artikel wird beschrieben, wie Einzelhandelsprodukte in Microsoft Dynamics 365 for Operations - Retail eingerichtet.

Bevor Sie Produkte zum Verkauf in den Einzelhandelskanälen anbieten können, müssen Sie die Produkte im Einzelhandel und Handel in Microsoft Dynamics 365 for Operations - Retail erstellen und konfigurieren. Einzelhandel verwendet die Produktfunktionen in Microsoft Dynamics 365 for Operations, um organisationsweite Produkte im Produktmaster zu erstellen. Sie können die Produkte erstellen, die Produkteigenschaften und Attribute definieren und die Produkte den Einzelhandelskategoriehierarchien zuweisen. Um die Produkte für Ihre Einzelhandelskanäle verfügbar zu machen und sie einem aktive Sortiment hinzuzufügen, müssen die Produkte für die juristischen Personen freigegeben werden, in denen sie verfügbar sind. Führen Sie zum Einrichten der Produkte, die Sie über Einzelhandelskanäle verkaufen, die folgenden Aufgaben aus:

1.  Definieren Sie eine Einzelhandelsprodukthierarchie. Wenn Sie die Kategoriehierarchiefunktionen in Dynamics 365 for Operations verwenden, können Sie Einzelhandelskategoriehierarchien definieren, um die Produkte, die Sie an die Einzelhandelskanäle vertreiben, zu gruppieren und zu kategorisieren. Benutzerdefinierte und Systemattribute können auf der Kategorieebene definiert werden. Daraufhin erben alle Produkte, die der Kategorie zugewiesen sind, diese Attribute. Mehrere Kategoriehierarchien können definiert werden, und jedes Produkt kann mehreren Hierarchien zugewiesen werden. In einer einzelnen Hierarchie kann ein Produkt jedoch nur einer Kategorie zugewiesen werden.
2.  Fügen Sie Produkte und Produktvarianten zum Produktmaster hinzu. Produkte, die dem Produktmaster hinzugefügt werden, stellen eine globale Liste von Produkten dar. Sie können Produkte manuell und einzeln hinzufügen, oder Sie können Produktdaten von Ihren Kreditoren importieren.
3.  Geben Sie die Produkte für juristische Personen frei. Nur Produkte, die für juristische Personen freigegeben wurden, können in Ihren Einzelhandelskanälen verfügbar gemacht werden. Wenn Sie ein Produkt erstmals definieren, definieren Sie das Produkt auf organisationsweiter Ebene. Sie können mindestens eine juristische Person auswählen, um das Produkt freigeben. Das Produkt wird dann in mehreren Einzelhandelskanälen in Ihrer Organisation verfügbar. Sie können diese Funktion verwenden, um ein Produkt einmal zu erstellen, Produktattribute und Eigenschaften an einer Stelle hinzuzufügen und zu aktualisieren, und das Produkt dann in Ihrer Organisation an die Einzelhandelskanäle zu vertreiben, in denen es verfügbar ist.
4.  Fügen Sie Produkte Sortimenten hinzu. Ein Sortiment stellt eine Sammlung von Produkten dar, die Sie in den Einzelhandelskanälen anbieten. Sie können ein oder mehrere Sortimente definieren, und jedes Produkt kann einem oder mehreren Sortimenten zugewiesen werden. Um Produkte den Einzelhandelskanälen zuzuweisen, weisen Sie die Sortimente diesen Einzelhandelskanälen zu. Wenn Sie ein Sortiment erstellen, können Sie Produkte hinzufügen, die noch nicht für eine juristische Person freigegeben wurden. Sie müssen die Produkte jedoch für eine juristische Person freigeben, bevor die Produkte in den Einzelhandelskanälen verfügbar gemacht werden.
5.  Hinzufügen von Produkten Navigationshierarchien hinzu. Bevor Produkte online oder in Verkaufsstellen durchsucht werden können, müssen sie in einer Einzelhandels-Navigationshierarchie kategorisiert werden.
6.  Produkte zum Katalog hinzufügen Obwohl dieser Schritt für Verkaufsstellen optional ist, erfordern Onlineshops, dass Produkte in mindestens einem Katalog enthalten sind.




