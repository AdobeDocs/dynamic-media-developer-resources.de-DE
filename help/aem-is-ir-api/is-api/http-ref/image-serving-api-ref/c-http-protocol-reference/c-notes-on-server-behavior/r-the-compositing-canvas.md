---
description: Wenn req=img, wird die Größe der Arbeitsfläche zum Erstellen von Compositing vollständig von der Größe der Ebene 0 bestimmt.
seo-description: Wenn req=img, wird die Größe der Arbeitsfläche zum Erstellen von Compositing vollständig von der Größe der Ebene 0 bestimmt.
seo-title: Die Arbeitsfläche zum Erstellen von Kompositionen
solution: Experience Manager
title: Die Arbeitsfläche zum Erstellen von Kompositionen
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---


# Die Arbeitsfläche zum Erstellen von Kompositionen{#the-compositing-canvas}

Wenn req=img, wird die Größe der Arbeitsfläche zum Erstellen von Compositing vollständig von der Größe der Ebene 0 bestimmt.

Wenn `size=` für Ebene 0 nicht explizit angegeben ist, werden die Ebenentransformate verwendet, um die Größe der Arbeitsfläche zu berechnen (siehe unten).

Wenn `req=tmb`, wird die Größe der Arbeitsfläche für die Komposition durch die für Ebene 0 angegebene `size=`-Größe bestimmt oder, falls keine Größe angegeben ist, wird die Größe der Arbeitsfläche für die Komposition auf die Ansicht rect (siehe unten) eingestellt.
