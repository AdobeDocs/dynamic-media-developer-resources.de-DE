---
title: TimeStamp
description: Zeitstempel der Dateiänderung. Gibt Datum/Uhrzeit der letzten Änderung des Bildes und/oder der an diesen Katalogdatensatz angehängten Datendateien an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Zeitstempel der Dateiänderung. Gibt Datum/Uhrzeit der letzten Änderung des Bildes und/oder der an diesen Katalogdatensatz angehängten Datendateien an.

Wenn `attribute::UseLastModified` festgelegt ist, wird der letzte der `catalog::TimeStamp` - und `vignette::TimeStamp` -Werte aller Materialien und die Vignette, die an der Anfrage beteiligt sind, in der HTTP-Antwort als zuletzt geänderte Kopfzeile zurückgegeben.

>[!NOTE]
>
>Die tatsächlichen Dateizeiten der Bilder oder Datendateien, die an diesen Katalogdatensatz angehängt sind, werden zu diesem Zweck nie verwendet.

Der `catalog::TimeStamp` wird auch für die Katalogbasierte Cache-Validierung verwendet (siehe [Attribut::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)).

## Eigenschaften {#section-42f09e375e72492b87a3a486da7df808}

Datums-/Uhrzeitwert im Java™-Format. Dies kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, der 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert mit einem der folgenden Formate sein:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* liegt im Bereich von 0-23.
* *[!DNL zzz]* ist ein aus drei oder vier Zeichen bestehender Zeitzonen-Code, z. B. &quot;GMT&quot;oder &quot;PST&quot;. Die Sommerzeit muss im Zeitzonencode berücksichtigt werden. Beispiel: &quot;PST&quot;für die Pacific Standard-Zeit im Vergleich zu &quot;PDT&quot;für die Sommerzeit im Pazifik.
* *[!DNL offset]* ist ein Zeitzonenversatz in Stunden oder Stunden:Minuten relativ zu GMT. Beispielsweise entspricht &quot;PDT&quot;GMT -7.

Alle Elemente von Datums-/Uhrzeitwerten im Zeichenfolgenformat müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und stattdessen wird die Änderungszeit der Datei *catalog*.ini verwendet.

## Standard {#section-e2c126c9e7294662b23944ab8d14866b}

Der Wert `attribute::TimeStamp` ist das leere oder nicht vorhandene Feld.

## Verwandte Themen {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
