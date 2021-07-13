---
description: Zur Manipulation von Grafiken können Sie Referenzpunkte verwenden, die den Orientierungspunkten auf einem Kompass gleichen.
solution: Experience Manager
title: FXG-Serverprotokoll
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 85%

---

# FXG-Serverprotokoll{#fxg-server-protocol}

Zur Manipulation von Grafiken können Sie Referenzpunkte verwenden, die den Orientierungspunkten auf einem Kompass gleichen.

Mit Referenzpunkten können Sie eine Grafik in Relation zu einem Referenzpunkt drehen, skalieren oder ihre Größe ändern. Die Bezugspunkte sind `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` und `southeast`. Beispielsweise können Sie eine Grafik auf ihrem Mittelpunkt 45 Grad drehen, indem Sie den Referenzpunkt center verwenden. Auf der nachfolgenden Abbildung werden die Positionen der Referenzpunkte gezeigt, eine Grafik, die auf Basis des Referenzpunkts `northWest` um 20 Grad gedrehte Grafik und die auf Basis des Referenzpunkts `east` um 20 Grad gedrehte Grafik.

![](assets/wp_ref_points.png)

* A. Referenzpunktstandorte
* B. Grafik
* C. Die um 20 Grad gedrehte Grafik vom `northWest`-Bezugspunkt
* D. Die um 20 Grad vom `east`-Bezugspunkt gedrehte Grafik

Die Syntax lautet:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

Der Standardwert ist none. Der Wert `inherit` leitet den Wert `s7:referencePoint` vom Seitenanfang oder der übergeordneten Gruppenebene an alle untergeordneten Elemente weiter, sofern der Wert nicht `none` lautet. Die Einstellung `none` bedeutet, dass kein Referenzpunkt für das Objekt festgelegt wurde und das FXG-Koordinatensystem verwendet wird.

>[!NOTE]
>
>Wenn Sie einen Referenzpunkt verwenden möchten und Verschiebungen im Objekt nach dessen Manipulierung vermeiden möchten, aktualisieren Sie die x- und y-Werte des Objekts, nachdem Sie es manipuliert haben.

Wenn ein Wert aus `s7:referencePoint` mit Gruppen (oder Pfaden, Linienelementen oder Elementen, die über keine explizite Breiten- und Höhendefinition verfügen) verwendet wird, gilt der Wert für den gesamten Begrenzungsrahmen der Gruppe. So dient beispielsweise die obere linke Ecke des Begrenzungsrahmens aller Objekte der Gruppe als Referenzpunkt `northWest` für die Gruppe; die rechte untere Ecke dient als Referenzpunkt `southEast`.
