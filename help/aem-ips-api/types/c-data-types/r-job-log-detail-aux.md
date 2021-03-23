---
description: Enthält zusätzliche Meldungen, die mit der Hauptauftragsprotokollmeldung (JobDetail) verknüpft sind. Beinhaltet Warnungen und andere Details, die mit dem aktuell verarbeiteten Asset verknüpft sind.
seo-description: Enthält zusätzliche Meldungen, die mit der Hauptauftragsprotokollmeldung (JobDetail) verknüpft sind. Beinhaltet Warnungen und andere Details, die mit dem aktuell verarbeiteten Asset verknüpft sind.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 5%

---


# JobLogDetailAux{#joblogdetailaux}

Enthält zusätzliche Meldungen, die mit der Hauptauftragsprotokollmeldung (JobDetail) verknüpft sind. Beinhaltet Warnungen und andere Details, die mit dem aktuell verarbeiteten Asset verknüpft sind.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Eine Hilfsmeldung. |
| `*`logType`*` | `xsd:string` | Protokolltyp: `IPSJobLog.gcUploadWarning` oder `IPSJobLog.gcUploadError`. |
| `*`dateCreated`*` | `xsd:dateTime` | Zusätzliches Erstellungsdatum des Auftragsprotokolls. |

