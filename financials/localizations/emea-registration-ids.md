---
title: Registrierungskennungen
description: Unter den Themen in diesem Abschnitt finden Sie Informationen zum Einrichten und Verwalten von Anmelde-IDs.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264824
ms.assetid: e86f0a35-be58-4ef5-b5ab-bcfc495eaa13
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 712eb9ec22f4eea4a969a7bd23b7d3728b35772e
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="registration-ids"></a>Registrierungskennungen

[!include[banner](../includes/banner.md)]


Unter den Themen in diesem Abschnitt finden Sie Informationen zum Einrichten und Verwalten von Anmelde-IDs.

Viele Länder und Regionen haben unterschiedliche Bestimmungen und Anforderungen für das Erfassen Registrierungsnummern oder IDs. Dieses Thema enthält einen Überblick der erforderlichen Einstellungen und dem Verarbeiten der unterstützten Erfassungstypen für Parteien in verschiedenen europäischer Länder/Regionen. Alle Länder/Regionen habe Ihre Anforderungen zur Unterstützung von verschiedenen landesspezifischen Funktionen, die Registrierungsnummern zugeordnet werden, die von verschiedenen Stellen bereitgestellt werden. Beispiele für Registrierungsnummern enthalten Sozialversicherungsnummer (SSN), Steuerkennungsnummer (TIN) und die Kennung der MwSt-Kennung (EU MwSt. ID). Diese Funktion bietet ein einheitliches Framework für alle Länder in allen Regionen, die Anforderungen von einigen landesspezifischen europäischen Ländern berücksichtigen. Die folgenden Abschnitte beschreiben den allgemeinen Informationsfluss, der für die Einrichtung und Verwaltung der Registrations-IDs verwendet wird.

## <a name="registration-type-creation"></a>Registrationstyperfassung
Bevor Sie Registrierungsnummern-IDs einrichten können, müssen Sie die Registrierungstypen für die unterschiedlichen Arten von Registrierungsnummern, denen die einzelnen Parteien unterworfen sind. Gehen Sie zu **Organisationsverwaltung** &gt; **Globales Adressbuch** &gt; **Erfassungstypen** &gt;, um die **Erfassungstypen** für Kreditoren, Debitoren, Arbeitskräfte und juristischen Personen in verschiedenen Ländern/Region zu erstellen und zu verwalten.

|Feld                 |Beschreibung      |
|------------------------------|----------------------------|                                                                           
| Name                | Hier können Sie den Namen des Registrationstyps eingeben. |                                                                           
| Beschreibung         | Beschreibung des Reigstrationstyps. |
| Land/Region      | Die eindeutige Kennung für Land/Region.|
| Steuerbehörde       | Die Steuerbehörte, die dem Registrationstyp zugeordnet ist|
| Beschränkt auf       | Der Typ der Einschränkung, die auf den Steuererfassungstyp gilt: Keine, Organisation, Person.|
| Formate              | Das Überprüfungsformat für den Steuerregistrierungstyp.|
| Aktualisierbar      | Wenn dieses Kontrollkästchen aktiviert ist, kann die Registrierungsnummer aktualisiert werden, nachdem sie für den Steuerregistrierungstyp eingegeben wurde.|
| Eindeutig              | Wenn dieses Kontrollkästchen aktiviert ist, ist die Registrierungsnummer für den Steuerregistrierungstyp eindeutig. |
| Primär für Land | Wenn eine Partei Ländern mit einer oder mehreren Lieferverarbeitungs-Adressen zugeordnet ist und die Erfassungskennung für alle Adressen gültig ist, müssen Sie eine Hauptadresse für das Land auswählen. Sie können nur eine Kennung als primär erfassen. Definiert, wenn die Registrierungsnummer nur promär für Landadresse eingegeben werden kann. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Zuweisen eines Typs für eine Kategoriehierarchie.
Erfassungskategorie ist die Land/Regionskennung, die für Länder/Regionen für Steuer, Zoll und insbesondere anderen Zwecken verwendet wird. Diese Kategorie definiert Validierungsregeln bestimmter Erfassungskennung (einschließlich Prüfzifferenvusw.) und unter Einbeziehung der Erfassungskennung in den unterschiedlichen Berichten. Verwenden Sie die Seite **Organisationsverwaltung** &gt; **Globales Adressbuch** &gt; **Erfassungstypen** &gt; **Erfassungskategorien**, Erfassungstypen des bestimmtes Land zuzuweisen, um die Erfassungskategorie zu unterstützen..

| Feld            | Beschreibung|
|-----------------------|----------------|
| Registrierungstyp     | Das Land/Region des Erfassungstyps|
| Beschränkt auf         | Der Typ der Einschränkung, die auf den Steuererfassungstyp gilt: Keine, Organisation, Person.|
| Registrierungskategorie | …Die eindeutige Erfassungskennung genehmigt für die Verwendung im Land. Die vollständige Liste der unterstütztem in den Kategorien AX7.1 befindet sich unten. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Geben die Erfassung-ID für globale Adressbuchdatensätze ein
Das globale Adressbuch (GAB) in Microsoft Dynamics 365 or Operations enthält konsolidierte Adressinformationen für Debitoren, Kreditoren, Kontakte, Geschäftsbeziehungen und juristischen Personen. Weitere Informationen finden Sie unter [Globales Adressbuch](/dynamics365/operations/organization-administration/overview-global-address-book). Die Parteidatensätze, die im globalen Adressbuch gespeichert sind, können einen oder mehrere Adressdatensätze enthalten. Diese Adressen werden für verschiedene Zwecke verwendet, z. B. für Rechnungsstellung oder Lieferung. Sie können Erfassungs-IDs für Adressinformationen für Debitoren, Kreditoren, Arbeitskräfte und juristische Personen einrichten. Suchen Sie den Datensatz für die Partei (juristische Personen, Kreditoren, Debitoren, Arbeitskraft) für die Sie die Registerkennung eingeben möchten, und klicken dann **Erfassungs-IDs** in den Formularen, die mit der Partei, juristischen Personen, Kreditoren, Debitoren, Arbeitskraft verknüpft ist, um die Seite **Adresse verwalten** zu öffnen. Auf der **Steuerregistrierung** Registerkarte klicken Sie **Hinzufüge** und geben folgende Informationen zur Erfassungs-ID ein

