---
title: Verbesserungen der Auszugsbuchung
description: In diesem Thema wird beschrieben, welche Verbesserungen der Auszugsbuchungsfunktion vorgenommen wurden.
author: josaw1
manager: AnnBe
ms.date: 04/26/2016
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: anpurush
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 86b301833f3655f7172e2d38ddca4239be71760c
ms.openlocfilehash: bcb4af426e5967643a1c438bb19495576ce51b63
ms.contentlocale: de-de
ms.lasthandoff: 04/26/2018

---

# <a name="improvements-to-statement-posting"></a>Verbesserungen der Auszugsbuchung

[!include[banner](includes/banner.md)]

In diesem Thema wird beschrieben, welche Verbesserungen der Auszugsbuchungsfunktion vorgenommen wurden. Diese Verbesserungen sind in Microsoft Dynamics 365 for Finance and Operations 7.3.2 verfügbar.

## <a name="activation"></a>Aktivieren

Standardmäßig ist das Programm beim Deployment von Finance and Operations 7.3.2 so eingestellt, dass es das Legacy-Feature für Kontoauszugsbuchungen verwendet. Um die verbesserte Auszugsbuchung zu aktivieren, müssen Sie den Konfigurationsschlüssel dafür einschalten.

- Gehen Sie zu **Systemverwaltung** \> **Einstellungen** \> **Lizenzkonfiguration**, und deaktivieren Sie dann unter den Knoten **Einzelhandel** das Kontrollkästchen **Einzelhandelsaufstellungen (Vorversion)** und das Kontrollkästchen **Einzelhandelsaufstellungen**.

Wenn der neue Konfigurationsschlüssel **Einzelhandelsaufstellungen** eingeschaltet ist, steht ein neuer Menüpunkt mit dem Namen **Einzelhandelsaufstellungen** zur Verfügung. Mit diesem Menüeintrag können Sie Auszüge manuell erstellen, berechnen und buchen. Jede Auszug, der bei der Verwendung des Stapelbuchungsprozesses einen Fehler verursacht, ist ebenfalls über diesen Menüeintrag verfügbar. (Wenn der neue Konfigurationsschlüssel **Einzelhandelsaufstellungen (Vorversion)** eingeschaltet ist, steht ein neuer Menüpunkt mit dem Namen **Offene Aufstellungen** zur Verfügung.)

Finance and Operations umfasst die folgenden Validierungen, die sich auf diese Konfigurationsschlüssel beziehen:

- Beide Konfigurationsschlüssel können nicht gleichzeitig eingeschaltet werden.
- Für alle Operationen, die während des Lebenszyklus einer Anweisung durchgeführt werden (Anlegen, Berechnen, Löschen, Buchen usw.), müssen dieselben Konfigurationsschlüssel verwendet werden. Beispielsweise können Sie keine Anweisung erstellen und berechnen, während die **Einzelhandelsaufstellungen (Vorversion)** Konfigurationsschlüssel eingeschaltet ist, und dann versuchen, die gleiche Anweisung zu posten, während die **Einzelhandelsauszug** Konfigurationsschlüssel eingeschaltet ist.

> [!NOTE]
> Wir empfehlen die Verwendung des Konfigurationsschlüssels **Einzelhandelsauszug** für die verbesserte Auszugsbuchung, es sei denn, Sie haben zwingende Gründe, stattdessen den Konfigurationsschlüssel **Einzelhandelsaufstellungen (Vorversion)** zu verwenden. Microsoft wird weiterhin in die neue und verbesserte Funktion zur Kontoauszugsbuchung investieren, und es ist wichtig, dass Sie so schnell wie möglich darauf umsteigen, um davon zu profitieren. Die Funktion zur Verbuchung von Vorversion-Auszägen wird in einem zukünftigen Release veraltet sein.

## <a name="setup"></a>Einrichten

Als Teil der Verbesserungen der Auszugsbuchungsfunktion wurden drei neue Parameter auf dem Inforegister **Aufstellung** auf der Registerkarte **Buchung** der Seite **Einzelhandelsparameter** eingeführt:

