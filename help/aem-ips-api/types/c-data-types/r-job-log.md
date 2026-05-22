---
description: Das Vorgangslog, nachdem der Vorgang ausgeführt wurde.
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
TQID: 'https://experienceleague.adobe.com/R3h5NRNxH00Qskdzvw6ul55STF234SudJbjLGYrd238'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 187
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