|Feld                |Beschreibung                                                |
|---------------------|-----------------------------------------------------------|
| Registrierungstyp   | Der Erfassungstyp des ausgewählten Lands/Region.     |
| Registrierungsnummer | Die Partei-Kennungs-ID.                                |
| Beschreibung         | Beschreibung des Reigstrationsnummer.               |
| Abschnitt             | Die zusätzlichen Informationen über die Registrationsnummer. |
| Ausstellende Behörde      | Die Behörde, von der die Registrierungsnummer stammt.        |
| Ausstellungsdatum         | Das Ausgabedatum für die Steuernummer.              |
| Gültig           | Das effektive Datum für die Steuernummer.           |
| Ablauf          | Das Ablaufdatum für die Registrationsnummer.          |

> [!NOTE]
> Die Umsatzsteuernummer der juristischen Person, Kreditor, Debitor kann von der Registrations-IDs ausgewählt werden, die der MwSt.-ID zugeordnet sind und für die Partei eingegeben wurden.

## <a name="search-for-records-by-registration-id"></a>Suche für Datensätze nach Erfassungskennung
Suche für Parteidatensätze auf einer Erfassungskennung ist in die Steuerformulare verfügbar, die für die Partei, zur juristischen Person, den Kreditor, z Debitor und der Arbeitskraft zugeordnet werden. Klicken Sie auf **Erfassung ID-Suche**, um die Seite**Erfassung ID-Suchkriterien** zu öffnen. Definieren Sie die Suchkriterien und klicken Sie auf **Suchen**. Im System werden die ausgewählten Datensätze aus dem globalen Adressbuch zugeordnet und die Typen des Parteidatensatzes angezeigt.

## <a name="supported-registration-categories"></a>Unterstützte Registrierungskategorien
In der folgenden Tabelle werden die unterstützten Erfassungstypen in Dynamics 365 for Operations aufgeführt. Wenn Sie mit den Microsoft Dynamics AX 2012-Feldern für IDs Erfassung vertraut sind, ordnet diese Tabelle auch diese Felder in Dynamics 365 for Operations Registrationskategorien zu.

| Dynamics 365 für Operations-Erfassungskategorie         |Land/Region  | Dynamics AX 2012 Begriff/Feld|
|---------------------------------------------------------------|---------------------|---------------------------------|
| MwSt.-Kennung                                                        | Alle Länder der Europäischen Union (EU)|  Steuernummer (Gesetzgebungstyp in STEUER-ID AX2012 R3)|
| Enterprise-ID (COID)                                          | Belgien, Tschechische Republik, Estland, Ungarn, Lettland, Litauen, Polen, Schweiz | Unternehmensnummer (EnterpriseNumber) Registrationsnummer (RegNum\_W) Registrationsnummer (RegNum\_W) Registrationsnummer (RegNum\_W) Registrationsnummer (RegNum\_W) Unternehmenscode (EnterpriseCode) Registrationsnummer (RegNum\_W) UID (Gesetzgebungstyp UID in AX2012 R3) |
| Zweigstellenkennung                                                     | Belgien            | Zweigstellennummer (BranchNumber)|
| (Spisová-značka Registrierungsnummer, ausgebende Behörde, Abschnitt) | Tschechische Republik     | Einsatznummer (CommercialRegisterInsetNumber). Im Handelsregister CommercialRegister) Abschnitt des Handelsregisters (CommercialRegisterSection )|
| Zolldebitorkennung                                           | Finnland | Zolldebitorennummer (CustomsCustomerNumber\_FI)|
| INN                                                           | Russische Föderation| INN (Gesetzgebungstyp in INN AX2012 R3)|
| RRC                                                           | Russische Föderation| RRC (Gesetzgebungstyp in RRC AX2012 R3)|
| OKDP                                                          | Russische Föderation| OKDP (Gesetzgebungstyp in OKDP AX2012 R3)|
| OKPO                                                          | Russische Föderation| OKPO (Gesetzgebungstyp in OKPO AX2012 R3)|
| RCOAD                                                         | Russische Föderation| RCOAD (Gesetzgebungstyp in RCOAD AX2012 R3)|
| OGRN                                                          | Russische Föderation| OGRN (Gesetzgebungstyp in OGRN AX2012 R3) |
| SNILS                                                         | Russische Föderation| SNILS (Gesetzgebungstyp in SNILS AX2012 R3)|
| CIFTS                                                         | Russische Föderation| CIFTS (Gesetzgebungstyp in CIFTS AX2012 R3)|

Weitere Informationen zum Zuordnen von Erfaassungskennungen einschließlich erforderliche Voraussetzungen, finden Sie in den folgenden Aufgabenaufzeichnungen für Mehrwertsteuer-IDs in den Lebenszyklus-Dienstleistungen (LCS):

-   Einrichten der MwSt Kennung
-   MwSt-Registrierungs-ID des der Kreditors
-    Suche nach Partei per MwSt.-Kennung