- **Klare Aufstellung deaktivieren** – Diese Option ist nur für die Vorversions-Auszugsbuchungsfunktion anwendbar. Wir empfehlen, diese Option auf **Nein** zu setzen, um zu verhindern, dass Benutzer Clearing-Anweisungen, die sich in einem halbgebuchten Zustand befinden, löschen. Wenn Anweisungen, die sich in einem halbgebuchten Zustand befinden, gelöscht werden, werden die Daten beschädigt. Sie sollten diese Option nur in Ausnahmefällen auf **Ja** setzen.
- **Bestand bei der Berechnung reservieren** – Es empfiehlt sich, dass Sie den **Lager buchen**-Stapelverarbeitungsauftrag für die Lagerreservierung verwenden und Sie die Option auf **Nein** setzen. Wenn diese Option auf **Nein** gesetzt ist, versucht die verbesserte Auszugsbuchungsfunktion nicht, Bestandsreservierungseinträge zum Zeitpunkt der Berechnung zu erstellen (wenn die Einträge nicht bereits über den Batch-Job **Bestandsbuchung** erstellt wurden). Stattdessen erzeugt die Funktion Bestandsreservierungseinträge nur zum Zeitpunkt der Buchung. Diese Implementierung war eine Designwahl und basierte auf der Tatsache, dass das Zeitfenster zwischen dem Berechnungsvorgang und dem Buchungsvorgang typischerweise klein ist. Wenn Sie jedoch den Bestand zum Zeitpunkt der Berechnung reservieren möchten, können Sie diese Option auf **Ja** setzen.

    Die Funktion zur Verbuchung von Vorversion-Auszügen reserviert den Bestand immer während der Auszugsberechnung (wenn die Reservierung nicht bereits über den Batch-Job **Lager buchen** durchgeführt wurde), unabhängig von der Einstellung dieser Option.

- **Deaktivieren der Zählung erforderlich** - Wenn diese Option auf **Ja** gesetzt ist, wird der Buchungsprozess für eine Auszug fortgesetzt, auch wenn die Differenz zwischen dem gezählten Betrag und dem Transaktionsbetrag auf dem Auszug außerhalb der Schwelle liegt, die auf der FastTab **Inforegister**für Einzelhandelsgeschäfte definiert ist.

Zusätzlich wurde das Feld **Maximale Anzahl paralleler Auszugsbuchungen** auf dem Inforegister **Stapelverarbeitung** eingeführt. Dieses Feld definiert die Anzahl der Stapelaufgaben, die gleichzeitig ausgeführt werden sollen. Derzeit müssen Sie den Wert dieses Feldes manuell setzen.

Beachten Sie, daß alle Einstellungen und Parameter, die sich auf Auszugsbuchungen beziehen und die für Einzelhandelsgeschäfte und auf der Seite **Einzelhandelsparameter** definiert sind, auf die verbesserte Auszugsbuchung anwendbar sind.

## <a name="processing"></a>Bearbeitung
Auszüge können über die Menüpunkte **Auszüge im Stapel berechnen** und **Auszüge im Stapel buchen** berechnet und gebucht werden. Alternativ können die Auszüge auch manuell berechnet und gebucht werden, indem Sie den Menüpunkt **Einzelhandelsauszüge** verwenden, den die verbesserte Auszugsbuchung bietet.

Der Ablauf und die Schritte für die Berechnung und Buchung von Auszügen in einem Stapel sind derselbe wie in der Funktion zum Buchen von Altauszügen. Allerdings wurden wesentliche Verbesserungen in der Kern-Backend-Verarbeitung der Auszüge vorgenommen. Diese Verbesserungen machen den Prozess widerstandsfähiger und sorgen für eine bessere Einsicht in die Zustände und Fehlerinformationen. So kann der Benutzer die Fehlerursache beheben und den Buchungsprozess fortsetzen, ohne dass es zu Datenbeschädigungen kommt und ohne dass Datenkorrekturen erforderlich sind.

