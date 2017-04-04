---
title: "Mehrwertsteuersätze auf Grundlage die Berechnungsgrundlage und Berechnungsmethoden die"
description: In diesem Artikel wird beschrieben, wie die Werte in den Feldern &quot;Berechnungsgrundlage und Berechnungsmethode&quot; den Steuersatz in Verkaufs- und Einkaufsbuchungstransaktionen bestimmen.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ad731401fe553cdc50665cc87aaac64dc48813f2
ms.lasthandoff: 03/31/2017


---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a>Mehrwertsteuersätze auf Grundlage die Berechnungsgrundlage und Berechnungsmethoden die

In diesem Artikel wird beschrieben, wie die Werte in den Feldern "Berechnungsgrundlage und Berechnungsmethode" den Steuersatz in Verkaufs- und Einkaufsbuchungstransaktionen bestimmen.

Die Berechnungsgrundlage im Berechnungs-Inforegister auf der Mehrwertsteuercodeseite bestimmt, welcher Betrag verwendet wird, um den/die entsprechenden Steuersatz/‑sätze auf der Seite Mehrwertsteuercodewerte auszuwählen. Der Betragstyp im Feld "Berechnungsgrundlage" in Kombination mit der Methode im Feld Berechnungsmethode bestimmt die Logik, um den richtigen Steuersatz für eine Buchung zu finden. 

Aus unterschiedlichen Kombinationen von Werten in diesen Feldern ergeben sich verschiedene Mehrwertsteuerberechnungen, wie aus den folgenden Beispielen ersichtlich. In den Beispielen werden die gleichen Steuerintervallwerte verwendet, die für jeden Steuercode auf der Seite Mehrwertsteuercodewerte eingerichtet werden. Um diese Seite zu öffnen, klicken Sie auf Mehrwertsteuercode- Darstellungen in der Mehrwertsteuercodeseite.

> [!Important]                                                                                                                  
> Wenn die Berechnungsgrundlage für mindestens einen der Mehrwertsteuercodes auf Positionen oder Einheiten basiert, muss der Wert des Feldes Berechnungsmethode auf der Seite Hauptbuchparameter auf Position festgelegt werden. |

## <a name="net-amount-per-line"></a>Nettobetrag pro Position
Wählen Sie diese Option, um die Mehrwertsteuer auf der Grundlage des Nettobetrags für die Rechnungspositionen ausschließlich sonstiger Steuern zu bestimmen.

### <a name="example"></a>Beispiel

Für die Mehrwertsteuersätze sind die unten stehenden Intervalle eingerichtet.

| Betragsintervall    | Steuersatz |
|--------------------|----------|
| 0 bis 50             | 30 %      |
| 50 bis 100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

> [!NOTE]                                                                                                             
> Die Null (0) für das obere Limit im letzten Intervall bedeutet, dass alle Beträge über 100 in das Intervall eingeschlossen werden.

" Begrenzte Basis: ** ** Nettobetrag pro Position 

Berechnungsmethode: ** Intervall ** 

Sie kaufen 8 Lampen für jeweils 25,00 Euro. 

Der Nettobetrag der Rechnungsposition ist 200,00. 

Die Steuer wird folgendermaßen berechnet: 

Mehrwertsteuer gesamt = 50 x 30 % + 50 x 20 % + 100 x 10 % = 15 + 10 + 10 = 35,00. 

Rechnungsgesamtbetrag = 200,00 + 35,00 = 235,00. 

**Variation** 

Wenn die Rechnung zwei Positionen mit vier Artikeln in jeder Position ist, beträgt der Nettobetrag auf jeder Position 100,00 und die Mehrwertsteuer wird folgendermaßen berechnet, wie folgt: 

Mehrwertsteuerposition 1 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00. 

Mehrwertsteuerposition 2 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00. 

Mehrwertsteuer gesamt = 25,00 + 25,00 = 50,00 

Rechnungsgesamtbetrag = 200,00 + 50,00 = 250,00.

