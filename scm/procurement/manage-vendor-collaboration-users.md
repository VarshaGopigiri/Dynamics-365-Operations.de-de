---
title: "Benutzer für Kreditor-Kooperationen verwalten"
description: "In diesem Thema wird beschrieben, wie Sie die Bereitstellung neuer Kreditorenzusammenarbeitsbenutzer anfordern können und wie neue Kreditorenzusammenarbeitkontakte hinzugefügt werden."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 380f1bcdf7109dc12fd898199033eac7710d863c
ms.lasthandoff: 03/31/2017


---

# <a name="manage-vendor-collaboration-users"></a>Benutzer für Kreditor-Kooperationen verwalten

In diesem Thema wird beschrieben, wie Sie die Bereitstellung neuer Kreditorenzusammenarbeitsbenutzer anfordern können und wie neue Kreditorenzusammenarbeitkontakte hinzugefügt werden. 

Die Kreditorenzusammenarbeitschnittstelle in Microsoft Dynamics 365 for Operations zeigt Informationen zu Bestellungen, Rechnungen und Lieferbestand externer Kreditoren an. Sie können neue Kreditorenzusammenarbeitkontakte erstellen und anfordern, dass neuen Benutzer bereitgestellt werden, wenn Sie als externer Kreditor mit der Sicherheitsrolle **Kreditorenadministrator (extern)** oder einer ähnlichen Berechtigung arbeiten. Sie können diese Aufgaben auch ausführen, wenn Sie als Beschaffungsspezialist arbeiten. In diesem Thema bezieht sich diese Rolle auf einen Beschaffungsspezialisten, der im Unternehmen arbeitet, das die Instanz von Microsoft Dynamics 365 for Operations besitzt. Weitere Informationen dazu, wie Kreditorenzusammenarbeit, wenn Sie ein externer Anbieter sind, finden Sie Kreditoren mit Debitoren verwendet []( vendor-collaboration-work-customers-dynamics-365-operations.md).  

Weitere Informationen dazu, wie Kreditorenzusammenarbeit, wenn Sie ein Beschaffungsspezialist sind, finden Sie im Kreditorenzusammenarbeit mit [für externe Kreditoren vendor-collaboration-work-external-vendors.md] ().

## <a name="add-new-vendor-collaboration-contacts"></a>Hier können Sie neue Kreditorenzusammenarbeitkontakte hinzufügen
Wenn Sie jemandem Zugriff auf die Kreditorenzusammenarbeit gewähren möchten, müssen sie die Person zunächst als Kreditorenzusammenarbeitskontakt hinzufügen. Sie sollten auch Kontakte für Mitarbeiter Ihres Unternehmens hinzufügen, die die Kreditorenzusammenarbeit nicht verwenden werden. So könnten sie beispielsweise der Punkt der Kontaktperson für andere Arten von  Beschaffungsinformationen sein. Neue Kontakte werden in alle Kontakte ** ** der Seite hinzuzufügen, die von den Kreditorenzusammenarbeit ** ** ** Kontakte ** Menü aus &gt; zugegriffen wird. Hinzufügen eines neuen Kontakts:

