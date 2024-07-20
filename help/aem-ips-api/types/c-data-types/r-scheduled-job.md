---
description: Ein Auftrag, der ausgeführt werden soll.
solution: Experience Manager
title: ScheduledJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 4%

---

# [!DNL ScheduledJob]{#scheduledjob}

Ein Auftrag, der ausgeführt werden soll.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| companyHandle | `xsd:string` | Handle des Unternehmens. |
| jobHandle | `xsd:string` | Handhabung geplanter Aufträge. |
| name | `xsd:string` | Auftragsname. |
| originalName | `xsd:string` | Originalname des geplanten Auftrags. |
| Typ | `xsd:string` | Auftragstyp. |
| submitUserEmail | `xsd:string` | Die E-Mail-Adresse des Benutzers, der den Auftrag geplant hat. |
| standort | `xsd:string` | Das Gebietsschema, das für Auftragsprotokolldetails und die E-Mail-Lokalisierung verwendet werden soll. Gebietsschemata werden als &quot;`<language_code>[- <country_code>]`&quot;angegeben, wobei der Sprachcode ein aus zwei Kleinbuchstaben bestehender Code gemäß ISO-639 ist und der optionale Ländercode ein aus zwei Buchstaben bestehender Code aus Großbuchstaben ist, wie in ISO-3166 angegeben. Die Gebietsschema-Zeichenfolge für Englisch (USA) lautet beispielsweise: `en-US`. |
| description | `xsd:string` | Eine Beschreibung des Auftrags, wie ursprünglich in `submitJob` angegeben. |
| execSchedule | `xsd:string` | Wann der Auftrag ausgeführt werden soll. |
| nextFireTime | `xsd:dateTime` | Datum, Uhrzeit und Zeitzone, zu der der Auftrag ausgelöst wird. |
| timeZone | `xsd:dateTime` | Die Zeitzone des geplanten Auftrags. |
| triggerState | `xsd:int` | Auswahl des Status des Triggers. |
| imageServingPublishJob | `types:ImageServingPublishJob` | Auftragsdetails für einen Image-Serving-Veröffentlichungsauftrag. |
| imageServingRenderJob | `types:ImageServingRenderJob` | Auftragsdetails für einen Bildrendering-Auftrag. |
| videoPublishJob | `types:VideoPublishJob` | Auftragsdetails für einen Video-Veröffentlichungsauftrag. Siehe [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| serverDirectoryPublishJob | `types:ServerDirectoryPublishJob` | Auftragsdetails für einen Veröffentlichungsauftrag in Serverordnern. |
| uploadDirectoryJob | `types:UploadDirectoryJob` | Auftragsdetails für einen Upload-Ordnerauftrag. |
| uploadUrlsJob | `types:UploadUrlsJob` | Auftragsdetails für einen Upload-URLs-Auftrag. |
| optimizeImagesJob | `types:OptimizeImagesJob` | |
| ripPdfsJob | `types:RipPdfsJob` | |
| reprocessAssetsJob | `types:ReprocessAssetsJob` | |
| exportJob | `types:ExportJob` | Zulassen des autorisierten Exports von zuvor hochgeladenen Dateien. Siehe [Exportauftrag](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Anmerkungen {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Wenn Sie in `submitJob` einen Auftragstyp angeben, gibt das System einen Auftrag zurück, der auf diesem Typ basiert. Die folgenden Aufträge können zurückgegeben werden:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
