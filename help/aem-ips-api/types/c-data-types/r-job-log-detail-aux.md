---
description: Enthält zusätzliche Meldungen, die mit der Hauptauftragsprotokollmeldung (JobDetail) verknüpft sind. Enthält Warnungen und andere Details, die mit dem aktuell verarbeiteten Asset verknüpft sind.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
TQID: 'https://experienceleague.adobe.com/Hl3L69Hd6Hm8acRaPgFVQCfo8PffGCn5fNGxthmStFM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 64
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
