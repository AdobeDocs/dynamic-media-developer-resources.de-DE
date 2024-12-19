---
description: Wenn req=img, wird die Größe der Compositing-Leinwand vollständig durch die Größe der Schicht 0 bestimmt.
solution: Experience Manager
title: Die Arbeitsfläche für die Komposition
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Die Arbeitsfläche für die Komposition{#the-compositing-canvas}

Wenn req=img, wird die Größe der Compositing-Leinwand vollständig durch die Größe der Schicht 0 bestimmt.

Wenn die `size=` für Ebene 0 nicht explizit angegeben ist, werden die Ebenentransformationen verwendet, um die Größe der Arbeitsfläche für die Komposition zu berechnen (siehe unten).

Wenn `req=tmb`, wird die Größe der Arbeitsfläche für das Erstellen durch die für Ebene 0 angegebene `size=` bestimmt. Wenn die Größe nicht angegeben ist, wird die Größe der Arbeitsfläche für das Erstellen auf die rechte Ansicht festgelegt (siehe unten).
