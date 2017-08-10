---
title: Spesenverwaltungsparameter
description: Die folgenden Parameter steuern das Verhalten in der Spesenverwaltung.
author: knelson
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 5fd3a821719a3b4180cfcd4f26d0007accecee39
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="expense-management-parameters"></a>Spesenverwaltungsparameter
-----------------------------

Die Parameter steuern das allgemeine Verhalten in der Spesenverwaltung.

### <a name="general"></a>Allgemein

| **Feld**                                                | **Beschreibung**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standardsatz für gefahrene Kilometer**                             | Geben Sie die Erstattung für Spesen für gefahrene Kilometer ein. Der Satz wird mit der auf dem Spesenformular eingetragenen Kilometerleistung multipliziert, um den für die Reisespesen erstatteten Betrag zu berechnen.                       |
|**Persönliche Ausgaben**                             | Wählen Sie aus, wer für Kreditkartentransaktionsbeträge verantwortlich ist, die als persönlich eingeordnet werden.                                                                                                     |
|**Gesamten detaillierten Spesenbericht anzeigen**               | Wählen Sie diese Option, um alle Spesen für einen Spesenbericht anzuzeigen, um die Details des Originaldokuments für einen bestimmten Beleg anzuzeigen, der bei der Buchung des Spesenberichts erzeugt wurde.              |
|**Reisen müssen zwingend vorab genehmigt werden**                 | Wählen Sie diese Option, um zu fordern, dass vor der Vorlage eines Spesenberichts durch einen Mitarbeiter eine Reiseanforderung vorgelegt und genehmigt werden muss.                                                                    |
|**Bearbeitung von Aufteilungen vor der Buchung zulassen**            | Wählen Sie aus, ob die Aufteilungen eines Spesenberichts vor der Buchung bearbeitet werden können.                                                                                                                 |
|**Spesenverwaltungsrichtlinien auswerten**                     | Wählen Sie dies aus, wenn Spesen ausgewertet werden, um festzustellen, ob eine Spesenrichtlinie verletzt wurde. Spesen können auf Verletzungen überprüft werden, wenn der Speseneintrag eingegeben und gespeichert wird, oder wenn der Spesenantrag zur Genehmigung vorgelegt wird. Die Richtlinien für erforderliche Belege werden beim Speichern der Spesenposition überprüft.                   |
|**Zwischenbetriebliche Spesenpositionen zulassen**                         | Wählen Sie hiermit aus, ob der Eintrag von Spesen für andere juristische Entitäten in einem Spesenbericht zulässig ist.                                                                                                          |
|**Bearbeitung des Wechselkurses für Kreditkartenausgaben zulassen** | Wählen Sie diese Option, um dem Benutzer zu gestatten, den Wechselkurs für importierte Kreditkartenausgaben zu bearbeiten.                                                                        |
|**Anzeige mehrstufiger Hierarchiefelder**                  | Wählen Sie aus, welche Genehmigerfelder angezeigt werden sollen, wenn der Zuweisungstyp für den Workflow des Spesenberichts auf Hierarchie gesetzt ist, und die Hierarchie die mehrstufige Genehmigungshierarchie für Spesen verwenden soll. Wenn die mehrstufige Genehmigungshierarchie für den Workflow verwendet wird, werden die ausgewählten Felder angezeigt und können im Spesenbericht bearbeitet werden. |
|**Eingabe der Kreditkartennummer des Mitarbeiters (Update vom Juli 2017)**     | Wählen Sie aus, ob eine 15- oder 16-stellige Nummer eingegeben und im Feld **Karten-ID** der Seite **Kreditkarten** für einen Mitarbeiter gespeichert werden kann.                                                                          |

### <a name="financial"></a>Kosten