In den folgenden Abschnitten werden einige der wichtigsten Verbesserungen für die Funktion der Auszugsbuchung beschrieben, die in der Benutzungsoberfläche für Einzelhandelsauszüge und gebuchte Auszüge erscheinen.

### <a name="status-details"></a>Statusdetails
In der Auszugsbuchungsroutine wurde ein neues Zustandsmodell über die Berechnungs- und Buchungsprozesse hinweg eingeführt.

Die folgende Tabelle beschreibt die verschiedenen Zustände und deren Reihenfolge bei der Berechnung.

| Statusreihenfolge | Zustand      | Beschreibung |
|-------------|------------|-------------|
| 1           | Gestartet    | Der Auszug wurde erstellt und ist bereit zur Berechnung. |
| 2           | Markiert     | Die Transaktionen, die in den Umfang des Auszugs fallen, werden anhand der Auszugsparameter identifiziert und mit der Auszugs-ID gekennzeichnet. |
| 3           | Berechnet | Die Auszugspositionen sind berechnet und angezeigt. |

Die folgende Tabelle beschreibt die verschiedenen Zustände und deren Reihenfolge während des Buchungsvorgangs.

| Statusreihenfolge | Zustand                   | Beschreibung |
|-------------|-------------------------|-------------|
| 1           | Geprüft                 | Es werden mehrere Validierungen durchgeführt, die sich auf Parameter (z.B. die Dispositionsgebühr) und auf die Auszugs- und Auszugspositionen (z.B. die Differenz zwischen dem gezählten Betrag und dem Transaktionsbetrag) beziehen. |
| 2           | Zusammengeführt              | Verkaufstransaktionen für benannte und unbenannte Kunden werden anhand der Konfiguration aggregiert. Jede aggregierte Transaktion wird schließlich in einen Auftrag umgesetzt. |
| 3           | Debitorenauftrag erstellt  | Abhängig von der aggretierten Transaktion werden Aufträge im System erstellt. |
| 4           | Debitorenauftrag fakturiert | Aufträge sind fakturiert. |
| 5           | Rabatte gebucht        | Abhängig von der Konfiguration werden periodische Rabatterfassungen gebucht. |
| 6           | Erträge/Aufwendungen gebucht   | Erträge/Aufwendungen werden als Belege gebucht. |
| 7           | Belege verknüpft         | Zahlungsjournale werden erstellt und mit der entsprechenden Rechnung verknüpft. |
| 8           | Zahlungen gebucht         | Zahlungsjournale werden gebucht. |
| 9           | Geschenkkarten gebucht       | Geschenkkartentransaktionen werden als Gutscheine gebucht. |
| 10          | Veröffentlicht                  | Der Auszug wird als gebucht gekennzeichnet. |

Jeder Zustand in den vorhergehenden Tabellen ist unabhängig und es wird eine hierarchische Abhängigkeit zwischen den Statusarten aufgebaut. Diese Abhängigkeit fließt von oben nach unten. Wenn das System während der Verarbeitung eines Zustands auf Fehler stößt, wird der Status des Auszugs auf den vorherigen Zustand zurückgesetzt. Jeder nachfolgende Wiederholungsversuch des Prozesses setzt sich aus dem gescheiterten Zustand fort und geht weiter. Dieser Ansatz hat folgende Vorteile:

