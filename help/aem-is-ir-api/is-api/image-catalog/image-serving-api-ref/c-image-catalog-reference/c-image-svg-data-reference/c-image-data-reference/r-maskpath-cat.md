---
description: Pfad der Maskendatei. Relativer oder absoluter Pfad und Name für eine mit diesem Katalogdatensatz verknüpfte Maskenbilddatei.
seo-description: Pfad der Maskendatei. Relativer oder absoluter Pfad und Name für eine mit diesem Katalogdatensatz verknüpfte Maskenbilddatei.
seo-title: MaskPath
solution: Experience Manager
title: MaskPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a2d1f08a-0a26-41a6-9be2-f5cc2afb15c4
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# MaskPath{#maskpath}

Pfad der Maskendatei. Relativer oder absoluter Pfad und Name für eine mit diesem Katalogdatensatz verknüpfte Maskenbilddatei.

Ermöglicht das Anhängen separater Masken an Bilder.

Der Server verwendet die unter [Verwalten der Quelldaten](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) beschriebenen Pfadauflösungsregeln, um die Datendatei zu finden.

## Eigenschaften {#section-cdc3b7e2811e41008479cd97887c01b7}

Textzeichenfolgenwert. Optional. Wenn angegeben, muss es sich um einen gültigen relativen oder absoluten Image Server-Dateipfad handeln. `attribute::DefaultExt` wird angehängt, wenn kein Dateisuffix vorhanden ist.

Wenn sowohl ein Hauptbild ( `catalog::Path`) als auch ein Maskenbild ( `catalog::MaskPath`) in einem Katalogdatensatz definiert sind, müssen beide exakt dieselbe Pixelgröße haben. Maskenbilder müssen 8-Bit-Graustufen aufweisen.

`mask=` in der Anforderung außer Kraft `catalog::MaskPath`.

`catalog::MaskPath` überschreibt den Alpha-Kanal im Hauptbild ( `catalog::Path`), falls vorhanden und wenn der Alpha-Kanal nicht zugeordnet ist (d. h. nicht vormultipliziert). Wenn das Alpha-Bild vormultipliziert wird, `catalog::MaskPath` wird es ignoriert und der Alpha-Kanal wird immer verwendet.

## Standard {#section-78533e35bfec469ba087cb68a35bb81b}

Keine.

## Verwandte Themen {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
