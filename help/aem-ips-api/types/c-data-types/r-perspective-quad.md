---
description: Bildstandortkoordinaten, die vom getFotoshopPath-Vorgang zurückgegeben werden.
solution: Experience Manager
title: PerectiveQuad
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 17%

---


# PerectiveQuad{#perspectivequad}

Bildstandortkoordinaten, die vom getFotoshopPath-Vorgang zurückgegeben werden.

Syntax

## Parameter {#section-59792c446366456d90de7f5875bad1b0}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`x0`*` | `xsd:double` | Die X-Achsen-Koordinate oben links. |
| `*`y0`*` | `xsd:double` | Koordinate der y-Achse oben links |
| `*`x1`*` | `xsd:double` | Koordinate oben rechts x-Achse. |
| `*`y1`*` | `xsd:double` | Koordinate rechts oben. |
| `*`x2`*` | `xsd:double` | Die X-Achsen-Koordinate unten rechts. |
| `*`y2`*` | `xsd:double` | Unten rechts y-Achsen-Koordinate. |
| `*`x3`*` | `xsd:double` | X-Achsen-Koordination unten links. |
| `*`y3`*` | `xsd:double` | Koordinate der Y-Achse unten links |

## Beispiel {#section-19ed4409ff3a41c9b52a9c9424612927}

Der Typ `PerspectiveQuad` gibt Daten in dieser Reihenfolge zurück:

```
<complexType name="PerspectiveQuad">
        <sequence>
            <element name="x0" type="xsd:double"/>
            <element name="y0" type="xsd:double"/>
            <element name="x1" type="xsd:double"/>
            <element name="y1" type="xsd:double"/>
            <element name="x2" type="xsd:double"/>
            <element name="y2" type="xsd:double"/>
            <element name="x3" type="xsd:double"/>
            <element name="y3" type="xsd:double"/>
        </sequence>
```

>[!MORELIKETHIS]
>
>* [getFotoshopPath](../../operations/c-operations-intro/c-methods/r-get-photoshop-path.md#reference-545f902f84194951ac04e947fdc803b9)