- Der Benutzer hat vollständige Einsicht in den Zustand, in dem der Fehler aufgetreten ist.
- Datenkorruption wird vermieden. So gab es z. B. bei der Verbuchung von Legacy-Auszügen Situationen, in denen einige Debitorenaufträge fakturiert, andere aber offen gelassen wurden. Es gab auch Fälle, in denen einige Zahlungsjournale keine entsprechende Rechnung zu begleichen hatten, weil die Rechnungsbuchung fehlerhaft war.
- Benutzer können den aktuellen Status eines Auszugs mit der Schaltfläche **Statusdetails** in der Gruppe **Ausführungsdetails** des Auszugs sehen. Die Status-Detailseite besteht aus drei Abschnitten:

    - Der erste Abschnitt zeigt den aktuellen Status des Auszugs zusammen mit dem Fehlercode und einer detaillierten Fehlermeldung, falls ein Fehler aufgetreten ist.
    - Der zweite Abschnitt zeigt die verschiedenen Zustände des Berechnungsprozesses. Visuelle Hinweise zeigen Zustände an, die erfolgreich ausgeführt wurden, Zustände, die aufgrund von Fehlern nicht ausgeführt werden konnten, und Zustände, die noch nicht ausgeführt wurden.
    - Der dritte Abschnitt zeigt die verschiedenen Zustände des Buchungsprozesses. Visuelle Hinweise zeigen Zustände an, die erfolgreich ausgeführt wurden, Zustände, die aufgrund von Fehlern nicht ausgeführt werden konnten, und Zustände, die noch nicht ausgeführt wurden.

Zusätzlich zeigt die Kopfzeile des zweiten und dritten Abschnitts den Gesamtstatus des jeweiligen Prozesses an.

### <a name="event-logs"></a>Ereignisprotokolle
Ein Auszug durchläuft mehrere Operationen (z.B. Anlegen, Berechnen, Löschen und Buchen), wobei mehrere Instanzen desselben Vorgangs während des Lebenszyklus des Auszugs aufgerufen werden können. Beispielsweise kann ein Benutzer nach der Erstellung und Berechnung eines Auszugs den Auszug löschen und neu berechnen. Die Schaltfläche **Ereignisprotokolle** in der Gruppe **Ausführungsdetails** der Anweisung bietet einen vollständigen Audit-Trail der verschiedenen Operationen, die auf einer Anweisung aufgerufen wurden, zusammen mit Informationen darüber, wann diese Operationen aufgerufen wurden.

### <a name="aggregated-transactions"></a>Zusammengeführte Transaktionen
Während des Buchungsvorgangs werden die Verkaufsbuchungen gemäß den Einstellungen zusammengefasst. Diese aggregierten Transaktionen werden im System gespeichert und zum Anlegen von Debitorenaufträgen verwendet. Jede aggregierte Transaktion erzeugt einen entsprechenden Debitorenauftrag im System. Sie können die aggregierten Transaktionen über die Schaltfläche **Zusammengeführte Transaktionen** in der Gruppe **Ausführungsdetails** des Auszugs anzeigen.

Die Registerkarte **Debitorenauftragsdetail** einer aggregierten Transaktion zeigt die folgenden Informationen an:

- **Datensatz-ID** - Die ID der aggregierten Transaktion.
- **Auszugsnumber** - Der Auszug, zu dem die aggregierte Transaktion gehört.
- **Datum** - Das Datum, an dem die aggregierte Transaktion angelegt wurde.
- **Verkaufskennung** - Beim Anlegen eines Debitorenauftrags aus der aggregierten Transaktion wird die Debitorenauftrags-ID angezeigt. Wenn dieses Feld leer ist, wurde der entsprechende Debitorenauftrag nicht angelegt.
- **Anzahl aggregierter Positionen** - Gesamtzahl der Zeilen für den aggregierten Vorgang und Debitorenauftrag.
- **Status** - Der letzte Status der aggregierten Transaktion.
- **Rechnungskennung** - Wenn der Debitorenauftrag für den aggregierten Vorgang fakturiert wird, wird die Verkaufsrechnungs-ID angezeigt. Wenn dieses Feld leer ist, wurde die Rechnung für den Debitorenauftrag nicht gebucht.

Die Registerkarte **Transaktionsdetails** einer aggregierten Transaktion zeigt alle Einzelhandelstransaktionen, die in die aggregierte Transaktion gezogen wurden. Die aggregierten Zeilen der aggregierten Transaktion zeigen alle aggregierten Datensätze der Einzelhandelstransaktionen. Die aggregierten Positionen zeigen auch Details wie Artikel, Variante, Menge, Preis, Nettobetrag, Einheit und Lager. Grundsätzlich entspricht jede aggregierte Zeile einer Auftragszeile.

