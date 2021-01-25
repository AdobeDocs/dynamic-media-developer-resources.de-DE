---
description: Ebenen werden in der vom Befehl layer= festgelegten Reihenfolge zusammengefügt, wobei Ebenen mit einer höheren Nummerierung Ebenen mit einer niedrigeren Nummerierung ausblenden.
seo-description: Ebenen werden in der vom Befehl layer= festgelegten Reihenfolge zusammengefügt, wobei Ebenen mit einer höheren Nummerierung Ebenen mit einer niedrigeren Nummerierung ausblenden.
seo-title: Die Arbeitsfläche zum Erstellen von Kompositionen
solution: Experience Manager
title: Die Arbeitsfläche zum Erstellen von Kompositionen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# Die Arbeitsfläche zum Erstellen von Kompositionen{#the-compositing-canvas}

Ebenen werden in der vom Befehl layer= festgelegten Reihenfolge zusammengefügt, wobei Ebenen mit einer höheren Nummerierung Ebenen mit einer niedrigeren Nummerierung ausblenden.

Ebene 0 bildet die Hintergrundschicht, die immer benötigt wird und die die Größe des Composite-Bildes definiert. Für Ebene 0 sind alle Ebenentypen zulässig. Die Größe der Ebene 0 muss definiert werden, entweder explizit mit `size=` oder implizit, basierend auf dem Inhaltsbild oder Text. Bereiche anderer Ebenen, die außerhalb des Bereichs 0 liegen, werden nicht in das Ausgabebild aufgenommen.

>[!NOTE]
>
>Nachdem alle Ebenen reduziert wurden, wird das Composite-Bild in das endgültige Antwortbild konvertiert, wie mit den Befehlen und Attributen [Ansicht](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90) angegeben.

