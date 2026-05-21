---
description: Bildkataloge bieten viele Server-Konfigurationseinstellungen sowie Schriftarten, ICC-Profile und Befehlsmakros.
solution: Experience Manager
title: Bildkataloge
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
TQID: 'https://experienceleague.adobe.com/kfojwk0K5RfRtZdxJmdojqsLirnP6LoXbtFRJ5272lg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# Bildkataloge{#image-catalogs}

Bildkataloge bieten viele Server-Konfigurationseinstellungen sowie Schriftarten, ICC-Profile und Befehlsmakros.

Sie ordnen Bild- und statische Inhalts-IDs, die in -Anfragen verwendet werden, tatsächlichen Dateipfaden zu, speichern verschiedene Bildmetadaten, z. B. Imagemaps, und stellen Container für Vorlagen und Bildsets bereit.

Auf Bildkataloge kann nur über den [!DNL Platform Server] zugegriffen werden, nicht über den Bildserver. Katalogattributdateien müssen das Suffix &quot;.ini“ aufweisen und im Katalogordner des [!DNL Platform Server] platziert werden ( `PS::CatalogFolder`). Zumindest der Standardbildkatalog ist erforderlich und muss mit allen Attributen ausgefüllt werden, damit das [!DNL Platform Server] ordnungsgemäß funktioniert.
