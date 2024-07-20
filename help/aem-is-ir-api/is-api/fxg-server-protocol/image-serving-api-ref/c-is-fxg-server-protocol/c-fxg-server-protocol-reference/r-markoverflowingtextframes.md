---
description: Übersatztextrahmen mit Pluszeichen anzeigen. Ein Überlaufanzeiger für Text wird angezeigt, wenn der Text den in einem Textrahmen (oder im letzten Textrahmen im Fall von Text mit Gewinde) zugewiesenen Platz überschreitet. Der Indikator ist ein rotes Feld mit einem Pluszeichen.
solution: Experience Manager
title: markOverloadingTextFrames
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1e2a3d4-ef1f-4d5e-be9c-eeec36f46603
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---

# markOverloadingTextFrames{#markoverflowingtextframes}

Übersatztextrahmen mit Pluszeichen anzeigen. Ein Überlaufanzeiger für Text wird angezeigt, wenn der Text den in einem Textrahmen (oder im letzten Textrahmen im Fall von Text mit Gewinde) zugewiesenen Platz überschreitet. Der Indikator ist ein rotes Feld mit einem Pluszeichen.

<table id="simpletable_F17FD29EB52043BF9000923ED5195A26"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;markOverloadingTextFrames</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Wenn der Modifikator `markOverflowingTextFrames=1` über einen URL-Aufruf festgelegt wird, werden alle Textrahmen markiert, in denen Text durch ein Pluszeichen überschrieben wird. Außerdem ist die Textübersatzanzeige in der Dynamic Media Classic-Vorschau standardmäßig auf &quot;`TRUE`&quot; eingestellt.

Die Standardgrenze ist 0.
