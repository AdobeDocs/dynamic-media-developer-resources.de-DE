---
description: Senden Sie einen neuen Stapelauftrag.
solution: Experience Manager
title: batchjobsubmit
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '46'
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
