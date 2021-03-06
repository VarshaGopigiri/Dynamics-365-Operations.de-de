---
title: Kreditorenportalbenutzersicherheit
description: "In diesem Artikel wird beschrieben, wie Sie die Sicherheit für externe Kreditoren einrichten, die das Kreditorenportal verwenden. Diese Informationen gelten nur für die Versionen Februar 2016 &amp; und Mai 2016 von Dynamics AX."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5819d21a91ac2a7c91f19fd6d80fd7b983411545
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="vendor-portal-user-security"></a>Kreditorenportalbenutzersicherheit

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie die Sicherheit für externe Kreditoren einrichten, die das Kreditorenportal verwenden. Diese Informationen gelten nur für die Versionen Februar 2016 &amp; und Mai 2016 von Dynamics AX.

Die Kreditorenportalfunktion wurde durch die erweiterte Kreditorenzusammenarbeitfunktion in Dynamics 365 for Operations Version 1611 ersetzt. Weitere Informationen zur Einrichtung der Sicherheit für Kreditorenzusammenarbeit finden Sie unter [Konfiguration und Verwaltung der Sicherheit für Kreditorenzusammenarbeit](set-up-maintain-vendor-collaboration.md) Das Kreditorenportal macht einen begrenzten Satz von Informationen zu Bestellungen (POs) für externe Kreditoren verfügbar. Es ist wichtig, dass Sie die Benutzerrechte für das Kreditorenportal in Microsoft Dynamics AX ordnungsgemäß einrichten, damit Kreditoren nicht unerwünschten Zugriff auf zusätzliche Informationen in Ihrer Dynamics AX-Installation haben. **Wichtig:** Im Gegensatz zu anderen Benutzer sollten externe Kreditoren nicht die Rolle **SystemUser** haben. Die Rolle **SystemUser** gewährt Zugriff auf eine Reihe von Rechten, die nicht für externe Benutzer geeignet sind.

## <a name="setting-up-a-vendor-portal-user"></a>Einrichten eines Kreditorenportalbenutzers
Bevor Sie ein Benutzerkonto für jemanden, der das Kreditorenportal verwenden wird, erstellen, müssen Sie den Kreditor einrichten, um eine Kreditorenportalzusammenarbeit zuzulassen. Verwenden Sie das Feld **Bestellungszusammenarbeit** auf der Registerkarte **Allgemeines** auf der Seite **Kreditoren**. Externe Kreditoren, die das Kreditorenportal verwenden, müssen die folgenden Einstellungen haben:

-   Ein Microsoft Azures Active Directory(AAD)-Benutzerkonto muss für den Kreditor auf der Seite **Benutzer** in Dynamics AX registriert werden.
-   Der Kreditor muss die Sicherheitsrolle **Kreditor (extern)** und nicht die Rolle **SystemUser** haben. **Hinweis:** Die Rolle **SystemUser** wird automatisch gewährt, wenn Sie ein neues Benutzerkonto in Dynamics AX erstellen. Daher müssen Sie diese Rolle entfernen und die Warnmeldung bestätigen, die Sie erhalten.
-   Dem Kreditorenbenutzer sollte keine Berechtigung erteilt werden, zusätzliche Felder aus den Bestellungstabellen zu seiner Ansicht der Bestellung hinzuzufügen. Legen Sie auf der Registerkarte **Benutzereinstellungen** auf der Registerkarte **Benutzer** die Option **Zulässige explizite Personalisierung** für den Benutzer auf **Nein** fest.
-   Das Benutzerkonto muss einer registrierten Kontaktperson zugeordnet werden. Wählen Sie auf der Seite **Benutzer** eine Kontaktperson im Feld **Name** aus. Die Person, die Sie auswählen, sollte die Rolle **Kontakt** für den relevanten Kreditor haben.

Wenn die gleiche Person Zugriff auf das Kreditorenportal für mehrere Kreditorenkontos (eventuell für unterschiedliche juristische Personen) benötigt, muss jedes der Benutzerkonten dieser Person derselben registrierten Kontaktperson zugeordnet werden. Die Rolle **Kreditor (extern)** umfasst alle grundlegenden Funktionen, die erforderlich sind, um die Funktionen zu verwenden, die im Kreditorenportal verfügbar sind. Durch diese Einstellung wird sichergestellt, dass die Benutzeroberfläche, die der externe Benutzer sieht, ausschließlich auf das gewünschte Szenario fokussiert ist.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Kreditor-Kooperation](collaborate-vendors-vendor-portal.md)




