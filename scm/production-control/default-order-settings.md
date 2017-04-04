---
title: "Standardauftragseinstellungen für Dimensionen und Produktvarianten"
description: "Standardauftragseinstellungen definieren den Standort und Lagerort, aus dem Artikel bezogen oder in dem sie gelagert werden, die Mindest-, Höchst-, Mehrfach- und Standardmengen, die für den Handel oder die Lagerverwaltung verwendet werden, die Lieferzeiten, das Beendigungskennzeichen sowie die Auftragszusagemethode. Standardauftragseinstellungen werden verwendet, wenn Bestellungen, Aufträge, Umlagerungsaufträge, Bestandsjournale erstellt werden, sowie durch den Produktprogrammplan für die Generierung geplanter Aufträge. Standardauftragseinstellungen können artikelspezifisch, standortpsezifsch, produktvariantenspezfisch oder produktdimensionsspezifisch sein."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventItemOrderSetup
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 60abaa69debd891b2fe2dd98184c0dab50b0bf9f
ms.lasthandoff: 03/29/2017


---

# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Standardauftragseinstellungen für Dimensionen und Produktvarianten

Standardauftragseinstellungen definieren den Standort und Lagerort, aus dem Artikel bezogen oder in dem sie gelagert werden, die Mindest-, Höchst-, Mehrfach- und Standardmengen, die für den Handel oder die Lagerverwaltung verwendet werden, die Lieferzeiten, das Beendigungskennzeichen sowie die Auftragszusagemethode. Standardauftragseinstellungen werden verwendet, wenn Bestellungen, Aufträge, Umlagerungsaufträge, Bestandsjournale erstellt werden, sowie durch den Produktprogrammplan für die Generierung geplanter Aufträge. Standardauftragseinstellungen können artikelspezifisch, standortpsezifsch, produktvariantenspezfisch oder produktdimensionsspezifisch sein.

Sie können die Standardauftragseinstellungen auf der Seite **Standardauftragseinstellungen** definieren. Um diese Seite zu öffnen, wechseln ** Produktinformationsverwaltung ** ** &gt; Produkte ** ** &gt; freigegebene Produkte ** Sie wählen &gt; ein freigegebenes &gt; Produkt im ** Plan aus ** **** verwalten oder Bestand **** Aktivitätsbereich ** &gt; Auftragseinstellungen ** ** Standardauftragseinstellungen &gt; **.

## <a name="default-order-settings"></a>Standardauftragseinstellungen
Es gibt drei Typen von Standardauftragseinstellungen für Einkäufe, Verkäufe und den Bestand. Die Standardauftragseinstellungen für Einkäufe werden verwendet, wenn Folgendes erstellt wird:

-   Bestellpositionen
-   Rahmenbestellungspositionen
-   Angebotsanforderungspositionen
-   Bestellanforderungspositionen
-   Lieferungswiederbeschaffungspositionen
-   Geplante Einkaufsbestellungen

Die Standardauftragseinstellungen für Verkäufe werden verwendet, wenn Folgendes erstellt wird:

-   Auftragspositionen
-   Kaufvertragspositionen
-   Verkaufsangebotspositionen
-   Rücklieferungspositionen und Artikelersetzungspositionen
-   Bedarfsplanungspositionen

Die Standardauftragseinstellungen gelten auch beim Erstellen von:

-   Projektartikelanforderungen
-   Artikelbedarf für Serviceauftrag

Die Standardauftragseinstellungen für den Bestand werden verwendet, wenn Folgendes erstellt wird:

-   Lagererfassungen
-   Umlagerungsaufträge
-   Geplante Umlagerungsaufträge

Die Standardlagerauftragseinstellungen gelten auch beim Erstellen von:

-   Quarantäneaufträge
-   Qualitätsprüfungsaufträge
-   Produktionsaufträge
-   Stücklistenpositionen
-   Geplante Produktionsaufträge

## <a name="full-definition-of-a-released-product"></a>Vollständige Definition eines freigegebenen Produkts
Wenn Sie eine Buchung erstellen, müssen Sie die vollständigen Definition eines gemeinsamen Produkts auf der Position angeben bevor Dynamics 365, damit Arbeitsgangsversuche die Standardauftragseinstellungen identifizieren. Vollständige Definition des Produkts freigegebenen bedeutet, dass alle aktiven Artikelnummer und Produktdimensionen, beispielsweise Konfiguration, Größe, Farbe, Stil und für die Buchung angegeben werden. Wenn Sie beispielsweise manuell eine Bestellposition für eine freigegebene Produktvariante erstellen, müssen Sie alle erforderlichen Produktdimensionen angeben, bevor der Standort, Lagerort, die Menge sowie die Lieferzeit standardmäßig in der Auftragsposition angezeigt werden. 

