---
title: Organisationen und Organisationshierarchien
description: "Eine Organisation ist eine Gruppe von Personen, die zusammenarbeiten, um einen Geschäftsprozess durchzuführen oder ein Ziel zu erreichen. Organisationshierarchien stellen die Beziehungen zwischen den Organisationen dar, aus denen das Unternehmen besteht."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17291
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5dc866e2d366138d2fd9d0f9c41cb66892051f3c
ms.lasthandoff: 03/31/2017


---

# <a name="organizations-and-organizational-hierarchies"></a>Organisationen und Organisationshierarchien

Eine Organisation ist eine Gruppe von Personen, die zusammenarbeiten, um einen Geschäftsprozess durchzuführen oder ein Ziel zu erreichen. Organisationshierarchien stellen die Beziehungen zwischen den Organisationen dar, aus denen das Unternehmen besteht.

<a name="organizations"></a>Organisation
-------------

In Microsoft Dynamics 365 für Arbeitsgänge, können Sie die folgenden Typen von internen Organisationen definieren: juristische Personen, Organisationseinheiten und Teams.

Alle internen Organisationen sind Typen der **Partei** Entität. Daher verwenden diese Organisationen die Adressbuch, um Adressen und Kontaktinformationen zu speichern. Eine Partei, die einer Person oder Organisation entspricht, kann mindestens einem Adressbuch zugeordnet sein.
### <a name="legal-entities"></a>Juristische Personen

Eine juristische Person ist eine Organisation mit einer registrierten oder eingetragenen Rechtsform. Juristische Personen können Verträge abschließen und sind verpflichtet, Finanzaufstellungen zum Erstellen eines Berichts über ihre Vermögens-, Finanz- und Ertragslage vorzubereiten. Ein Unternehmen ist eine Art von juristischer Person. In diesem Release von Microsoft Dynamics 365 für Arbeitsgänge, sind Unternehmen die einzige Art von juristischer Person, die Sie erstellen können, und jeder juristischen Person ist eine Unternehmenskennung zugeordnet. Diese Zuordnung ist notwendig, da einige Funktionsbereiche im Programm eine Unternehmenskennung (oder "DataAreaId") in den Datenmodellen verwenden. In diesen Funktionsbereichen werden Unternehmen als Grenze für die Datensicherheit verwendet. Benutzer können nur auf Daten für das Unternehmen zugreifen, bei dem sie derzeit angemeldet sind.

### <a name="operating-units"></a>Organisationseinheiten

Eine Organisationseinheit ist eine Organisation, die dazu dient, die Kontrolle über wirtschaftliche Ressourcen und Betriebsprozesse in einem Unternehmen aufzuteilen. Die Personen in einer Organisationseinheit sind verpflichtet, die Nutzung knapper Ressourcen zu maximieren, die Prozesse zu verbessern und Rechenschaft über ihre Leistung abzulegen. In Microsoft Dynamics 365 für Arbeitsgänge, enthalten die Typen von Organisationseinheiten Kostenstellen, Unternehmenseinheiten, Wertströme, Abteilungen und Einzelhandelskanäle. Die folgende Tabelle enthält weitere Informationen zu jedem Organisationseinheitstyp.
| Organisationseinheitstyp | Beschreibung                                                                                                                                    | Zweck                                                                                                                                 |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Kostenstelle         | Eine Organisationseinheit, deren Manager für die budgetierten und tatsächlichen Aufwendungen verantwortlich sind.                                                      | Dient zur Verwaltung und operativen Kontrolle der Geschäftsprozesse, die sich über juristische Personen erstrecken.                                         |
| Unternehmenseinheit       | Eine halbautomatische Organisationseinheit, die zum Erreichen strategischer Unternehmensziele erstellt wird.                                                        | Dient zur Finanzberichterstattung, die auf Branchen oder Produktlinien basiert, die die Organisation unabhängig von juristischen Personen bedient. |
| Wertstrom        | Eine Organisationseinheit, die mindestens einen Produktionsfluss steuert.                                                                                  | Wird häufig im Lean Manufacturing zum Steuern der Aktivitäten und Ströme verwendet, die erforderlich sind, um Konsumenten Produkte zu liefern oder Dienstleistungen bereitzustellen.  |
| Abteilung          | Eine Organisationseinheit, die eine Kategorie oder einen funktionalen Teil einer Organisation darstellt und eine bestimmte Aufgabe erfüllt, beispielsweise Vertrieb oder Buchhaltung. | Dient zur Berichterstattung für Funktionsbereiche. Eine Abteilung kann für Gewinn und Verlust verantwortlich sein und aus einer Gruppe von Kostenstellen bestehen.   |
| Vertriebsweg      | Eine Organisationseinheit stellt einen physischen Laden, einen Onlineshop oder einen Onlinemarktplatz dar.                                          | Dient zur Verwaltung und operativen Kontrolle einer oder mehreren Filialen innerhalb der juristischen Person oder mehrere übergreifend.                                  |

### <a name="teams"></a>Teams

Ein Team ist eine Organisation, deren Mitglieder gemeinsame Interessen, Zuständigkeiten und Ziele haben und in gemeinsamer Verantwortung arbeiten. Teams können nicht in Organisationshierarchien verwendet werden.
Organisationshierarchien
--------------------------

Organisationshierarchien werden eingerichtet, um unterschiedliche Perspektiven des Unternehmens anzuzeigen und entsprechende Berichte zu erstellen. So können Sie beispielsweise eine Hierarchie juristischer Personen für die Steuererklärung sowie für rechtlich relevante oder für gesetzlich vorgeschriebene Berichte einrichten. Richten Sie eine auf Organisationseinheiten basierende Hierarchie ein, um anhand von Finanzdaten Berichte zu erstellen, die zwar gesetzlich nicht erforderlich sind, aber zur internen Kontrolle dienen. Sie können beispielsweise eine Einkaufshierarchie erstellen, um Einkaufsrichtlinien, Regeln und Geschäftsprozesse zu kontrollieren. Jede Hierarchie wird ein Kostenträger in Microsoft Dynamics 365 für Arbeitsgänge zugewiesen. Der Zweck der Hierarchie bestimmt die Organisationstypen, die der Hierarchie hinzugefügt werden können. Der Zweck definiert auch die Anwendungsszenarien, in denen die Hierarchie verwendet werden kann. Organisationen in einer Hierarchie können Parameter, Richtlinien und Buchungen gemeinsam nutzen. Eine Organisation kann die Parameter der übergeordneten Organisation erben oder überschreiben. Gemeinsam genutzte Masterdaten, z. B. Produkte und Adressbücher, betreffen jedoch die gesamte Organisation und können für einzelne Organisationen nicht überschrieben werden. Das Erstellen von Organisationen und Hierarchien erfordert eine sorgfältige Planung. Weitere Informationen finden Sie unter [Die Organisationshierarchie planen](plan-organizational-hierarchy.md).



