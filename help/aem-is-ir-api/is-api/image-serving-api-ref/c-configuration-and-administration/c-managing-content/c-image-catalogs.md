---
description: Bildkataloge bieten viele Serverkonfigurationseinstellungen sowie Schriftarten, ICC-Profile und Befehlsmakros.
seo-description: Bildkataloge bieten viele Serverkonfigurationseinstellungen sowie Schriftarten, ICC-Profile und Befehlsmakros.
seo-title: Bildkataloge
solution: Experience Manager
title: Bildkataloge
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Bildkataloge{#image-catalogs}

Bildkataloge bieten viele Serverkonfigurationseinstellungen sowie Schriftarten, ICC-Profile und Befehlsmakros.

Sie ordnen Bild- und statische Inhalts-IDs, die in Anforderungen verwendet werden, den tatsächlichen Dateipfaden zu, speichern verschiedene Bildmetadaten wie Imagemaps und bieten Container für Vorlagen und Bildsätze.

Auf Bildkataloge kann nur vom Plattformserver zugegriffen werden, nie vom Image-Server. Katalogattributdateien müssen das Suffix .ini haben und im Katalogordner des Plattformservers ( `PS::CatalogFolder`) abgelegt werden. Mindestens der Standardbildkatalog ist erforderlich und muss mit allen Attributen gefüllt werden, damit der Plattformserver ordnungsgemäß funktioniert.
