---
title: "Berechnungen für Produktkonfigurationsmodelle FAQ"
description: "In diesem Artikel wird beschrieben Berechnungen für Produktkonfigurationsmodelle und es wird beschrieben, wie Sie Berechnungen zusammen mit Einschränkungen verwendet."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: 3a82fdb8532c79e33c167c43554a3de7d3061fcb
ms.lasthandoff: 03/31/2017


---

# <a name="calculations-for-product-configuration-models-faq"></a>Berechnungen für Produktkonfigurationsmodelle FAQ

In diesem Artikel wird beschrieben Berechnungen für Produktkonfigurationsmodelle und es wird beschrieben, wie Sie Berechnungen zusammen mit Einschränkungen verwendet.

Berechnungen können für Arithmetik oder logische Operationen verwendet werden. Sie ergänzen Ausdruckseinschränkungen in Produktkonfigurationsmodellen. Sie können Berechnungen auf der Seite **Details zum einschränkungsbasierten Produktkonfigurationsmodell** definieren und Ausdrücke für Berechnungen im Ausdrucks-Editor dann aufbauen. Weitere Informationen finden Sie unter Berechnungen erstellen.

## <a name="what-is-a-calculation"></a>Was ist eine Berechnung?
Eine Berechnung ist ein Element, das Sie in einem Produktkonfigurationsmodell verwenden können. Berechnungen ergänzen Einschränkungen, indem Sie Ihnen ermöglichen, Werte mithilfe von Dezimalzahlen zu berechnen, wenn Sie ein Produkt konfigurieren. Darüber hinaus verfügen Berechnungen über einen größeren Satz von Operatoren als bei Einschränkungen.  

Wie eine Einschränkung ist eine Berechnung mit einer bestimmten Komponente in einem Produktkonfigurationsmodell verbunden und kann nicht von einer anderen Komponente wiederverwendet werden oder mit einer solchen geteilt werden. Ein wichtiger Unterschied zwischen Berechnungen und Einschränkungen ist, dass Berechnungen imperativ (unidirektional) sind, während Einschränkungen deklarativ sind (bidirektional). Weitere Informationen zu Einschränkungen finden Sie unter [Ausdruckseinschränkungen und Tabelleneinschränkungen](expression-constraints-table-constraints-product-configuration-models.md).  

Eine Berechnung besteht aus einem Zielattribut und einem Berechnungsausdruck.

## <a name="what-is-a-target-attribute"></a>Was ist ein Zielattribut?
Ein Zielattribut ist ein Attribut, das das Berechnungsergebnis in einem Ausdruck erhält.  

Im folgenden Ausdruck ist das Zielattribut eine Tischdeckenmessung:  

** Ausdruck: ** Wenn \[decimalAttribute1 &lt;= decimalAttribute2, True, falsches\]  

** DecimalAttribute1 ** ist und die Tabellenlänge ** decimalAttribute2 ** ist die Tischdeckenlänge. Der Ausdruck gibt dem Zielattribut den Wert **Wahr** zurück, wenn **decimalAttribute2** größer oder gleich **decimalAttribute1** ist. Andernfalls gibt der Ausdruck den Wert **Falsch** zurück. Daher ist die Tischdeckenabmessung akzeptabel, wenn die Tischdeckenlänge gleich oder größer als die Länge des Tisches ist.

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a>Welche Attributtypen können für Attribute festgelegt werden?
Alle Attributtypen, die der Variantenkonfigurator unterstützt, können für Attribute festgelegt werden, mit Ausnahme von Text ohne eine feste Liste.

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a>Kann der Wert eines Zielattributs die Werte der Eingabeattribute in einer Berechnung einschränken?
Nein, der Wert eines Zielattributs kann die Werte der Eingabeattribute in einer Berechnung nicht einschränken, da Berechnungen unidirektional sind. Daher wird der Wert des Zielattributs auf Grundlage von Wertänderungen bei den Eingabeattributen festgelegt, aber eine Änderung des Werts des Ziels wirkt sich nicht auf den Wert der Eingabeattribute aus. Dieses Verhalten unterscheidet sich vom Verhalten für Einschränkungen. Einschränkungen treten in beiden Richtungen auf.

### <a name="example"></a>Beispiel

Im folgenden Ausdruck ist das Ziel zur Berechnung die Länge eines Netzanschlusskabels, und der Eingabewert ist eine Farbe:  

** Ausdruck: ** \[wenn "Farbe == Grün" 1,5, 1,0,\]  