Von der Seite **Aggregierte Transaktionen** können Sie das XML für eine bestimmte aggregierte Transaktion über die Schaltfläche **Auftrags-XML exportieren** herunterladen. Sie können das XML verwenden, um Probleme zu debuggen, die das Anlegen und Buchen von Aufträgen betreffen. Laden Sie einfach das XML herunter, laden Sie es in eine Testumgebung hoch und debuggen Sie das Problem in der Testumgebung. Die Funktionalität zum Herunterladen des XML für aggregierte Transaktionen steht für gebuchte Auszüge nicht zur Verfügung.

Die aggregierte Transaktionssicht bietet folgende Vorteile:

- Der Benutzer hat Einblick in die aggregierten Transaktionen, die bei der Debitorenauftragserstellung fehlgeschlagen sind, und die Debitorenaufträge, die bei der Fakturierung fehlgeschlagen sind.
- Der Benutzer hat Transparenz darüber, wie Transaktionen aggregiert werden.
- Der Benutzer verfügt über ein vollständiges Protokoll, das von den Einzelhandelstransaktionen über die Aufträge bis hin zu den Verkaufsrechnungen reicht. Diese Historie war in der Funktion zum Buchen von Legacy-Auszügen nicht verfügbar.
- Eine aggregierte XML-Datei erleichtert die Identifizierung von Problemen bei der Auftragserstellung und Fakturierung.

### <a name="journal-vouchers"></a>Erfassungsbelege
Die Schaltfläche **Erfassungsbelege** in der Gruppe **Ausführungsdetails** des Auszugs zeigt alle verschiedenen Belegtransaktionen, die für einen Auszug erstellt werden und die sich auf Rabatte, Einnahmen-/Ausgabenkonten, Geschenkkarten usw. beziehen.

Derzeit zeigt das Programm diese Daten nur für gebuchte Auszüge an.

### <a name="payment-journals"></a>Zahlungserfassungen
Die Schaltfläche **Zahlungserfassungen** in der Gruppe **Ausführungsdetails** des Auszugs zeigt alle verschiedenen Zahlungsjournale, die zu einem Auszug erstellt werden.

Derzeit zeigt das Programm diese Daten nur für gebuchte Auszüge an.

## <a name="other-improvements"></a>Weitere Verbesserungen

Weitere Backend-Verbesserungen, die der Benutzer sehen kann, wurden an der Auszugsbuchung vorgenommen. Nachfolgend finden Sie einige Beispiele:

