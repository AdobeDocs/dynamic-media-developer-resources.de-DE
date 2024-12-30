---
title: Verwenden mehrerer Beleuchtungskarten
description: Einige Anwendungen erfordern möglicherweise eine andere Beleuchtungskarte für verschiedene Arten von Materialien.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Verwenden mehrerer Beleuchtungskarten{#using-multiple-illumination-maps}

Einige Anwendungen erfordern möglicherweise eine andere Beleuchtungskarte für verschiedene Arten von Materialien.

Für jede Vignette können bis zu drei Beleuchtungskarten erstellt werden. Die Beleuchtungszuordnung für einen Render-Vorgang wird mit den Befehlen `illum=` und/oder `gloss=` ausgewählt.

**Standardauswahl** - Wenn keine `illum=` oder `gloss=` angegeben sind, verwendet der Renderer die erste erstellte Illumination Map (in der Regel Map A, auch „Flache“ Illumination Map genannt).

**Automatische Auswahl mit`gloss=`** - Wenn `illum=` nicht angegeben oder auf `-1` gesetzt ist, vergleicht der Renderer den angegebenen `gloss=` mit den Glanzwerten, die jeder Illuminationskarte in der Vignette zugeordnet sind. Sie wählt die Beleuchtungskarte aus, deren Glanzwert am nächsten an der angegebenen `gloss=` liegt.

**Explizite Auswahl mit`illum=`** - Wenn `illum=` angegeben und auf `0`, `1` oder `2` gesetzt ist, verwendet der Renderer die entsprechende Beleuchtungszuordnung. `gloss=` wird bei der Auswahl der Beleuchtungszuordnung ignoriert.

Wenn die Vignette nur eine Illumination Map enthält, verwendet der Renderer diese Map und ignoriert die `illum=`- und `gloss=`.
