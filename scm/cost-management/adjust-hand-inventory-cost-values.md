---
title: "Regulieren der Einstandswerte für verfügbaren Bestand"
description: "Verwenden Sie die Seite &quot;Anpassung des verfügbaren Lagerbestands&quot;, um den Einstandswert der Mengen des verfügbaren Lagerbestands zu regulieren, nachdem ein Lagerabschlusses durchgeführt wurde."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d1ef775c9783b975fd0f852dc7112506d3897605
ms.lasthandoff: 03/31/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>Regulieren der Einstandswerte für verfügbaren Bestand

Verwenden Sie die Seite "Anpassung des verfügbaren Lagerbestands", um den Einstandswert der Mengen des verfügbaren Lagerbestands zu regulieren, nachdem ein Lagerabschlusses durchgeführt wurde.

Verwenden Sie die Seite **Anpassung des verfügbaren Lagerbestands**, um den Einstandswert der Mengen des verfügbaren Lagerbestands zu regulieren, nach Ausführung eines Lagerabschlusses. ** Hinweis: ** ** Die Anpassung des verfügbaren Lagerbestands ** Seite, auf ** der Abschluss und Regulierung ** Seite zu öffnen, wählen Sie den Datensatz eines bereits abgeschlossenen Lagerabschlusses aus und klicken dann ** Regulierung ** &gt; ** am Lager **. **Beispiel:** Im Februar liegen die folgenden Buchungen vor:

-   1. Februar: Wertmäßiger Lagerzugang für die Menge "2" mit einem Einstandspreis von EUR 10,00
-   5. Februar: Wertmäßiger Lagerzugang für die Menge "1" mit einem Einstandspreis von EUR 13,00
-   19. Februar: Wertmäßiger Lagerabgang für die Menge "1" mit einem laufenden Durchschnittseinstandspreis von EUR 11,00

Dieser Artikel wurde mit dem FIFO-Lagermodell (First In, First Out) eingerichtet, und der Lagerabschluss erfolgte am 28. Februar. Die wertmäßige Abgangsbuchung von EUR 11,00 wird mit dem wertmäßigen Zugang ausgeglichen, der vom 1. Februar ist, und eine Regulierung von EUR 1,00 wird vorgenommen. Die folgenden Lagerzugänge enthalten dann offene Lagermengen:

-   1. Februar: Menge "1" mit einem Einstandspreis von EUR 10,00
-   5. Februar: Menge "1" mit einem Einstandspreis von EUR 13,00

Verwenden Sie die Option für die Regulierung des verfügbaren Bestands, um die Kosten dieser beiden Artikel auf EUR 15,00 festzulegen, und regulieren Sie die offenen verfügbaren Bestandsmengen zum Datum der letzten Lagerabschlussperiode. **Hinweis:** Als Buchungsdatum für die Regulierung des verfügbaren Bestands wird das Datum des letzten Lagerabschlusses verwendet. Dieses Datum kann nicht geändert werden.

