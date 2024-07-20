---
title: Effekt
description: Wählen Sie Effektebene aus. Wählt eine Effektebene aus und startet ein neues Ebenensegment in der Anforderungszeichenfolge, das mit der aktuellen Ebene verknüpft ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# Effekt{#effect}

Wählen Sie Effektebene aus. Wählt eine Effektebene aus und startet ein neues Ebenensegment in der Anforderungszeichenfolge, das mit der aktuellen Ebene verknüpft ist.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Effektschichtnummer (int nicht gleich 0). </p></td> 
 </tr> 
</table>

Alle Befehle im neuen Segment werden auf die angegebene Effektebene angewendet. Ein Effekt-Layer-Segment wird durch den nächsten `layer=` - oder `effect=` -Befehl oder durch das Ende der Anfrage beendet.

Der Wert *`n`* muss für äußere Ebeneneffekte kleiner als 0 (d. h. Effekte hinter der übergeordneten Ebene) und größer als 0 für innere Ebeneneffekte (d. h. Effekte innerhalb der übergeordneten Ebene) sein. Die Anzahl der Effektebenen muss nicht aufeinander folgen.

Die Ebenennummer des Effekts gibt die z-Reihenfolge an, wenn mehrere Effektebenen für dieselbe übergeordnete Ebene vorhanden sind. Höhere Ebenen werden auf unternummerierten Ebenen platziert.

Effektebenen können an `layer=comp` angehängt werden.

## Eigenschaften {#section-e11f795deff345779ce280a82cf221ca}

Effekt-Layer-Befehl. Der Wert *`n`* darf nicht 0 sein.

## Standard {#section-84bbe1cfe7a94040827c994323ac59d4}

Keine.

## Beispiel {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Verwandte Themen {#section-573273e9e0e64103a5764075f5e50180}

[layer=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
