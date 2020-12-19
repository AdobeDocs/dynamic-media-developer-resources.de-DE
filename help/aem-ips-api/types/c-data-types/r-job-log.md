---
description: Das Auftragsprotokoll nach Ausführung des Auftrags.
seo-description: Das Auftragsprotokoll nach Ausführung des Auftrags.
seo-title: JobLog
solution: Experience Manager
title: JobLog
topic: Scene7 Image Production System API
uuid: d267009a-e4ad-4a21-ae0e-caf51d2f338b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 3%

---


# JobLog{#joblog}

Das Auftragsprotokoll nach Ausführung des Auftrags.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Firma Handle. |
| ` *`jobHandle`*` | `xsd:string` | Auftragsbearbeitung |
| ` *`jobName`*` | `xsd:string` | Auftragsname. |
| ` *`originalJobName`*` | `xsd:string` | Der ursprüngliche Name, der für den Auftrag mit `submitJob` gesendet wurde. |
| ` *`submitUserEmail`*` | `xsd:string` | Die E-Mail-Adresse des Benutzers, der den Auftrag gesendet hat. |
| ` *`logType`*` | `xsd:string` | Auswahl der Auftragsprotokolltypen. |
| ` *`jobSubType`*` | `xsd:string` | Zusätzliche Auftragsinformationen. |
| ` *`startDate`*` | `xsd:dateTime` | Datum, Uhrzeit und Zeitzone des Beginns des Auftrags. |
| ` *`endDate`*` | `xsd:dateTime` | Enddatum, Uhrzeit und Zeitzone des Auftrags. |
| ` *`description`*` | `xsd:string` | Eine Beschreibung des Auftrags, wie ursprünglich unter `submitJob` angegeben. |
| ` *`fileSuccessCount`*` | `xsd:int` | Anzahl der erfolgreich verarbeiteten Dateien. |
| ` *`fileErrorCount`*` | `xsd:int` | Anzahl der Dateien, die einen Fehler verursacht haben. |
| ` *`fileWarningCount`*` | `xsd:int` | Anzahl der Dateien, die eine Warnung generiert haben. |
| ` *`fileDuplicateCount`*` | `xsd:int` | Anzahl der Duplikat-Dateien. |
| ` *`fileUpdateCount`*` | `xsd:int` | Anzahl der aktualisierten Dateien. |
| ` *`totalFileCount`*` | `xsd:int` | Anzahl der Dateien, die vom protokollierten Auftrag verarbeitet werden. |
| ` *`transferSuccessCount`*` | `xsd:int` | Anzahl der erfolgreichen Transfers. |
| ` *`transferErrorCount`*` | `xsd:int` | Anzahl der Übertragungsfehler. |
| ` *`transferWarningCount`*` | `xsd:int` | Anzahl der Übertragungswarnungen. |
| ` *`fatalError`*` | `xsd:boolean` | Gibt an, ob der Auftrag einen schwerwiegenden Fehler verursacht hat. |
| ` *`detailTotalRows`*` | `xsd:int` | Die Gesamtanzahl der Zeilen, die mit der Abfrage übereinstimmen, die aufgrund von Seitengrößenbeschränkungen größer als `detailArray` sein kann. |
| ` *`detailArray`*` | `types:JobLogDetailArray` | Das Array mit Details zum protokollierten Auftrag. |

