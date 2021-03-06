---
title: Unterlieferung einrichten
description: "In diesem Thema wird erläutert, wie eingehende Lieferungsbestandsvorgänge konfiguriert werden."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 758ea8b658693910edeada3a4c27c34ae187b28c
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-consignment"></a>Unterlieferung einrichten

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie eingehende Lieferungsbestandsvorgänge konfiguriert werden.

Beim Lieferungsbestand handelt es sich um Bestand, der im Besitz eines Kreditors ist, der aber an Ihrem Standort gelagert ist. Wenn Sie bereit sind, den Bestand zu verbrauchen oder verwenden, übernehmen Sie den Besitz des Bestands. In diesem Thema werden die Einstellungen beschrieben, die benötigt werden, um Lieferungsprozesse zu ermöglichen. Weitere Informationen zu Lieferungsprozessen finden Sie unter [Lieferung](consignment.md).

## <a name="inventory-owners"></a>Bestandsbesitzer
Um physischen, eingehenden Lieferungsbestand zu erfassen, müssen Sie einen Kreditoreneigentümer definieren. Dies erfolgt auf der Seite **Bestandseigentümer**. Wenn Sie ein **Kreditorenkonto** auswählen, generiert dies Standardwerte für die Felder **Name** und **Besitzer**. Der Wert im Feld **Besitzer** wird für den Kreditor angezeigt, somit möchten Sie ihn möglicherweise ändern, wenn die Namen Ihres Kreditorenkontos von externen Personen nicht einfach erkannt werden können. Es ist möglich, das Feld **Besitzer** zu bearbeiten. Dies gilt jedoch nur bis zu dem Zeiptunkt, an dem Sie den Datensatz **Bestandsbesitzer** speichern. Das Feld **Name** wird mit dem Namen der Partei aufgefüllt, dem das Kreditorenkonto zugeordnet ist, und dieser kann nicht geändert werden.

[![Bestandsbesitzer](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Rückverfolgungsgruppe
Artikel, die bei Lieferungsprozessen verwendet werden, müssen einer **Rückverfolgungsangabengruppe** zugeordnet werden, wobei die Dimension **Besitzer** auf **Aktiv** festgelegt ist. Bei der „Besitzerdimension” sind die Optionen **Physischer Bestand** und **Wertmäßiger Bestand** immer aktiviert. Die Option **Disposition nach Dimensionen** ist nie aktiviert.

[![Rückverfolgungsangabengruppe](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Erfassung für die Änderung von Bestandseigentümern
Die Erfassung **Bestandsbesitzänderung**wird verwendet, um die Übertragung des Besitzes des Lieferungsbestands vom Kreditor zur juristischen Person, die ihn verbraucht, aufzuzeichnen. Wie jede Bestandserfassung muss sie mit einem Bestandserfassungsname identifiziert werden. Diese Namen werden auf der Seite **Bestandserfassungsnamen** erstellt, und der **Erfassungstyp** muss auf **Besitzänderung** festgelegt werden.

[![Bestandeigentümer-Änderungserfassung](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Kreditorenzusammenarbeit in den Lieferungsprozessen
Wenn Ihre Kreditoren die Kreditorenzusammenarbeitschnittstelle verwenden, können sie diese verwenden, um den Verbrauch des Bestands an Ihrem Standort zu überwachen. Weitere Informationen zur Einrichtung von Kreditoren zur Verwendung der Kreditorenzusammenarbeit finden Sie unter [Konfiguration der Sicherheit für Kreditoren-Zusammenarbeitsbenutzer](../procurement/configure-security-vendor-portal-users.md)

