---
description: In der URL- oder Catalog Modifier-Befehlssequenz beginnt eine Ebenendefinitionssequenz mit dem Befehl layer= und endet mit einem anderen Layer=-Befehl, einem Effekt=-Befehl oder dem Ende der URL.
solution: Experience Manager
title: Festlegen von Ebenen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
TQID: 'https://experienceleague.adobe.com/jNFpOYrBFWWc53JvzwENSjpM-SkIpenxxWPUgGX-p0Q'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 0%

---

# Festlegen von Ebenen{#specifying-layers}

In der Befehlsfolge URL oder catalog::Modifier beginnt eine Ebenendefinitionssequenz mit dem Befehl layer= und endet mit einem anderen Befehl layer= , einem Befehl effect= oder dem Ende der URL.

Alle Befehle innerhalb der Ebenendefinitionssequenz sind mit der Ebene verknüpft.

Der Befehl `layer=` gibt eine Ebenennummer an, die eine ganze Zahl 0 oder größer sein muss. Alle Befehle in Ebenendefinitionssequenzen mit derselben Ebenennummer werden auf dieselbe Ebene angewendet. Wenn derselbe Befehl mehrmals auftritt, hat die letzte Instanz Vorrang.
