---
description: Ebenen werden in der durch den Befehl layer= angegebenen Reihenfolge zusammengesetzt, wobei Ebenen mit höherer Nummer die Ebenen mit niedrigerer Nummer ausblenden.
solution: Experience Manager
title: Die Arbeitsfläche für die Komposition
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
TQID: 'https://experienceleague.adobe.com/WNvq6dLRetz3iEbtP0ugmOPagUfTCaa5eXdB3lEzEaQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 0%

---

# Die Arbeitsfläche für die Komposition{#the-compositing-canvas}

Ebenen werden in der durch den Befehl layer= angegebenen Reihenfolge zusammengesetzt, wobei Ebenen mit höherer Nummer die Ebenen mit niedrigerer Nummer ausblenden.

Ebene 0 bildet die immer erforderliche Hintergrundschicht, die die Größe des zusammengesetzten Bildes definiert. Jeder der Ebenentypen ist für die Ebene 0 zulässig. Die Größe der Ebene 0 muss entweder explizit mithilfe von `size=` oder implizit basierend auf dem Inhaltsbild oder dem Text definiert werden. Alle Bereiche anderer Schichten, die außerhalb des Bereichs der Schicht 0 liegen, sind nicht im Ausgabebild enthalten.

>[!NOTE]
>
>Nachdem alle Ebenen reduziert wurden, wird das zusammengesetzte Bild in das endgültige Antwortbild konvertiert, wie mit den [Ansichtsbefehlen und -attributen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90) angegeben.
