---
description: Ebenen werden in der Reihenfolge zusammengefügt, die durch den Befehl layer= festgelegt wird, wobei Ebenen mit höherer Nummerierung Bereiche mit niedrigerer Nummerierung ausblenden.
solution: Experience Manager
title: Die Arbeitsfläche für die Zusammenstellung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Die Arbeitsfläche für die Zusammenstellung{#the-compositing-canvas}

Ebenen werden in der Reihenfolge zusammengefügt, die durch den Befehl layer= festgelegt wird, wobei Ebenen mit höherer Nummerierung Bereiche mit niedrigerer Nummerierung ausblenden.

Ebene 0 bildet die Hintergrundebene, die immer erforderlich ist und die die Größe des zusammengesetzten Bildes definiert. Alle Ebenentypen sind für Ebene 0 zulässig. Die Größe der Ebene 0 muss entweder explizit mithilfe von `size=` oder implizit basierend auf dem Inhaltsbild oder Text definiert werden. Alle Bereiche anderer Ebenen, die außerhalb des Bereichs der Ebene 0 liegen, werden nicht in das Ausgabebild aufgenommen.

>[!NOTE]
>
>Nachdem alle Ebenen reduziert wurden, wird das Composite-Bild in das endgültige Antwortbild konvertiert, wie mit den [View Befehlen und Attributen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90) angegeben.
