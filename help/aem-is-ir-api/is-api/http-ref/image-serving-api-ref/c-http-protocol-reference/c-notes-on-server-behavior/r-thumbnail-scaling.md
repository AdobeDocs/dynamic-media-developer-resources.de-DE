---
description: Die Transformationen der Bildebene werden in Schritt 2 für Miniaturansichten wie folgt geändert (d. h. bei req=tmb).
seo-description: Die Transformationen der Bildebene werden in Schritt 2 für Miniaturansichten wie folgt geändert (d. h. bei req=tmb).
seo-title: Skalierung von Miniaturbildern
solution: Experience Manager
title: Skalierung von Miniaturbildern
topic: Scene7 Image Serving - Image Rendering API
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# Skalierung von Miniaturbildern{#thumbnail-scaling}

Die Transformationen der Bildebene werden in Schritt 2 für Miniaturansichten wie folgt geändert (d. h. bei req=tmb).

* `2.` Wenn `size=` angegeben, passen Sie das Bild (zugeschnitten) mithilfe von Miniaturansichtsregeln in den `size=` Rekt ein. Wenn `size=` keine Angabe gemacht wird, passen Sie die Skalierung auf Grundlage `res=``res=` oder, falls nicht angegeben, passen Sie das (zugeschnittene) Bild mithilfe der unten aufgeführten Miniaturansichtsregeln in den Arbeitsflächenrect ein.

