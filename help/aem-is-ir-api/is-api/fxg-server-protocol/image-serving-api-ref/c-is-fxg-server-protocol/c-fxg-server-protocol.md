---
title: FXG-Serverprotokoll
description: Zur Manipulation von Grafiken können Sie Referenzpunkte verwenden, die den Orientierungspunkten auf einem Kompass gleichen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
TQID: 'https://experienceleague.adobe.com/DXmhIshiUYoP-BlVe5cJFXbII9sEIdyo5YDkoKP-t0w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 28%

---

# FXG-Serverprotokoll{#fxg-server-protocol}

Zur Manipulation von Grafiken können Sie Referenzpunkte verwenden, die den Orientierungspunkten auf einem Kompass gleichen.

Mit Referenzpunkten können Sie eine Grafik in Relation zu einem Referenzpunkt drehen, skalieren oder ihre Größe ändern. Die Referenzpunkte sind `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` und `southeast`. Beispielsweise können Sie eine Grafik mithilfe des Bezugspunkts des Mittelpunkts um 45° in der Mitte drehen. Die folgende Abbildung zeigt, wo sich die Referenzpunkte befinden, eine Grafik, die Grafik um 20° von ihrem `northWest` Referenzpunkt gedreht, und die Grafik um 20° von ihrem `east` Referenzpunkt gedreht.

![Referenzpunktbild](assets/wp_ref_points.png)

* A. Positionen der Referenzpunkte
* B. Eine Grafik
* C. Die Grafik rotierte um 20° von ihrem `northWest` Bezugspunkt
* D. Die Grafik rotierte um 20° von ihrem `east` Bezugspunkt

Die Syntax lautet:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

Der Standardwert ist „Ohne“. Der `inherit`-Wert übergibt den `s7:referencePoint`-Wert, sofern er nicht `none` ist, vom oberen Rand der Seiten- oder Gruppenebene an alle untergeordneten Elemente. Die `none` bedeutet, dass es keinen Referenzpunkt für das Objekt gibt und das FXG-Koordinatensystem verwendet wird.

>[!NOTE]
>
>Wenn Sie einen Referenzpunkt verwenden möchten und Verschiebungen im Objekt nach dessen Manipulierung vermeiden möchten, aktualisieren Sie die x- und y-Werte des Objekts, nachdem Sie es manipuliert haben.

Wenn ein Wert aus `s7:referencePoint` für Gruppen (oder Pfade, Linienelemente oder Elemente ohne explizite Breiten- und Höhendefinitionen) verwendet wird, gilt der Wert für den kumulativen Begrenzungsrahmen der Gruppe. Beispielsweise dient der obere linke Punkt des Begrenzungsrahmens aller Objekte in der Gruppe als `northWest` Referenzpunkt für die Gruppe; der untere rechte Punkt dient als `southEast` Referenzpunkt.
