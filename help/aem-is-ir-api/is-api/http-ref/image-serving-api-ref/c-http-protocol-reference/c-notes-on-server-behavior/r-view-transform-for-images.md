---
description: Transformation für Bilder anzeigen
solution: Experience Manager
title: Transformation für Bilder anzeigen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Transformation für Bilder anzeigen{#view-transform-for-images}

Das Bild, das als Antwort auf eine `req=img`-Anfrage an den Client zurückgegeben wird, wird aus dem zusammengesetzten Bild unter Berücksichtigung der folgenden Werte abgeleitet: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` und die Größe des zusammengesetzten Bildes.

Wenn `wid=` und `hei=` angegeben sind und `scl=` nicht angegeben ist, wird das zusammengesetzte Bild so skaliert, dass es vollständig in das von `wid=` und `hei=` definierte Ansichtsrect passt. Wenn das Seitenverhältnis der Ansichtsrect sich von dem des zusammengesetzten Bildes unterscheidet, wird das skalierte zusammengesetzte Bild innerhalb der Ansichtsrect mit dem `align=` -Wert ausgerichtet, sofern angegeben, oder es wird anderweitig zentriert. Alle Leerzeichen, die nicht von Bilddaten abgedeckt werden, werden mit `bgc=` oder, falls nicht angegeben, mit `attribute::BkgColor` gefüllt.

Wenn `scl=` angegeben ist, wird das zusammengesetzte Bild um diesen Skalierungsfaktor skaliert. Wenn auch `wid=` und/oder `hei=` angegeben ist, wird das skalierte Bild dann auf `wid=` zugeschnitten und/oder `hei=` oder es wird nach Bedarf zusätzlicher Speicherplatz hinzugefügt. `align=` gibt an, wo das Bild beschnitten oder zusätzlicher Speicherplatz hinzugefügt wird und zusätzlicher Speicherplatz mit  `bgc=` oder  `attribute::BkgColor`aufgefüllt wird.

Wenn weder `wid=`, `hei=` noch `scl=` angegeben sind und die Breite oder Höhe des zusammengesetzten Bildes `attribute::DefaultPix` überschreitet, wird das zusammengesetzte Bild skaliert, um `attribute::DefaultPix` nicht zu überschreiten. Andernfalls wird das zusammengesetzte Bild ohne Skalierung verwendet.

Um sicherzustellen, dass das Ansichtsbild ohne weitere Skalierung zurückgegeben wird, geben Sie `scl=1` an.

Wenn `rgn=` angegeben ist, wird das Antwortbild entsprechend zugeschnitten, um die endgültige Antwortbildgröße zu erreichen. Diese Größe wird mit `attribute::MaxPix` (sofern definiert) verglichen und ein Fehler wird erzeugt, wenn das Antwortbild in beiden Dimensionen größer ist.

Wenn `fmt=` Daten ohne Alpha angibt, werden alle transparenten Bereiche im Antwortbild mit `bgc=` oder `attribute::BkgColor` gefüllt.
