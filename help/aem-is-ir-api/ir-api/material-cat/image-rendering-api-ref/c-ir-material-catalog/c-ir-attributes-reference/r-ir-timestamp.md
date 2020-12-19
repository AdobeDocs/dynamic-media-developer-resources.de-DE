---
description: Standardzeitstempel für die Änderung. Stellt einen Standardwert für den Katalog TimeStamp und Vignette TimeStamp bereit. Falls nicht angegeben, verwendet der Server das Änderungsdatum/-zeitpunkt dieser Datei "catalog.ini".
seo-description: Standardzeitstempel für die Änderung. Stellt einen Standardwert für den Katalog TimeStamp und Vignette TimeStamp bereit. Falls nicht angegeben, verwendet der Server das Änderungsdatum/-zeitpunkt dieser Datei "catalog.ini".
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 10ceb600-1ed9-46a1-ae07-889d601ac0f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# TimeStamp{#timestamp}

Standardzeitstempel für die Änderung. Stellt einen Standardwert für Katalog bereit::TimeStamp und Vignette::TimeStamp. Falls nicht angegeben, verwendet der Server das Änderungsdatum/-zeitpunkt dieser Datei &quot;catalog.ini&quot;.

## Eigenschaften {#section-910e2562b41c47b78ee6216deeabbbd5}

Datums-/Uhrzeitwert im Java-Format. Kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, dem 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert mit einem der folgenden Formate sein:

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* GMT  *[!DNL offset]*

*[!DNL hh]* liegt im Bereich von 0 bis 23.

*[!DNL zzz]* ist ein 3- oder 4-stelliger Zeitzonencode wie &#39;GMT&#39; oder &#39;PST&#39;. Die Sommerzeit muss im Zeitzonencode berücksichtigt werden (z. B. &quot;PST&quot;für Pacific Standard Time im Vergleich zu &quot;PDT&quot;für Pacific Daylight Savings Time).

*[!DNL offset]* ist ein Zeitzonenversatz in Stunden oder Stunden:Minuten relativ zum GMT. Beispielsweise entspricht &quot;PDT&quot;GMT -7.

Alle Elemente der String-formatierten Datums-/Uhrzeitwerte müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und stattdessen die Änderungszeit der Datei [!DNL *[!DNL catalog]*.ini] verwendet.

## Standard {#section-65fb29a9ea2044df8cb9fe295eb14872}

Wenn leer oder nicht definiert, verwendet der Server die Dateiänderungszeit dieser [!DNL *[!DNL catalog]*.ini] Datei.

## Verwandte Themen {#section-764188f9b1734ad1a6270f5fecd28532}

[Katalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [Vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1),  [Attribut::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [Attribut::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
