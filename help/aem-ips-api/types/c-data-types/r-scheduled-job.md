---
description: Ein für die Ausführung geplanter Vorgang.
solution: Experience Manager
title: Geplanter Auftrag
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
TQID: 'https://experienceleague.adobe.com/OFG30nHlkuRT7HeNob0hkEfaygi8b2gNFEiu67LJBmU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 276
ht-degree: 3%

---

# [!DNL ScheduledJob]{#scheduledjob}

Ein für die Ausführung geplanter Vorgang.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| companyHandle | `xsd:string` | Firmengriff. |
| jobHandle | `xsd:string` | Handle des geplanten Auftrags. |
| name | `xsd:string` | Vorgangsname. |
| originalName | `xsd:string` | Originalname des geplanten Auftrags. |
| Typ | `xsd:string` | Vorgangstyp. |
| submitUserEmail | `xsd:string` | Die E-Mail-Adresse des Benutzers, der den Auftrag geplant hat. |
| standort | `xsd:string` | Das Gebietsschema, das für Auftragsprotokolldetails und E-Mail-Lokalisierung verwendet werden soll. Gebietsschemata werden als `<language_code>[- <country_code>]` angegeben, wobei der Sprach-Code ein Code mit zwei Kleinbuchstaben gemäß ISO-639 ist und der optionale Länder-Code ein Code mit zwei Großbuchstaben gemäß ISO-3166 ist. Die Gebietsschema-Zeichenfolge für Englisch (Vereinigte Staaten) wäre beispielsweise: `en-US`. |
| description | `xsd:string` | Eine Beschreibung des Auftrags, wie ursprünglich in `submitJob` angegeben. |
| execSchedule | `xsd:string` | Wann die Ausführung des Auftrags geplant ist. |
| nextFireTime | `xsd:dateTime` | Das Datum, die Uhrzeit und die Zeitzone, in der der Auftrag ausgelöst wurde. |
| timeZone | `xsd:dateTime` | Die Zeitzone des geplanten Auftrags. |
| triggerState | `xsd:int` | Auswahl des Status des Job-Triggers. |
| imageServingPublishJob | `types:ImageServingPublishJob` | Auftragsdetails für einen Image-Serving-Veröffentlichungsauftrag. |
| imageServingRenderJob | `types:ImageServingRenderJob` | Auftragsdetails für einen Bild-Rendering-Auftrag. |
| videoPublishJob | `types:VideoPublishJob` | Auftragsdetails für einen Videoveröffentlichungsauftrag. Siehe [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| serverDirectoryPublishJob | `types:ServerDirectoryPublishJob` | Auftragsdetails für einen Veröffentlichungsauftrag für ein Serververzeichnis. |
| uploadDirectoryJob | `types:UploadDirectoryJob` | Auftragsdetails für einen Upload-Verzeichnisauftrag. |
| uploadUrlsJob | `types:UploadUrlsJob` | Auftragsdetails für einen Upload-URL-Auftrag. |
| optimizeImagesJob | `types:OptimizeImagesJob` | |
| RIPpdfsJob | `types:RipPdfsJob` | |
| reprocessAssetsJob | `types:ReprocessAssetsJob` | |
| exportJob | `types:ExportJob` | Zulassen des autorisierten Exports zuvor hochgeladener Dateien. Siehe [Exportvorgang](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Anmerkungen {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Wenn Sie in `submitJob` einen Vorgangstypwert angeben, gibt das System einen auf diesem Typ basierenden Vorgang zurück. Die folgenden Aufträge können zurückgegeben werden:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
