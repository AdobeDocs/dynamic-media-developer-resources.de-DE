---
description: Rufen Sie die Ausgabe eines gesendeten Auftrags ab.
solution: Experience Manager
title: batchjobgetoutput
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fb48c39-b15a-45b7-9aca-ed33f9c46c93
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 1%

---

# batchjobgetoutput{#batchjobgetoutput}

Rufen Sie die Ausgabe eines gesendeten Auftrags ab.

Dieser Parameter:

<table id="simpletable_D8AA325968AD4FAEA7B214F0CBBF3F08"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>Auftrags-ID, die zum Zeitpunkt der Übermittlung abgerufen wurde. </p> </td> 
 </tr> 
</table>

Gibt Folgendes zurück:

Die PDF-Ausgabe des Auftrags wird als Antwort gestreamt. Fehler, wenn `jobid` ungültig ist oder der Auftrag gelöscht wurde.

## Beispiel {#section-0319e615fa254132a9dab59351b4c252}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobgetoutput&jobid=1005907604914d8eb63126b98f7172n76a5]
