---
description: Bildkataloge bieten viele Serverkonfigurationseinstellungen, Schriftarten, ICC-Profile und Befehlsmakros.
solution: Experience Manager
title: Bildkataloge
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# Bildkataloge{#image-catalogs}

Bildkataloge bieten viele Serverkonfigurationseinstellungen, Schriftarten, ICC-Profile und Befehlsmakros.

Sie ordnen Bild- und statische Inhalts-IDs, die in Anforderungen verwendet werden, den tatsächlichen Dateipfaden zu, speichern verschiedene Bild-Metadaten wie Imagemaps und stellen Container für Vorlagen und Bildsets bereit.

Auf Bildkataloge kann nur vom Platform-Server und nie vom Image-Server zugegriffen werden. Katalogattributdateien müssen das Suffix .ini aufweisen und im Katalogordner des Platform-Servers ( `PS::CatalogFolder`) abgelegt werden. Mindestens der Standard-Bildkatalog ist erforderlich und muss mit allen Attributen gefüllt werden, damit Platform Server ordnungsgemäß funktioniert.
