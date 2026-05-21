---
description: Wenn req=img, wird die Größe der Compositing-Leinwand vollständig durch die Größe der Schicht 0 bestimmt.
solution: Experience Manager
title: Die Arbeitsfläche für die Komposition
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
TQID: 'https://experienceleague.adobe.com/62uvC05pApoYR5lY4A-KA5RHmW8Xz0r2-2yvOpdAkOo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 0%

---

# Die Arbeitsfläche für die Komposition{#the-compositing-canvas}

Wenn req=img, wird die Größe der Compositing-Leinwand vollständig durch die Größe der Schicht 0 bestimmt.

Wenn die `size=` für Ebene 0 nicht explizit angegeben ist, werden die Ebenentransformationen verwendet, um die Größe der Arbeitsfläche für die Komposition zu berechnen (siehe unten).

Wenn `req=tmb`, wird die Größe der Arbeitsfläche für das Erstellen durch die für Ebene 0 angegebene `size=` bestimmt. Wenn die Größe nicht angegeben ist, wird die Größe der Arbeitsfläche für das Erstellen auf die rechte Ansicht festgelegt (siehe unten).
