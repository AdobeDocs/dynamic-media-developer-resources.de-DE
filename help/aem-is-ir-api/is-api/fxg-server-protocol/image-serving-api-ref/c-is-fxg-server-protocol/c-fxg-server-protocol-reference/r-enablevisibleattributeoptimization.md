---
description: Aktiviert die Optimierung von FXG.
seo-description: Aktiviert die Optimierung von FXG.
seo-title: enableVisibleAttributeOptimization
solution: Experience Manager
title: enableVisibleAttributeOptimization
topic: Scene7 Image Serving - Image Rendering API
uuid: 7f79aa12-6364-4b34-b547-88d4a778c015
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---


# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

Aktiviert die Optimierung von FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Entfernt die Elemente, deren Sichtbarkeit in FXG als &quot;false&quot;festgelegt ist, während diese FXG-Datei übergeben wird, was wiederum die Verarbeitungszeit von FXG verringert. Es werden zwar nur die Elemente mit der Sichtbarkeit als &quot;false&quot;entfernt, die sich nicht auf andere Elemente in FXG auswirken würden. Wenn beispielsweise Text auf `Path` vorhanden ist und die Sichtbarkeit von `Path` auf &quot;false&quot;gesetzt ist, wird er auch bei aktiviertem Modifikator nicht aus FXG entfernt, da auf diesem Pfad Text gezeichnet werden muss.

Der Standardwert ist „1“.
