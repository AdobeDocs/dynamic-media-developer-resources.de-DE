---
title: batchJobBriefStatus
description: Abrufen des zusammengefassten Status eines übermittelten Vorgangs.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b31bdbb-3c2c-4f7f-ba95-d3e710270be0
source-git-commit: 13991f71ab54d1003a79a496b861d53a61899bdc
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 2%

---

# batchJobBriefStatus{#batchjobbriefstatus}

Abrufen des zusammengefassten Status eines übermittelten Vorgangs.

Dieser Parameter:

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> JobId-</span> </p> </td> 
  <td class="stentry"> <p>Vorgangs-ID, die zum Zeitpunkt der Übermittlung abgerufen wurde. </p> </td> 
 </tr> 
</table>

Gibt zurück:

Kurzer Status des Vorgangs im XML-Format; Fehler, wenn die Vorgangs-ID ungültig ist oder der Vorgang gelöscht wurde.

## Beispiel {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
