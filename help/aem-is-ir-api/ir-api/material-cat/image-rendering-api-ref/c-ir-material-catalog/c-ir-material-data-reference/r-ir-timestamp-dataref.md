---
description: Zeitstempel der Dateiänderung. Gibt Datum/Uhrzeit der letzten Änderung des Bildes und/oder der an diesen Katalogdatensatz angehängten Datendateien an.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Zeitstempel der Dateiänderung. Gibt Datum/Uhrzeit der letzten Änderung des Bildes und/oder der an diesen Katalogdatensatz angehängten Datendateien an.

Wenn `attribute::UseLastModified` festgelegt ist, werden die neuesten `catalog::TimeStamp`- und `vignette::TimeStamp`-Werte aller Materialien und die an der Anforderung beteiligte Vignette in der HTTP-Antwort als zuletzt geänderte Kopfzeile zurückgegeben.

>[!NOTE]
>
>Die tatsächlichen Dateizeiten der Bilder oder Datendateien, die an diesen Katalogdatensatz angehängt sind, werden zu diesem Zweck nie verwendet.

`catalog::TimeStamp` wird auch für die Katalogbasierte Cache-Validierung verwendet (siehe  ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Eigenschaften {#section-42f09e375e72492b87a3a486da7df808}

Datums-/Uhrzeitwert im Java-Format. Kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, dem 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert mit einem der folgenden Formate sein:

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* GMT  *[!DNL offset]*

* *[!DNL hh]* liegt im Bereich von 0 bis 23.
* *[!DNL zzz]* ist ein 3- oder 4-stelliger Zeitzonen-Code wie &quot;GMT&quot;oder &quot;PST&quot;. Die Sommerzeit muss im Zeitzonencode berücksichtigt werden (z. B. &quot;PST&quot;für die Pacific Standard Time, im Gegensatz zu &quot;PDT&quot;für die Sommerzeit im Pazifik).
* *[!DNL offset]* ist ein Zeitzonenversatz in Stunden oder Stunden:Minuten relativ zu GMT. Beispielsweise entspricht &quot;PDT&quot;GMT -7.

Alle Elemente von String formatierten Datums-/Uhrzeitwerten müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und stattdessen wird die Änderungszeit der Datei *catalog*.ini verwendet.

## Standard {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` ist, ist das Feld leer oder nicht vorhanden.

## Verwandte Themen {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4),  [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
