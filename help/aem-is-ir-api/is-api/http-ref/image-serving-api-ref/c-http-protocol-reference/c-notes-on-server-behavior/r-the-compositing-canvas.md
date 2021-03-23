---
description: Wenn req=img, wird die Größe der Arbeitsfläche zum Erstellen von Compositing vollständig von der Größe der Ebene 0 bestimmt.
seo-description: Wenn req=img, wird die Größe der Arbeitsfläche zum Erstellen von Compositing vollständig von der Größe der Ebene 0 bestimmt.
seo-title: Die Arbeitsfläche zum Erstellen von Kompositionen
solution: Experience Manager
title: Die Arbeitsfläche zum Erstellen von Kompositionen
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# Die Arbeitsfläche zum Erstellen von Kompositionen{#the-compositing-canvas}

Wenn req=img, wird die Größe der Arbeitsfläche zum Erstellen von Compositing vollständig von der Größe der Ebene 0 bestimmt.

Wenn `size=` für Ebene 0 nicht explizit angegeben ist, werden die Ebenentransformate verwendet, um die Größe der Arbeitsfläche zu berechnen (siehe unten).

Wenn `req=tmb`, wird die Größe der Arbeitsfläche für die Komposition durch die für Ebene 0 angegebene `size=`-Größe bestimmt oder, falls keine Größe angegeben ist, wird die Größe der Arbeitsfläche für die Komposition auf die Ansicht rect (siehe unten) eingestellt.