| **Feld**                                                            | **Beschreibung**     |
|----------------------------------------------------------------------|------------------------------------|
|**Tagesjournalname des Sachkontos**                                         | Wählen Sie den Namen des Sachkontenjournals, auf das die genehmigten Spesenberichte gebucht werden.            |
|**Steuererstattung für Spesen aktivieren**                                  | Wählen Sie diese Option, um eine Steuererstattung bei dafür in Frage kommenden Spesen zu aktivieren. Diese Option kann nicht aktiviert werden, wenn US-Umsatzsteuer- und Gebrauchssteuerregeln aktiviert sind.      |
|**Barvorschüsse unmittelbar buchen**                                     | Wählen Sie diese Option um einen genehmigten Barvorschuss zu buchen, wenn der Prozess für die Zahlung und den Transfer abgeschlossen ist. Wenn diese Option nicht gewählt ist, erzeugt der Prozess für die Zahlung und den Transfer einen nicht gebuchten allgemeinen Journaleintrag. |
|**Korrektur des Buchungsdatums während der Buchung**                             | Wählen Sie diese Option, um das Buchungsdatum zu aktualisieren, wenn Sie Spesen buchen und der aktuelle Zeitraum zurückgestellt oder geschlossen ist. Das Buchungsdatum wird auf den nächsten offenen Zeitraum gesetzt.   |
|**Gruppierung von Transaktionen basierend auf einem in der Zahlungsmethode angegebenen Verrechnungskonto zulassen**      | Wählen Sie diese Option, um die Spesentransaktionen für einen Spesenbericht zusammenzufassen, basierend auf einem in der Zahlungsmethode für die Spesen angegebenen Verrechnungskonto.   
|**Steuern enthalten**                                                   | Wählen Sie diese Option aus, um standardmäßig die Umsatzsteuer in den Spesenbetrag aufzunehmen.             |
|**Freigabe von Belastungen beim Abschluss von Reiseanforderungen**            | Wählen Sie diese Option, um belastete Geldmittel freizugeben, wenn eine genehmigte Reiseanforderung abgeschlossen wird.                                                                                   |
|**Zulassen der Vorlage einer Reiseanforderung bei Budgetüberschreitung des Budgetregisters oder des Projektbudgets** | Wählen Sie diese Option, um Mitarbeitern zu erlauben, Reiseanforderungen zur Genehmigung vorzulegen, die entweder das zulässige Budget überschreiten, das im Budgetregister eingerichtet ist, oder das für ein Projekt zugelassene Budget.            |
|**Zulassen der Vorlage einer Spesenberichts bei Budgetüberschreitung des Budgetregisters oder des Projektbudgets**    | Wählen Sie diese Option, um Mitarbeitern zu erlauben, Spesenberichte zur Genehmigung vorzulegen, die entweder das zulässige Budget überschreiten, das im Budgetregister eingerichtet ist, oder das für ein Projekt zugelassene Budget.                |
|**Zulassen der Spesenberichtsgenehmigung bei Budgetüberschreitung nur des Budgetregisters**                | Wählen Sie diese Option, um Genehmigern zu gestatten, Spesenberichte zu genehmigen, die das zulässige Budget überschreiten, das im Budgetregister eingerichtet ist.                                                                       |

### <a name="per-diem"></a>Tagessatz

