---
title: Zeitstempel
description: Zeitstempel der Standardänderung. Stellt einen Standardwert für Katalog-Zeitstempel und Vignetten-Zeitstempel bereit. Wenn nicht anders angegeben, verwendet der Server das Änderungsdatum/die Änderungszeit dieser Datei catalog.ini.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 1%

---

# Zeitstempel{#timestamp}

Zeitstempel der Standardänderung. Stellt einen Standardwert für `catalog::TimeStamp` und `vignette::TimeStamp` bereit. Wenn nicht anders angegeben, verwendet der Server das Änderungsdatum/die Änderungszeit dieser Datei catalog.ini.

## Eigenschaften {#section-910e2562b41c47b78ee6216deeabbbd5}

Datums-/Uhrzeitwert im Java™-Format. Kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, dem 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert mit einem der folgenden Formate sein:

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* liegt im Bereich von 0 bis 23.

*[!DNL zzz]* ist ein drei- oder vierstelliger Zeitzonencode wie „GMT“ oder „PST“. Die Sommerzeit muss im Zeitzonencode berücksichtigt werden (z. B. „PST“ für Pacific Standard Time im Vergleich zu „PDT“ für Pacific Daylight Savings Time).

*[!DNL offset]* ist ein Zeitzonenversatz in Stunden oder Stunden:Minuten, relativ zu GMT. „PDT“ entspricht beispielsweise „GMT -7“.

Alle Elemente von zeichenfolgenformatierten Datums-/Uhrzeitwerten müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und stattdessen die Änderungszeit der Datei [!DNL *[!DNL catalog]*.ini] verwendet.

## Standard {#section-65fb29a9ea2044df8cb9fe295eb14872}

Wenn leer oder nicht definiert, verwendet der Server die Dateiänderungszeit dieser [!DNL *[!DNL catalog]*.ini]-Datei.

## Verwandte Themen {#section-764188f9b1734ad1a6270f5fecd28532}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1), [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
