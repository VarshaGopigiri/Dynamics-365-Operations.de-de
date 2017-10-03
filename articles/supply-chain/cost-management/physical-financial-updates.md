---
title: "Physische und wertmäßige Aktualisierungen"
description: "Dieses Thema bietet einen Überblick darüber, welche Buchungsarten eine Erhöhung oder eine Verringerung der Lagermenge zur Folge haben."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a0eeb5a57f9b82150150752c64e89c2c91856889
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017

---

# <a name="physical-and-financial-updates"></a>Physische und wertmäßige Aktualisierungen

[!include[banner](../includes/banner.md)]


Dieses Thema bietet einen Überblick darüber, welche Buchungsarten eine Erhöhung oder eine Verringerung der Lagermenge zur Folge haben. 

Lagerbuchungen können in Microsoft Dynamics 365 for Finance and Operations sowohl physisch als auch wertmäßig aktualisiert werden. Einige Typen physischer und wertmäßiger Buchungen erhöhen die Lagermenge, während andere die Menge verringern.

## <a name="physical-increases"></a>Physische Erhöhung
Beim Ausführen einer physischen Buchung besitzt der Buchungsdatensatz den Status **Eingegangen**. Folgende Buchungen gelten als physische Zunahmen:

-   Bestellungszugang
-   Lieferschein-Retoure für einen Auftrag
-   Einen Produktionsauftrag als abgeschlossen melden
-   Nebenprodukt der Entnahmeliste eines Produktionsauftrags

## <a name="financial-increases"></a>Wertmäßige Erhöhung
Beim Ausführen einer wertmäßigen Buchung besitzt der Buchungsdatensatz, durch den sich eine Zunahme der Menge ergibt, den Status **Eingekauft**. Folgende Buchungen gelten als wertmäßige Zunahmen:

-   Kreditorenrechnung
-   Auftragsrechnung für eine Retoure
-   Nachkalkulation für einen Produktionsauftrag
-   Lagererfassungen mit positiver Menge (beispielsweise Bewegungs-, Gewinn- und Verlust-, Inventur-, Stücklisten- oder Umlagerungserfassungen)

## <a name="transactions-that-increase-quantity"></a>Buchungen mit Mengenerhöhung
Buchungen, durch die sich eine Erhöhung der Menge ergibt, werden zum laufenden Durchschnittseinstandspreis ausgeführt. Finance and Operations berechnet einen laufenden Durchschnittseinstandspreis, der auf den Kosten der einzelnen Buchungen für jede Lagerungsdimension basiert, die wertmäßig verfolgt wird. Informationen zu laufenden Durchschnittseinstandspreisen finden Sie unter [Laufender Durchschnittseinstandspreis](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Buchungen mit Mengenverringerung
Der laufende Durchschnittseinstandspreis wird von Finance and Operations beim Ausführen einer Buchung verwendet, durch die sich eine Verringerung der Menge ergibt – unabhängig davon, welches Lagermodell dem jeweiligen Bestand zugeordnet ist. Die Buchung, durch die sich eine Verringerung der Menge ergibt, darf vor der Buchung nicht per Markierung mit einer anderen Buchung verknüpft worden sein. Wird der Wert des physisch verfügbaren Bestands negativ, werden von Finance and Operations die Lagerkosten verwendet, die für den Artikel auf der Seite **Artikel** definiert sind. **Hinweis:** Bei aktivierter Funktion für mehrere Standorte werden statt dieser Kosten die Lagerkosten verwendet, die auf der Seite **Standardauftragseinstellungen** für den Standort definiert sind.

## <a name="physical-issues-vs-financial-issues"></a>Vergleich zwischen physischen und wertmäßigen Abgängen
Beim Ausführen einer physischen Abgangsbuchung besitzt der Buchungsdatensatz den Status **Abgesetzt**. Folgende Buchungen gelten als physische Abgänge:

-   Kommissionierlistenerfassung für einen Produktionsauftrag
-   Auftragslieferschein
-   Lieferschein-Retoure für eine Bestellung

Beim Ausführen einer wertmäßigen Buchung besitzt der Buchungsdatensatz den Status **Verkauft**. Folgende Buchungen gelten als wertmäßige Abgänge:

-   Einen Produktionsauftrag beenden
-   Auftragsrechnungen
-   Rücksendung einer Kreditorenrechnung
-   Lagererfassungen mit negativer Menge (beispielsweise Bewegungs-, Gewinn- und Verlust-, Inventur-, Stücklisten- oder Umlagerungserfassungen)

Buchungen, durch die sich eine Verringerung der Menge ergibt, werden zum laufenden Durchschnittseinstandspreis ausgeführt. Daher müssen Abgangsbuchungen beim Lagerabschluss mit Zugangsbuchungen ausgeglichen werden. Die Grundlage hierfür bildet das den einzelnen Artikeln zugewiesene Lagermodell.



