---
title: Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch
description: "In diesem Thema wird beschrieben wie ein Artikel, der die Site-Dimension für den Deckung gesetzt hat, geplant wird."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: dde8bee2b068b1054735cd01dd0859e372c47172
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch

[!include[banner](../includes/banner.md)]


In diesem Thema wird beschrieben wie ein Artikel, der die Site-Dimension für den Deckung gesetzt hat, geplant wird.

Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:

-   Die Standortdimension ist als obligatorische Dimension festgelegt und muss für die Bedarfsbuchung angegeben werden.
-   Die Lagerortdimension ist nicht auf obligatorisch festgelegt. Der Lagerort ist unter Umständen bekannt, wird jedoch nicht in der Produktprogrammplanberechnung verwendet.
-   Die Standortdimension ist für die Disposition festgelegt.
-   Die Lagerortdimension ist nicht für die Disposition festgelegt. Deshalb werden Angebot und Nachfrage nach Standort und möglicherweise auch nach weiteren Dispositionsdimensionen zusammengefasst.

In der folgenden Grafik wird der Ablauf der Produktprogrammplanung veranschaulicht. Die Parameter, auf die in der Grafik Bezug genommen wird, sowie deren Position werden im Folgenden erläutert:
-   Für den Artikel ist die Artikeldeckung definiert. Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**. Wählen Sie den Artikel aus, und klicken Sie auf **Planen &gt; Artikeldeckung**.
-   Für den Lagerort sind Auffüllbeziehungen definiert. Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**. Wählen Sie auf der Registerkarte **Produktprogrammplanung** die Feldgruppe **Hauptlagerort**.
-   Der standardmäßige Auftragstyp wird zur Produktion, der Bestellung oder dem Kanban festgelegt. Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**. Wählen Sie den Artikel aus, und klicken Sie auf **Planen &gt; Standardauftragseinstellungen**. Im Formular **Standardauftragseinstellungen** sehen Sie das Feld **Standardauftragstyp**.

![Bedarf für Disposition an Standort, Lagerort nicht obligatorisch](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="see-also"></a>Siehe auch
--------

[Produktprogrammplanung und Funktion für mehrere Standorte](master-plan-multisite-functionality.md)

[Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch](master-plan-site-coverage-warehouse-mandatory.md)

[Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Produktprogrammplanungslauf - Ermittlung der Stücklistenversion](master-plan-bom-version-determined.md)



