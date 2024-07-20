---
title: batchjobdelete
description: Löschen Sie die Ausgabe eines Auftrags.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# batchjobdelete{#batchjobdelete}

Löschen Sie die Ausgabe eines Auftrags.

Wenn derzeit ein Auftrag ausgeführt wird, wird er sofort beendet und alle zugehörigen Verarbeitungsinformationen werden gelöscht. Wenn der Auftrag erfolgreich abgeschlossen wurde, wird seine Ausgabedatei gelöscht.

Dieser Parameter:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> job_id</span> </p> </td> 
  <td class="stentry"> <p>Auftrags-ID, die zum Zeitpunkt der Übermittlung abgerufen wurde. </p></td> 
 </tr> 
</table>

Gibt Folgendes zurück:

Status des Auftrags zum Zeitpunkt des Empfangs der Löschanfrage, Fehler, wenn `jobid` ungültig ist oder der Auftrag bereits gelöscht wurde.

## Beispiel {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5`
