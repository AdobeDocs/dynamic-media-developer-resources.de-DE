---
description: Die vom Vorgang getFotoshopPath zurückgegebenen Bildortkoordinaten.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 8%

---

# [!DNL PerspectiveQuad]{#perspectivequad}

Die vom Vorgang getFotoshopPath zurückgegebenen Bildortkoordinaten.

Syntax

## Parameter {#section-59792c446366456d90de7f5875bad1b0}

| Name | Typ | Beschreibung |
|---|---|---|
| x0 | `xsd:double` | Koordinate der oberen linken X-Achse. |
| Y0 | `xsd:double` | Koordinate der oberen linken Y-Achse. |
| x1 | `xsd:double` | Obere rechte X-Achsen-Koordinate. |
| Y1 | `xsd:double` | Obere rechte Y-Achsen-Koordinate. |
| x2 | `xsd:double` | Koordinate der X-Achse unten rechts. |
| Y2 | `xsd:double` | Koordinate der unteren rechten Y-Achse. |
| x3 | `xsd:double` | Linke untere X-Achsen-Koordinate. |
| Y3 | `xsd:double` | Koordinate der unteren linken Y-Achse. |

## Beispiel {#section-19ed4409ff3a41c9b52a9c9424612927}

Der `PerspectiveQuad` gibt Daten in dieser Reihenfolge zurück:

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
