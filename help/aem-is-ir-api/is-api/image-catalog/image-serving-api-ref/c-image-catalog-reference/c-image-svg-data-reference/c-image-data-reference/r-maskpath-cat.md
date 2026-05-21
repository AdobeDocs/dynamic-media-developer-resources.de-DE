---
description: Dateipfad maskieren. Relativer oder absoluter Pfad und Name für eine Maskenbilddatei, die mit diesem Katalogeintrag verknüpft ist.
solution: Experience Manager
title: Maskenpfad
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
TQID: 'https://experienceleague.adobe.com/tUXD-vnkr3qkaH3B-dE-e9wfSPXAcnwRbqG9KuJej9E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 175
ht-degree: 2%

---

# Maskenpfad{#maskpath}

Dateipfad maskieren. Relativer oder absoluter Pfad und Name für eine Maskenbilddatei, die mit diesem Katalogeintrag verknüpft ist.

Ermöglicht das Anhängen separater Masken an Bilder.

Der Server verwendet die unter „Verwalten von Source-Daten[ beschriebenen Regeln ](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) Pfadauflösung, um die Datendatei zu finden.

## Eigenschaften {#section-cdc3b7e2811e41008479cd97887c01b7}

Text-Zeichenfolgenwert. Optional. Wenn angegeben, muss es sich um einen gültigen relativen oder absoluten Dateipfad des Image-Servers handeln. `attribute::DefaultExt` wird angehängt, wenn keine Dateiendung vorhanden ist.

Wenn sowohl ein Hauptbild (`catalog::Path`) als auch ein Maskenbild (`catalog::MaskPath`) in einem Katalogdatensatz definiert sind, müssen beide exakt die gleiche Pixelgröße haben. Maskenbilder müssen 8-Bit-Graustufen aufweisen.

`mask=` in der Anfrage überschreibt `catalog::MaskPath`.

`catalog::MaskPath` überschreibt den Alphakanal im Hauptbild (`catalog::Path`), falls vorhanden, und wenn der Alphakanal nicht zugeordnet (d. h. nicht vormultipliziert) ist. Wenn das Bild Alpha vormultipliziert ist, wird `catalog::MaskPath` ignoriert und der Alphakanal wird immer verwendet.

## Standard {#section-78533e35bfec469ba087cb68a35bb81b}

Keine.

## Verwandte Themen {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
