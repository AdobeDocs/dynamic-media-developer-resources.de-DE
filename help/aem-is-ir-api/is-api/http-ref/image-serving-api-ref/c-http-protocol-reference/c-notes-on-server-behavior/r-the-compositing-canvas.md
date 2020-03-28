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

---


# Die Arbeitsfläche zum Erstellen von Kompositionen{#the-compositing-canvas}

Wenn req=img, wird die Größe der Arbeitsfläche zum Erstellen von Compositing vollständig von der Größe der Ebene 0 bestimmt.

Wenn `size=` für Ebene 0 nicht explizit angegeben wird, werden die Ebenentransformate verwendet, um die Größe der Arbeitsfläche zu berechnen (siehe unten).

Wenn `req=tmb`die Größe der Arbeitsfläche bestimmt wird durch die für Ebene 0 angegebene `size=` Größe oder, falls keine Größe angegeben ist, die Größe der Arbeitsfläche zum Erstellen von Compositing auf die Ansicht rect (siehe unten) eingestellt ist.
