---
description: Maskieren Sie den Dateipfad. Relativer oder absoluter Pfad und Name für eine mit diesem Katalogdatensatz verknüpfte Maskenbilddatei.
solution: Experience Manager
title: MaskPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# MaskPath{#maskpath}

Maskieren Sie den Dateipfad. Relativer oder absoluter Pfad und Name für eine mit diesem Katalogdatensatz verknüpfte Maskenbilddatei.

Ermöglicht das Anhängen separater Masken an Bilder.

Der Server verwendet die in [Verwalten von Quelldaten](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) , um die Datendatei zu finden.

## Eigenschaften {#section-cdc3b7e2811e41008479cd97887c01b7}

Textzeichenfolgenwert. Optional. Wenn angegeben, muss es sich um einen gültigen relativen oder absoluten Image Server-Dateipfad handeln. `attribute::DefaultExt` wird angehängt, wenn kein Dateisuffix vorhanden ist.

Wenn beide Hauptbilder ( `catalog::Path`) und ein Maskenbild ( `catalog::MaskPath`) in einem Katalogdatensatz definiert sind, müssen beide genau dieselbe Pixelgröße aufweisen. Maskenbilder müssen 8-Bit-Graustufen sein.

`mask=` in der Anfrage überschreiben `catalog::MaskPath`.

`catalog::MaskPath` überschreibt den Alphakanal im Hauptbild ( `catalog::Path`), sofern vorhanden und wenn der Alphakanal nicht zugeordnet ist (d. h. nicht vormultipliziert). Wenn das Bild-Alpha vormultipliziert wird, `catalog::MaskPath` wird ignoriert und der Alphakanal wird immer verwendet.

## Standard {#section-78533e35bfec469ba087cb68a35bb81b}

Keine.

## Verwandte Themen {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
