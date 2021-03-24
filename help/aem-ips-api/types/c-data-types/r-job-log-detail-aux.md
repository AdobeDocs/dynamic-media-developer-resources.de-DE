---
description: Enthält zusätzliche Meldungen, die mit der Hauptauftragsprotokollmeldung (JobDetail) verknüpft sind. Beinhaltet Warnungen und andere Details, die mit dem aktuell verarbeiteten Asset verknüpft sind.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

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

