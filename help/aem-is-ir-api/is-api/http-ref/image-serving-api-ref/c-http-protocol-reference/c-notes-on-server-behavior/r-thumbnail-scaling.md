---
description: Schritt 2 der Bildschicht ändert sich wie folgt für Miniaturansichten (d. h. wenn req=tmb).
solution: Experience Manager
title: Skalierung von Miniaturansichten
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# Skalierung von Miniaturansichten{#thumbnail-scaling}

Schritt 2 der Bildschicht ändert sich wie folgt für Miniaturansichten (d. h. wenn req=tmb).

* `2.` Wenn  `size=` angegeben ist, passen Sie das Bild (beschnitten) mithilfe von Miniaturregeln in das  `size=` rect an. Wenn `size=` nicht angegeben ist, skalieren Sie basierend auf `res=` oder, wenn `res=` nicht angegeben ist, passen Sie das (zugeschnittene) Bild mithilfe der unten beschriebenen Regeln für die Miniaturansicht in den Arbeitsflächenrect an.
