---
description: Es werden vier Ebenen unterstützt.
solution: Experience Manager
title: Ebenentypen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Ebenentypen{#layer-types}

Es werden vier Ebenen unterstützt.

## Bildebenen {#section-3e53df1437694272aca03f927fc0db07}

Bildebenen müssen über einen Befehl `src=` verfügen, der das Bild angibt, das als Ebene verwendet werden soll. Es kann ein separates Bild mit `mask=` angegeben werden, das als Ebenenmaske verwendet werden soll, oder das Bild kann bereits über einen Alphakanal verfügen. Die Größe der Bildebenen wird immer aus dem Bild abgeleitet, aber das Bild wird häufig mithilfe des Befehls `size=` skaliert, um es an die Größe anzupassen. Ein Clip-Pfad kann mit `clipPath=` angewendet werden.

## Textebenen {#section-dc2aec6416a340bcb20c1f884323c8d0}

Muss über einen Befehl `text=` oder `textPs=` verfügen, der den Textinhalt in Form eines RTF-Textfragments (Rich-Text-Format) bereitstellt. Textebenen können ihre Inhalte selbst anpassen oder explizite Größen erhalten (z. B. wenn Text in eine bestimmte Breite eingeschlossen werden soll oder wenn der Text in einem bestimmten Bereich begrenzt werden muss). `textPs=` Unterstützung des Textflusses in beliebige Formen, definiert mit  `textFlowPath=` und auf beliebige Pfade definiert mit  `textPath=`. `textPs=` unterstützt auch das Rendern von Text in das Textfeld oder die angegebene Form in beliebigen Winkeln (  `textAngle=`).

## Feste Farbschichten {#section-56dfb672756643dda08dc93294809eb0}

In Vorlagen werden häufig durchgehende Farbschichten für Ebene 0 verwendet, sodass die Größe des zusammengesetzten Bildes fest und unabhängig von Bildinhalten ist. Solide Farbschichten erfordern ein `color=`-Attribut, entweder `size=` oder `mask=`, und unterstützen die meisten anderen Befehle und Attribute, um das Erscheinungsbild zu ändern. Solide Farbschichten können beliebige Formen mit `clipPath=` erhalten.

## Effektebenen {#section-dd3b628bc6734077af4c0ddcebcee05f}

Ebeneneffekte im Photoshop-Stil, wie z. B. Schlagschatten und Glüheffekte, werden vom IS mithilfe spezieller Unterschichten implementiert, die an Bild-, Text- und Vollfarbschichten angehängt werden können. Diese Effektebenen übernehmen die übergeordnete Ebenenmaske und -position von der übergeordneten Ebene und sind in ihrer Funktion eingeschränkt.
