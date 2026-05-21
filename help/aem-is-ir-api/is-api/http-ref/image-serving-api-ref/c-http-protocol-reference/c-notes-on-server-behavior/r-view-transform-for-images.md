---
description: Ansichtstransformation für Bilder
solution: Experience Manager
title: Ansichtstransformation für Bilder
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
TQID: 'https://experienceleague.adobe.com/PPSeNhcaJ4Nx8ojXOt9vqJFp7F9NGo4LO3UxdLKzmwo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 271
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
