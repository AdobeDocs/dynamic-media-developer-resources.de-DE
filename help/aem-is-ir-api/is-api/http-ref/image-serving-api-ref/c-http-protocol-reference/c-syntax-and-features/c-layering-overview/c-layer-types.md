---
description: Es werden vier Arten von Ebenen unterstützt.
solution: Experience Manager
title: Ebenentypen
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---


# Ebenentypen{#layer-types}

Es werden vier Arten von Ebenen unterstützt.

## Bildebenen {#section-3e53df1437694272aca03f927fc0db07}

Bildebenen müssen über einen Befehl `src=` verfügen, mit dem das Bild angegeben wird, das als Ebene verwendet werden soll. Es kann ein separates Bild mit `mask=` angegeben werden, das als Ebenenmaske verwendet werden soll, oder das Bild hat möglicherweise bereits einen Alpha-Kanal. Die Größe der Bildebenen wird immer aus dem Bild abgeleitet, das Bild wird jedoch oft mit dem Befehl `size=` skaliert, um es passend zu gestalten. Ein Clip-Pfad kann mit `clipPath=` angewendet werden.

## Textebenen {#section-dc2aec6416a340bcb20c1f884323c8d0}

Muss über einen Befehl `text=` oder `textPs=` verfügen, der den Textinhalt in Form eines RTF-Textfragments (Rich-Text-Format) bereitstellt. Textebenen können ihre Größe selbst bestimmen oder explizit Größen erhalten (z. B. wenn Text auf eine bestimmte Breite umgebrochen werden soll oder wenn der Text innerhalb eines bestimmten Bereichs begrenzt werden muss). `textPs=` Unterstützung der Textübertragung in beliebige Formen, die mit  `textFlowPath=` und auf beliebige Pfade definiert wurden, mit  `textPath=`. `textPs=` unterstützt auch das Rendering von Text in das Textfeld oder in die angegebene Form bei beliebigen Winkeln (  `textAngle=`).

## Farbflächenebenen {#section-56dfb672756643dda08dc93294809eb0}

Einfarbige Ebenen werden häufig für Ebene 0 in Vorlagen verwendet, sodass die Größe des zusammengesetzten Bildes fest und unabhängig von Bildinhalten ist. Farbflächenebenen erfordern ein `color=`-Attribut und entweder `size=` oder `mask=` und unterstützen die meisten anderen Befehle und Attribute, um das Erscheinungsbild zu ändern. Einfarbige Ebenen können beliebige Formen mit `clipPath=` erhalten.

## Effektebenen {#section-dd3b628bc6734077af4c0ddcebcee05f}

Ebeneneffekte im Photoshop-Stil, wie z. B. Schlagschatten und Schein-Effekte, werden von IS mithilfe spezieller Unterebenen implementiert, die an Bild-, Text- und Vollfarben-Ebenen angehängt werden können. Diese Effektebenen übernehmen die Maske und Position der übergeordneten Ebene und sind in ihrer Funktionalität eingeschränkt.
