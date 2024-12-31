---
description: Bildkataloge bieten viele Server-Konfigurationseinstellungen sowie Schriftarten, ICC-Profile und Befehlsmakros.
solution: Experience Manager
title: Bildkataloge
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Bildkataloge{#image-catalogs}

Bildkataloge bieten viele Server-Konfigurationseinstellungen sowie Schriftarten, ICC-Profile und Befehlsmakros.

Sie ordnen Bild- und statische Inhalts-IDs, die in -Anfragen verwendet werden, tatsächlichen Dateipfaden zu, speichern verschiedene Bildmetadaten, z. B. Imagemaps, und stellen Container für Vorlagen und Bildsets bereit.

Auf Bildkataloge kann nur über den [!DNL Platform Server] zugegriffen werden, nicht über den Bildserver. Katalogattributdateien müssen das Suffix &quot;.ini“ aufweisen und im Katalogordner des [!DNL Platform Server] platziert werden ( `PS::CatalogFolder`). Zumindest der Standardbildkatalog ist erforderlich und muss mit allen Attributen ausgefüllt werden, damit das [!DNL Platform Server] ordnungsgemäß funktioniert.
