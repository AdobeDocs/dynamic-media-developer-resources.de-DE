---
description: Abrufen des detaillierten Status eines gesendeten Auftrags.
seo-description: Abrufen des detaillierten Status eines gesendeten Auftrags.
seo-title: batchjobdetailler Status
solution: Experience Manager
title: batchjobdetailler Status
uuid: a79302ce-745b-44d8-9cb6-ed8d37530197
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---


# batchjobdetaillstatus{#batchjobdetailedstatus}

Abrufen des detaillierten Status eines gesendeten Auftrags.

Dieser Parameter:

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>Job-ID, die zum Zeitpunkt der Übermittlung abgerufen wurde. </p> </td> 
 </tr> 
</table>

Gibt zurück:

Detaillierter Status des Auftrags im XML-Format; Fehler, wenn `jobid` ungültig ist oder der Auftrag gelöscht wurde.

## Beispiel {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
