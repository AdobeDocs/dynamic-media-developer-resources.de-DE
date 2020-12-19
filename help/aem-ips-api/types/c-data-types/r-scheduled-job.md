---
description: Ein Auftrag, der ausgeführt werden soll.
seo-description: Ein Auftrag, der ausgeführt werden soll.
seo-title: ScheduledJob
solution: Experience Manager
title: ScheduledJob
topic: Scene7 Image Production System API
uuid: cf0db523-2138-48c6-abbd-460a961e7de1
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 4%

---


# ScheduledJob{#scheduledjob}

Ein Auftrag, der ausgeführt werden soll.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Firma Handle. |
| ` *`jobHandle`*` | `xsd:string` | Terminierte Auftragsverwaltung. |
| ` *`name`*` | `xsd:string` | Auftragsname. |
| ` *`originalName`*` | `xsd:string` | Ursprünglicher Name des geplanten Auftrags. |
| ` *`type`*` | `xsd:string` | Auftragstyp. |
| ` *`submitUserEmail`*` | `xsd:string` | Die E-Mail-Adresse des Benutzers, der den Auftrag geplant hat. |
| ` *`locale`*` | `xsd:string` | Das Gebietsschema, das für Auftragsprotokolldetails und E-Mail-lokale Anpassungen verwendet wird. Gebietsschemata werden als `<language_code>[- <country_code>]` angegeben, wobei der Sprachencode aus Kleinbuchstaben und aus zwei Buchstaben besteht, wie in ISO-639 angegeben, und der optionale Ländercode aus Großbuchstaben besteht, und aus zwei Buchstaben, wie in ISO-3166 angegeben. Die Zeichenfolge für Englisch (USA) lautet beispielsweise: `en-US`. |
| ` *`description`*` | `xsd:string` | Eine Beschreibung des Auftrags, wie ursprünglich unter `submitJob` angegeben. |
| ` *`execSchedule`*` | `xsd:string` | Wenn die Ausführung des Auftrags geplant ist. |
| ` *`nextFireTime`*` | `xsd:dateTime` | Datum, Uhrzeit und Zeitzone, in der der Auftrag ausgelöst wird. |
| ` *`timeZone`*` | `xsd:dateTime` | Die Zeitzone des geplanten Auftrags. |
| ` *`triggerState`*` | `xsd:int` | Auswahl des Auftragsauslöserstatus. |
| ` *`imageServingPublishJob`*` | `types:ImageServingPublishJob` | Auftragsdetails für einen Image Serving-Veröffentlichungsauftrag. |
| ` *`imageServingRenderJob`*` | `types:ImageServingRenderJob` | Auftragsdetails für einen Bildwiedergabeauftrag. |
| ` *`videoPublishJob`*` | `types:VideoPublishJob` | Auftragsdetails für einen Videoveröffentlichungsauftrag. Siehe [VideoPublishJob](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| ` *`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | Auftragsdetails für einen Veröffentlichungsauftrag im Serververzeichnis. |
| ` *`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | Auftragsdetails für einen Upload-Ordnerauftrag. |
| ` *`uploadUrlsJob`*` | `types:UploadUrlsJob` | Auftragsdetails für einen Upload-URLs-Auftrag. |
| ` *`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| ` *`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| ` *`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| ` *`exportJob`*` | `types:ExportJob` | Zulassen des autorisierten Exports von zuvor hochgeladenen Dateien. Siehe [Exportauftrag](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Anmerkungen {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Wenn Sie in `submitJob` einen Auftragstypwert angeben, gibt das System einen Auftrag basierend auf diesem Typ zurück. Die folgenden Aufträge können zurückgegeben werden:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

