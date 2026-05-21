---
description: Überlagerte Textrahmen mit Pluszeichen anzeigen. Ein Indikator für einen Textüberlauf wird angezeigt, wenn Text den für ihn in einem Textrahmen zugewiesenen Platz überschreitet (oder im letzten Textrahmen bei Text mit Gewinde). Der Indikator ist ein rotes Kästchen mit einem Pluszeichen.
solution: Experience Manager
title: markOverflowingTextFrames
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1e2a3d4-ef1f-4d5e-be9c-eeec36f46603
TQID: 'https://experienceleague.adobe.com/Wy5VLpT5I1KzXUrKaPoetj2ejv4wbUOsU1My9vEA5gM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 21%

---

# markOverflowingTextFrames{#markoverflowingtextframes}

Überlagerte Textrahmen mit Pluszeichen anzeigen. Ein Indikator für einen Textüberlauf wird angezeigt, wenn Text den für ihn in einem Textrahmen zugewiesenen Platz überschreitet (oder im letzten Textrahmen bei Text mit Gewinde). Der Indikator ist ein rotes Kästchen mit einem Pluszeichen.

<table id="simpletable_F17FD29EB52043BF9000923ED5195A26"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;markOverloadingTextFrames</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Wenn Sie den Modifikator `markOverflowingTextFrames=1` über einen URL-Aufruf festlegen, werden alle Textrahmen markiert, bei denen Text mit einem Pluszeichen überschrieben wird. In der Dynamic Media Classic-Vorschau ist die Textübersatzanzeige außerdem standardmäßig auf &quot;`TRUE`&quot; eingestellt.

Der Standardwert ist „0“.
