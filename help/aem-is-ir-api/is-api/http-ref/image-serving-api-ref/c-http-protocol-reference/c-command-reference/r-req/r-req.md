---
description: Anforderungstyp Gibt den Anforderungstyp an.
seo-description: Anforderungstyp Gibt den Anforderungstyp an.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: b888be10-89e5-4b41-a2bd-f83533ea2481
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 9%

---


# req{#req}

Anforderungstyp Gibt den Anforderungstyp an.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`optionen`*]`

* [Katalogprops](r-catalogprops.md)
* [vorhanden](r-exists.md)
* [imageprops](r-imageprops.md)
* [imageset](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [Karte](r-map-req.md)
* [Maske](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [message](r-message.md)
* [props](r-props.md)
* [auflösen](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [setzen](r-set.md)
* [als Target vorsehen](r-targets.md)
* [tmb](r-tmb.md)
* [userdata](r-userdata.md)
* [validieren](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

Sofern in den detaillierten Beschreibungen nichts anderes angegeben ist, gibt der Server `text` Antworten mit dem MIME-Typ `text/plain` zurück. Bei vielen Anforderungstypen können Sie einen Antworttyp angeben, z. B. `text`, das ist in der Regel der Standardwert `javascript`, `xml` oder `json`. Die zugehörigen Antwort-MIME-Typen sind `text/plain`, `text/javascript`, `text/xml` und `text/javascript`.

Sofern nicht anders angegeben, formatieren Antworten die Antwort als Satz von `name=value`-Paaren.

Siehe [Eigenschaften](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
