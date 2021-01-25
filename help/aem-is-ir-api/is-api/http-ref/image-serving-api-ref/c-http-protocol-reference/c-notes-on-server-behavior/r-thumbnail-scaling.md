---
description: Die Transformationen der Bildebene werden in Schritt 2 für Miniaturansichten wie folgt geändert (d. h. bei req=tmb).
seo-description: Die Transformationen der Bildebene werden in Schritt 2 für Miniaturansichten wie folgt geändert (d. h. bei req=tmb).
seo-title: Skalierung von Miniaturbildern
solution: Experience Manager
title: Skalierung von Miniaturbildern
topic: Dynamic Media Image Serving - Image Rendering API
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# Miniaturansicht-Skalierung{#thumbnail-scaling}

Die Transformationen der Bildebene werden in Schritt 2 für Miniaturansichten wie folgt geändert (d. h. bei req=tmb).

* `2.` Wenn  `size=` angegeben, passen Sie das Bild (zugeschnitten) mithilfe von Miniaturansichtsregeln in das  `size=` Rechteck ein. Wenn `size=` nicht angegeben ist, passen Sie die Skalierung basierend auf `res=` oder, wenn `res=` nicht angegeben ist, passen Sie das (zugeschnittene) Bild mithilfe der unten aufgeführten Miniaturansichtsregeln in den Arbeitsflächenrect ein.

