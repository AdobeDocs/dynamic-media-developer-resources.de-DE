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

Für jede Vignette können bis zu drei Beleuchtungskarten erstellt werden. Die Beleuchtungskarte für einen Rendervorgang wird mit den Befehlen `illum=` und `gloss=` ausgewählt.

**Standardauswahl** - Wenn `illum=` oder `gloss=` nicht angegeben sind, verwendet der Renderer die erste erstellte Beleuchtungskarte (normalerweise Zuordnung A, auch als &quot;flache&quot;Beleuchtungskarte bezeichnet).

**Automatische Auswahl mit`gloss=`** - Wenn `illum=` nicht angegeben oder auf `-1` gesetzt ist, vergleicht der Renderer den angegebenen `gloss=` -Wert mit den Glanzwerten, die jeder Beleuchtungskarte in der Vignette zugeordnet sind. Sie wählt die Beleuchtungskarte aus, deren Glanzwert dem angegebenen `gloss=` am nächsten ist.

**Explizite Auswahl mit`illum=`** - Wenn `illum=` angegeben und auf `0`, `1` oder `2` festgelegt ist, verwendet der Renderer die entsprechende Beleuchtungskarte. `gloss=` wird bei Auswahl der Beleuchtungskarte ignoriert.

Wenn die Vignette nur eine Beleuchtungskarte enthält, verwendet der Renderer diese Zuordnung und ignoriert die Befehle `illum=` und `gloss=`.
