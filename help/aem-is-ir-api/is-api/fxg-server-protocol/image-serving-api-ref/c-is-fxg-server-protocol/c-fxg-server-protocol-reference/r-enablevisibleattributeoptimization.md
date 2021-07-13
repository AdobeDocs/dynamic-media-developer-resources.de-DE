---
description: Aktiviert die Optimierung von FXG.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
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

Entfernt die Elemente, deren Sichtbarkeit in FXG als &quot;false&quot;festgelegt ist, während dieses FXG übergeben wird, wodurch wiederum die Verarbeitungszeit von FXG verringert wird. Es werden zwar nur die Elemente mit Sichtbarkeit als &quot;false&quot;entfernt, die sich nicht auf andere Elemente in FXG auswirken würden. Wenn beispielsweise Text auf `Path` vorhanden ist und die Sichtbarkeit von `Path` auf &quot;false&quot;gesetzt ist, wird dieser Text auch bei aktiviertem Modifikator nicht aus FXG entfernt, da auf diesem Pfad Text gezeichnet werden muss.

Der Standardwert ist „1“.
