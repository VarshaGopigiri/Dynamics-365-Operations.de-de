---
title: "Produktbezogene Übersetzungen FAQ"
description: "In diesem Thema wird beschrieben, wie Übersetzungen für Produkte, Produktdimensionswerte und Produktattribute verwaltet werden."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a9c991a5afaebd10b8812dfc1d67120ed4ebdfd2
ms.lasthandoff: 03/31/2017


---

# <a name="product-related-translations-faq"></a>Produktbezogene Übersetzungen FAQ

In diesem Thema wird beschrieben, wie Übersetzungen für Produkte, Produktdimensionswerte und Produktattribute verwaltet werden. 

<a name="what-product-related-data-can-be-translated"></a>Welche produktbezogenen Daten können übersetzt werden?
--------------------------------------------

Sie können Übersetzungen für folgende produktbezogene Informationen erstellen:
-   Namen und Beschreibungen von Produkten.
-   Beschreibungen, Anzeigenamen und Hilfetext von Produktattributwerten.
-   Namen und Beschreibungen von Produktdimensionswerten.

Sie können die produktbezogenen Informationen in jede Sprache übersetzen, die auf der Seite **Textübersetzung** verfügbar ist. Weitere Informationen finden Sie im Abschnitt **Wie erstelle ich Übersetzungen für produktbezogene Informationen**.

## <a name="where-can-i-view-the-translated-information"></a>Wo kann ich die übersetzten Informationen anzeigen lassen?
Sie können Übersetzungen von produktbezogenen Informationen in jedem externen Quelldokument anzeigen, beispielsweise in einer Rechnung, falls es in einer Sprache verfasst ist, für die Übersetzungen verfügbar sind.

## <a name="how-do-i-create-translations-for-productrelated-information"></a>Wie erstelle ich Informationen zu Übersetzungen productrelated?
Gehen Sie folgendermaßen vor, um Übersetzungen für ein Produkt zu erstellen:
1.  Produktinformationsverwaltung auf ** ** ** &gt; Common ** ** &gt; freigegebene Produkte **.
2.  Wählen Sie ein Produkt, und klicken Sie im Aktivitätsbereich in der Gruppe, ** ** Sprachen auf aus ** Übersetzungen **.
3.  Wählen Sie auf der Seite **Textübersetzung** im Feld **Sprache** die Sprache aus. Um weitere Sprachen hinzugefügt, erweitern Sie das ** Sprache ** Feld, und klicken Sie anschließend auf OK ** **.
4.  Geben Sie in der Gruppe **Übersetzter Text** im Feld **Beschreibung** und **Produktname** die Übersetzungen ein.

Gehen Sie folgendermaßen vor, um Übersetzungen für Produktattribute zu erstellen:
1.  Produktinformationsverwaltung auf ** ** ** &gt; Common ** ** &gt; freigegebene Produkte **.
2.  Unter **Einstellungen** klicken Sie auf **Attribute** und klicken dann auf **Attribute**.
3.  Auf der Seite **Attribute** klicken Sie auf **Übersetzen**.
4.  Wählen Sie auf der Seite **Textübersetzung** im Feld **Sprache** die Sprache aus. Um weitere Sprachen hinzugefügt, erweitern Sie das ** Sprache ** Feld, und klicken Sie anschließend auf OK ** **.
5.  Geben Sie in der Gruppe **Übersetzter Text** im Feld **Beschreibung**, **Produktname** und **Hilfetext** die Übersetzungen ein.

Gehen Sie folgendermaßen vor, um Übersetzungen für Produktdimensionswerte zu erstellen:
1.  Produktinformationsverwaltung auf ** ** ** &gt; Common ** ** &gt; freigegebene Produkte **.
2.  Wählen Sie eine Produkt und klicken dann auf **Produktdimension**.
3.  Wählen Sie einen der Links für die Produktdimensionen aus: **Konfigurationen****Größen**, **Farben** oder **Stil**.
4.  Wählen Sie einen Dimensionswert aus, und klicken Sie anschließend auf **Übersetzen**.
5.  Wählen Sie auf der Seite **Textübersetzung** im Feld **Sprache** die Sprache aus. Um weitere Sprachen hinzugefügt, erweitern Sie das ** Sprache ** Feld, und klicken Sie anschließend auf OK ** **.
6.  In der ** übersetzter Text ** Gruppe geben Sie Übersetzungen auf ** ** ** Name und Beschreibung ** die Felder ein.

## <a name="can-the-names-of-product-variants-be-translated"></a>Können die Namen von Produktvarianten übersetzt werden?
Produktvarianten basieren auf den Dimensionen eines freigegebenen Produkts. Produktvariantennamen basieren auf einer Kombination von Dimensionswerten. Wenn die Dimensionswerte, die einer Produktvariante zugeordnet sind, übersetzt werden, wird der Name der Produktvariante in der übersetzten Version angezeigt.  

**Beispiel**  

