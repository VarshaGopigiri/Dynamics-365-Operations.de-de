---
title: Vereinbarungen zum Servicelevel
description: In einer SLA stimmt der Debitor einer Mindestantwortzeit zu, basierend auf der Zeit zwischen der Aufzeichnung des Problems durch das Serviceunternehmen bis zum Beheben des Problems.
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServicelevelagreement
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
ms.openlocfilehash: 63389ed348e9b1bebe00d9aaa9f78b97ac39317b
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="service-level-agreements"></a><span data-ttu-id="5fbcb-103">Vereinbarungen zum Servicelevel</span><span class="sxs-lookup"><span data-stu-id="5fbcb-103">Service level agreements</span></span>        

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5fbcb-104">Eine Vereinbarung zum Servicelevel (Service Level Agreement, SLA) ist eine Vereinbarung zwischen einem Serviceunternehmen und einem Debitor.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="5fbcb-105">In einer SLA stimmt der Debitor einer Mindestantwortzeit zu, basierend auf der Zeit zwischen der Aufzeichnung des Problems durch das Serviceunternehmen bis zum Beheben des Problems.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="5fbcb-106">Eine SLA setzt einen Standard-Servicelevel durch, der Debitoren angeboten wird, und zeigt außerdem einem Serviceunternehmen an, wann ein Servicevorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="5fbcb-107">Es kann eine beliebige Zahl von SLAs erstellt werden, um Debitoren verschiedene Servicelevels zu bieten.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="5fbcb-108">Erstellen einer Vereinbarung zum Servicelevel</span><span class="sxs-lookup"><span data-stu-id="5fbcb-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="5fbcb-109">Klicken Sie auf **Serviceverwaltung** \> **Einstellungen** \> **Servicevereinbarungen** \> **Vereinbarungen zum Servicelevel**.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="5fbcb-110">Geben Sie einen Namen für eine Vereinbarung zum Servicelevel im Feld **Vereinbarung zum Servicelevel** ein.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="5fbcb-111">Geben Sie die Zeit ein, die Sie für die Ausführung von Serviceeinsätzen einräumen möchten, die der Vereinbarung zum Servicelevel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="5fbcb-112">Wählen Sie dann einen Kalender aus, wenn die Vereinbarung zum Servicelevel auf einem bestimmten Kalender beruhen soll.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="5fbcb-113">Anwenden einer Vereinbarung zum Servicelevel</span><span class="sxs-lookup"><span data-stu-id="5fbcb-113">Apply a service level agreement</span></span>

<span data-ttu-id="5fbcb-114">Die SLA wird direkt auf eine Servicevereinbarung angewendet.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="5fbcb-115">Serviceaufträge, die Sie manuell erstellen und einer Servicevereinbarung zuordnen, die eine SLA hat, werden anhand dieser SLA gemessen.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="5fbcb-116">Automatisch erstellte Serviceaufträge werden keiner Vereinbarung zum Servicelevel zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="5fbcb-117">Anwenden der Vereinbarung zum Servicelevel auf die Servicevereinbarung</span><span class="sxs-lookup"><span data-stu-id="5fbcb-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="5fbcb-118">Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="5fbcb-119">Wählen Sie die Servicevereinbarung aus, auf die Sie die SLA anwenden möchten, und klicken Sie anschließend im **Aktivitätsbereich** auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="5fbcb-120">Wählen Sie im **Vereinbarung zum Servicelevel** Feld die Vereinbarung zum Servicelevel, die Sie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="5fbcb-121">Anwenden der Vereinbarung zum Servicelevel auf die Servicevereinbarungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5fbcb-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="5fbcb-122">Klicken Sie auf **Serviceverwaltung** \> **Einstellungen** \> **Servicevereinbarungen** \> **Serviceverinbarungsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="5fbcb-123">Wählen Sie im **Vereinbarung zum Servicelevel** Feld die Vereinbarung zum Servicelevel, die Sie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="5fbcb-124">Zeiterfassung für einen Serviceauftrag anhand der Vereinbarung zum Servicelevel</span><span class="sxs-lookup"><span data-stu-id="5fbcb-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="5fbcb-125">Wenn Sie einen neuen Serviceauftrag für eine Servicevereinbarung erstellen, der eine SLA zugewiesen ist, wird das Zeitintervall für die Lieferung des Services gestartet, und das System beginnt mit der Erfassung der Lieferzeit.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="5fbcb-126">Darüber hinaus können Sie die folgenden Optionen festlegen:</span><span class="sxs-lookup"><span data-stu-id="5fbcb-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="5fbcb-127">Sie können die Zeitaufzeichnung für den Serviceauftrag starten und anhalten, um die Gesamtzeit für Serviceaufträge zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="5fbcb-128">Sie können die Einhaltung des in der Vereinbarung zum Servicelevel festgelegten Zeitrahmens überwachen.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="5fbcb-129">Sie können Ursachencodes definieren, die festgelegt sein müssen, wenn der Zeitrahmen der Vereinbarung zum Servicelevel überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fbcb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fbcb-130">See also</span></span>

[<span data-ttu-id="5fbcb-131">Anzeigen der Konformität mit Vereinbarungen zum Servicelevel</span><span class="sxs-lookup"><span data-stu-id="5fbcb-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


