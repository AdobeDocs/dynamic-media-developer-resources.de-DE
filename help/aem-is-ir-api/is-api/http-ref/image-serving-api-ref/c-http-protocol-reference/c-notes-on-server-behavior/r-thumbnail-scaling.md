---
title: Skalierung von Miniaturansichten
description: Schritt 2 der Bildschicht ändert sich für Miniaturansichten wie folgt (d. h. wenn req=tmb ist).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# Skalierung von Miniaturansichten{#thumbnail-scaling}

Schritt 2 der Bildschicht ändert sich für Miniaturansichten wie folgt (d. h. wenn req=tmb ist).

* `2.` Wenn `size=` angegeben ist, passen Sie das (zugeschnittene) Bild mithilfe von Miniaturregeln in den `size=` -rect an. Wenn `size=` nicht angegeben ist, skalieren Sie basierend auf `res=` oder, wenn `res=` nicht angegeben ist, passen Sie das (zugeschnittene) Bild mithilfe der unten beschriebenen Miniaturregeln in den Arbeitsflächenrect an.
