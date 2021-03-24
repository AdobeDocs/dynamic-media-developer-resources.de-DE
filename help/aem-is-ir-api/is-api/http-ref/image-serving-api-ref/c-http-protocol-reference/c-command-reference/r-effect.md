---
description: Wählen Sie Effektebene. Wählt eine Effektebene aus und Beginn ein neues Ebenensegment in der Anforderungszeichenfolge, das mit der aktuellen Ebene verknüpft ist.
solution: Experience Manager
title: effect
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---


# effect{#effect}

Wählen Sie Effektebene. Wählt eine Effektebene aus und Beginn ein neues Ebenensegment in der Anforderungszeichenfolge, das mit der aktuellen Ebene verknüpft ist.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Anzahl der Effektebenen (int ist nicht gleich 0). </p></td> 
 </tr> 
</table>

Alle Befehle im neuen Segment werden auf die angegebene Effektebene angewendet. Ein Effekt-Ebenensegment wird durch den nächsten Befehl `layer=` oder `effect=` oder durch das Ende der Anforderung beendet.

*`n`* muss bei äußeren Ebeneneffekten kleiner als 0 (d. h. bei Effekten hinter der übergeordneten Ebene) und größer als 0 bei inneren Ebeneneffekten (d. h. bei Effekten innerhalb der übergeordneten Ebene) sein. Die Nummern der Effektebenen müssen nicht aufeinander folgen.

Die Nummer der Effektebene gibt die z-Reihenfolge an, wenn mehrere Effektebenen für dieselbe übergeordnete Ebene vorhanden sind. Ebenen mit einer höheren Nummerierung werden über Ebenen mit einer niedrigeren Nummerierung platziert.

Effektebenen können an `layer=comp` angehängt werden.

## Eigenschaften {#section-e11f795deff345779ce280a82cf221ca}

Effektebene, Befehl. *`n`* darf nicht 0 sein.

## Standard {#section-84bbe1cfe7a94040827c994323ac59d4}

Keine.

## Beispiel {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Verwandte Themen {#section-573273e9e0e64103a5764075f5e50180}

` [layer=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d)`
