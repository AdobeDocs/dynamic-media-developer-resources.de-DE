---
description: Anfragetyp. Gibt den Anfragetyp an.
solution: Experience Manager
title: Erf
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 8%

---

# Erf{#req}

Anfragetyp. Gibt den Anfragetyp an.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`options`*]`

* [catalogProps](r-catalogprops.md)
* [vorhanden](r-exists.md)
* [imageProps](r-imageprops.md)
* [Bildsatz](r-imageset-req.md)
* [img](r-img.md)
* [LoadCache](r-loadcache.md)
* [Karte](r-map-req.md)
* [Maske](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [message](r-message.md)
* [props](r-props.md)
* [auflösen](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [setzen](r-set.md)
* [als Target vorsehen](r-targets.md)
* [TMB](r-tmb.md)
* [UserData](r-userdata.md)
* [validieren](r-is-http-validate.md)
* [spätplattieren](r-xlate.md)
* [XMP](r-xmp.md)

Sofern in den detaillierten Beschreibungen nicht anders angegeben, gibt der Server `text` Antworten mit dem MIME-Typ `text/plain` zurück. Bei vielen Anfragetypen können Sie einen Antworttyp angeben, z. B. `text`, der normalerweise der Standard-, `javascript`-, `xml`- oder `json` ist. Die zugehörigen Antwort-MIME-Typen sind `text/plain`, `text/javascript`, `text/xml` bzw. `text/javascript`.

Sofern nicht anders angegeben, formatieren Antworten die Antwort als Satz von `name=value`.

Siehe [Eigenschaften](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
