---
description: Senden Sie einen neuen Stapelauftrag.
seo-description: Senden Sie einen neuen Stapelauftrag.
seo-title: batchjobsubmit
solution: Experience Manager
title: batchjobsubmit
topic: Dynamic Media Image Serving - Image Rendering API
uuid: eb695666-fcaf-40bc-8b56-452819f058d2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 2%

---


# batchjobsubmit{#batchjobsubmit}

Senden Sie einen neuen Stapelauftrag.

Dieser Parameter:

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobdata  </span> </p> </td> 
  <td class="stentry"> <p>XML-Snippet mit vollständigen Auftragsdaten. </p> </td> 
 </tr> 
</table>

Gibt zurück:

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Auftragsstatus </p> </td> 
  <td class="stentry"> <p>ob die Übermittlung erfolgreich war oder fehlgeschlagen ist; sofern erfolgreich, Job-ID im XML-Format. </p> </td> 
 </tr> 
</table>

## Beispiel {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
