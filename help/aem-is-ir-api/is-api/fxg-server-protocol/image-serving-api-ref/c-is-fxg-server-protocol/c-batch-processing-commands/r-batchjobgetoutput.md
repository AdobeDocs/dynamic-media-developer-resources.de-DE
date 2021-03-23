---
description: Rufen Sie die Ausgabe eines gesendeten Auftrags ab.
seo-description: Rufen Sie die Ausgabe eines gesendeten Auftrags ab.
seo-title: batchjobgetoutput
solution: Experience Manager
title: batchjobgetoutput
uuid: c2d49cc2-3223-4f0f-8ba7-4f74a5f76789
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 1%

---


# batchjobgetoutput{#batchjobgetoutput}

Rufen Sie die Ausgabe eines gesendeten Auftrags ab.

Dieser Parameter:

<table id="simpletable_D8AA325968AD4FAEA7B214F0CBBF3F08"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>Job-ID, die zum Zeitpunkt der Übermittlung abgerufen wurde. </p> </td> 
 </tr> 
</table>

Gibt zurück:

Die PDF-Ausgabe des Auftrags wird als Antwort gestreamt. Fehler, wenn `jobid` ungültig ist oder der Auftrag gelöscht wurde.

## Beispiel {#section-0319e615fa254132a9dab59351b4c252}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobgetoutput&jobid=1005907604914d8eb63126b98f7172n76a5]
