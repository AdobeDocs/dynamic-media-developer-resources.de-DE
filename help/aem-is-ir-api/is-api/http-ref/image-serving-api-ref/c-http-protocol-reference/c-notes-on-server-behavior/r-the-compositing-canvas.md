---
description: Wenn req=img, wird die Größe der Arbeitsfläche zum Erstellen von Compositing vollständig von der Größe der Ebene 0 bestimmt.
solution: Experience Manager
title: Die Arbeitsfläche zum Erstellen von Kompositionen
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# Die Arbeitsfläche zum Erstellen von Kompositionen{#the-compositing-canvas}

Wenn req=img, wird die Größe der Arbeitsfläche zum Erstellen von Compositing vollständig von der Größe der Ebene 0 bestimmt.

Wenn `size=` für Ebene 0 nicht explizit angegeben ist, werden die Ebenentransformate verwendet, um die Größe der Arbeitsfläche zu berechnen (siehe unten).

Wenn `req=tmb`, wird die Größe der Arbeitsfläche für die Komposition durch die für Ebene 0 angegebene `size=`-Größe bestimmt oder, falls keine Größe angegeben ist, wird die Größe der Arbeitsfläche für die Komposition auf die Ansicht rect (siehe unten) eingestellt.
