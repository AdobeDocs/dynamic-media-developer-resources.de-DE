---
description: Die Transformationen der Bildebene werden in Schritt 2 für Miniaturansichten wie folgt geändert (d. h. bei req=tmb).
seo-description: Die Transformationen der Bildebene werden in Schritt 2 für Miniaturansichten wie folgt geändert (d. h. bei req=tmb).
seo-title: Skalierung von Miniaturbildern
solution: Experience Manager
title: Skalierung von Miniaturbildern
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Miniaturansicht-Skalierung{#thumbnail-scaling}

Die Transformationen der Bildebene werden in Schritt 2 für Miniaturansichten wie folgt geändert (d. h. bei req=tmb).

* `2.` Wenn  `size=` angegeben, passen Sie das Bild (zugeschnitten) mithilfe von Miniaturansichtsregeln in das  `size=` Rechteck ein. Wenn `size=` nicht angegeben ist, passen Sie die Skalierung basierend auf `res=` oder, wenn `res=` nicht angegeben ist, passen Sie das (zugeschnittene) Bild mithilfe der unten aufgeführten Miniaturansichtsregeln in den Arbeitsflächenrect ein.

