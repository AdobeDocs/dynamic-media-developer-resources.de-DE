---
description: 'Das Bild, das als Antwort auf eine req=tmb-Anfrage an den Client zurückgegeben wird, wird aus dem zusammengesetzten Bild abgeleitet, indem die folgenden Werte berücksichtigt werden: wid=, hei=, attribute, DefaultThumbPix und attribute MaxPix.'
solution: Experience Manager
title: Ansichtstransformation für Miniaturen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
TQID: 'https://experienceleague.adobe.com/yx1jgWnx-cwMDmBY2NOzYEyEjCqehPqGBK31MvGo-4o'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 245
ht-degree: 0%

---

# Ansichtstransformation für Miniaturen{#view-transform-for-thumbnails}

Das Bild, das als Antwort auf eine req=tmb-Anfrage an den Client zurückgegeben wird, wird aus dem zusammengesetzten Bild abgeleitet, indem die folgenden Werte berücksichtigt werden: wid=, hei=, attribute::DefaultThumbPix und attribute::MaxPix.

1. **Ansicht rekt berechnen** - Verwenden Sie `wid=` oder den Breitenwert von `attribute::DefaultThumbPix` für die Breite der Ansicht rekt. Verwenden Sie `hei=` oder den Höhenwert von `attribute::DefaultThumbPix` für die Höhe. Die reaktive Ansicht muss in diesem Schritt vollständig angegeben werden. (Beachten Sie, dass die Ansicht rect mit der Ebene 0 rect identisch ist, wenn kein `size=`für Ebene 0 angegeben ist).
1. **Verbund skalieren** - Wenn `catalog::ThumbType=Crop`, wird der Verbund auf das kleinstmögliche Bild skaliert, während die gesamte Ansicht noch vollständig gefüllt ist. Zusätzliche Bilddaten werden abgeschnitten. Wenn `catalog::ThumbType= Fit`, wird der Verbund auf das größtmögliche Bild skaliert, während der gesamte Verbund immer noch in die rete Ansicht passt. Wenn `catalog::ThumbType=Texture`, wird das zusammengesetzte Element überhaupt nicht skaliert, um die in `catalog::ThumbRes` angegebene Auflösung beizubehalten.
1. **Füllen und Zuschneiden** - Die rechte Ansicht wird mit der `bgc=` Farbe gefüllt (oder, falls nicht anders angegeben, mit `attribute::ThumbBkgColor`). Der skalierte Verbund wird mithilfe des Attributs: `ThumbHorizAlign` und des Attributs: `ThumbVertAlign` mit der Ansicht rect ausgerichtet. Der skalierte Verbund wird dann ohne weitere Skalierung mit der ausgefüllten Ansicht zusammengeführt. Alle Bereiche des zusammengesetzten Elements, die über die reine Ansicht hinausgehen, werden abgeschnitten.
