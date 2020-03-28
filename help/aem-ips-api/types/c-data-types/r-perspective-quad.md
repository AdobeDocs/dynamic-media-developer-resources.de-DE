---
description: Bildstandortkoordinaten, die vom getFotoshopPath-Vorgang zurückgegeben werden.
seo-description: Bildstandortkoordinaten, die vom getFotoshopPath-Vorgang zurückgegeben werden.
seo-title: PerectiveQuad
solution: Experience Manager
title: PerectiveQuad
topic: Scene7 Image Production System API
uuid: e83b7b8c-995b-4ac0-ace5-491f7e98674d
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4

---


# PerectiveQuad{#perspectivequad}

Bildstandortkoordinaten, die vom getFotoshopPath-Vorgang zurückgegeben werden.

Syntax

## Parameter {#section-59792c446366456d90de7f5875bad1b0}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`x0`*` | `xsd:double` | Die X-Achsen-Koordinate oben links. |
| ` *`y0`*` | `xsd:double` | Koordinate der y-Achse oben links |
| ` *`x1`*` | `xsd:double` | Koordinate oben rechts x-Achse. |
| ` *`y1`*` | `xsd:double` | Koordinate rechts oben. |
| ` *`x2`*` | `xsd:double` | Die X-Achsen-Koordinate unten rechts. |
| ` *`y2`*` | `xsd:double` | Unten rechts y-Achsen-Koordinate. |
| ` *`x3`*` | `xsd:double` | X-Achsen-Koordination unten links. |
| ` *`y3`*` | `xsd:double` | Koordinate der Y-Achse unten links |

## Beispiel {#section-19ed4409ff3a41c9b52a9c9424612927}

Der `PerspectiveQuad` Typ gibt Daten in der folgenden Reihenfolge zurück:

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

