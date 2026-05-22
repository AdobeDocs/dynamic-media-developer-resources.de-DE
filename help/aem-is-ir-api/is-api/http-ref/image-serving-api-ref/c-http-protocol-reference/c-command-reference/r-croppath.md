---
title: CropPathE
description: Ermöglicht das Zuschneiden zum Begrenzungsrahmen eines eingebetteten benannten Pfads. Durch dieses Zuschneiden ändert sich wiederum die Größe des Bildes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
TQID: 'https://experienceleague.adobe.com/zjmnN-7ACO78rMKs7H2S6b989IEHi2I9nPrS5FPaEFA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 173
ht-degree: 1%

---

# CropPathE{#croppathe}

Ermöglicht das Zuschneiden zum Begrenzungsrahmen eines eingebetteten benannten Pfads. Durch dieses Zuschneiden ändert sich wiederum die Größe des Bildes.

`cropPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Name des Pfads, der in das Ebenenquellbild eingebettet ist (nur ASCII). </p> <p> <span class="codeph"><span class="varname"> pathName</span></span> ist der Name eines Pfads, der in das Ebenenquellbild eingebettet ist. Der Pfad wird nach Bedarf automatisch transformiert, um die relative Ausrichtung mit dem Bildinhalt beizubehalten. Wenn mehr als ein <span class="codeph"><span class="varname"> pathName</span></span> angegeben ist, schneidet der Server den Begrenzungsrahmen jedes Pfads einzeln zu. Alle <span class="codeph"><span class="varname"> pathName</span></span>, die nicht im Quellbild gefunden werden, werden ignoriert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Ebenenattribut. Gilt für die aktuelle Ebene oder das zusammengesetzte Bild, falls `layer=comp`. Von Effektebenen ignoriert.

`cropPathE=` wird ignoriert, wenn im Ebenenquellbild kein Pfad mit dem angegebenen Namen gefunden wird oder wenn die Ebenenquelle kein Bild ist.

## Standard {#section-d1986aa31af14767aeb1b4a57add67f4}

Keine, für keinen zusätzlichen Zuschnitt der Ebene.

## Verwandte Themen {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[Zuschneiden](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab), [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
