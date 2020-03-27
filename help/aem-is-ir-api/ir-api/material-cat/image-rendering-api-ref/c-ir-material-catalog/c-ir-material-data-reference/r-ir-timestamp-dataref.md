---
description: Zeitstempel der Dateiänderung. Gibt das Datum/die Uhrzeit der letzten Änderung des Bildes und/oder der mit diesem Katalogeintrag verknüpften Datendateien an.
seo-description: Zeitstempel der Dateiänderung. Gibt das Datum/die Uhrzeit der letzten Änderung des Bildes und/oder der mit diesem Katalogeintrag verknüpften Datendateien an.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 77ce8bee-7b55-4ff8-8dfb-ebd3ce9c7a8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TimeStamp{#timestamp}

Zeitstempel der Dateiänderung. Gibt das Datum/die Uhrzeit der letzten Änderung des Bildes und/oder der mit diesem Katalogeintrag verknüpften Datendateien an.

Wenn `attribute::UseLastModified` diese Einstellung aktiviert ist, werden die neuesten Werte `catalog::TimeStamp` `vignette::TimeStamp` und Werte aller Materialien und die Vignette, die an der Anforderung beteiligt sind, in der HTTP-Antwort als zuletzt geänderte Kopfzeile zurückgegeben.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Die tatsächlichen Dateizeiten der Bilder oder Datendateien, die an diesen Katalogdatensatz angehängt werden, werden zu diesem Zweck nicht verwendet.

`catalog::TimeStamp` wird auch für die Katalogbasierte Cache-Validierung verwendet (siehe ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Eigenschaften {#section-42f09e375e72492b87a3a486da7df808}

Datums-/Uhrzeitwert im Java-Format. Kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, dem 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert mit einem der folgenden Formate sein:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* liegt im Bereich von 0 bis 23.
* *[!DNL zzz]* ist ein 3- oder 4-stelliger Zeitzonencode wie &#39;GMT&#39; oder &#39;PST&#39;. Die Sommerzeit muss im Zeitzonencode berücksichtigt werden (z. B. &quot;PST&quot;für Pacific Standard Time im Vergleich zu &quot;PDT&quot;für Pacific Daylight Savings Time).
* *[!DNL offset]* ist ein Zeitzonenversatz in Stunden oder Stunden:Minuten relativ zum GMT. Beispielsweise entspricht &quot;PDT&quot;GMT -7.

Alle Elemente der String-formatierten Datums-/Uhrzeitwerte müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und stattdessen die Änderungszeit der Datei *catalog*.ini verwendet.

## Standard {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` ist das Feld leer oder nicht vorhanden.

## Verwandte Themen {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [Vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
