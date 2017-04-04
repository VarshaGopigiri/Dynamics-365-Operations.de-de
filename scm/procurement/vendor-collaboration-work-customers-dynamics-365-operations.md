---
title: Kreditorenzusammenarbeit mit Debitoren
description: "In diesem Thema wird beschrieben, wie Sie Kreditorenzusammenarbeit verwenden können, um in Microsoft Dynamics 365 for Operations mit Bestellungen zu arbeiten und Lieferungsbestand zu überwachen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 11cd2242b5a575ae87b0dbcf6f8ce268fcea5377
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-with-customers"></a>Kreditorenzusammenarbeit mit Debitoren

In diesem Thema wird beschrieben, wie Sie Kreditorenzusammenarbeit verwenden können, um in Microsoft Dynamics 365 for Operations mit Bestellungen zu arbeiten und Lieferungsbestand zu überwachen.

In diesem Thema wird beschrieben, wie Sie Kreditorenzusammenarbeit verwenden können, um mit Debitoren in Microsoft Dynamics 365 for Operations zu arbeiten. Zudem enthält Informationen darüber, wie auf Bestellungen und überwacht reagiert und wie Lieferungsbestand überwacht. Es ist auch möglich, Kreditorenzusammenarbeit verwendet, um mit Rechnungen arbeiten. Weitere Informationen finden Sie Kreditorenzusammenarbeit-Rechnungsstellungsarbeitsbereich [] (/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace ).

## <a name="working-with-purchase-orders"></a>Mit Bestellungen arbeiten
Der Arbeitsbereich**Bestellungsbestätig** ermöglicht Ihnen, auf Bestellungen zu antworten, die zur Prüfung gesendet wurden. Er ermöglicht es Ihnen außerdem, Informationen zu Bestellungen, die eine Aktivität vom Debitor erfordern und Bestellungen, die bestätigt wurden aber noch offen sind, anzuzeigen. Es gibt drei Listen im Arbeitsbereich **Bestellungsbestätigung**:

-   ** Bestellungen zur Prüfung ** - Diese Liste enthält PO an, an, sich gesendet wurde und eine Antwort von Ihnen ein. Nachdem Sie reagieren, verschwindet die Bestellung in der Liste. Wenn der Debitor Ihnen eine neue Version der Bestellung sendet, bevor Sie auf die frühere geantwortet haben, wird nur die aktuelle Version angezeigt.
-   **Debitorenaktivität abwarten** - Diese Liste ermöglicht es Ihnen, Bestellungen anzuzeigen, auf die Sie geantwortet haben, die aber vom Debitor noch nicht bestätigt wurden. Wenn Sie die Bestellung akzeptiert haben, können Sie sie in dieser Liste überwachen, bis der Status auf **bestätigt** ändert. Wenn Sie die Bestellung zurückgewiesen oder sie mit Änderungen akzeptiert haben, können Sie die Bestellung hier überwachen, bis der Debitor eine neue Version übermittelt.
-   **Bestätigte Bestellungen öffnen** - Diese Liste enthält alle Bestellungen für das Konto, die den Status **Bestätigt** haben. Wenn Produkte oder Dienste für die Bestellung vollständig eingegangen sind, verschwindet die Bestellung in der Liste.

Die folgende Liste zeigt die vier Seiten, die Sie verwenden können, um mit Bestellungen zu arbeiten, wobei zwei die gleichen Informationen wie Listen im Arbeitsbereich enthalten:

-   **Bestellungen zur Prüfung** (siehe oben)
-   **Bestellungskreditoren-Bestätigungsverlauf** - Diese Seite enthält alle Bestellungen allen Versionen von Bestellungen, die an den Kreditor gesendet wurden, sowie alle Antworten, die vom Kreditor zurückgeliefert wurden.
-   **Offene bestätigte Bestellungen** (siehe oben)
-   **Alle bestätigten Bestellungen** - Diese Seite enthält alle Bestellungen, die bestätigt wurden, einschließlich jener, von denen Produkte oder Dienstleistungen empfangen wurden. Sie können diese Liste verwenden, um zu überprüfen, für welche Bestellungen Sie Rechnungen übermitteln können.

