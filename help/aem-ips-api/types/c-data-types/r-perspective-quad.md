---
description: Bildstandortkoordinaten, die vom getFotoshopPath -Vorgang zurückgegeben werden.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 18%

---

# PerspectiveQuad{#perspectivequad}

Bildstandortkoordinaten, die vom getFotoshopPath -Vorgang zurückgegeben werden.

Syntax

## Parameter {#section-59792c446366456d90de7f5875bad1b0}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`x0`*` | `xsd:double` | X-Achsen-Koordinate oben links. |
| `*`y0`*` | `xsd:double` | Koordinate der Y-Achse oben links. |
| `*`x1`*` | `xsd:double` | Koordinate der X-Achse oben rechts. |
| `*`y1`*` | `xsd:double` | Koordinate der y-Achse oben rechts. |
| `*`x2`*` | `xsd:double` | Koordinate der X-Achse unten rechts. |
| `*`y2`*` | `xsd:double` | Koordinate der Y-Achse unten rechts. |
| `*`x3`*` | `xsd:double` | X-Achsen-Koordinate unten links. |
| `*`y3`*` | `xsd:double` | Koordinate der Y-Achse unten links. |

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

