---
title: "Produkteingang für Bestellungen"
description: "Dieser Artikel beschreibt die verschiedenen Optionen für die Registrierung von zugehenden Produkten."
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, Retail
ms.custom: 93113
ms.assetid: d4ec3e86-fce2-4546-911b-e0acf64c8887
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c227664da360f6f8d54b49f15e1b7160aa142ba9
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="product-receipt-against-purchase-orders"></a>Produkteingang für Bestellungen

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Dieser Artikel beschreibt die verschiedenen Optionen für die Registrierung von zugehenden Produkten.

Der Produktzugang ist der Vorgang des Festhaltens des Zugangs von bestellten Produkten. So können die Bestellpositionen für die Fakturierung verarbeitet werden. In einigen Fällen durchlaufen Produkte eine Vorregistrierung, bei der weitere Informationen vom Lieferanten vor dem Zugang der Produkte festgehalten werden. Wenn Produkte zugehen werden sie zuerst als **Registriert** markiert. Produkte können dann zusätzliche Prozesse durchlaufen – beispielsweise die Qualitätssicherung – bevor Sie letztendlich als **Eingegangen** markiert werden.

## <a name="preregistration-asn"></a>Vorregistrierung (ASN)
Lieferanten können Informationen zu den zu liefernden Produkten weitergeben. In diesem Fall können Sie die Produkte vorregistrieren, um diese Informationen aufzuzeichnen, bevor die Produkte empfangen werden. Durch die Vorregistrierung von Produkten verringern Sie den Umfang der Arbeit, die bei der Artikelregistrierung und beim Zugang erforderlich ist. Lieferanten können Produktinformationen elektronisch über eine ASN (Advance Shipment Notice) bereitstellen. Diese wird automatisch im System erfasst. Die Informationen in der ASN umfassen die Menge der Produkte die geliefert werden sollen und wann diese geliefert werden. Die ASN kann auch Informationen wie Chargen- oder Seriennummern umfassen. Die Registrierung der ASN findet im Modul **Transportverwaltung** statt.

## <a name="registration"></a>Umsatzsteuernummer
Eine Produkteingangsregistrierung tritt häufig an Entladerampen in einem Lagerort auf. Sie wird über Handgeräte oder über Wareneingangserfassungen durchgeführt. Alternativ können Sie den Produktzugang manuell registrieren, indem Sie die Aktion **Registrierung** auf der **Bestellung**-Seite nutzen. In beiden Fällen werden die Produkte als **Registriert** markiert. Beachten Sie, dass die Produkte noch nicht als **Empfangen** markiert werden.  

Produkte, die am Lagerort eingehen, können Qualitätskontrollen durchlaufen, bevor sie im Lager eingelagert werden. Qualitätsprüfungsaufträge oder Quarantäneaufträge können zur Qualitätskontrolle genutzt werden. Wenn Qualitätsprüfungsaufträge verwendet werden, können Sie den Prozess für die vorübergehend Blockierung der Produkte während der Prüfung konfigurieren. Wenn Quarantäneaufträge verwendet werden, werden Produkte zur Überprüfung an einen anderen Lagerplatz verschoben. Dieser Lagerort wird als Quarantänelagerort bezeichnet. Bei beiden Überprüfungsprozessen werden möglicherweise einige Waren verschrottet. Entweder, weil Sie die Qualitätsvorgaben nicht erfüllen, oder, weil die Qualitätskontrolle Zerstörungstests für eine Probe des Produkts umfasst.

## <a name="product-receipt"></a>Produktzugang
In den meisten Fällen wird die Aktion **Produktzugang** auf der Seite **Bestellungen** verwendet, um Produkte für die Bestellung als **Empfangen** zu kennzeichnen. Die Seite **Buchen des Produktzugangs** hat verschiedene Optionen für die als geliefert gebuchte Menge. Sie können z. B. das Feld **Menge** auf **Bestellte menge** oder **Menge der aktuellen Lieferung** festlegen. Alternativ nutzen Sie bei einem Lagereingangsprozess das Feld **Registrierte Menge**. Sie können die Mengen für jede Auftragsposition die als **Empfangen** gekennzeichnet wird ändern, um eventuelle Differenzen zu berücksichtigen (z. B. zu große oder kleine Lieferungen). Während des Produktzugangs müssen Sie einen Produktezugangsbezeichner festlegen. Dieser ist in der Regel ein Verweis auf den Lieferschein des Lieferanten. Dieser Bezeichner ist für Buchung erforderlich. Er ermöglicht Prüfungen oder Audits der Lieferscheine des Lieferanten gegen den Zugang und die gebuchten Bestände oder Ausgaben.  

