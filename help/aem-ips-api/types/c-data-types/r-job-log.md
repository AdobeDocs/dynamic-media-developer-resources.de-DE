---
description: Das Auftragsprotokoll nach Ausführung des Auftrags.
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# [!DNL JobLog]{#joblog}

Das Auftragsprotokoll nach Ausführung des Auftrags.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| companyHandle | `xsd:string` | Handle des Unternehmens. |
| jobHandle | `xsd:string` | Auftragshandle. |
| jobName | `xsd:string` | Auftragsname. |
| originalJobName | `xsd:string` | Der ursprüngliche Name, der für den Auftrag mit `submitJob` gesendet wurde. |
| submitUserEmail | `xsd:string` | Die E-Mail-Adresse des Benutzers, der den Auftrag gesendet hat. |
| logType | `xsd:string` | Auswahl der Auftragsprotokolltypen. |
| jobSubType | `xsd:string` | Zusätzliche Auftragsinformationen. |
| startDate | `xsd:dateTime` | Datum, Uhrzeit und Zeitzone des Auftrags. |
| endDate | `xsd:dateTime` | Enddatum, -zeit und Zeitzone des Auftrags. |
| [!DNL description] | `xsd:string` | Eine Beschreibung des Auftrags, wie ursprünglich in `submitJob` angegeben. |
| fileSuccessCount | `xsd:int` | Anzahl der erfolgreich verarbeiteten Dateien. |
| fileErrorCount | `xsd:int` | Anzahl der Dateien, die einen Fehler verursacht haben. |
| fileWarningCount | `xsd:int` | Anzahl der Dateien, die eine Warnung generiert haben. |
| fileDuplicateCount | `xsd:int` | Anzahl der duplizierten Dateien. |
| fileUpdateCount | `xsd:int` | Anzahl der aktualisierten Dateien. |
| totalFileCount | `xsd:int` | Anzahl der vom protokollierten Auftrag verarbeiteten Dateien. |
| transferSuccessCount | `xsd:int` | Anzahl erfolgreicher Übertragungen. |
| transferErrorCount | `xsd:int` | Anzahl der Übertragungsfehler. |
| transferWarningCount | `xsd:int` | Anzahl der Übertragungswarnungen. |
| fatalError | `xsd:boolean` | Gibt an, ob der Auftrag einen schwerwiegenden Fehler erzeugt hat. |
| detailTotalRows | `xsd:int` | Die Gesamtzahl der mit der Abfrage übereinstimmenden Zeilen, die aufgrund von Größenbeschränkungen der Seite größer als `detailArray` sein können. |
| detailArray | `types:JobLogDetailArray` | Das Array mit Details zum protokollierten Auftrag. |
