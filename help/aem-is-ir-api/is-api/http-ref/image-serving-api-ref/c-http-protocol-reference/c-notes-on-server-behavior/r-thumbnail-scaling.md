---
description: Die Transformationen der Bildebene werden in Schritt 2 für Miniaturansichten wie folgt geändert (d. h. bei req=tmb).
solution: Experience Manager
title: Skalierung von Miniaturbildern
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Miniaturansicht-Skalierung{#thumbnail-scaling}

Die Transformationen der Bildebene werden in Schritt 2 für Miniaturansichten wie folgt geändert (d. h. bei req=tmb).

* `2.` Wenn  `size=` angegeben, passen Sie das Bild (zugeschnitten) mithilfe von Miniaturansichtsregeln in das  `size=` Rechteck ein. Wenn `size=` nicht angegeben ist, passen Sie die Skalierung basierend auf `res=` oder, wenn `res=` nicht angegeben ist, passen Sie das (zugeschnittene) Bild mithilfe der unten aufgeführten Miniaturansichtsregeln in den Arbeitsflächenrect ein.