## <a name="net-amount-per-unit"></a> Nettobetrag pro Einheit
Wählen Sie diese Option aus, um die Mehrwertsteuer auf der Grundlage des Werts jeder Einheit ausschließlich sonstiger Steuern zu bestimmen. Wenn eine stückbasierte Berechnungsgrundlage ausgewählt wird, muss auch eine Einheit für den Mehrwertsteuercode angegeben werden.

### <a name="example"></a>Beispiel

Für die Mehrwertsteuersätze sind die unten stehenden Intervalle eingerichtet.

| Betrag             | Steuersatz |
|--------------------|----------|
| 0 bis 50             | 30 %      |
| 50 bis 100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

" Begrenzte Basis: ** ** Nettobetrag pro Einheit 

Berechnungsmethode: ** ** " Gesamtbetrag 

Sie kaufen 8 Lampen für jeweils 25,00 Euro. 

Der Nettobetrag der Rechnungsposition ist 200,00. 

Die Steuer wird berechnet, wie folgt: Mehrwertsteuer pro Einheit = 25,00 x 30 % = 7,50 Euro; Gesamtumsatzsteuer = 7,50 x 8 Einheiten = 60,00 Euro; Rechnungsgesamtbetrag = 200,00 + 60,00 = 260,00 Euro

## <a name="net-amount-of-invoice-balance"></a> Nettobetrag des Rechnungssaldos

Wählen Sie diese Option, um die Mehrwertsteuer auf der Grundlage des Gesamtwerts der Rechnung ausschließlich sonstiger Steuern zu bestimmen.

### <a name="example"></a>Beispiel

Für die Mehrwertsteuersätze sind die unten stehenden Intervalle eingerichtet.

| Betrag            | Steuersatz |
|-------------------|----------|
| 0 bis 50            | 30 %      |
| 50 bis 100          | 20 %      |
| 100 -0 (&gt; 100) | 10 %      |

" Begrenzte Basis: ** Nettobetrag des Rechnungssaldos ** 

Berechnungsmethode: ** Intervall ** eine Verkaufsrechnung besitzt 2 Positionen mit 4 Lampen auf jedem Positionen für 25,00. Der Nettobetrag des Rechnungssaldos ist 4 x 25,00 + 4 x 25,00 = 200,00 Euro. Die Steuer wird berechnet, wie folgt: Gesamtumsatzsteuer = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Euro; Rechnungsgesamtbetrag = 200,00 + 35,00 = 235,00 Euro

## <a name="gross-amount-per-line"></a> Bruttobetrag pro Position

Wählen Sie diese Option, um die Mehrwertsteuer auf der Grundlage des Positionswerts einschließlich aller sonstigen Steuern für diese Position zu bestimmen.

> [!NOTE]
> In einer Mehrwertsteuergruppe darf nur ein Mehrwertsteuercode mit dieser Auswahl im Feld Berechnungsgrundlage vorliegen.

### <a name="example"></a>Beispiel

Für die Mehrwertsteuersätze sind die unten stehenden Intervalle eingerichtet.

| Betrag             | Steuersatz |
|--------------------|----------|
| 0 bis 50             | 30 %      |
| 50 bis 100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

Begrenzte Basis: **Bruttobetrag pro Position** Berechnungsmethode: **Intervall** Darüber hinaus gibt es einen weiteren Steuercode, der für eine spezielle Abgabe von 5,00 Euro auf jede Lampe berechnet wird. Die Abgabe wird vor der Berechnung der Mehrwertsteuer zum Nettobetrag hinzuaddiert. Sie kaufen 8 Lampen für jeweils 25,00 Euro. Der Nettobetrag der Rechnungsposition ist 200,00. Der Bruttobetrag für die Rechnungsposition ist 8 x 25,00 + 8 x 5,00 = 240,00 Euro. Die Steuer wird folgendermaßen berechnet, wie folgt: Mehrwertsteuer gesamt = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Gesamtabgabe = 5,00 x 8 = 40,00 Rechnungsgesamtbetrag = 200,00 + 39,00 + 40,00 = 279,00

**Variation** 

