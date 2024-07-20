---
title: Beispiel C
description: Erstellen Sie eine Überlagerungsanwendung "Papierpuppe".
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Beispiel C{#example-c}

Erstellen Sie eine Überlagerungsanwendung &quot;Papierpuppe&quot;.

Ein Hintergrundbild enthält das Foto eines Modells oder Mannequins. Zusätzliche Datensätze im Bildkatalog enthalten verschiedene Bekleidungsartikel und Zubehörartikel, die so fotografiert werden, dass sie der Mannequin in Form und Größe entsprechen.

Jedes Kleidungsstück/Zubehörfoto ist maskiert und auf den Maskenbegrenzungsrahmen zugeschnitten, um die Bildgröße zu minimieren. Bildanker und -auflösungen werden sorgfältig kontrolliert, um die Ausrichtung zwischen den Ebenen und dem Hintergrundbild beizubehalten. Alle Bilder werden einem Bildkatalog hinzugefügt, wobei die entsprechenden Werte in `catalog::Resolution` und `catalog::Anchor` gespeichert sind.

Zusätzlich zur Überlagerung möchten Sie auch die Farbe für ausgewählte Elemente ändern. Die Datensätze für diese Elemente werden vorverarbeitet, um die Originalfarbe zu entfernen und die Helligkeit und den Kontrast in einer für den Farbbefehl geeigneten Weise anzupassen. Diese Vorverarbeitung kann offline mithilfe eines Bildbearbeitungswerkzeugs wie Adobe Photoshop durchgeführt werden oder in einfachen Fällen durch Hinzufügen von `op_brightness=` und `op_contrast=` zum Feld `catalog::Modifier`erfolgen.

Diese Anwendung rechtfertigt keine separate Vorlage, da alle Objekte bereits ordnungsgemäß durch ihre Bildanker ( `catalog::Anchor`) ausgerichtet und skaliert ( `catalog::Resolution`) sind. Es bleibt dem Client überlassen, eine angemessene Ebenenreihenfolge sicherzustellen.

Eine typische Anfrage könnte wie folgt aussehen:

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Nur die Höhe wird angegeben. Auf diese Weise kann das zurückgegebene Bild je nach Seitenverhältnis des Miniaturbilds variieren, ohne dass die Ränder mit der Hintergrundfarbe gefüllt werden.

Es sollte keine Rolle spielen, welche Auflösung für jede Ebene festgelegt ist, solange sie alle gleich sind. In dieser Version dürfen Ansichten nicht größer sein als die zusammengesetzten Bilder. Durch die Angabe eines Werts mit großer Auflösung werden Probleme im Zusammenhang mit dieser Beschränkung vermieden. Die Verarbeitung und Komposition erfolgt in der optimalen Auflösung für die angeforderte Bildgröße, um die beste Leistung und Ausgabequalität zu erzielen.

Die Befehle &quot;`res=`&quot;können weggelassen werden, wenn alle Quellbilder in voller Skalierung dieselbe Auflösung aufweisen (was bei dieser Art von Anwendung wahrscheinlich der Fall ist).

Die `rootId` muss für alle `src=` -Befehle angegeben werden, auch wenn sie mit den im URL-Pfad angegebenen `rootId` übereinstimmen.

Wenn kein Bildkatalog verwendet werden soll, ist ein auflösungsbasierter Ansatz zur Skalierung nicht möglich. In diesem Fall müssen die expliziten Skalierungsfaktoren für jedes Ebenenelement basierend auf dem Verhältnis der `catalog::Resolution` -Werte für jede Ebene zum `catalog::Resolution` -Wert der Hintergrundebene berechnet werden. Die Zusammenstellungsanforderung (mit weniger Ebenen) könnte daher wie folgt aussehen:

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
