---
title: FXG-Serverprotokoll
description: Zur Manipulation von Grafiken können Sie Referenzpunkte verwenden, die den Orientierungspunkten auf einem Kompass gleichen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 69%

---

# FXG-Serverprotokoll{#fxg-server-protocol}

Zur Manipulation von Grafiken können Sie Referenzpunkte verwenden, die den Orientierungspunkten auf einem Kompass gleichen.

Mit Referenzpunkten können Sie eine Grafik in Relation zu einem Referenzpunkt drehen, skalieren oder ihre Größe ändern. Die Bezugspunkte sind `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` und `southeast`. Beispielsweise können Sie eine Grafik mit dem mittleren Bezugspunkt um 45° drehen. Die folgende Abbildung zeigt, wo sich die Referenzpunkte befinden, eine Grafik, die um 20° von ihrem `northWest`-Bezugspunkt gedrehte Grafik und die um 20° von ihrem `east`-Bezugspunkt aus gedrehte Grafik.

![Referenz-Punktbild](assets/wp_ref_points.png)

* A. Referenzpunktstandorte
* B. Grafik
* C. Die um 20° vom Bezugspunkt `northWest` gedrehte Grafik
* D. Die um 20° vom `east`-Bezugspunkt gedrehte Grafik

Die Syntax lautet:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

Der Standardwert ist none. Der Wert `inherit` leitet den Wert `s7:referencePoint` vom Seitenanfang oder der übergeordneten Gruppenebene an alle untergeordneten Elemente weiter, sofern der Wert nicht `none` lautet. Die Einstellung `none` bedeutet, dass kein Referenzpunkt für das Objekt festgelegt wurde und das FXG-Koordinatensystem verwendet wird.

>[!NOTE]
>
>Wenn Sie einen Referenzpunkt verwenden möchten und Verschiebungen im Objekt nach dessen Manipulierung vermeiden möchten, aktualisieren Sie die x- und y-Werte des Objekts, nachdem Sie es manipuliert haben.

Wenn ein Wert aus `s7:referencePoint` mit Gruppen (oder Pfaden, Linienelementen oder Elementen, die über keine explizite Breiten- und Höhendefinition verfügen) verwendet wird, gilt der Wert für den gesamten Begrenzungsrahmen der Gruppe. So dient beispielsweise die obere linke Ecke des Begrenzungsrahmens aller Objekte der Gruppe als Referenzpunkt `northWest` für die Gruppe; die rechte untere Ecke dient als Referenzpunkt `southEast`.
