---
description: Ansichtstransformation für Bilder
solution: Experience Manager
title: Ansichtstransformation für Bilder
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Ansichtstransformation für Bilder{#view-transform-for-images}

Das Bild, das als Antwort auf eine `req=img` an den Client zurückgegeben wird, wird aus dem zusammengesetzten Bild abgeleitet, indem die folgenden Werte berücksichtigt werden: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` und die Größe des zusammengesetzten Bildes.

Wenn `wid=` und `hei=` angegeben sind und `scl=` nicht, wird das zusammengesetzte Bild so skaliert, dass es vollständig in die von `wid=` und `hei=` definierte Ansicht passt. Wenn das Seitenverhältnis der Ansicht rect sich von dem des zusammengesetzten Bildes unterscheidet, wird das skalierte zusammengesetzte Bild innerhalb der Ansicht rect ausgerichtet, indem der `align=` verwendet wird, falls angegeben, oder es wird anderweitig zentriert. Jeder Raum, der nicht von Bilddaten abgedeckt wird, wird mit `bgc=` oder, falls nicht anders angegeben, mit `attribute::BkgColor` gefüllt.

Wenn `scl=` angegeben ist, wird das zusammengesetzte Bild um diesen Skalierungsfaktor skaliert. Wenn `wid=` und/oder `hei=` ebenfalls angegeben sind, wird das skalierte Bild auf `wid=` zugeschnitten und/oder `hei=` oder zusätzlicher Platz hinzugefügt. `align=` gibt an, wo das Bild abgeschnitten oder zusätzlicher Platz hinzugefügt wird und jeder zusätzliche Platz mit `bgc=` oder `attribute::BkgColor` gefüllt wird.

Wenn weder `wid=`, `hei=` noch `scl=` angegeben sind und eine Breite oder Höhe des zusammengesetzten Bildes `attribute::DefaultPix` überschreitet, wird das zusammengesetzte Bild so skaliert, dass es `attribute::DefaultPix` nicht überschreitet. Andernfalls wird das zusammengesetzte Bild ohne Skalierung verwendet.

Um sicherzustellen, dass das Ansichtsbild ohne weitere Skalierung zurückgegeben wird, geben Sie `scl=1` an.

Wenn `rgn=` angegeben ist, wird das Antwortbild entsprechend abgeschnitten, um die endgültige Größe des Antwortbildes zu erhalten. Diese Größe wird mit `attribute::MaxPix` verglichen (falls definiert), und ein Fehler wird erzeugt, wenn das Antwortbild in einer der Dimensionen größer ist.

Wenn `fmt=` Daten ohne Alpha angibt, werden alle transparenten Bereiche im Antwortbild mit `bgc=` oder `attribute::BkgColor` gefüllt.
