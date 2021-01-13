---
description: Ansicht-Transformation für Bilder
solution: Experience Manager
title: Ansicht-Transformation für Bilder
topic: Scene7 Image Serving - Image Rendering API
uuid: 8594f746-0e58-4a59-933c-a44dc0b06c25
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---


# Ansicht-Transformation für Bilder{#view-transform-for-images}

Das Bild, das dem Client als Antwort auf eine `req=img`-Anforderung zurückgegeben wird, wird vom Composite-Bild abgeleitet, indem die folgenden Werte berücksichtigt werden: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` und die Größe des Composite-Bildes.

Wenn `wid=` und `hei=` angegeben sind und `scl=` nicht, wird das Composite-Bild so skaliert, dass es vollständig in den durch `wid=` und `hei=` definierten Ansicht-Rekt passt. Wenn das Seitenverhältnis des Ansicht rect sich von dem des Composite-Bilds unterscheidet, wird das skalierte Composite-Bild innerhalb des Ansicht-Rects mit dem Wert `align=` (sofern angegeben) ausgerichtet oder anderweitig zentriert. Alle Leerzeichen, die nicht von Bilddaten abgedeckt werden, werden mit `bgc=` oder, falls nicht angegeben, mit `attribute::BkgColor` gefüllt.

Wenn `scl=` angegeben ist, wird das Composite-Bild um diesen Skalierungsfaktor skaliert. Wenn auch `wid=` und/oder `hei=` angegeben ist, wird das skalierte Bild auf `wid=` zugeschnitten und/oder `hei=` oder es wird nach Bedarf zusätzlicher Speicherplatz hinzugefügt. `align=` gibt an, wo das Bild beschnitten wird oder zusätzlicher Speicherplatz hinzugefügt wird und zusätzlicher Speicherplatz mit  `bgc=` oder  `attribute::BkgColor`gefüllt wird.

Wenn weder `wid=` noch `hei=` noch `scl=` angegeben sind und die Breite oder Höhe des Composite-Bildes `attribute::DefaultPix` überschreitet, wird das Composite-Bild skaliert, um nicht größer als `attribute::DefaultPix` zu sein. Andernfalls wird das Composite-Bild ohne Skalierung verwendet.

Um sicherzustellen, dass das Ansicht-Image ohne weitere Skalierung zurückgegeben wird, geben Sie `scl=1` an.

Wenn `rgn=` angegeben ist, wird das Antwortbild entsprechend beschnitten, um die endgültige Antwortbildgröße zu erhalten. Diese Größe wird mit `attribute::MaxPix` (sofern definiert) verglichen. Wenn das Antwortbild größer ist, wird ein Fehler erzeugt.

Wenn `fmt=` Daten ohne Alpha angibt, werden transparente Bereiche im Antwortbild mit `bgc=` oder `attribute::BkgColor` gefüllt.