Nicht alle Standardauftrags-Einstellungsparameter werden angewendet, wenn Auftrags- oder Erfassungspositionen erstellt werden. Mengen und Lieferzeiten Anzeigen nur standardmäßig an, nach. Wenn beispielsweise nur diese eine Erfassungsposition, der Standort und der Lagerort angezeigt wird standardmäßig zählen, wenn die Position erstellt wird. Offensichtlich wird ihnen kein Mengenden standardwert angenommen oder -Schecks auf mehrere und und ausgeführt, wenn die Position erstellt oder die Erfassung buchen. 

Das System versucht immer, einen Standardstandort und -lagerort zu finden, wenn eine Auftrags- oder Erfassungsposition erstellt wird Der Standort wird nicht immer standardmäßig von den Auftragseinstellungen angezeigt. Wenn Sie beispielsweise einen Auftrag oder eine Bestellung erstellen, wird der Standort aus dem Auftragskopf automatisch in den Auftragspositionen verwendet. Wird eine Stücklistenposition erstellt, wird der Standort aus dem Stücklistenkopf verwendet. Nachdem der Standort besteht, wird sie verwendet, um eine bestimmte Auftragseinstellungen des Standorts suchen, die als Standard für den Lagerort dann verwendet werden können. 

Der Standardauftragstyp, Einkauf und die Bestandslieferzeiten können die von Dispositionsregeln des Artikels auf der Artikeldeckung ** ** Seite überschrieben werden. Zwar werden die Standardauftragseinstellungen nicht die Unterscheidung zwischen der Produktion und der Übergangslieferzeit zulassen, lassen die Artikeldeckungsregeln sie zu. Allerdings werden die Artikeldeckungseinstellungen nur vom Nettobedarf verwendet, wenn geplante Produktions- und geplante Übertragungsaufträge erstellt werden, und sie werden nicht angewendet, wenn Produktions- und Übertragungsaufträge manuell erstellt werden. 

## <a name="default-order-settings-rules"></a>Standardmäßige Auftragseinstellungsregeln
Sie können allgemeine Standardauftragseinstellungen und jede Anzahl von Standardauftragseinstellungsregeln definieren, die nur unter bestimmten Umständen gelten, wie beispielsweise Standort oder eine spezifische Produktdimension oder Produktdimensionskombination. Sie können keine lagerortspezifischen Auftragseinstellungen definieren.

### <a name="rank-in-default-order-settings"></a>Nach standardmäßige Auftragseinstellungen einen Rang zuweisen

Die Standardauftrags-Einstellungsregeln haben Ränge. Je höher der Rang, desto wichtiger ist die Regel. Das bedeutet, dass sie eine höhere Priorität hat und vor den Regeln mit niedrigeren Rängen verwendet wird. Die allgemeinen Standardauftragseinstellungen haben den Rang null, der nicht geändert werden kann. Es kann nur eine Regel mit dem Rang null vorhanden sein. Regeln können denselben Rang haben, vorausgesetzt, dass die Dimensionen, die diese anwenden, um diese zu unterscheiden. Dies ist nützlich für die Modellierung von standordspezifischen Auftragseinstellungen. Wenn eine neue Standardauftrags-Einstellungsregel erstellt wird, werden die Werte für Auftragswerte, Beendigungskennzeichen usw. von der Regel mit Rang null geerbt, können aber überschrieben werden.

### <a name="default-order-settings-for-released-products"></a>Standardmäßige Auftragseinstellungen für freigegebene Produkte

Für eindeutig identifizierbare, freigegebene Produkte können Sie allgemeine Auftragseinstellungen oder standortspezifische Auftragseinstellungen definieren. Die allgemeinen Auftragseinstellungen haben immer den Rang null. Wenn Sie neue Verkaufs-, Einkaufs- und Lagerauftragseinstellungen zusammen zur gleichen Zeit einrichten, ist es zu empfehlen, dass Sie die **Detailansicht** auf der Seite **Standardauftragseinstellungen **verwenden. Wenn Sie zur Detailansicht wechseln, Gehe zum ** Optionen ** Aktivitätsbereich &gt; ** Seitenvorschubangaben ** &gt; ** Änderungsansicht ** ** &gt; Detailansicht **.

