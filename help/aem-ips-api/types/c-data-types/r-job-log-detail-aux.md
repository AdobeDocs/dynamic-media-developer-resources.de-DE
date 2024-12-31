---
description: Enthält zusätzliche Meldungen, die mit der Hauptauftragsprotokollmeldung (JobDetail) verknüpft sind. Enthält Warnungen und andere Details, die mit dem aktuell verarbeiteten Asset verknüpft sind.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# [!DNL JobLogDetailAux]{#joblogdetailaux}

Enthält zusätzliche Meldungen, die mit der Hauptauftragsprotokollmeldung (JobDetail) verknüpft sind. Enthält Warnungen und andere Details, die mit dem aktuell verarbeiteten Asset verknüpft sind.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| LogMessage | `xsd:string` | Eine Zusatzmeldung. |
| logType | `xsd:string` | Protokolltyp: `IPSJobLog.gcUploadWarning` oder `IPSJobLog.gcUploadError`. |
| dateCreated | `xsd:dateTime` | Datum der Erstellung des Zusatzauftragsprotokolls. |
