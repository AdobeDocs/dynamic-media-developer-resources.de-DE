---
title: Zeitstempel
description: Zeitstempel der Dateiänderung. Gibt das Datum/die Uhrzeit der letzten Änderung des Bildes und/oder der Datendateien an, die an diesen Katalogdatensatz angehängt sind.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 1%

---

# Zeitstempel{#timestamp}

Zeitstempel der Dateiänderung. Gibt das Datum/die Uhrzeit der letzten Änderung des Bildes und/oder der Datendateien an, die an diesen Katalogdatensatz angehängt sind.

Wenn `attribute::UseLastModified` festgelegt ist, wird der neueste der `catalog::TimeStamp`- und `vignette::TimeStamp`-Werte aller Materialien und der an der Anfrage beteiligten Vignette in der HTTP-Antwort als Kopfzeile der letzten Änderung zurückgegeben.

>[!NOTE]
>
>Die tatsächlichen Dateizeiten der an diesen Katalogdatensatz angehängten Bild- oder Datendateien werden zu diesem Zweck nie verwendet.

Die `catalog::TimeStamp` wird auch für die katalogbasierte Cache-Validierung verwendet (siehe [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)).

## Eigenschaften {#section-42f09e375e72492b87a3a486da7df808}

Datums-/Uhrzeitwert im Java™-Format. Dies kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, dem 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert in einem der folgenden Formate sein:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* liegt im Bereich von 0-23.
* *[!DNL zzz]* ist ein drei- oder vierstelliger Zeitzonencode wie „GMT“ oder „PST“. Die Sommerzeit muss im Zeitzonen-Code berücksichtigt werden. Beispiel: „PST“ für Pacific Standard Time im Vergleich zu „PDT“ für Pacific Daylight Saving Time.
* *[!DNL offset]* ist ein Zeitzonenversatz in Stunden oder Stunden:Minuten, relativ zu GMT. „PDT“ entspricht beispielsweise „GMT -7“.

Alle Elemente von zeichenfolgenformatierten Datums-/Uhrzeitwerten müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und stattdessen die Änderungszeit der Datei *catalog*.ini verwendet.

## Standard {#section-e2c126c9e7294662b23944ab8d14866b}

Das `attribute::TimeStamp` ist das Feld, das leer oder nicht vorhanden ist.

## Verwandte Themen {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
