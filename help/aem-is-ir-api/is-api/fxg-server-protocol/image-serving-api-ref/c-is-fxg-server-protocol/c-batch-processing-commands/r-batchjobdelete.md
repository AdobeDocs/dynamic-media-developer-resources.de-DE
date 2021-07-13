---
description: Löschen Sie die Ausgabe eines Auftrags.
solution: Experience Manager
title: batchjobdelete
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---

# batchjobdelete{#batchjobdelete}

Löschen Sie die Ausgabe eines Auftrags.

Wenn ein Auftrag derzeit ausgeführt wird, wird er sofort angehalten und alle Verarbeitungsinformationen werden gelöscht. Wenn der Auftrag erfolgreich abgeschlossen wurde, wird seine Ausgabedatei gelöscht.

Dieser Parameter:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>Auftrags-ID, die zum Zeitpunkt der Übermittlung abgerufen wurde. </p></td> 
 </tr> 
</table>

Gibt Folgendes zurück:

Status des Auftrags zum Zeitpunkt des Empfangs der Löschanfrage, Fehler, wenn `jobid` ungültig ist oder der Auftrag bereits gelöscht wurde.

## Beispiel {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