### <a name="site-specific-order-settings"></a>Standortspezifische Auftragseinstellungen

Um standortspezifische Auftragseinstellungen zu erstellen, klicken Sie auf **Neu**. ** In Detailansicht **, füllen Sie den Standort im ** die Einstellungen zu für ** &gt; ** Standort aus ** Feld. Füllen Sie in der **Rasteransicht** den Standort in der Spalte **Standort** aus. Die neue Regel ruft automatisch einen neuen Rangwert ab, der über null liegt. Sie so viele standortspezifische Regeln wie erforderlich erstellen und Sie können alle standortspezifischen Regeln demselben Rang zuweisen, um zu modellieren, dass sie gleich wichtig sind. 

Wenn Sie sich in der **Detailansicht** befinden, können Sie die Übersicht der Regeln nicht erhalten, die für den Artikel erstellt wurden. Schalten Sie die Schaltfläche **Liste anzeigen/ausblenden** ein und aus, um Übersichtsinformationen anzuzeigen. Wenn eine Auftragsposition eines beliebigen Typs erstellt und diese keinen Standort bereitstellen können, Dynamics 365 für Arbeitsgangssuchen für eine Regel ohne den Standort angegeben. Dies kann dazu beitragen, einen Standardstandort in der Auftragsposition verwendet. Dieser Standort wird dann verwendet, um nach einer standortspezifischen Regel zu suchen, bei der möglicherweise ein Standardlagerort festgelegt wurde. Dieser Lagerort wird auf die Auftragsposition angewendet.

### <a name="specific-order-settings-for-product-dimension"></a>Spezifische Auftragseinstellungen für Produktdimension

Sie können Auftragseinstellungsregeln für jede aktive Produktdimension oder Kombination aus aktiven Produktdimensionen definieren. Wenn ein Produktdimensionsfeld leer bleibt, dann gilt diese Regel für alle Werte der Produktdimension. 

Berücksichtigen Sie das folgende Beispielprodukt.

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Produktname**                                    | Photoelektrischer Sensor                    |
| **Item number**                                     | XW56                                    |
| **Konfiguration** (wird verwendet, um den Typ des Lichts zu modellieren) | C1-sichtbares rotes Licht, C2-Infrarotlicht |
| **Stil** (wird zum Modellieren der Techniküberarbeitung verwendet)  | R1, R2, R3                              |

Nehmen Sie für dieses Beispiel an, dass das Produkt beschafft und nicht produziert wird. Nehmen Sie außerdem an, dass die Konfiguration C1 häufiger verwendet wird, sodass es kürzere Lieferzeiten hat. 

Erstellen Sie folgende Standardauftragseinstellungen, um dieses Szenario zu modellieren.

| Rang | Standort | Variante | Formatvorlage | Einkauf – Standardeinstellungen überschreiben | Lieferzeit Einkauf | Einkauf – Angehalten | Vertrieb – Standardeinstellungen überschreiben | Vertrieb – Angehalten |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Wenn eine Bestellposition oder eine geplante Einkaufsbestellung für XW56, Konfiguration C1, erstellt wird, wird die Lieferzeit als 2 behandelt, unabhängig von der Überarbeitung oder dem Standort, wo die Position platziert wird. Nehmen Sie an, dass alle Überarbeitungen, außer R3, angehalten werden.

Sie können die folgenden standardmäßigen Auftragseinstellungsregeln erstellen.

| Rang | Standort | Variante | Formatvorlage | Einkauf – Standardeinstellungen überschreiben | Lieferzeit Einkauf | Einkauf – Angehalten | Vertrieb – Standardeinstellungen überschreiben | Vertrieb – Angehalten |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | R2    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 20   |      |               | R1    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Die zwei Regeln für die Beendigung der alten Überarbeitungen haben dieselbe Bewertung, was bedeutet, dass sie gleich wichtig sind. Alle beide haben einen höheren Rang als die Regel für Konfiguration C1, was bedeutet, dass sie den Vorrang vor der Regel für Konfiguration C1 haben. 

