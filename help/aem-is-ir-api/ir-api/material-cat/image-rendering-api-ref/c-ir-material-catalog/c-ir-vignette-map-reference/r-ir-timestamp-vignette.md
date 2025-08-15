---
title: Zeitstempel
description: Zeitstempel der Änderung. Gibt das Datum/die Uhrzeit der letzten Änderung dieser Vignette an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# Zeitstempel{#timestamp}

Zeitstempel der Änderung. Gibt das Datum/die Uhrzeit der letzten Änderung dieser Vignette an.

Wenn `attribute::UseLastModified` festgelegt ist, werden der neueste `vignette::TimeStamp` und `catalog::TimeStamp`Wert der Vignette und aller an der Anfrage beteiligten Materialien in der HTTP-Antwort als Kopfzeile der letzten Änderung zurückgegeben.

>[!NOTE]
>
>Die eigentliche Dateizeit der Vignettendatei wird zu diesem Zweck nie verwendet.

Die `catalog::TimeStamp` wird auch für die katalogbasierte Cache-Validierung verwendet. Siehe [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## Eigenschaften {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Datums-/Uhrzeitwert im Java™-Format. Dies kann entweder die ganzzahlige Anzahl von Millisekunden seit Mitternacht, dem 1. Januar 1970 UTC/GMT oder ein Datums-/Uhrzeitzeichenfolgenwert in einem der folgenden Formate sein:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*&#x200B;GMT *[!DNL offset]*

* *[!DNL hh]* liegt im Bereich von 0-23.
* *[!DNL zzz]* ist ein drei- oder vierstelliger Zeitzonencode wie „GMT“ oder „PST“. Die Sommerzeit muss im Zeitzonencode berücksichtigt werden (z. B. „PST“ für Pacific Standard Time im Vergleich zu „PDT“ für Pacific Daylight Savings Time).
* *[!DNL offset]* ist ein Zeitzonenversatz in Stunden oder Stunden:minutes relativ zum GMT. „PDT“ entspricht beispielsweise „GMT -7“.

Alle Elemente von zeichenfolgenformatierten Datums-/Uhrzeitwerten müssen vorhanden sein. Wenn der Datums-/Uhrzeitwert nicht korrekt formatiert ist, wird er ignoriert und stattdessen die Änderungszeit der Datei [!DNL *[!DNL catalog]*.ini] verwendet.

## Standard {#section-562c221d2e8b4a97ab5e9a3605f22140}

Das `attribute::TimeStamp` ist das Feld, das leer oder nicht vorhanden ist.

## Verwandte Themen {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
