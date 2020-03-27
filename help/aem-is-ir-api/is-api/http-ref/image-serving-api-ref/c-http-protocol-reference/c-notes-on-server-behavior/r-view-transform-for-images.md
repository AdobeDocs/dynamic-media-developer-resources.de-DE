---
description: 'null'
seo-description: 'null'
seo-title: Ansicht-Transformation für Bilder
solution: Experience Manager
title: Ansicht-Transformation für Bilder
topic: Scene7 Image Serving - Image Rendering API
uuid: 8594f746-0e58-4a59-933c-a44dc0b06c25
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ansicht-Transformation für Bilder{#view-transform-for-images}

Das Bild, das dem Client als Antwort auf eine `req=img` Anforderung zurückgegeben wird, wird vom Composite-Bild abgeleitet, indem die folgenden Werte berücksichtigt werden: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`und die Größe des Composite-Bildes.

Wenn `wid=` und `hei=` Sie dies nicht tun, wird das Composite-Bild so skaliert, dass es vollständig in die Ansicht rect von `scl=` und `wid=` `hei=`. Wenn das Seitenverhältnis des Ansicht rect sich von dem des Composite-Bilds unterscheidet, wird das skalierte Composite-Bild innerhalb des Ansicht-Rects mit dem `align=` Wert (falls angegeben) ausgerichtet oder anderweitig zentriert. Alle Leerzeichen, die nicht von Bilddaten abgedeckt werden, werden mit `bgc=` oder, falls nicht angegeben, mit `attribute::BkgColor`gefüllt.

Wenn `scl=` angegeben, wird das Composite-Bild um diesen Skalierungsfaktor skaliert. Wenn `wid=` und/oder `hei=` auch angegeben wird, wird das skalierte Bild zugeschnitten `wid=` `hei=` und/oder es wird zusätzlicher Speicherplatz hinzugefügt, je nach Bedarf. `align=` gibt an, wo das Bild beschnitten wird oder zusätzlicher Speicherplatz hinzugefügt wird und zusätzlicher Speicherplatz mit `bgc=` oder `attribute::BkgColor`gefüllt wird.

Wenn weder `wid=`noch `hei=` noch `scl=` angegeben wurden und die Breite oder Höhe des Composite-Bilds größer ist `attribute::DefaultPix`, wird das Composite-Bild skaliert, um nicht größer zu sein `attribute::DefaultPix`. Andernfalls wird das Composite-Bild ohne Skalierung verwendet.

Um sicherzustellen, dass das Bild der Ansicht ohne weitere Skalierung zurückgegeben wird, geben Sie `scl=1`an.

Wenn dies angegeben `rgn=` ist, wird das Antwortbild entsprechend abgeschnitten, um die endgültige Antwortbildgröße zu erhalten. Diese Größe wird mit `attribute::MaxPix` (sofern definiert) verglichen und es wird ein Fehler generiert, wenn das Antwortbild in beiden Dimensionen größer ist.

Wenn Daten ohne Alpha `fmt=` angegeben werden, werden alle transparenten Bereiche im Antwortbild mit `bgc=` oder `attribute::BkgColor`gefüllt.
