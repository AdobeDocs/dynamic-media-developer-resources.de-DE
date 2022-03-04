---
description: 'Das Bild, das als Antwort auf eine req=tmb-Anfrage an den Client zurückgegeben wird, wird aus dem zusammengesetzten Bild abgeleitet, indem die folgenden Werte berücksichtigt werden: wid=, hei=, attribute DefaultThumbPix und attribute MaxPix.'
solution: Experience Manager
title: Transformation für Miniaturansichten anzeigen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Transformation für Miniaturansichten anzeigen{#view-transform-for-thumbnails}

Das Bild, das als Antwort auf eine req=tmb-Anfrage an den Client zurückgegeben wird, wird aus dem zusammengesetzten Bild unter Berücksichtigung der folgenden Werte abgeleitet: wid=, hei=, attribute::DefaultThumbPix und attribute::MaxPix.

1. **Ansichtsrect berechnen** - Verwendung `wid=` oder der Breitenwert von `attribute::DefaultThumbPix` für die Breite des Ansichtsrects. Verwendung `hei=` oder der Höhenwert von `attribute::DefaultThumbPix` für die Höhe. Der Ansichtsrect muss in diesem Schritt vollständig angegeben werden. (Beachten Sie, dass die Ansichtsrect mit der Ebene 0 rect übereinstimmt, falls nicht `size=`ist für Ebene 0 angegeben).
1. **Skalieren des Composite** - Wenn `catalog::ThumbType=Crop`, wird der Verbund auf das kleinstmögliche Bild skaliert, während weiterhin die gesamte Ansicht zurückgesetzt wird. zusätzliche Bilddaten abgeschnitten werden. Wenn `catalog::ThumbType= Fit`, dann wird der Verbund auf das größtmögliche Bild skaliert, während der gesamte Verbund in die Ansicht rect einpasst. Wenn `catalog::ThumbType=Texture`, wird der Verbund überhaupt nicht skaliert, um die in `catalog::ThumbRes`.
1. **Füllen und Zuschneiden** - Der Ansichtsrect wird mit dem `bgc=` Farbe (oder, falls nicht angegeben, mit `attribute::ThumbBkgColor`). Das skalierte Composite ist mit dem Attribut view rect ausgerichtet: `ThumbHorizAlign` und Attribut: `ThumbVertAlign`. Der skalierte Verbund wird dann ohne weitere Skalierung mit dem ausgefüllten Ansichtsrect zusammengeführt. Alle Bereiche des Verbundes, die über die Ansicht-Rect hinausgehen, werden abgeschnitten.
