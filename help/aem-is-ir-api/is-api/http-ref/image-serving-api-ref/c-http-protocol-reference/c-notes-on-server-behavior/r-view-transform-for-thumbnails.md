---
description: Das Bild, das dem Client als Antwort auf eine Anforderung von req=tmb zurückgegeben wird, wird vom Composite-Bild abgeleitet, indem die folgenden Werte mit wid=, hei=, attribute DefaultThumbPix und attribute MaxPix berücksichtigt werden.
seo-description: Das Bild, das dem Client als Antwort auf eine Anforderung von req=tmb zurückgegeben wird, wird vom Composite-Bild abgeleitet, indem die folgenden Werte mit wid=, hei=, attribute DefaultThumbPix und attribute MaxPix berücksichtigt werden.
seo-title: Ansicht-Transformation für Miniaturansichten
solution: Experience Manager
title: Ansicht-Transformation für Miniaturansichten
topic: Scene7 Image Serving - Image Rendering API
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# Ansicht-Transformation für Miniaturansichten{#view-transform-for-thumbnails}

Das Bild, das dem Client als Antwort auf eine Anforderung von req=tmb zurückgegeben wird, wird aus dem Composite-Bild abgeleitet, indem die folgenden Werte berücksichtigt werden: wid=, hei=, attribute::DefaultThumbPix, and attribute::MaxPix.

1. **Berechnen Sie die Ansicht rect** - Use `wid=` or the width value of `attribute::DefaultThumbPix` for the width of the Ansicht rect. Verwenden Sie `hei=` oder den Höhenwert `attribute::DefaultThumbPix` für die Höhe. In diesem Schritt muss das Ansichten-Rechteck vollständig angegeben werden. (Beachten Sie, dass die Ansicht rect mit der Ebene 0 rect identisch ist, wenn für Ebene 0 keine Angabe `size=`vorliegt).
1. **Verbundwerkstoff** skalieren: Wenn `catalog::ThumbType=Crop`das Verbundwerkstoff auf das kleinstmögliche Bild skaliert wird, während gleichzeitig die gesamte Ansicht rect gefüllt wird; Zusätzliche Bilddaten werden abgeschnitten. Wenn `catalog::ThumbType= Fit`dann wird das Composite auf das größtmögliche Bild skaliert, während das gesamte Composite in der Ansicht rect. Wenn `catalog::ThumbType=Texture`das Composite nicht skaliert wird, um die in `catalog::ThumbRes`angegebene Auflösung zu erhalten.
1. **Füllung und Beschneiden** - Die Ansicht rect wird mit der `bgc=` Farbe gefüllt (oder, falls nicht angegeben, mit `attribute::ThumbBkgColor`). Das skalierte Composite ist mit dem Attribut &quot;Ansicht rect&quot;ausgerichtet: `ThumbHorizAlign` und Attribut: `ThumbVertAlign`. Das skalierte Composite wird dann ohne weitere Skalierung mit der ausgefüllten Ansicht zusammengeführt. Alle Bereiche des Verbundwerkstoffes, die über die Ansicht hinausgehen, werden abgeschnitten.

