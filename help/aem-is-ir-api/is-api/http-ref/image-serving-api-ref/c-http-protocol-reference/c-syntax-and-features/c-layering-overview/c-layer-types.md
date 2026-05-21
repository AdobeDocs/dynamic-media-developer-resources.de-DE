---
description: Es werden vier Ebenentypen unterstützt.
solution: Experience Manager
title: Ebenentypen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
TQID: 'https://experienceleague.adobe.com/F2ZE-uepvnDVG2OImJIzXm44Wm3KLYfLZrBnk11tE6I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 283
ht-degree: 0%

---

# Ebenentypen{#layer-types}

Es werden vier Ebenentypen unterstützt.

## Bildebenen {#section-3e53df1437694272aca03f927fc0db07}

Bildebenen müssen einen `src=`-Befehl aufweisen, der das als Ebene zu verwendende Bild angibt. Ein separates Bild kann mit `mask=` als Ebenenmaske angegeben werden oder das Bild kann bereits einen Alphakanal haben. Die Größe der Bildebenen wird immer aus dem Bild abgeleitet, aber das Bild wird oft mit dem Befehl `size=` skaliert, um es anzupassen. Ein Clip-Pfad kann mit `clipPath=` angewendet werden.

## Textebenen {#section-dc2aec6416a340bcb20c1f884323c8d0}

Muss einen `text=`- oder `textPs=`-Befehl haben, der den Textinhalt in Form eines RTF-Textfragments (Rich-Text-Formatted) bereitstellt. Textebenen können ihre Größe an ihren Inhalt anpassen oder explizite Größen erhalten. Wenn beispielsweise Text auf eine bestimmte Breite umgebrochen werden soll oder der Text in einem bestimmten Bereich eingeschränkt werden muss. `textPs=` Unterstützung des Flusses von Text in beliebige Formen, die mit `textFlowPath=` definiert wurden, und auf beliebige Pfade, die mit `textPath=` definiert wurden. `textPs=` unterstützt auch das Rendern von Text im Textfeld oder in der angegebenen Form unter beliebigen Winkeln ( `textAngle=`).

## Volltonfarbschichten {#section-56dfb672756643dda08dc93294809eb0}

Für Ebene 0 in Vorlagen werden häufig Volltonfarbschichten verwendet, sodass die Größe des zusammengesetzten Bildes fest und unabhängig von Bildinhalten ist. Für einfarbige Ebenen ist ein `color=` und entweder `size=` oder `mask=` erforderlich. Sie unterstützen die meisten anderen Befehle und Attribute, um das Erscheinungsbild zu ändern. Feste Farbschichten können mit `clipPath=` beliebige Formen erhalten.

## Effektebenen {#section-dd3b628bc6734077af4c0ddcebcee05f}

Ebeneneffekte im Photoshop-Stil, wie z. B. Schlagschatten und Leuchteffekte, werden von IS mithilfe spezieller Unterschichten implementiert, die an Bild-, Text- und Volltonfarbschichten angehängt werden können. Diese Effektebenen übernehmen die Maske und Position der übergeordneten Ebene und sind in ihrer Funktionalität eingeschränkt.
