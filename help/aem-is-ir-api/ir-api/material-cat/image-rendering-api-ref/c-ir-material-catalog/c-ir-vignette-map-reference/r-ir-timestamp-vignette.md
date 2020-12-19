---
description: Änderungszeitstempel. Gibt das Datum/die Uhrzeit der letzten Änderung dieser Vignette an.
seo-description: Änderungszeitstempel. Gibt das Datum/die Uhrzeit der letzten Änderung dieser Vignette an.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: d2649e86-8a6f-4f63-ab6a-8b2d8c03f8c0
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---


# TimeStamp{#timestamp}

Änderungszeitstempel. Gibt das Datum/die Uhrzeit der letzten Änderung dieser Vignette an.

Wenn `attribute::UseLastModified` eingestellt ist, werden der letzte `vignette::TimeStamp`- und `catalog::TimeStamp`Wert der Vignette und alle an der Anforderung beteiligten Materialien in der HTTP-Antwort als zuletzt geänderte Kopfzeile zurückgegeben.

>[!NOTE]
>
>Die tatsächliche Dateizeit der Vignettendatei wird zu diesem Zweck nicht verwendet.

`catalog::TimeStamp` wird auch für die Katalogbasierte Cache-Validierung verwendet (siehe  ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Eigenschaften {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Datums-/Uhrzeitwert im Java-Format. Kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, dem 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert mit einem der folgenden Formate sein:

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*: *[!DNL ss]*GMT  *[!DNL offset]*

* *[!DNL hh]* liegt im Bereich von 0 bis 23.
* *[!DNL zzz]* ist ein 3- oder 4-stelliger Zeitzonencode wie &#39;GMT&#39; oder &#39;PST&#39;. Die Sommerzeit muss im Zeitzonencode berücksichtigt werden (z. B. &quot;PST&quot;für Pacific Standard Time im Vergleich zu &quot;PDT&quot;für Pacific Daylight Savings Time).
* *[!DNL offset]* ist ein Zeitzonenversatz in Stunden oder Stunden:Minuten relativ zum GMT. Beispielsweise entspricht &quot;PDT&quot;GMT -7.

Alle Elemente der String-formatierten Datums-/Uhrzeitwerte müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und stattdessen die Änderungszeit der Datei [!DNL *[!DNL catalog]*.ini] verwendet.

## Standard {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` ist das Feld leer oder nicht vorhanden.

## Verwandte Themen {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319),  [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
