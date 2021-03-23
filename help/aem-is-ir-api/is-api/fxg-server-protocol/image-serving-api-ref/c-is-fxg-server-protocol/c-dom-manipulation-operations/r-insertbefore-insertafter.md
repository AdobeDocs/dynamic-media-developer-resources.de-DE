---
description: Legen Sie XML vor oder nach einer Node fest.
seo-description: Legen Sie XML vor oder nach einer Node fest.
seo-title: insertBefore,insertAfter
solution: Experience Manager
title: insertBefore,insertAfter
uuid: 5ac0f675-333b-4f85-abe0-642cf96de425
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 2%

---


# insertBefore,insertAfter{#insertbefore-insertafter}

Legen Sie XML vor oder nach einer Node fest.

`insertBefore=<xml>, insertAfter=<xml>`

Wenn für ein FXG-Knotenelement ein `s7:elementID` definiert ist, können mit diesem Befehl XML-Fragmente vor oder nach diesem Knoten hinzugefügt werden.

## Beispiel {#section-1fc8d4135ef94b60b838391e1568e70e}

Wenn wir ein Gruppen-Tag wie dieses haben:

`<Group visible="true" s7:elementID="inner_shape">`

dann:

`insertBefore.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

Ergebnisse:

`<Rect height="75" rotation="0" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" width="75" x="74.354" y="182.762"><fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill></Rect><Group s7:elementID="inner_shape" visible="true">`

`insertAfter.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

Ergebnisse:

`<Group s7:elementID="inner_shape" visible="true"> <Rect ai:knockout="0" d:userLabel="Background" height="392.581" visible="true" width="319.953" x="0.75" y="0.75"> <fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill> </Rect>`
