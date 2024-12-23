---
description: Das Vorgangslog, nachdem der Vorgang ausgeführt wurde.
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

Das Vorgangslog, nachdem der Vorgang ausgeführt wurde.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| companyHandle | `xsd:string` | Firmengriff. |
| jobHandle | `xsd:string` | Auftragsverarbeitung. |
| jobName | `xsd:string` | Vorgangsname. |
| originalJobName | `xsd:string` | Der ursprüngliche Name, der für den Auftrag mit `submitJob` übermittelt wurde. |
| submitUserEmail | `xsd:string` | Die E-Mail-Adresse des Benutzers, der den Auftrag gesendet hat. |
| logType | `xsd:string` | Auswahl von Vorgangslog-Typen. |
| jobSubType | `xsd:string` | Zusätzliche Auftragsinformationen. |
| startDate | `xsd:dateTime` | Startdatum, -zeit und -zeitzone des Auftrags. |
| endDate | `xsd:dateTime` | Das Enddatum, die Uhrzeit und die Zeitzone des Auftrags. |
| [!DNL description] | `xsd:string` | Eine Beschreibung des Auftrags, wie ursprünglich in `submitJob` angegeben. |
| fileSuccessCount | `xsd:int` | Anzahl der erfolgreich verarbeiteten Dateien. |
| fileErrorCount | `xsd:int` | Anzahl der Dateien, die einen Fehler verursacht haben. |
| fileWarningCount | `xsd:int` | Anzahl der Dateien, die eine Warnung erzeugt haben. |
| fileDuplicateCount | `xsd:int` | Anzahl der doppelten Dateien. |
| fileUpdateCount | `xsd:int` | Anzahl der aktualisierten Dateien. |
| totalFileCount | `xsd:int` | Anzahl der Dateien, die vom protokollierten Auftrag verarbeitet wurden. |
| transferSuccessCount | `xsd:int` | Anzahl erfolgreicher Übertragungen. |
| transferErrorCount | `xsd:int` | Anzahl der Übertragungsfehler. |
| transferWarningCount | `xsd:int` | Anzahl der Übertragungswarnungen. |
| Schwerwiegender Fehler | `xsd:boolean` | Ob der Auftrag einen schwerwiegenden Fehler verursacht hat. |
| detailTotalRows | `xsd:int` | Die Gesamtzahl der Zeilen, die mit der Abfrage übereinstimmen. Diese kann aufgrund von Seitengrößenbeschränkungen größer als die Größe von `detailArray` sein. |
| detailArray | `types:JobLogDetailArray` | Das Array von Details zum protokollierten Auftrag. |
