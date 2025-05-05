---
description: Ein für die Ausführung geplanter Vorgang.
solution: Experience Manager
title: Geplanter Auftrag
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 4%

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
| videoPublishJob | `types:VideoPublishJob` | Auftragsdetails für einen Videoveröffentlichungsauftrag. Siehe [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html?lang=de). |
| serverDirectoryPublishJob | `types:ServerDirectoryPublishJob` | Auftragsdetails für einen Veröffentlichungsauftrag für ein Serververzeichnis. |
| uploadDirectoryJob | `types:UploadDirectoryJob` | Auftragsdetails für einen Upload-Verzeichnisauftrag. |
| uploadUrlsJob | `types:UploadUrlsJob` | Auftragsdetails für einen Upload-URL-Auftrag. |
| optimizeImagesJob | `types:OptimizeImagesJob` | |
| RIPpdfsJob | `types:RipPdfsJob` | |
| reprocessAssetsJob | `types:ReprocessAssetsJob` | |
| exportJob | `types:ExportJob` | Zulassen des autorisierten Exports zuvor hochgeladener Dateien. Siehe [Exportvorgang](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html?lang=de). |

## Anmerkungen {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Wenn Sie in `submitJob` einen Vorgangstypwert angeben, gibt das System einen auf diesem Typ basierenden Vorgang zurück. Die folgenden Aufträge können zurückgegeben werden:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
