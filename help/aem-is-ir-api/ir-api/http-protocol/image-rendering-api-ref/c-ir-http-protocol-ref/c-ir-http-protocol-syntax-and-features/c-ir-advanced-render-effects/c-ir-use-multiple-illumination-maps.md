---
description: Einige Anwendungen erfordern möglicherweise eine andere Beleuchtungskarte für verschiedene Materialien.
seo-description: Einige Anwendungen erfordern möglicherweise eine andere Beleuchtungskarte für verschiedene Materialien.
seo-title: Verwenden mehrerer Beleuchtungskarten
solution: Experience Manager
title: Verwenden mehrerer Beleuchtungskarten
topic: Scene7 Image Serving - Image Rendering API
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# Verwenden mehrerer Beleuchtungskarten{#using-multiple-illumination-maps}

Einige Anwendungen erfordern möglicherweise eine andere Beleuchtungskarte für verschiedene Materialien.

Für jede Vignette können bis zu drei Beleuchtungskarten erstellt werden. Die Beleuchtungszuordnung für einen Rendervorgang wird mit den Befehlen `illum=` und `gloss=` ausgewählt.

**Standardmäßige** AuswahlWenn weder  `illum=` noch  `gloss=` angegeben, verwendet der Renderer die erste erstellte Beleuchtungskarte (normalerweise Zuordnung A, auch als &quot;flache&quot; Beleuchtungskarte bezeichnet).

**Automatische Auswahl mit`gloss=`** Wenn  `illum=` nicht angegeben oder auf -1 eingestellt ist, vergleicht der Renderer den angegebenen  `gloss=` Wert mit den Glanzwerten, die jeder Beleuchtungskarte in der Vignette zugeordnet sind, und wählt die Beleuchtungskarte, deren Glanzwert der angegebenen  `gloss=`am nächsten ist.

**Explizite Auswahl mit`illum=`** Wenn  `illum=` angegeben und auf 0, 1 oder 2 eingestellt ist, verwendet der Renderer die entsprechende Beleuchtungskarte.  `gloss=` wird zur Auswahl der Beleuchtungskarte ignoriert.

Wenn die Vignette nur eine Beleuchtungszuordnung enthält, verwendet der Renderer diese Zuordnung und ignoriert die Befehle `illum=` und `gloss=`.
