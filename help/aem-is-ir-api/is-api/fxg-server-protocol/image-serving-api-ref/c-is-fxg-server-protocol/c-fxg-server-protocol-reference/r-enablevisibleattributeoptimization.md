---
description: Aktiviert die Optimierung von FXG.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

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
