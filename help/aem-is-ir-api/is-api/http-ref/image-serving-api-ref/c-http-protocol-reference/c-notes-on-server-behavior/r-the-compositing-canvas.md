---
description: Wenn req=img, wird die Größe der Arbeitsfläche für die Zusammenstellung vollständig durch die Größe der Ebene 0 bestimmt.
solution: Experience Manager
title: Die Arbeitsfläche für die Zusammenstellung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# Die Arbeitsfläche für die Zusammenstellung{#the-compositing-canvas}

Wenn req=img, wird die Größe der Arbeitsfläche für die Zusammenstellung vollständig durch die Größe der Ebene 0 bestimmt.

Wenn `size=` für Layer 0 nicht explizit angegeben ist, werden die Ebenen-Transformationen verwendet, um die Größe der Arbeitsfläche für die Zusammenstellung zu berechnen (siehe unten).

Wenn `req=tmb` die Größe der Arbeitsfläche für die Zusammenstellung durch die für Ebene 0 angegebene `size=` bestimmt wird, oder wenn die Größe nicht angegeben ist, wird die Größe der Arbeitsfläche für die Zusammenstellung auf die Anzeige-Referenz eingestellt (siehe unten).
