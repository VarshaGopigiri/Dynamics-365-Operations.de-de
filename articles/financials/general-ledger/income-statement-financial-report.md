---
title: "Finanzbericht für die Einkommensaufstellung"
description: "In diesem Artikel werden die Standardberichte für Einkommensaufstellung beschrieben. Er beschreibt zudem die die Bausteine, die diesen Bericht zugeordnet werden."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: f07aea0b87bc3e09982f9ba248d3c28540fd2dc5
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017

---

# <a name="income-statement-financial-report"></a>Finanzbericht für die Einkommensaufstellung

[!include[banner](../includes/banner.md)]


In diesem Artikel werden die Standardberichte für Einkommensaufstellung beschrieben. Er beschreibt zudem die die Bausteine, die diesen Bericht zugeordnet werden. 

<a name="default-income-statement-report"></a>Standardbericht für die Einkommensaufstellung
-------------------------------

| Standardbericht             | Funktionsweise                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| Einkommensaufstellung – Standard | Enthält eine Ansicht der Rentabilität der Organisation für die aktuelle Periode und seit Jahresbeginn. |

## <a name="building-blocks"></a>Bausteine
Der Finanzbericht für die Einkommensaufstellung verwendet die folgenden Bausteine.

| Standardbericht             | Zeilendefinition                     | Spaltendefinition          |
|----------------------------|------------------------------------|----------------------------|
| Einkommensaufstellung - Standard | Zusammengefasste Einkommensaufstellung - Standard | Periodisch und seit Jahresbeginn - Standard |

### <a name="row-definition"></a>Zeilendefinition

Die Zeilendefinition, zusammengefasste Einkommensaufstellung - Standard enthält einen Abschnitt für jeden Teil einer herkömmlichen Einkommensaufstellung. Die Hauptkontokategoriedimension wird verwendet, um diese Zeilendefinition aufzubauen. Daher kann jeder Benutzer den Bericht erstellen, ohne Änderungen vorzunehmen zu müssen.

### <a name="column-definition"></a>Spaltendefinition

Die Spaltendefinitionen enthalten verschieden Spaltentypen, um verschiedene Stufen der Genauigkeit und der Finanzdaten bereitzustellen.

-   **Periodisch und seit Jahresbeginn - Standardspaltentypen:**
    -   **DESC** - Die Beschreibung der Zeilendefinition
    -   **FD** - Finanzdaten für die aktuelle Periode
    -   **FD** - Finanzdaten seit Jahresbeginn

 

<a name="see-also"></a>Siehe auch
--------

[Finanzberichterstellung](financial-reporting-getting-started.md)

[Finanzberichte anzeigen](view-financial-reports.md)

[Dynamics Financial Reporting-Blog](http://blogs.msdn.com/b/dynamics_financial_reporting/)



