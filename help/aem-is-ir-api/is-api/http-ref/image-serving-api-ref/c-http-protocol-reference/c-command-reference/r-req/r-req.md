---
description: Anfragetyp. Gibt den Anfragetyp an.
solution: Experience Manager
title: Erf
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
TQID: 'https://experienceleague.adobe.com/-WzHmELeamQBbVFlzXNKbDE3fKVXw4x6pSoEz0LHav4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 90
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
