---
description: Abrufen des zusammengefassten Status eines gesendeten Auftrags.
seo-description: Abrufen des zusammengefassten Status eines gesendeten Auftrags.
seo-title: batchjobbriefstatus
solution: Experience Manager
title: batchjobbriefstatus
topic: Scene7 Image Serving - Image Rendering API
uuid: 601e8395-8a77-4324-9cd7-5fe321bc91e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---


# batchjobbriefstatus{#batchjobbriefstatus}

Abrufen des zusammengefassten Status eines gesendeten Auftrags.

Dieser Parameter:

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>Job-ID, die zum Zeitpunkt der Übermittlung abgerufen wurde. </p> </td> 
 </tr> 
</table>

Gibt zurück:

Kurzer Status des Auftrags im XML-Format; Fehler, wenn die Job-ID ungültig ist oder der Auftrag gelöscht wurde.

## Beispiel {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
