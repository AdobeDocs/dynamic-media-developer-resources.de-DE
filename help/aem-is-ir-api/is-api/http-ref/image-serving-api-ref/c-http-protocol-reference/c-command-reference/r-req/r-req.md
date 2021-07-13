---
description: Anfragetyp. Gibt den Anforderungstyp an.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 9%

---

# req{#req}

Anfragetyp. Gibt den Anforderungstyp an.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`optionen`*]`

* [Katalogproben](r-catalogprops.md)
* [vorhanden](r-exists.md)
* [imageprops](r-imageprops.md)
* [imageset](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [Karte](r-map-req.md)
* [mask](r-mask-req.md)
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

Sofern in den detaillierten Beschreibungen nichts anderes angegeben ist, gibt der Server `text` Antworten mit dem MIME-Typ `text/plain` zurück. Bei vielen Anfragetypen können Sie einen Antworttyp angeben, z. B. `text`, der normalerweise der Standardwert `javascript`, `xml` oder `json` ist. Die zugehörigen Antwort-MIME-Typen sind `text/plain`, `text/javascript`, `text/xml` und `text/javascript`.

Sofern nicht anders angegeben, formatieren Antworten die Antwort als Satz von `name=value`-Paaren.

Siehe [Eigenschaften](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
