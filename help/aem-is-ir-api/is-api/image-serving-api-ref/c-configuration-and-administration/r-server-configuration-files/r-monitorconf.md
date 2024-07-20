---
description: Enthält Einstellungen für das Überwachungs-/Warnsystem.
solution: Experience Manager
title: monitor.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 09c30680-dd9f-4744-b5ec-105721058883
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# monitor.conf{#monitor-conf}

Enthält Einstellungen für das Überwachungs-/Warnsystem.

Diese Datei ist eine JAVA-Eigenschaftendatei. Es ist darauf zu achten, dass die entsprechenden Konventionen eingehalten werden. Andernfalls kann der [!DNL Platform Server] nicht starten. Beachten Sie insbesondere, dass in Windows-Dateipfaden ein doppelter umgekehrter Schrägstrich &quot;\&quot;oder ein einfacher Schrägstrich &quot;/&quot;anstelle eines umgekehrten Schrägstrichs &quot;\&quot;verwendet werden muss, da der umgekehrte Schrägstrich in diesem Dateityp als Escape-Zeichen verwendet wird.

Änderungen an dieser Datei werden kurz nach dem Speichern der Datei wirksam.

<table id="simpletable_91557E1162FF4FEC8BE1722D6656CFEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Allgemein </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> monitorAlertGenerator.enableGlobalAlerting=false </span> </p> <p> <span class="codeph"> mailSender.host=127.0.0.1 </span> </p> <p> <span class="codeph"> mailSender.port=25 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageTo=noone@scene7.com </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageFrom=noone@scene7.com </span> </p> <p> <span class="codeph"> monitorAlertGenerator.alertInterval=600000 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.heapSpaceResetInterval=600000 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.minTrafficForAlerts=0.0 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Warnschwellen </p> </td> 
  <td class="stentry"> <p> monitorAlertGenerator.maxAverageResponseTime=200 </p> <p> monitorAlertGenerator.maxErrorRate=0.05 </p> <p> monitorAlertGenerator.minRequestRate=0.0 </p> <p> monitorAlertGenerator.minFreeHeapSpace=52428800 </p> <p> monitorAlertGenerator.maxOverlap=20 </p> <p> monitorAlertGenerator.lockedThreshold=60000 </p> </td> 
 </tr> 
</table>
