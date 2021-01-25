---
description: Bildkataloge bieten viele Serverkonfigurationseinstellungen sowie Schriftarten, ICC-Profile und Befehlsmakros.
seo-description: Bildkataloge bieten viele Serverkonfigurationseinstellungen sowie Schriftarten, ICC-Profile und Befehlsmakros.
seo-title: Bildkataloge
solution: Experience Manager
title: Bildkataloge
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# Bildkataloge{#image-catalogs}

Bildkataloge bieten viele Serverkonfigurationseinstellungen sowie Schriftarten, ICC-Profile und Befehlsmakros.

Sie ordnen Bild- und statische Inhalts-IDs, die in Anforderungen verwendet werden, den tatsächlichen Dateipfaden zu, speichern verschiedene Bildmetadaten wie Imagemaps und bieten Container für Vorlagen und Bildsätze.

Auf Bildkataloge kann nur vom Plattformserver zugegriffen werden, nie vom Image-Server. Katalogattributdateien müssen das Suffix .ini haben und im Katalogordner des Plattformservers ( `PS::CatalogFolder`) abgelegt werden. Mindestens der Standardbildkatalog ist erforderlich und muss mit allen Attributen gefüllt werden, damit der Plattformserver ordnungsgemäß funktioniert.
