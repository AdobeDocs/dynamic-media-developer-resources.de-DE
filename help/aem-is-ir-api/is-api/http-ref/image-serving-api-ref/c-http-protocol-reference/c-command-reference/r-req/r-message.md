---
description: Client-Nachricht. Stellt einen Mechanismus bereit, mit dem Clients kurze Textnachrichten in das Serverprotokoll einfügen können.
solution: Experience Manager
title: message
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 47e51181-714c-4b25-a375-f3b2238cd534
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 3%

---

# message{#message}

Client-Nachricht. Stellt einen Mechanismus bereit, mit dem Clients kurze Textnachrichten in das Serverprotokoll einfügen können.

`req=message&message= *`Zeichenfolge`*`

<table id="simpletable_9AF29AA336C4447BBC2FD4A7D43ED91B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Zeichenfolge</span> </p> </td> 
  <td class="stentry"> <p>Nachrichtenzeichenfolge. </p></td> 
 </tr> 
</table>

Die HTTP-Antwort kann nicht zwischengespeichert werden. Eine leere Antwort wird mit dem MIME-Typ `text/plain` zurückgegeben.
