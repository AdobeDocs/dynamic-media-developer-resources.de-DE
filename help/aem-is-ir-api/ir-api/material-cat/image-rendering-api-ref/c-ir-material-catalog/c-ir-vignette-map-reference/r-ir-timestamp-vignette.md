---
description: Zeitstempel der Änderung. Gibt Datum/Uhrzeit der letzten Änderung dieser Vignette an.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Zeitstempel der Änderung. Gibt Datum/Uhrzeit der letzten Änderung dieser Vignette an.

Wenn `attribute::UseLastModified` festgelegt ist, wird die neueste `vignette::TimeStamp` und `catalog::TimeStamp`-Wert der Vignette und alle an der Anfrage beteiligten Materialien werden in der HTTP-Antwort als Header der letzten Änderung zurückgegeben.

>[!NOTE]
>
>Die tatsächliche Dateizeit der Vignettendatei wird zu diesem Zweck nie verwendet.

`catalog::TimeStamp` wird auch für die Katalogbasierte Cache-Validierung verwendet (siehe [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## Eigenschaften {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Datums-/Uhrzeitwert im Java-Format. Kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, dem 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert mit einem der folgenden Formate sein:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* liegt im Bereich von 0 bis 23.
* *[!DNL zzz]* ist ein 3- oder 4-stelliger Zeitzonen-Code wie &quot;GMT&quot;oder &quot;PST&quot;. Die Sommerzeit muss im Zeitzonencode berücksichtigt werden (z. B. &quot;PST&quot;für die Pacific Standard Time, im Gegensatz zu &quot;PDT&quot;für die Sommerzeit im Pazifik).
* *[!DNL offset]* ist ein Zeitzonenversatz in Stunden oder Stunden:Minuten relativ zu GMT. Beispielsweise entspricht &quot;PDT&quot;GMT -7.

Alle Elemente von String formatierten Datums-/Uhrzeitwerten müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und die Änderungszeit von [!DNL *[!DNL catalog]* Die .ini]-Datei wird stattdessen verwendet.

## Standard {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` ist, ist das Feld leer oder nicht vorhanden.

## Verwandte Themen {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
