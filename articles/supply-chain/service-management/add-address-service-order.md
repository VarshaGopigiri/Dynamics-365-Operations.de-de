---
title: "Hinzufügen einer Adresse zu einem Serviceauftrag"
description: "In diesem Thema wird beschrieben, wie eine Debitorenadresse zu einem Serviceauftrag hinzugefügt wird."
author: YuyuScheller
manager: AnnBe
ms.date: 05/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e6dfa27b2101e84fbab678e781c26126cf1db898
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="add-an-address-to-a-service-order"></a>Hinzufügen einer Adresse zu einem Serviceauftrag    

[!include [banner](../includes/banner.md)]


In diesem Thema wird beschrieben, wie eine Debitorenadresse zu einem Serviceauftrag hinzugefügt wird. Beim Erstellen eines Serviceauftrags werden die Adressinformationen aus dem Projekt übertragen, dem der Serviceauftrag zugeordnet ist. Allerdings können Sie einen alternativen Speicherort von Adressen auswählen, die bereits in Microsoft Dynamics AX für Debitoren, Kreditoren, Standorte, Lagerorte, Serviceaufträge und Projekte eingegeben sind.

Zudem können Sie eine neue Adresse erstellen. Standardmäßig wird die neue Adresse in das Projekt übertragen. Allerdings können Sie angeben, dass die neue Adresse für diese Instanz des Services relevant ist. Die neue Adresse wird dann nicht in das Projekt übertragen.

## <a name="create-a-customer-address-for-a-service-order"></a>Erstellen einer Debitorenadresse für einen Serviceauftrag

Um einem Serviceauftrag eine Adresse hinzuzufügen, führen Sie folgende Schritte aus:

1.  Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.

2.  Öffnen Sie den Serviceauftrag, für den eine Adresse erstellt werden soll.

3.  Klicken Sie im **Aktivitätsbereich** auf **Bearbeiten**, und klicken Sie anschließend auf **Kopfzeilenansicht**.

4.  Klicken Sie auf dem Inforegister **Adresse** auf **Adresse hinzufügen**.

5.  Geben Sie im Formular **Neue Adresse** einen eindeutigen Namen für die Adresse ein, und füllen Sie die verbleibenden Felder aus. 
    

    > [!WARNING]
    > <P>Wenn Sie denselben Namen als vorhandene Adresse eingeben, überschreiben die Informationen, die Sie in die verbleibenden Felder eingeben, die Informationen für die vorhandene Adresse.</P>


6.  Klicken Sie auf **OK**, um die neue Adresse in Ihren Serviceauftrag zu kopieren.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Angeben einer alternativen Adresse für einen Serviceauftrag

Um einem Serviceauftrag eine alternative Adresse hinzuzufügen, führen Sie folgende Schritte aus:

1.  Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.

2.  Öffnen Sie den Serviceauftrag, für den eine alternative Adresse erstellt werden soll.

3.  Klicken Sie im **Aktivitätsbereich** auf **Bearbeiten**, und klicken Sie anschließend auf **Kopfzeilenansicht**.

4.  Klicken Sie auf dem Inforegister **Adresse** auf **Weitere Adresse**.

5.  In der **Adressauswahl** Formular auf das Feld **Datensatztyp**, wählen Sie **Serviceaufträge** aus.

6.  Wählen Sie eine Adresse aus, und klicken Sie auf **OK**, um sie in Ihren Serviceauftrag zu kopieren.


  



