---
title: Ergebnis
description: Wählen Sie Effektebene. Wählt eine Effektebene aus und startet ein neues Ebenensegment in der Anfragezeichenfolge, das der aktuellen Ebene zugeordnet ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# Ergebnis{#effect}

Wählen Sie Effektebene. Wählt eine Effektebene aus und startet ein neues Ebenensegment in der Anfragezeichenfolge, das der aktuellen Ebene zugeordnet ist.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> N</span></span> </p> </td> 
  <td class="stentry"> <p>Effekt-Ebenennummer (int ungleich 0). </p></td> 
 </tr> 
</table>

Alle Befehle innerhalb des neuen Segments werden auf die angegebene Effektebene angewendet. Ein Effektebenen-Segment wird durch den nächsten `layer=` oder `effect=` Befehl oder durch das Ende der Anfrage beendet.

Der Wert *`n`* muss für die Effekte der äußeren Ebene (d. h. hinter der übergeordneten Ebene) kleiner als 0 und für die Effekte der inneren Ebene (d. h. innerhalb der übergeordneten Ebene) größer als 0 sein. Effektebenenzahlen müssen nicht aufeinander folgend sein.

Die Effektebenennummer gibt die z-Reihenfolge an, wenn mehrere Effektebenen für dieselbe übergeordnete Ebene vorhanden sind. Ebenen mit höheren Nummern werden auf Ebenen mit niedrigeren Nummern platziert.

Effektebenen können mit `layer=comp` verbunden werden.

## Eigenschaften {#section-e11f795deff345779ce280a82cf221ca}

Effekt-Ebenenbefehl. Der Wert *`n`* darf nicht 0 sein.

## Standard {#section-84bbe1cfe7a94040827c994323ac59d4}

Keine.

## Beispiel {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Verwandte Themen {#section-573273e9e0e64103a5764075f5e50180}

[Layer=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