Wenn Sie den Artikel konfigurieren, wird die Länge des Netzanschlusskabels auf festgelegt ** 1,5 ** wenn Sie ** Grün ** als der Wert des attributs Farben angeben. Wenn Sie eine andere Farbe angeben, ist die Länge **1,0**. Da jedoch Berechnungen unidirektional sind, legt die Berechnung den Wert des Farbenattributs nicht auf **Grün** fest, wenn Sie eine Länge von **1,5** angeben.

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a>Was passiert, wenn eine Berechnung ein Zielattribut vom Typ "Ganzzahl" aufweist, eine Berechnung aber eine Dezimalzahl generiert?
Wenn ein Zielattribut vom Typ Ganzzahl ist, jedoch eine Berechnung eine Dezimalzahl erzeugt, wird nur der ganzzahlige Teil des berechneten Ergebnisses zurückgegeben. Der Dezimalteil wird entfernt, und das Ergebnis wird nicht gerundet. So wird beispielsweise das Ergebnis 12,70 als 12 angezeigt.

## <a name="when-do-calculations-occur"></a>Wann treten Berechnungen auf?
Berechnungen treten auf, wenn ein Wert für alle Eingabeattribute bereitgestellt wurde.

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a>Kann ich den Wert überschreiben, der für das Zielattribut berechnet wird?
Sie können den Wert überschreiben, der für das Zielattribut berechnet wird, es sei denn, das Zielattribut ist als ausgeblendet oder schreibgeschützt festgelegt.

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-readonly"></a>Wie werden ich ein Zielattribut fest, z ausgeblendet oder schreibgeschützt?
Um ein Attribut als ausgeblendet oder schreibgeschützt festzulegen, führen Sie folgende Schritte aus.

1.  Produktinformationsverwaltung auf ** ** ** &gt; Common ** ** &gt; Produktkonfigurationsmodelle **.
2.  Wählen Sie ein Produktkonfigurationsmodell aus, und klicken Sie im Aktivitätsbereich auf **Bearbeiten**.
3.  Wählen Sie auf der Seite **Details zum einschränkungsbasierten Produktkonfigurationsmodell** das Attribut aus, das als Zielattribut verwendet werden soll.
4.  Wählen Sie auf dem Inforegister **Attribute** entweder **Ausgeblendet** oder **Schreibgeschützt** aus.

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a>Kann eine Berechnung die Werte überschreiben, die ich setze?
Nr. Die Werte, wenn Sie festgelegt, wenn Sie ein Produkt konfigurieren, wie Werte sind, die verwendet werden. Die Berechnung, die auftritt, wenn die Eingabewerte in einer Berechnung geändert werden, kann die Werte nicht überschreiben, die Sie für ein bestimmtes Attribut bereitstellen.

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a>Was passiert, wenn ich einen Eingabewert in einer Berechnung entferne?
Wenn Sie einen Eingabewert in einer Berechnung entfernen, wird der Wert des Zielattributs ebenfalls entfernt.

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a>Warum erhalte ich eine Fehlermeldung, die darauf hinweist, dass mein Modell im Widerspruch steht?
Diese Meldung wird angezeigt, wenn eine Berechnung einen Fehler enthält, oder ein Widerspruch in mindestens einer Einschränkung vorhanden ist. Weitere Informationen zu Widersprüchen finden Sie unter [Ausdruckseinschränkungen und Tabelleneinschränkungen](expression-constraints-table-constraints-product-configuration-models.md). Nachfolgend sind einige Situationen, wo Fehler in Berechnungen auftreten können:

-   Ein Wert wird durch 0 (Null) geteilt.
-   Ein Konflikt zwischen den folgenden zwei Elementen liegt vor:
    -   Die Werte, die für ein Attribut verfügbar sind und die durch eine Einschränkung beschränkt werden
    -   Ein Wert, der durch eine Berechnung generiert wird
-   Die Werte, die von der Berechnung zurückgegeben werden, sind außerhalb der Domäne des Attributs. Ein Beispiel ist eine Ganzzahl zwischen \[1..10\], das durch 0 berechnet wird.

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a>Warum erhalte ich eine Fehlermeldung, obwohl ich mein Produktmodell erfolgreich geprüft habe?
Berechnungen werden nicht in die Überprüfung einbezogen. Sie müssen das Produktkonfigurationsmodell testen, um Berechnungsfehler zu suchen. Führen Sie zum Testen eines Produktkonfigurationsmodells die folgenden Schritte aus.

1.  Produktinformationsverwaltung auf ** ** ** &gt; Common ** ** &gt; Produktkonfigurationsmodelle **.
2.  Wählen Sie ein Produktkonfigurationsmodell aus, und klicken Sie in der Gruppe **Ausführen** auf **Testen**.


