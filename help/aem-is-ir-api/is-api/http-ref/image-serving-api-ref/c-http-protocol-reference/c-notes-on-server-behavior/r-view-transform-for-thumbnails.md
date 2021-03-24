---
description: Das Bild, das dem Client als Antwort auf eine Anforderung von req=tmb zurückgegeben wird, wird vom Composite-Bild abgeleitet, indem die folgenden Werte mit wid=, hei=, attribute DefaultThumbPix und attribute MaxPix berücksichtigt werden.
solution: Experience Manager
title: Ansicht-Transformation für Miniaturansichten
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Ansicht-Transformation für Miniaturansichten{#view-transform-for-thumbnails}

Das Bild, das dem Client als Antwort auf eine Anforderung von req=tmb zurückgegeben wird, wird aus dem Composite-Bild abgeleitet, indem die folgenden Werte berücksichtigt werden: wid=, hei=, attribute::DefaultThumbPix, and attribute::MaxPix.

1. **Berechnen Sie die Ansicht rect** - Use  `wid=` or the width value of  `attribute::DefaultThumbPix` for the width of the Ansicht rect. Verwenden Sie für die Höhe `hei=` oder den Höhenwert `attribute::DefaultThumbPix`. In diesem Schritt muss das Ansichten-Rechteck vollständig angegeben werden. (Beachten Sie, dass die Ansicht rect mit der Ebene 0 rect identisch ist, wenn für Ebene 0 kein `size=`angegeben ist.)
1. **Composite**  skalieren: Wenn  `catalog::ThumbType=Crop`das Composite auf das kleinstmögliche Bild skaliert wird, während die gesamte Ansicht noch gefüllt wird; Zusätzliche Bilddaten werden abgeschnitten. Wenn `catalog::ThumbType= Fit`, dann wird das Composite auf das größtmögliche Bild skaliert, während das gesamte Composite in der Ansicht rect. Wenn `catalog::ThumbType=Texture`, wird das Composite überhaupt nicht skaliert, um die unter `catalog::ThumbRes` angegebene Auflösung beizubehalten.
1. **Ausfüllen und Beschneiden** : Die Ansicht rect wird mit der  `bgc=` Farbe (oder, falls nicht angegeben, mit  `attribute::ThumbBkgColor`) gefüllt. Das skalierte Composite ist mit dem Attribut &quot;Ansicht rect&quot;ausgerichtet: `ThumbHorizAlign` und Attribut: `ThumbVertAlign`. Das skalierte Composite wird dann ohne weitere Skalierung mit der ausgefüllten Ansicht zusammengeführt. Alle Bereiche des Verbundwerkstoffes, die über die Ansicht hinausgehen, werden abgeschnitten.

