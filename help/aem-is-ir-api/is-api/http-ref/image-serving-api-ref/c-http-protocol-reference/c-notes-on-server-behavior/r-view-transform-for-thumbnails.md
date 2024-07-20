---
description: 'Das Bild, das als Antwort auf eine req=tmb-Anfrage an den Client zurückgegeben wird, wird aus dem zusammengesetzten Bild abgeleitet, indem die folgenden Werte berücksichtigt werden: wid=, hei=, attribute DefaultThumbPix und attribute MaxPix.'
solution: Experience Manager
title: Transformation für Miniaturansichten anzeigen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# Transformation für Miniaturansichten anzeigen{#view-transform-for-thumbnails}

Das Bild, das als Antwort auf eine req=tmb-Anfrage an den Client zurückgegeben wird, wird aus dem zusammengesetzten Bild unter Berücksichtigung der folgenden Werte abgeleitet: wid=, hei=, attribute::DefaultThumbPix und attribute::MaxPix.

1. **Berechnen Sie den Ansichtsrect** - Verwenden Sie `wid=` oder den Breitenwert von `attribute::DefaultThumbPix` für die Breite des Ansichtsrects. Verwenden Sie `hei=` oder den Höhenwert von `attribute::DefaultThumbPix` für die Höhe. Der Ansichtsrect muss in diesem Schritt vollständig angegeben werden. (Beachten Sie, dass die Anzeige-rect mit der Ebene 0 rect übereinstimmt, wenn für Ebene 0 kein `size=`angegeben ist.)
1. **Composite skalieren** - Wenn `catalog::ThumbType=Crop`, wird der Composite auf das kleinstmögliche Bild skaliert, während weiterhin die gesamte Anzeige gefüllt wird. Zusätzliche Bilddaten werden abgeschnitten. Wenn der Wert `catalog::ThumbType= Fit` beträgt, wird der Verbund auf das größtmögliche Bild skaliert, während der Verbund dennoch in die Ansicht-Rect passt. Wenn `catalog::ThumbType=Texture`, wird der Verbund überhaupt nicht skaliert, um die in `catalog::ThumbRes` angegebene Auflösung beizubehalten.
1. **Füllen und Zuschneiden** - Die Anzeige-Rect wird mit der Farbe `bgc=` (oder, falls nicht angegeben, mit `attribute::ThumbBkgColor`) gefüllt. Der skalierte Verbund ist mit dem Attribut: `ThumbHorizAlign` und Attribut: `ThumbVertAlign` mit der Ansicht-Rect ausgerichtet. Der skalierte Verbund wird dann ohne weitere Skalierung mit dem ausgefüllten Ansichtsrect zusammengeführt. Alle Bereiche des Verbundes, die über die Ansicht-Rect hinausgehen, werden abgeschnitten.