1.  Klicken Sie auf **Neu.**
2.  Geben Sie die Details der Kontaktperson ein.
3.  Wählen Sie, welche juristische Person sie in Ihrem Unternehmen vertritt und mit welcher juristischen Person sie im Unternehmen zusammenarbeiten wird. Dazu verwenden Sie, indem eines ** juristische Person in meinem Unternehmen **/** juristische Person im Debitoren mit Paare ** auswählen.
4.  Klicken Sie auf **Erstellen.**

Wenn Sie einen Kontakt löschen möchten, ist es nur möglich, jene zu löschen, die Sie erstellt haben.

## <a name="vendor-collaboration-user-requests"></a>Benutzeranforderungen für Kreditor-Kooperationen
Kreditorenzusammenarbeitbenutzeranforderungen können von einem Beschaffungsspezialisten oder einem Administrator des externen Lieferanten verwendet werden.

-   Wenn Sie ein externer Anbieter sind, übermitteln Sie Anforderungen von der ** alle Kontakte ** Seite innerhalb des Kreditorenzusammenarbeit ** ** Moduls.
-   Wenn Sie ein Beschaffungsspezialist sind, übermitteln Sie Anforderungen von der Seite **Kontakte anzeigen**. Richten Sie dazu, auf den Kreditorendatensatz, ** ** Einstellungen im Abschnitt im Aktivitätsbereich zu bewerkstelligen, wählen ** Kontakte ** &gt; ** Ansichtskontakte ** aus.

Sie können eine Anfrage für die Bereitstellung eines Benutzers machen, ihn deaktivieren oder die Sicherheitsrollen ändern. Wenn Sie Administrator des externen Kreditors sind, müssen Sie für die Kreditorenkonten als Kontaktperson erfasst werden, für die Sie Bnutzeranforderungen erstellen möchten und Sie müssen Zugang zur Kreditorenzusammenarbeitschnittstelle für die Kreditorenkonten haben.  

Wird eine Anforderung übermittelt, wird sie der **Kreditorenzusammenarbeit-Benutzeranforderungsliste** im Modul **Kreditorenzusammenarbeit** und der Liste **Kreditorenzusammenarbeits-Benutzeranfrage**  im Modul **Beschaffung** hinzugefügt (das Beschaffungsmodul ist für externe Nutzer nicht zugänglich)

### <a name="provision-a-user"></a>Benutzer bereitstellen

Bevor Sie anfordern können, dass ein neuer Benutzer bereitgestellt wird, muss diese Person als Kontakt für einen oder mehrere Kreditoren eingerichtet werden. Um eine Anfrage für einen neuen Kreditorenzusammenarbeitsbenutzer zu erstellen:

1.  Auf der ** alle Kontakte ** Seite auf Rücklagekreditorenbenutzer ** **.
2.  Hier geben Sie die E-Mail-Adresse des Benutzers ein. Diese Adresse wird von dem Benutzer verwendet, um sich auf Dynamics 365 for Operations anzumelden. Wenn die E-Mail-Adresse einer Domäne angehört, die als Mandant mit Microsoft Azure erfasst wurde, muss die E-Mail-Adresse ein vorhandenes Azure Active Directory (ADD) Konto sein, um den Bereitstellungsprozess erfolgreich abzuschließen. Wenn die E-Mail-Adresse keiner Domäne angehört, die mit Microsoft Azure erfasst wird, wird ein ADD-Konto als Teil des Bereitstellungsprozesses erstellt und der neue Benutzer wird eine Einladungsmail erhalten. Heimanwendere-mail-adressen mit Domänen wie @hotmail.com@gmail.com@comcast.net nicht verwendet werden, um für Arbeitsgangsbenutzer Dynamics 365 zu erfassen.
3.  Setzen Sie die Option **Kreditorenzusammenarbeitzugriff zulässig** auf **Ja** für alle juristischen Personen, auf die der Benutzer zugreifen muss.
4.  Wählen Sie im Abschnitt **Benutzerrollen zuweisen** das Kontrollkästen **Zuweisen** für die Sicherheitsrollen, die der neue Benutzer besitzen sollte.
5.  Klicken Sie auf **Absenden**.

Wenn die Kreditorenbenutzeranforderung übermittelt wird, wird das zusammenarbeitzugriff ** der Kreditoren zulässig ** Feld auf Ja ** ** für das ausgewählte Kreditorenkonto festgelegt und ein Benutzeranforderungsworkflow wird gestartet. Im Rahmen des Workflows wird ein neuer Benutzer in Dynamics 365 for Operations erstellt und die Sicherheitsrollen zugewiesen. Darüber hinaus ist eine Azures B2B Dienstleistung aktiviert, die die Interaktion mit dem Azure Portal und  ein neues oder vorhandenes AAD-Konto dem Dynamics 365 for Operations Benutzerkonto initiiert.

### <a name="inactivate-a-user"></a>Benutzer deaktivieren

Es gibt zwei Möglichkeiten, den Zugriff auf die Kreditorenzusammenarbeit für einen Benutzer zu entfernen:

-   Auf der Seite **Kontakte** für den Kreditor, legen Sie die Option **Kreditorenzusammenarbeitzugriff erlaubt** auf **Nein** für den Kontakt fest. Dies kann einzeln pro juristische Person erfolgen, für die die Person als Kontakt fungiert. Diese Option kann nur von Beschaffungsspezialisten verwendet werden.
-   Deaktivieren Sie das gesamte Benutzerkonto, indem Sie eine Anforderung **Kreditorenbenutzer deaktivieren** übermitteln.

Klicken Sie anfordern, dass ein Benutzer deaktiviert wird:

1.  Auf der ** alle Kontakte ** Seite auf ** deaktivieren Sie Kreditorenbenutzer ** ** **.
2.  Schreiben Sie einen Kommentar im Feld**Geschäftsbegründung**.
3.  Klicken Sie auf **Absenden**.

### <a name="modify-security-roles"></a>Sicherheitsrollen ändern

** Die Verwalten von Kreditorenbenutzerrollen bei ** Seite ist die gleiche wie die Rücklagekreditorenbenutzer ** ** Seite, außer dass die Liste der Sicherheitsrollen kann bearbeitet werden.  

Wenn Sie auch anfordern, dass die für einen Benutzer Sicherheitsrollen geändert werden:

1.  Auf der ** alle Kontakte ** Seite auf ** Verwalten ** ** Kreditorenbenutzerrollen **.
2.  Schreiben Sie einen Kommentar im Feld**Geschäftsbegründung**.
3.  Wählen Sie im Abschnitt **Verwalten von Benutzerrollen** die Sicherheitsrollen aus, die Sie zuordnen möchten, und deaktivieren Sie jene, die Sie entfernen möchten.
4.  Click **Submit**.


