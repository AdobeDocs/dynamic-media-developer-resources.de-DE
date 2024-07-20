---
description: Ebenen werden in der Reihenfolge zusammengefügt, die durch den Befehl layer= festgelegt wird, wobei Ebenen mit höherer Nummerierung Bereiche mit niedrigerer Nummerierung ausblenden.
solution: Experience Manager
title: Die Arbeitsfläche für die Zusammenstellung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Die Arbeitsfläche für die Zusammenstellung{#the-compositing-canvas}

Ebenen werden in der Reihenfolge zusammengefügt, die durch den Befehl layer= festgelegt wird, wobei Ebenen mit höherer Nummerierung Bereiche mit niedrigerer Nummerierung ausblenden.

Ebene 0 bildet die Hintergrundebene, die immer erforderlich ist und die die Größe des Composite-Bilds definiert. Alle Ebenentypen sind für Ebene 0 zulässig. Die Größe der Ebene 0 muss entweder explizit mit `size=` oder implizit basierend auf dem Inhaltsbild oder Text definiert werden. Alle Bereiche anderer Ebenen, die außerhalb des Bereichs der Ebene 0 liegen, sind nicht im Ausgabebild enthalten.

>[!NOTE]
>
>Nachdem alle Ebenen reduziert wurden, wird das zusammengesetzte Bild in das endgültige Antwortbild konvertiert, wie mit den [Anzeigebefehlen und Attributen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90) angegeben.
