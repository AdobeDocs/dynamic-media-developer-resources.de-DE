---
description: Enthält Einstellungen für das Überwachungs-/Warnsystem.
seo-description: Enthält Einstellungen für das Überwachungs-/Warnsystem.
seo-title: monitor.conf
solution: Experience Manager
title: monitor.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: 31949797-df2c-4b7c-841b-4c623299a228
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# monitor.conf{#monitor-conf}

Enthält Einstellungen für das Überwachungs-/Warnsystem.

Diese Datei ist eine JAVA-Eigenschaftendatei. Es ist darauf zu achten, dass die entsprechenden Konventionen eingehalten werden. Andernfalls kann der Beginn des Plattformservers fehlschlagen. Beachten Sie insbesondere, dass ein umgekehrter Schrägstrich (\\) oder ein einzelner Schrägstrich (/) anstelle eines umgekehrten Schrägstrichs (\) in Windows-Dateipfaden verwendet werden muss, da der umgekehrte Schrägstrich in diesem Dateityp als Escape-Zeichen verwendet wird.

Änderungen an dieser Datei werden kurz nach dem Speichern der Datei wirksam.

<table id="simpletable_91557E1162FF4FEC8BE1722D6656CFEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Allgemein </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> monitorAlertGenerator.enableGlobalAlerting=false </span> </p> <p> <span class="codeph"> mailSender.host=127.0.0.1 </span> </p> <p> <span class="codeph"> mailSender.port=25 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageTo=noone@scene7.com </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageFrom=noone@scene7.com </span> </p> <p> <span class="codeph"> monitorAlertGenerator.alertInterval=600000 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.heapSpaceResetInterval=600000 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.minTrafficForAlerts=0.0 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Warnschwellenwerte </p> </td> 
  <td class="stentry"> <p> monitorAlertGenerator.maxAverageResponseTime=200 </p> <p> monitorAlertGenerator.maxErrorRate=0.05 </p> <p> monitorAlertGenerator.minRequestRate=0.0 </p> <p> monitorAlertGenerator.minFreeHeapSpace=52428800 </p> <p> monitorAlertGenerator.maxOverlap=20 </p> <p> monitorAlertGenerator.lockedThreshold=60000 </p> </td> 
 </tr> 
</table>

