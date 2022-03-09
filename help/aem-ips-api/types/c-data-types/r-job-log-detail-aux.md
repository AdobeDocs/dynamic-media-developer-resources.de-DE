---
description: Enthält zusätzliche Nachrichten, die mit der Hauptauftragsprotokollmeldung (JobDetail) verknüpft sind. Enthält Warnungen und andere Details, die mit dem aktuell verarbeiteten Asset verknüpft sind.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 7%

---

# JobLogDetailAux{#joblogdetailaux}

Enthält zusätzliche Nachrichten, die mit der Hauptauftragsprotokollmeldung (JobDetail) verknüpft sind. Enthält Warnungen und andere Details, die mit dem aktuell verarbeiteten Asset verknüpft sind.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| logMessage | `xsd:string` | Eine Hilfsnachricht. |
| logType | `xsd:string` | Protokolltyp: `IPSJobLog.gcUploadWarning` oder `IPSJobLog.gcUploadError`. |
| dateCreated | `xsd:dateTime` | Zusätzliches Erstellungsdatum des Auftragsprotokolls. |
