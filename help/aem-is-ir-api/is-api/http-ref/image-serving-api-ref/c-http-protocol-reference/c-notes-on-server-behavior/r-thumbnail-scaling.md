---
title: Miniaturansichten skalieren
description: Schritt 2 der Bildebenen-Transformationen wird für Miniaturen wie folgt geändert (d. h. wenn req=tmb ist).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
TQID: 'https://experienceleague.adobe.com/He10BtjrEIOQW6SZcaUhcExDjP05BR-pc3BCj9TRawU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 79
ht-degree: 0%

---

# Miniaturansichten skalieren{#thumbnail-scaling}

Schritt 2 der Bildebenen-Transformationen wird für Miniaturen wie folgt geändert (d. h. wenn req=tmb ist).

* `2.` Wenn `size=` angegeben ist, passen Sie das (zugeschnittene) Bild mithilfe von Miniaturansichtsregeln in das `size=` an. Wenn `size=` nicht angegeben ist, skalieren Sie anhand der `res=` oder fügen Sie, falls `res=` nicht angegeben ist, das (zugeschnittene) Bild mithilfe der unten beschriebenen Miniaturansichtsregeln in das Arbeitsflächen-React ein.
