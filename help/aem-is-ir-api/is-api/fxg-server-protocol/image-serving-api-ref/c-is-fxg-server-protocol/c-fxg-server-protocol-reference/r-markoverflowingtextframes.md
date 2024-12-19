---
description: Überlagerte Textrahmen mit Pluszeichen anzeigen. Ein Indikator für einen Textüberlauf wird angezeigt, wenn Text den für ihn in einem Textrahmen zugewiesenen Platz überschreitet (oder im letzten Textrahmen bei Text mit Gewinde). Der Indikator ist ein rotes Feld mit einem Pluszeichen darin.
solution: Experience Manager
title: markOverflowingTextFrames
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1e2a3d4-ef1f-4d5e-be9c-eeec36f46603
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---

# markOverflowingTextFrames{#markoverflowingtextframes}

Überlagerte Textrahmen mit Pluszeichen anzeigen. Ein Indikator für einen Textüberlauf wird angezeigt, wenn Text den für ihn in einem Textrahmen zugewiesenen Platz überschreitet (oder im letzten Textrahmen bei Text mit Gewinde). Der Indikator ist ein rotes Feld mit einem Pluszeichen darin.

<table id="simpletable_F17FD29EB52043BF9000923ED5195A26"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;markOverloadingTextFrames</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Wenn Sie den Modifikator `markOverflowingTextFrames=1` über einen URL-Aufruf festlegen, werden alle Textrahmen markiert, bei denen Text mit einem Pluszeichen überschrieben wird. In der Dynamic Media Classic-Vorschau ist die Textübersatzanzeige außerdem standardmäßig auf &quot;`TRUE`&quot; eingestellt.

Die Standardgrenze ist 0.