Wenn ein Mitarbeiter Waren über eine Bestellanforderung bestellt, kann dieser Mitarbeiter zur Bestätigung des Produkteingangs aufgefordert werden. Dieses Verhalten können Sie über einen Workflow konfigurieren. Sie können die Workflow-Bedingung so konfigurieren, dass sie Ihren Geschäftsprozessen entsprechen.  

POs können für Produkte erstellt werden, die nicht als Bestand vorgesehen sondern Ausgaben sind. Diese Kategorie umfasst Bestellpositionen bei denen Produkte als über ihre Lagersteuerungsgruppe als **Nicht gelagert** markiert werden sowie Positionen, die Beschaffungskategorien verwenden. In diesem Fall durchlaufen die Artikel möglicherweise nicht die Zugangsregistrierung am Lagerort. Stattdessen wir die Aktion **Produktzugang** verwendet, um den Zugang direkt auf der Bestellung festzuhalten. Der Zugang basiert auf der Bestellten menge und nicht auf der erfassten Menge.  

Sie können Bestellpositionen erstellen, bei denen die Option die **Neue Anlage** aktiviert ist. Diese Option gibt an, dass der Kauf als Anlage statt als Lagerbestand berücksichtigt werden soll. In diesem Fall wurden die Anlagenbestimmungsregeln konfiguriert, um zu bestimmten, ober Kauf des Produktes oder die Kategorie einen bestimmten Grenzwert überschreiten und daher als Anlage gebucht werden müssen (und die Anlagenverwaltung durchlaufen müssen). Käufe können außerdem auch für eine vorhandene Anlage durchgeführt werden. In diesem Fall wird die Menge entsprechend angepasst.  

Sie können mehrere Bestellungen auswählen und den Zugang für alle gemeinsam verarbeiten. Dieser Ansatz wird nicht sehr häufig verwendet. Sie können ihn nutzen, wenn ein Lieferant den Versand in einer einzigen Lieferung zusammengefasst hat. Während des Produktzugangs für den Kauf gibt es eine Funktion für Sammelaktualisierungen. Sammelaktualisierungen ermöglichen die Buchung eines Lieferscheins von einem Lieferanten für mehr als eine Bestellung.  

POs können über einen Auftrag mit der Option **Direktlieferung** erstellt werden. Wenn die Direktlieferung verwendet wird, gehen die Produkte niemals am Lagerort zu. Sie werden vom Lieferanten direkt an den Kunden geliefert. In diesem Fall wird der Zugang normalerweise direkt auf der Bestellung festgehalten. Der Zugang kann automatisch durchgeführt werden (beispielsweise über die EDI-Integration mit dem Lieferanten). Wenn die Bestellung eine Intercompany-Bestellung ist, automatisiert Microsoft Dynamics 365 for Finance and Operations den Zugang für den Intercompany-Auftrag bei Lieferung. Bei der Direktlieferung werden Produkte weiterhin als Lagerbestand gebucht – obwohl Sie nicht physisch im Lager eintreffen. Wenn ein Produktzugang für die Bestellung registriert wird, wird der Auftrag daher automatisch mit einem Lieferschein aktualisiert. So liegt die Gesamtänderung für den Lagerbestand bei Null (0). Bei Direktlieferungsszenarien sollten Sie keine Vorregistrierung nutzen. Wenn Sie mit Lagerorten mit Lagerortverwaltung arbeiten, können Sie die Ladungsträgerregistrierung über die Angabe eines virtuelles Lagerortes umgehen. Sie geben diesen Lagerort im Feld **Direktversand-Lagerort** des Produkts ein. 

Nachdem der Produktzugang für die Bestellung verarbeitet wurde, wird der Bestellstatus auf **Empfangen** gesetzt. Dies zeigt an, dass die Rechnung für die Bestellung verarbeitet werden kann. Über die Seite **Produktzugangserfassungen** können Sie Informationen zu empfangenden Produkten anzeigen.  

Sie können über die Aktivitätsgruppe **Zugang** auf der Seite **Bestellung** auf dieser Seite zugreifen. Die Informationen in den Erfassungen enthalten Informationen zu Mengen, Datumsangaben und Dimensionen.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Überblick über Bestellungen](purchase-order-overview.md)

[Bestellungserstellung](purchase-order-creation.md)

[Genehmigen und Bestätigen von Bestellungen](purchase-order-approval-confirmation.md)

[Überblick über Kreditorenrechnungen](../../financials/accounts-payable/vendor-invoices-overview.md)




