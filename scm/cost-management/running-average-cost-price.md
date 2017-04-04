---
title: Laufender Durchschnittseinstandspreis
description: "Durch den Lagerabschluss von werden Abgangsbuchungen mit Zugangsbuchungen ausgeglichen, auf Grundlage hierfür bildet die Lagerbewertungsmethode, die in der Artikelmodellgruppe des Artikels ausgewählt ist. Vor der Lagerabschluss ausgeführt wird, berechnet das System einen laufenden Durchschnittseinstandspreises, der normalerweise verwendet wird, wenn Abgangsbuchungen gebucht werden."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-07 15 - 11 - 47
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 685dfaa877699db3c36cc1ea77d956461f8e68ec
ms.lasthandoff: 03/29/2017


---

# <a name="running-average-cost-price"></a>Laufender Durchschnittseinstandspreis

Durch den Lagerabschluss von werden Abgangsbuchungen mit Zugangsbuchungen ausgeglichen, auf Grundlage hierfür bildet die Lagerbewertungsmethode, die in der Artikelmodellgruppe des Artikels ausgewählt ist. Vor der Lagerabschluss ausgeführt wird, berechnet das System einen laufenden Durchschnittseinstandspreises, der normalerweise verwendet wird, wenn Abgangsbuchungen gebucht werden.

Die Systemschätzungen dieses laufenden Durchschnittseinstandspreises für einen Artikel mithilfe der folgenden Formel: Vorkalkulierter Preis = (physischer Betrag + wertmäßiger Betrag) ÷ (physische Menge + wertmäßige Menge)

## <a name="using-the-running-average-cost-price"></a>Verwendung des laufenden Durchschnittseinstandspreises
Die folgenden Tabellenshows, wenn das System Lagerbuchungen an, indem den laufenden Durchschnittseinstandspreis verwendet, und wenn der Einstandspreis verwendet, der im Masterartikeldatensatz stattdessen definiert wird.

| Bedingung                                               | Das System verwendet den vorkalkulierten laufenden Durchschnittseinstandspreis | Das System verwendet den Einstandspreis, der aus dem Artikelmaster definiert wurde |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| \* ist der Zähler als auch Nenner positiv\*\*.  | Ja                                                      | Nr.                                                                |
| Zähler,\*Nenner\*\*oder beide sind negativ. | Nr.                                                       | Ja                                                               |
| Der \*und\* ist 0 (null).                        | Nr.                                                       | Ja                                                               |

\* Zähler = (physischer Betrag + wertmäßiger Betrag) Nenner \*\* (physische Menge + wertmäßige Menge) ** Hinweis: ** Wenn die ** zum Einbeziehen des physischen Wertes ein ** Option für einen Artikel nicht aktiviert, verwendet das System 0 (null) für den physischen Betrag und die physische Menge. Informationen zu dieser Option, finden Sie unter [Physischen Wert einbeziehen](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Preisverstärkung vermeiden
In seltenen Fällen tritt die System-Preise mehrere Probleme, bevor es genügend Zugänge hat, um Preis basieren soll. Dieses Szenario kann dazu führen, dass Vorkalkulationen des laufenden Durchschnittseinstandspreises , zu hoch werden. Diese Preisverstärkung lässt sich jedoch durch bestimmte Maßnahmen vermeiden oder zumindest abschwächen. **Szenario** Die folgenden Buchungen treten bei einem Artikel auf, für den Sie die Option **Physischen Wert einbeziehen** ausgewählt haben:

1.  Sie erhalten wertmäßig die Menge von 100 zu jeweils EUR 100,00.
2.  Sie geben wertmäßig eine Menge von 200 ab.
3.  Sie erhalten physikalisch eine Menge von 101 zu jeweils EUR 202,00.

Beim Betrachten des vorkalkulierten laufenden Durchschnittseinstandspreises für den Artikel haben Sie einen Einstandspreis von EUR 1,51 erwartet. Stattdessen finden Sie ein vorkalkulierter laufender Durchschnitt von EUR 102,00, die auf Basis der folgenden Formel entspricht: Vorkalkulierter Preis = \[202 + (- 100)\] ÷ \[101 + (- 100)\] = 102 ÷ 1 = 102 Preiskalkulationsverstärkung diese tritt auf, da, wenn 200 Artikel (Schritt 2) werden, das System 100 Preis der Artikel muss, bevor er allen entsprechenden Zugänge zur Verfügung stehen. Diese Situation verursacht negativen Bestand. Die Vorkalkulationen des Systems anschließend ein Einheitenpreis von EUR 1,00 übrig, wie Sie möglicherweise erwarteten. Wenn der entsprechende Zugang von 100 Stück erfolgt, besitzen diese einen Einheitenpreis von EUR 2.00. **Hinweis:** Obwohl sich durch die Abgänge ein negativer Bestand ergibt, ist der Bestand zum Zeitpunkt der Abgangspreisberechnung positiv. Aus diesem Grund wird anstelle des Preises aus dem Artikelmaster der laufende Durchschnittseinstandspreis verwendet. An diesem Punkt liegt in das System, der ein Lagerwertversatz von EUR 100,00 vor. Obwohl sich dieser Versatz für 100 Stück mit einem Versatz pro Einheit von EUR 1,00 kumuliert, enthält der Bestand jedoch nur noch ein Stück. Daher wird der Versatz von EUR 100,00 diesem einzelnen Stück zugeordnet. Daraus ergibt sich eine zu hohe Vorkalkulation des Einstandspreises. **Hinweis:** Wären die Schritte 2 und 3 des Szenarios vertauscht, würden 200 Artikel zu einem Einheitenpreis von EUR 1,51 ausgegeben, und ein Stück bliebe mit einem Einheitenpreis von EUR 1,51 übrig. Da diese Preisverstärkung auftreten kann, wenn negativer Bestand vorhanden ist, ist sie in den folgenden Fällen nur schwer vermeidbar:

-   Abgangspreise für Wert und Menge des verfügbaren Bestands müssen vorkalkuliert werden.
-   Sie müssen den Wert und die Menge der Ab- und Zugänge des verfügbaren Bestands regulieren.
-   Ihr Geschäftsmodell ermöglicht den Versand oder die Preisbildung für mehr Stücke als vorhanden sind.
-   Sie müssen alle an Sie übermittelten Zugangswerte und -mengen annehmen.

Sollten die folgenden Methoden im Rahmen des Geschäftsmodells zulässig sein, können sie dazu beitragen, negative Mengen zu vermeiden, die ansonsten eine Preisverstärkung begünstigen:

-   Wenn Sie die Option **Physischen Wert einbeziehen** für einen Artikel auswählen, müssen Sie das Kontrollkästchen **Physischer negativer Bestand** auf der Seite **Artikelmodellgruppen** deaktivieren.
-   Wenn Sie *nicht* die Option **Physischen Wert einbeziehen** für einen Artikel auswählen, müssen Sie das Kontrollkästchen **Wertmäßig negativer Bestand** auf der Seite **Artikelmodellgruppen** deaktivieren.

Bedenken Sie ausserdem, dass der maximale Versatz des physischen Lagerwerts durch die Anzahl der physischen Buchungen, sowie durch die Differenz zwischen physischen und wertmäßigen Preisen begrenzt wird. Vorausgesetzt, dass alle physischen Buchungen letzten Endes wertmäßig aktualisiert werden, kann der physische Wert keinen extrem hohen Wert erreichen. Beachten Sie, dass der Verstärkungseffekt sich deutlich abschwächt , wenn sich der kumulierte Versatz nicht auf einen verfügbaren Artikel beschränkt, sondern sich auf mehrere Artikel verteilt.

