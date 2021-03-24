---
description: Löschen Sie die Ausgabe eines Auftrags.
solution: Experience Manager
title: batchjobdelete
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 1%

---


# batchjobdelete{#batchjobdelete}

Löschen Sie die Ausgabe eines Auftrags.

Wenn derzeit ein Auftrag ausgeführt wird, wird er sofort beendet und alle zugehörigen Verarbeitungsinformationen werden gelöscht. Wenn der Auftrag erfolgreich abgeschlossen wurde, wird seine Ausgabedatei gelöscht.

Dieser Parameter:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>Job-ID, die zum Zeitpunkt der Übermittlung abgerufen wurde. </p></td> 
 </tr> 
</table>

Gibt zurück:

Status des Auftrags zum Zeitpunkt des Eingangs der Löschanforderung, Fehler, wenn `jobid` ungültig ist oder der Auftrag bereits gelöscht wurde.

## Beispiel {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