Wenn die Rechnung erstellt wird, indem 2 Rechnungspositionen mit 4 Artikeln in jeder Position verwendet, beträgt der Nettobetrag pro Rechnungsposition 100,00. Der Bruttobetrag (einschließlich Abgaben von 4 x 5,00 Euro) pro Rechnungsposition wäre 120,00 Euro, und die Mehrwertsteuer wird erstellt, wie folgt: Mehrwertsteuerrechnungsposition 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Euro; Mehrwertsteuerrechnungsposition 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Euro; Gesamtumsatzsteuer = 27,00 + 27,00 = 54,00 Euro; gesamte Abgabe = 5,00 x 8 = 40,00 Euro; Rechnungsgesamtbetrag = 200,00 + 54,00 + 40,00 = 294,00 Euro

## <a name="gross-amount-per-unit"></a> Bruttobetrag pro Einheit

Wählen Sie diese Option aus, um die Mehrwertsteuer auf der Grundlage des Werts der Einheit einschließlich sonstiger Steuern zu bestimmen.

> [!NOTE]
> In einer Mehrwertsteuergruppe darf nur ein Mehrwertsteuercode mit dieser Auswahl im Feld Berechnungsgrundlage vorliegen.

### <a name="example"></a>Beispiel

Für die Mehrwertsteuersätze sind die unten stehenden Intervalle eingerichtet.

| Betrag             | Steuersatz |
|--------------------|----------|
| 0 bis 50             | 30 %      |
| 50 bis 100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

Berechnungsgrundlage: **Bruttobetrag pro Einheit** Es gibt eine spezielle Abgabe von 5,00 Euro auf jede Lampe. Die Abgabe wird vor der Berechnung der Mehrwertsteuer zum Nettobetrag hinzuaddiert. Sie kaufen 8 Lampen für jeweils 25,00 Euro. Der Bruttobetrag pro Einheit ist 30,00. Die Steuer wird berechnet, wie folgt: Umsatzsteuer pro Einheit = 30 x 30 % = 9,00 Euro; Gesamtumsatzsteuer = 9,00 x 8 = 72,00 Euro; Gesamtabgabe = 5,00 x 8 = 40,00 Euro; Gesamtrechnungsbetrag = 200,00 + 72,00 + 40,00 = 312,00 Euro

## <a name="invoice-total-incl-other-sales-tax-amounts"></a> Rechnungssumme einschließlich sonstiger Mehrwertsteuerbeträge

Wählen Sie diese Option, um die Mehrwertsteuer auf der Grundlage des Gesamtwerts der Rechnung einschließlich sonstiger Steuern zu bestimmen.
> [!NOTE]
> In einer Mehrwertsteuergruppe darf Sie einen Mehrwertsteuercode mit dieser Auswahl im Berechnungsgrundlagenfeld niedrigen Feld nur dreimal

### <a name="example"></a>Beispiel

Für die Mehrwertsteuersätze sind die unten stehenden Intervalle eingerichtet.

| Betrag             | Steuersatz |
|--------------------|----------|
| 0 bis 50             | 30 %      |
| 50 bis 100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

" Begrenzte Basis: ** Rechnungssumme einschließlich sonstiger Mehrwertsteuerbeträge ** Berechnungsmethode: ** Intervall **   
Für jede Lampe gilt eine spezielle Abgabe von 5,00. Die Abgabe wird vor der Berechnung der Mehrwertsteuer zum Nettobetrag hinzuaddiert. Sie kaufen 8 Lampen für jeweils 25,00 Euro. Der Nettobetrag der Rechnung ist 200,00. Der Bruttobetrag der Rechnung ist 200,00 + (8 x 5,00) = 240,00. Die Steuer wird berechnet, wie folgt: Gesamtumsatzsteuer = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Euro; gesamte Abgabe = 5,00 x 8 = 40,00 Euro; Rechnungsgesamtbetrag = 200,00 + 39,00 + 40,00 = 279,00 Euro

Weitere Informationen finden Sie [Optionen Gesamtbetrag und der berechnung Intervall für Mehrwertsteuercodes "whole-amount-interval-options-sales-tax-codes.md)] und [Mehrwertsteuer-Berechnungsmethoden im Feld "Ursprung" sales-tax-calculation-methods-origin-field.md] ().