Ihr Produkt ist ein T-Shirt, das in verschiedene Größen und Farben erhältlich ist, und die verschiedenen Namen basieren auf den folgenden Details:
-   Produktnummer: \#3
-   Dimensionen: Größe und Farbe
-   Größendimensionswerte: Klein, mittel, groß
-   Farbdimensionswerte: Rot, grün, schwarz

Der Name eine Produktvariante, die auf Basis der Dimensionswerte darstellt, und die auszugleichende sind \#ist rot ** 3: Klein: Rot **.  

Ein Debitor möchte mehrere kleinere, rote T-Shirts kaufen und der Name des T-Shirts muss auf Französisch in der Rechnung angezeigt werden. Dimensionswerte, die Sie übersetzen und klein, in französisch und in den Namen der \#** Produktvariante ist rot: 3Klein: Rouge **.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tip</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Um die bevorzugte Sprache eines Debitors festzulegen, führen Sie folgende Schritte aus:
<ol>  
<li>Klicken <strong>Vertrieb und Marketing</strong> &gt; <strong>Gemeinsam</strong> &gt; <strong>Debitoren</strong> &gt; <strong>Alle</strong><strong>Debitoren</strong> Sie auf.</li>
<li>Doppelklicken Sie auf ein Debitorenkonto, um die Seite <strong>Debitor</strong> zu öffnen. Wählen Sie auf der Registerkarte <strong>Allgemeines</strong> im Feld <strong>Sprache</strong> die gewünschte <strong>Sprache</strong> aus.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Was passiert, wenn ein Debitor eine bevorzugte Sprache hat, für die keine Übersetzungen verfügbar sind?
Wenn Übersetzungen nicht in der bevorzugten Sprache des Debitors verfügbar sind, werden die Namen und Beschreibungen in der globalen Sprache des eigenen Unternehmens angezeigt.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Kann ich Übersetzungen für eine Reihe von Dimensionswerten gleichzeitig verwalten?
Dimensionswerte sind produktspezifisch und Sie können die Übersetzungen für die Dimensionswerte für jedes Produkt verwalten. Wenn Sie jedoch eine Dimensionswertgruppe erstellen und Übersetzungen für die Werte in der Wertsgruppe erstellen, erleichtert dies, die Übersetzungen zu verwalten.   

**Example**  

Das Unternehmen produziert T-Shirts in verschiedenen Formaten, jedes Format ist in den Größen Klein, Mittel und Groß verfügbar. Die Größen werden in einer Dimensionswertgruppe gesammelt. Wenn ein neues T-Shirt Format hinzugefügt wird, können Sie es der Dimensionswertgruppe zuordnen, die für Größen verwendet wird, sodass alle Größen für das Produkt verfügbar sind. Sie können auchÜbersetzungen für die Größen in der Dimensionswertgruppe jederzeit hinzufügen oder ändern.  

Ein Dimensionswert, der einem Produkt eine Dimensionsvariantnegruppe zugeordnet ist, muss vom Produktvariantengruppe verwaltet werden.   
Gehen Sie folgendermaßen vor, um eine Dimensionswertgruppe zu erstellen.
1.  Produktinformationsverwaltung auf ** ** ** &gt; Einstellungen ** ** &gt; Variantengruppen **.
2.  Wählen Sie **Größe** **Gruppen**, **Farbgruppen**, oder **Stilgruppen**.
3.  ** Der auf neu ** und geben Sie einen Namen für die Gruppe in der Größe ** ** ** Gruppe ein ** ** **, Farbgruppe oder Stilgruppe ** ** Feld. Klicken Sie auf **Größen**, **Farben**, oder **Stil**, um Positionen für die Gruppen zu erstellen.
4.  In der Größe ** ** ** Gruppe ** Positionen, ** Farbe ** ** Gruppe ** ** Positionen oder Stilgruppenpositionen ** ** ** Seite, der auf ** neu ** und erstellen Sie dann die Größen, Farben und Stile die für Gruppen.

Um Übersetzungen für Werte in einer Dimensionswertgruppe zu verwalten, führen Sie diese Schritte aus:
1.  Führen Sie die Schritte des vorherigen Verfahrens zum Erstellen einer Dimensionswertgruppe, aus, um die Seite **Größengruppenpositionen** **Farbgruppenpositionen** oder **Positionen von Stilgruppen** zu öffnen.
2.  Klicken Sie auf **Textübersetzung**. In der Textübersetzung ** ** Seite der ** übersetzter Text ** Gruppe, geben Sie Übersetzungen auf ** ** ** Name und Beschreibung ** die Felder ein.

## <a name="when-can-translations-of-productrelated-information-be-managed"></a>Wann können Übersetzungen von Informationen productrelated verwaltet werden?
Übersetzungen von produktbezogenen Informationen können jederzeit verwaltet werden. Wenn Übersetzungen für einen Dimensionswert aktualisiert werden, der einem Produkt zugeordnet ist, werden die Produktdaten aktualisiert, unabhängig davon, ob das Produkt Transaktionen hat.



