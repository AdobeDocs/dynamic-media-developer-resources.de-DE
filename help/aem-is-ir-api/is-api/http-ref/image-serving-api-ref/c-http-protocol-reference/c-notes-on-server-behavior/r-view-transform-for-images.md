---
description: Transformation für Bilder anzeigen
solution: Experience Manager
title: Transformation für Bilder anzeigen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Transformation für Bilder anzeigen{#view-transform-for-images}

Das Bild, das dem Client als Antwort auf eine `req=img` -Anfrage wird aus dem zusammengesetzten Bild unter Berücksichtigung der folgenden Werte abgeleitet: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`und die Größe des zusammengesetzten Bildes.

Wenn `wid=` und `hei=` festgelegt sind und `scl=` nicht festgelegt ist, wird das zusammengesetzte Bild so skaliert, dass es vollständig in die von `wid=` und `hei=`. Wenn sich das Seitenverhältnis der Ansichtsrect von dem des zusammengesetzten Bildes unterscheidet, wird das skalierte zusammengesetzte Bild mithilfe des `align=` -Wert, sofern angegeben, oder andernfalls zentriert. Alle Bereiche, die nicht von Bilddaten abgedeckt werden, werden mit `bgc=` oder, falls nicht angegeben, mit `attribute::BkgColor`.

Wenn `scl=` festgelegt ist, wird das zusammengesetzte Bild um diesen Skalierungsfaktor skaliert. Wenn `wid=` und/oder `hei=` auch angegeben ist, wird das skalierte Bild dann auf zugeschnitten `wid=` und/oder `hei=` oder es wird bei Bedarf zusätzlicher Speicherplatz hinzugefügt. `align=` gibt an, wo das Bild beschnitten wird oder zusätzlicher Speicherplatz hinzugefügt wird und zusätzlicher Platz mit `bgc=` oder `attribute::BkgColor`.

Wenn `wid=`, `hei=` nor `scl=` angegeben werden und wenn die Breite oder Höhe des zusammengesetzten Bildes `attribute::DefaultPix`, wird das zusammengesetzte Bild auf maximal maximal maximal maximal maximal `attribute::DefaultPix`. Andernfalls wird das zusammengesetzte Bild ohne Skalierung verwendet.

Um sicherzustellen, dass das Ansichtsbild ohne weitere Skalierung zurückgegeben wird, geben Sie `scl=1`.

Wenn `rgn=` angegeben ist, wird das Antwortbild entsprechend zugeschnitten, um die endgültige Antwortbildgröße zu erreichen. Diese Größe wird mit `attribute::MaxPix` (sofern definiert) und ein Fehler erzeugt wird, wenn das Antwortbild in beiden Dimensionen größer ist.

Wenn `fmt=` gibt Daten ohne Alpha an, transparente Bereiche im Antwortbild werden mit `bgc=` oder `attribute::BkgColor`.
