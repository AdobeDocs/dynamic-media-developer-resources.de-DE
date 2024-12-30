---
description: Abrufen des detaillierten Status eines übermittelten Vorgangs.
solution: Experience Manager
title: batchJobDetailsStatus
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd385327-29af-448c-9a25-75098b578272
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 2%

---

# batchJobDetailsStatus{#batchjobdetailedstatus}

Abrufen des detaillierten Status eines übermittelten Vorgangs.

Dieser Parameter:

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> JobId-</span> </p> </td> 
  <td class="stentry"> <p>Vorgangs-ID, die zum Zeitpunkt der Übermittlung abgerufen wurde. </p> </td> 
 </tr> 
</table>

Gibt zurück:

Detaillierter Status des Auftrags im XML-Format. Fehler, wenn der `jobid` ungültig ist oder der Auftrag gelöscht wurde.

## Beispiel {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