| **Feld**                             | **Beschreibung**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Mindeststunden für pro Tag**           | Geben Sie die Mindeststunden ein, die ein Mitarbeiter pro Tag arbeiten muss, um Reisespesen pro Tag erhalten zu können.                                                                                      |
|**Prozentwert für Mahlzeiten**                          | Geben Sie den Standardprozentwert pro Tag für Mahlzeiten ein, der am ersten und am letzten Tag der Reisespesen verwendet wird, wenn das Feld **Mahlzeitenabzug berechnen nach** auf **Mahlzeitentyp pro Tag** oder **Anzahl der Mahlzeiten pro Tag** gesetzt ist. Der Arbeitstag am ersten und letzten Tag der Periode kann kürzer als ein normaler Arbeitstag sein. Daher kann der Betrag des Tagessatzes an diesen Tagen vom Standardbetrag abweichen. Ist der Prozentwert gleich 0, ist der Abzug für den ersten und letzten Tag gleich 0,00. |
|**Prozentwert für das Hotel**                        | Geben Sie den Standardprozentsatz pro Tag für Hotels an, der für den ersten und letzten Tag der Reisespesen angewendet wird. Der Arbeitstag am ersten und letzten Tag der Periode kann kürzer als ein normaler Arbeitstag sein. Daher kann der Betrag des Tagessatzes an diesen Tagen vom Standardbetrag abweichen. Ist der Prozentwert gleich 0, ist der Abzug für den ersten und letzten Tag gleich 0,00.                                              |
|**Andere Prozentwerte**                        | Geben Sie den Standardprozentsatz pro Tag für verschiedene Spesen an, der für den ersten und letzten Tag der Reisespesen angewendet wird. Der Arbeitstag am ersten und letzten Tag der Periode kann kürzer als ein normaler Arbeitstag sein. Daher kann der Betrag des Tagessatzes an diesen Tagen vom Standardbetrag abweichen. Ist der Prozentwert gleich 0, ist der Abzug für den ersten und letzten Tag gleich 0,00.                                                                                                     |
|**Abzug für Frühstück in Prozent** | Geben Sie hier den Betrag ein, um den der Tagessatz für das Frühstück verringert wird. Erhält ein Mitarbeiter beispielsweise zusätzlich ein Frühstück, wollen Sie möglicherweise den Betrag pro Tag um 10 Prozent verringern.                               |
|**Abzug für Mittagessen in Prozent**    | Geben Sie hier den Betrag ein, um den der Tagessatz für das Mittagessen verringert wird. Erhält ein Mitarbeiter beispielsweise zusätzlich ein Mittagessen, wollen Sie möglicherweise den Betrag pro Tag um 15 Prozent verringern.                                       |
|**Abzug für Abendessen in Prozent**   | Geben Sie hier den Betrag ein, um den der Tagessatz für das Abendessen verringert wird. Erhält ein Mitarbeiter beispielsweise zusätzlich ein Abendessen, wollen Sie möglicherweise den Betrag pro Tag um 25 Prozent verringern.                                     |
|**Berechnung des Mahlzeitenabzugs nach**         | Wählen Sie aus, wie das System den Mahlzeitenabzug pro Tag berechnen soll, indem Sie auswählen, ob der Abzug auf dem Mahlzeitentyp pro Reise oder pro Tag basiert, oder ob der Abzug auf der Anzahl der pro Tag zulässigen Mahlzeiten basiert.|
|**Rundungen pro Tag**                  | Wählen Sie die Art der Rundung, die für Spesen pro Tag verwendet wird. Wenn sie eine normale Rundung auswählen, werden alle Spesen pro Tag mit einem Betrag von 0,50 auf 1,00 aufgerundet, und alle Spesen pro Tag mit einem Betrag von weniger als 0,50 auf 0,00 abgerundet.                                                                                              |
|**Berechnung pro Tag basierend auf**         | Wählen Sie aus, ob ein Betrag pro Tag auf einem Kalendertag oder einem 24-Stunden-Zeitraum basiert.       |

### <a name="fax-cover-pages"></a>Faxdeckblätter

| **Feld**                      | **Beschreibung**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Anweisungen**                   | Geben Sie die Anweisungen ein, die ein Mitarbeiter für die Erstellung eines Deckblatts für ein Fax einhalten muss, mit dem er Belege für einen Spesenbericht sendet. Klicken Sie auf die Schaltfläche **Übersetzungen**, um sprachspezifischen Text einzugeben, der abhängig von der Sprache des Benutzers angezeigt wird. |
|**Benutzer-ID (Barcodeinformation)** | Wählen Sie diese Option aus, um die eindeutige ID eines Mitarbeiters im Barcode auf dem Deckblatt des Fax zu speichern.                 |
|**Strichcode**                      | Wählen Sie hier den Strichcode aus, der auf dem Faxdeckblatt verwendet wird. Die Spesenverwaltung unterstützt die Barcodes 39 und 128.               |

### <a name="anti-corruption"></a>Anti-Korruption

| **Feld**                             | **Beschreibung**      |
|---------------------------------------|------------------------------------------------------------------------|
|**Anzeige einer Antikorruptionsbescheinigung**   | Wählen Sie diese Option aus, um beim Erstellen eines neuen Spesenberichts den Antikorruptionstext anzuzeigen. Bestimmte Spesenkategorien können dann aktiviert werden, für die eine Antikorruptionsbescheinigung auf dem Spesenbericht ausgewählt werden muss. Beispielsweise kann eine Geschenkekategorie für Spesen für einen Regierungsbeamten fordern, dass der Mitarbeiter bestätigt, dass die Spesen den Unternehmensrichtlinien im Hinblick auf Regierungsbeamte entsprechen. |
|**Antikorruptionsmitteilung für den Antragsteller** | Geben Sie den Text ein, der dem Mitarbeiter angezeigt wird, wenn er einen neuen Spesenbericht erstellt. Klicken Sie auf die Schaltfläche **Übersetzungen**, um sprachspezifischen Text einzugeben, der abhängig von der Sprache des Benutzers angezeigt wird.         |
|**Antikorruptionsmitteilung für Genehmiger**  | Geben Sie den Text ein, der dem Genehmiger angezeigt wird, wenn er einen neuen Spesenbericht erstellt. Klicken Sie auf die Schaltfläche **Übersetzungen**, um sprachspezifischen Text einzugeben, der abhängig von der Sprache des Benutzers angezeigt wird.        |