### <a name="responding-to-purchase-orders"></a>Antworten auf Bestellungen

Die Bestellungen, dass der Debitor Sie zur Prüfung eingereicht hat, sind im ** Bestellbestätigung ** Arbeitsbereich auf der ** Bestellungen zur Prüfung ** Seite angezeigt. Nachdem Sie eine Bestellung öffnen, können Sie festlegen, dass sie zu akzeptieren, sie ablehnen oder sie mit Änderungen zu bestätigen. Es kann im Bestellungskopf oder für einzelne Positionen Anlagen geben. Es ist auch möglich für Sie, Informationen zu Ihrer Antwort im Bestellungskopf oder einzelnen Positionen zuzuordnen. Zum Beispiel können einen Ersatzartikel für eine der Positionen vorschlagen. Sie können die Bestellung als PDF-Datei in der Vorschau anzeigen und drucken, indem Sie die Option **Vorschau anzeigen/Drucken** verwenden. Sie können die folgenden Dimensionsspalten mithilfe der Aktivität ausblenden oder anzeigen **Anzeigendimensionen** : Standort, Lagerort, Größe, Farbe, Stil, Konfiguration. Wenn Sie die ** nehmen Sie mit Änderungen an ** Option verwenden, können Sie einzelne Positionen annehmen oder ablehnen. Sie können die folgenden Änderungen für den auch Positionen vornehmen:

-   Ändern von Mengen oder Datumsangaben. Wenn Sie das bestätigte Lieferdatum für alle Positionen aktualisieren möchten, können Sie die Option **Lieferdatum aktualisieren** im Bestellungskopf verwenden.
-   Aufteilen von Positionen für sonstige Lieferdaten und Mengen.
-   Einen Artikel ersetzen. Um dies zu bewerkstelligen, geben Sie eine Artikelbeschreibung und die Artikelnummer im Feld **Extern** in Abschnitt **Positionsdetails** ein.

Sie können Preisgestaltungsinformationen oder Zuschlägen nicht ändern, doch können Sie Vorschläge für Änderungen dieser mithilfe von Hinweisen vornehmen. Wenn Ihnen der Kunde eine neue Version einer Bestellung sendet, gibt es einen Versionssuffix, um anzuzeigen, dass dies eine geänderte Version einer Bestellung ist, die zuvor mitgeteilt wurde. Die Seite **Bestellungskreditoren-Bestätigungsverlauf** ermöglicht es Ihnen und Ihren Lieferanten, den Verlauf jedes Auftrags zu verfolgen.

## <a name="monitoring-consignment-inventory"></a>Verfügbarer Lagerbestand überwachen
Wenn Sie Lieferungsbestand verwenden, können Sie die Kreditorenzusammenarbeitschnittstelle verwenden, um Informationen zu den folgenden Seiten anzeigen:

-   ** Die Bestellungen, die Lieferungsbestand verbrauchen ** - Bestellungen für Lieferungsbestand werden generiert, wenn der Debitor die Zuständigkeit des Lagers wird. Diese Lieferungsbestellungen werden nur auf der Seite **Bestellungen, die Lieferungsbestands verbrauchen** angezeigt. Sie sind nicht in der Seite **Alle bestätigten Bestellungen** enthalten.
-   **Produkte vom Lieferbestand erhalten** - Diese Seite enthält alle Transaktionen, bei  denen der Besitz der Produkte vom Kreditor an das Unternehmen übertragen wurde. Sie können diese Informationen verwenden für die Rechnungsstellung.
-   **Verfügbarer Lieferungsbestand** - Diese Seite zeigt  den Lieferungsbestand Ihres Unternehmens, der am Lager ist.


<a name="see-also"></a>Siehe auch
--------

[Benutzer für Kreditor-Kooperationen verwalten](manage-vendor-collaboration-users.md)