- Die Aggregation berücksichtigt nicht die Personal-, Terminal- und Schicht-Einheiten. Da es weniger Aggregationsparameter gibt, müssen weniger Auftragszeilen bearbeitet werden.
- Das Auftreten von Deadlocks auf Retail-Transaktionstabellen wird durch die Einführung zusätzlicher Erweiterungstabellen und durch Einfügeoperationen anstelle von Aktualisierungsoperationen auf den Retail-Transaktionstabellen reduziert.
- Die Anzahl der laufenden Stapelaufgaben wurde parametrisiert und begrenzt. Daher kann diese Zahl speziell auf die Umgebung des Kunden abgestimmt werden. In der Funktion zum Buchen von Legacy-Auszügen wurde eine unbegrenzte Anzahl von Stapelaufgaben gleichzeitig angelegt. Die Folge waren unüberschaubare Lasten, Overhead und Engpässe auf dem Batch-Server.
- Anweisungen werden effizient zur Verarbeitung in die Warteschlange gestellt, indem die Anweisungen mit der maximalen Anzahl von Transaktionen priorisiert werden.
- Stapelprozesse wie z. B. **Aufstellungen in Charge berechnen** und **Aufstellungen in Charge buchen** werden nur im Stapelbetrieb ausgeführt. In der Funktion zum Buchen von Legacy-Auszügen können Benutzer diese Stapelprozesse in einem interaktiven Modus ausführen, der im Gegensatz zu Stapelprozessen mit mehreren Threads nur ein Thread ist.
- In der Funktion zum Buchen von Legacy-Auszügen führt jeder Ausfall einer Stapelaufgabe dazu, dass der gesamte Stapeljob in einen Fehlerzustand versetzt wird. In der verbesserten Funktion wird der Stapelauftrag nicht in einen Fehlerzustand versetzt, wenn andere Stapelaufträge erfolgreich abgeschlossen werden. Sie sollten den Buchungsstatus für einen Stapelausführungslauf anhand der Seite **Einzelhandelsaufstellungen** beurteilen, auf der Sie alle Auszüge sehen können, die aufgrund von Fehlern nicht gebucht wurden.
- In der Funktion zum Buchen von Legacy-Auszügen führt das erste Auftreten eines Auszugsfehlers zum Ausfall des gesamten Stapels. Die restlichen Auszüge werden nicht verarbeitet. In der verbesserten Funktion verarbeitet der Stapelprozess weiterhin alle Auszüge, auch wenn einige der Auszüge fehlschlagen. Ein Vorteil ist, dass der Anwender die genaue Anzahl der fehlerhaften Auszüge einsehen kann. Daher müssen die Benutzer nicht in einer kontinuierlichen Schleife der Fehlerbehebung und des Buchungsanweisungsprozesses stecken bleiben, bis alle Auszüge gebucht sind.

## <a name="general-guidance-about-the-statement-posting-process"></a>Allgemeine Hinweise zum Ablauf der Auszugsbuchung

- Wir empfehlen, den Prozess der Auszugsbuchung im Stapel laufen zu lassen, da Batchläufe die Vorteile des Batch-Frameworks im Sinne von Multithreading nutzen. Multithreading ist erforderlich, um die großen Transaktionsvolumina zu bewältigen, die normalerweise bei Auszugsbuchungen anfallen.
- Wir empfehlen Ihnen, die negative Inventur auf der Artikelmodellgruppe einzuschalten, um eine reibungslose Buchung zu ermöglichen. In einigen Szenarien können negative Auszüge nur dann gebucht werden, wenn eine negative Inventur vorliegt. Wenn sich beispielsweise theoretisch nur eine Einheit eines Artikels im Bestand befindet und ein Verkaufsvorgang und ein Rückgabevorgang für den Artikel stattgefunden haben, sollte der Vorgang auch dann gebucht werden können, wenn der negative Bestand nicht aktiviert ist. Da der Prozess der Auszugsbuchung jedoch sowohl den Verkaufsvorgang als auch den Retourenvorgang in einem einzigen Auftrag zieht, gibt es keine Garantie dafür, dass die Verkaufsposition zuerst gebucht wird, gefolgt von der Retourenposition. Daher können Fehler auftreten. Wenn in diesem Szenario der negative Bestand eingeschaltet ist, wird die Transaktionsbuchung nicht negativ beeinflusst, und das System spiegelt den Bestand korrekt wider.
- Wir empfehlen, bei der Berechnung und Buchung von Auszügen die Aggregation zu verwenden. Daher werden für einige der Aggregationsparameter die folgenden Einstellungen empfohlen:

    - Klicken Sie auf **Einzelhandel** \> **Zentralverwaltungseinrichtun** \> **Parameter** \> **Einzelhandelsparamete**. Stellen Sie anschließend auf der Registerkarte **Buchung**, auf dem Inforegister **Lageraktualisierung**, auf dem Feld **Detailebene**, wählen Sie **Zusammenfassung** aus.
    - Klicken Sie auf **Einzelhandel** \> **Zentralverwaltungseinrichtun** \> **Parameter** \> **Einzelhandelsparamete**. Stellen Sie anschließend auf der Registerkarte **Buchung**, auf dem Inforegister **Aggregation**, Satz **Belegbuchungen** die Option **Ja**.

