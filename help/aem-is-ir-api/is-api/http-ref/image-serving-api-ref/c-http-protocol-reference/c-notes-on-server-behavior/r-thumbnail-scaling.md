---
title: Miniaturansichten skalieren
description: Schritt 2 der Bildebenen-Transformationen wird für Miniaturen wie folgt geändert (d. h. wenn req=tmb ist).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# Miniaturansichten skalieren{#thumbnail-scaling}

Schritt 2 der Bildebenen-Transformationen wird für Miniaturen wie folgt geändert (d. h. wenn req=tmb ist).

* `2.` Wenn `size=` angegeben ist, passen Sie das (zugeschnittene) Bild mithilfe von Miniaturansichtsregeln in das `size=` an. Wenn `size=` nicht angegeben ist, skalieren Sie anhand der `res=` oder fügen Sie, falls `res=` nicht angegeben ist, das (zugeschnittene) Bild mithilfe der unten beschriebenen Miniaturansichtsregeln in das Arbeitsflächen-React ein.
