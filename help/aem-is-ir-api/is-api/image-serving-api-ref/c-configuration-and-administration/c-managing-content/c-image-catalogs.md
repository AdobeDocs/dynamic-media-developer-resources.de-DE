---
description: Bildkataloge bieten viele Serverkonfigurationseinstellungen, Schriftarten, ICC-Profile und Befehlsmakros.
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

Bildkataloge bieten viele Serverkonfigurationseinstellungen, Schriftarten, ICC-Profile und Befehlsmakros.

Sie ordnen Bild- und statische Inhalts-IDs, die in Anforderungen verwendet werden, den tatsächlichen Dateipfaden zu, speichern verschiedene Bild-Metadaten wie Imagemaps und stellen Container für Vorlagen und Bildsets bereit.

Auf Bildkataloge kann nur durch die [!DNL Platform Server], niemals vom Image-Server. Katalogattributdateien müssen das Suffix .ini aufweisen und im [!DNL Platform Server]des Katalogordners ( `PS::CatalogFolder`). Mindestens der standardmäßige Bildkatalog ist erforderlich und muss mit allen Attributen gefüllt werden, damit die Funktion der [!DNL Platform Server].
