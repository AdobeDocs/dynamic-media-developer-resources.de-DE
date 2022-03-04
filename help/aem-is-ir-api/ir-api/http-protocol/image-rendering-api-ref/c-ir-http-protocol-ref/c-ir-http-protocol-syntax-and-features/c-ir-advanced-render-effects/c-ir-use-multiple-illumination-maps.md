---
title: Verwendung mehrerer Beleuchtungskarten
description: Einige Anwendungen erfordern möglicherweise eine andere Beleuchtungskarte für verschiedene Materialien.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Verwendung mehrerer Beleuchtungskarten{#using-multiple-illumination-maps}

Einige Anwendungen erfordern möglicherweise eine andere Beleuchtungskarte für verschiedene Materialien.

Für jede Vignette können bis zu drei Beleuchtungskarten erstellt werden. Die Beleuchtungskarte für einen Rendervorgang wird mit der `illum=` und `gloss=` Befehle.

**Standardauswahl** - Wenn `illum=` oder `gloss=` nicht angegeben sind, verwendet der Renderer die erste erstellte Beleuchtungskarte (normalerweise Karte A, auch &#39;flache&#39; Beleuchtungskarte genannt).

**Automatische Auswahl mit`gloss=`** - Wenn `illum=` ist nicht angegeben oder auf `-1`, vergleicht der Renderer die angegebene `gloss=` Wert mit den Glanzwerten, die mit jeder Beleuchtungskarte in der Vignette verknüpft sind. Sie wählt die Beleuchtungskarte aus, deren Glanzwert dem angegebenen Wert am nächsten kommt. `gloss=`.

**Explizite Auswahl mit`illum=`** - Wenn `illum=` festgelegt und auf `0`, `1`oder `2`, verwendet der Renderer die entsprechende Beleuchtungskarte. `gloss=` wird für die Auswahl der Beleuchtungskarte ignoriert.

Wenn die Vignette nur eine Beleuchtungskarte enthält, verwendet der Renderer diese Zuordnung und ignoriert die `illum=` und `gloss=` Befehle.
