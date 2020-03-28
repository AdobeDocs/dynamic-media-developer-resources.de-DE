---
description: Erstellen Sie eine Layeranwendung "Papierpuppe".
seo-description: Erstellen Sie eine Layeranwendung "Papierpuppe".
seo-title: Beispiel C
solution: Experience Manager
title: Beispiel C
topic: Scene7 Image Serving - Image Rendering API
uuid: 25f228c2-dc03-461a-aee8-40fdb3d4cf5e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Beispiel C{#example-c}

Erstellen Sie eine Layeranwendung &quot;Papierpuppe&quot;.

Ein Hintergrundbild enthält das Foto eines Modells oder Mannequins. Zusätzliche Datensätze im Bildkatalog enthalten verschiedene Bekleidung- und Zubehörteile, die nach Form und Größe des Mannequins fotografiert werden.

Jedes Bekleidungs-/Zubehörfoto wird maskiert und auf den Maskenbegrenzungsrahmen zugeschnitten, um die Bildgröße zu minimieren. Bildanker und -auflösungen werden sorgfältig gesteuert, um die Ausrichtung zwischen den Ebenen und dem Hintergrundbild beizubehalten. Alle Bilder werden einem Bildkatalog hinzugefügt, wobei die entsprechenden Werte in und `catalog::Resolution` `catalog::Anchor`gespeichert werden.

Neben der Überlagerung möchten wir auch die Farbe für ausgewählte Elemente ändern. Die Datensätze für diese Elemente werden vorverarbeitet, um die Originalfarbe zu entfernen und die Helligkeit und den Kontrast in einer Weise anzupassen, die für den Farbbefehl geeignet ist. Diese Vorverarbeitung kann offline mit einem Bildbearbeitungstool wie Fotoshop oder in einfachen Fällen trivial durchgeführt werden, indem Sie dem `op_brightness=` Feld hinzufügen `op_contrast=` und `catalog::Modifier`es hinzufügen.

Diese Anwendung benötigt keine separate Vorlage, da alle Objekte bereits korrekt an ihren Bildankern ( `catalog::Anchor`) ausgerichtet und skaliert ( `catalog::Resolution`) sind. Wir überlassen es dem Kunden, eine angemessene Ebenenreihenfolge sicherzustellen.

Eine typische Anforderung könnte wie folgt aussehen:

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Es wird nur die Höhe angegeben. Auf diese Weise kann das zurückgegebene Bild je nach Seitenverhältnis des Schaufensterbilds variieren, ohne dass die Ränder mit der Hintergrundfarbe gefüllt werden.

Es sollte nicht darauf ankommen, welche Auflösung für jede Ebene angegeben wird, solange sie alle gleich sind. In dieser Version ist es nicht zulässig, Ansichten größer als die Composite-Bilder zu sein. Wenn Sie einen Wert mit hoher Auflösung festlegen, werden Probleme im Zusammenhang mit dieser Einschränkung vermieden. Die Verarbeitung und Komposition erfolgt mit der optimalen Auflösung für die angeforderte Bildgröße, um eine optimale Leistung und Ausgabequalität zu erzielen.

Die `res=` Befehle können weggelassen werden, wenn alle Quellbilder dieselbe Auflösung im vollen Maßstab haben (was bei dieser Art von Anwendung wahrscheinlich der Fall ist).

Der `rootId` muss für alle `src=` Befehle angegeben werden, auch wenn sie mit dem im URL-Pfad angegebenen identisch sind `rootId` .

Wenn kein Bildkatalog verwendet werden soll, ist ein auflösungsbasierter Ansatz zur Skalierung nicht möglich. In diesem Fall müssen für jedes Ebenenelement explizite Skalierungsfaktoren berechnet werden, basierend auf dem Verhältnis der `catalog::Resolution` Werte für jede Ebene zum `catalog::Resolution` Wert der Hintergrundebene. Die Compositing-Anforderung (mit weniger Ebenen) könnte daher wie folgt aussehen:

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

