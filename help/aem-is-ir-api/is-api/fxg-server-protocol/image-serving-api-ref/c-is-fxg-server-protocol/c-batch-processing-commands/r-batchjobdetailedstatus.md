---
description: Abrufen des detaillierten Status eines gesendeten Auftrags.
solution: Experience Manager
title: batchjobdetailler Status
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '55'
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