In diesem Beispiel wird die Anforderung für den Rang erklärt. Wenn eine Bestellung für Konfiguration C1 und Überprüfung R2 erstellt wird, wären bei fehlendem Rang die beiden Regeln, die für R2 und C1 definiert werden, mehrdeutig. Um die Mehrdeutigkeit aufzuheben, durchsucht Dynamics 365 for Operations die Regeln in absteigender Rangreihenfolge und wendet die erste anwendbare Regel an. Im aktuellen Beispiel, wenn eine Bestellposition für Konfiguration C1 und Überarbeitung R2 erstellt wird, erhält der Benutzer eine Warnmeldung, dass der Artikel gesperrt ist und dass dies durch den Überarbeitungswert verursacht wird. Wenn die Regel für die Konfiguration größer wäre, als diejenige für die Überarbeitung, dann wäre die Erstellung einer Bestellposition für Konfiguration C1 und Überarbeitung R2 erfolgreich gewesen, und der Benutzer hätte keine Meldung "Artikel gesperrt" erhalten. 

Berücksichtigen Sie die folgenden standardmäßigen Auftragseinstellungsregeln.

| Rang | Standort | Variante | Formatvorlage | Standardstandort | Standardlagerort | Einkauf – Standardmäßige Lagerdimensionen überschreiben | Lagerort für Einkauf |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Ja                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Das System reicht die Sätze von Regeln zweimal weiter, um den Standort und Lagerort zu bestimmen. Wenn eine Bestellposition für Variante C1, Stil R2, der Standort erstellt wird, wird auf Grundlage die Regel mit Rang 10. bestimmt. Dann sucht für eine Regel für Standort 2 um einen Lagerort bestimmen. Regel 20 wird gefunden und da sie einen höheren Rang hat, wird der Lagerort in der Bestellposition 22 und nicht 21 sein. 

Als allgemeiner Leitfaden erhalten spezifische Regeln und Regeln für Dimensionen, die wichtiger als andere Dimensionen sind, höhere Ränge, während generischere Regeln niedrigere Ränge erhalten. 

Die Regel mit Rang null dient als Sicherheitsnetz. Wenn keine anderen Regeln betroffen sind, dann werden die Standardauftragseinstellungen von Regel null verwendet. 

Da die Rangnummer so wichtig ist, befinden sich im Aktionsbereich **Standardauftragseinstellungen **Funktionen, um eine Regel nach oben oder unten zu verschieben und um die Regeln neu zu nummerieren, sodass sie immer in Abstufungen von 10 sind. 

Die Anzahl von Regeln, die für ein freigegebenes Produkt erstellt werden, sind möglicherweise viele. Um einen besseren Eindruck davon zu erhalten, was jede Regel überschreibt und warum es notwendig ist, empfehlen wir Ihnen, die **Rasteransicht** auf der Seite** Standardauftragseinstellungen** zu verwenden. Auf der Rasteransicht aktivieren, indem Sie z ** Optionen ** Aktivitätsbereich ** Seitenvorschubangaben &gt; ** ** Änderungsansicht &gt; fahren ** ** Rasteransicht &gt; **. Die Anzahl der im Raster angezeigten Spalten könnte ziemlich bedeutsam sein, insbesondere für die Registerkarten "Vertrieb" und "Bestand". Um die Anzahl einzuschränken im Raster angezeigt, können Gruppen von Spalten werden ausgeblendet oder angezeigt werden mithilfe der Schaltflächen auf der Spaltenanzeige ** Standardauftragseinstellungen ** ** verwendet &gt; ** Menü.

### <a name="specific-order-settings-for-released-product-variant"></a>Spezifische Auftragseinstellungen für freigegebene Produktvariante

Wenn das Regelsystem für Standardauftragseinstellungen zu lästig ist, dann gibt es die Option, einfach Standardauftragseinstellungen für jede Produktvariante zu definieren. In den folgenden Beispielen wird gezeigt, wie dies für das Produkt und die oben beschriebenen Fälle aussieht.

| Rang | Standort | Variante | Formatvorlage | Einkauf – Standardeinstellungen überschreiben | Lieferzeit Einkauf | Einkauf – Angehalten | Vertrieb – Standardeinstellungen überschreiben | Vertrieb – Angehalten |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | R3    | Ja                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | R2    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C2            | R1    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | R3    | Ja                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | R2    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | R1    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

In diesem Fall ist der Rang tatsächlich unerheblich, sodass Sie ihn ausblenden können. Diese Lösung führt möglicherweise zu einem Wartungsproblem. Möglicherweise empfiehlt es sich jedoch, diese Einstellung zu verwenden, wenn Sie in Erwägung ziehen, eine Integration mit Product Lifecycle Management (PLM)-Systemen vorzunehmen.

