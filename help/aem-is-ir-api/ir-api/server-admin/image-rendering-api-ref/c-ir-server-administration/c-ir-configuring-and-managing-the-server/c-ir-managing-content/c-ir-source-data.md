---
description: Zu den Quelldatendateien für das Bild-Rendering gehören Vignettendateien, Materialdateien (Bilder für wiederholbare Texturen und Decals sowie Stildateien für Schachteln und Fenster) sowie ICC-Profile.
solution: Experience Manager
title: Quelldaten
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Quelldaten{#source-data}

Zu den Quelldatendateien für das Bild-Rendering gehören Vignettendateien, Materialdateien (Bilder für wiederholbare Texturen und Decals sowie Stildateien für Schachteln und Fenster) sowie ICC-Profile.

Alle Quelldatendateien müssen für die systemeigene Codekomponente des Image Rendering (gemeinsam mit dem Image-Server) verfügbar sein.

Wenn ein Materialkatalog beteiligt ist, wird die im Materialkatalog angegebene Datei (mit `vignette::Path`, `catalog::Path` oder `icc::ProfilePath`) vom Render-Server wie folgt nachgeschlagen:

* Wenn der Pfad absolut ist, wird er unverändert verwendet.
* Wenn der Pfad relativ ist, wird ihm `catalog::RootPath` (aus einem benannten Materialkatalog) vorangestellt.
* Wenn der Pfad absolut ist, wird er verwendet. Andernfalls wird `default::RootPath` vorangestellt (aus dem Standardkatalog).
* Wenn der Pfad absolut ist, wird er verwendet. ansonsten kombiniert der Server ihn mit dem in [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2) angegebenen Pfad.
* Wenn der Pfad jetzt absolut ist, wird er verwendet. Andernfalls wird angenommen, dass es relativ zu [!DNL *[!DNL install_folder]*] ist.

Wenn kein Bildkatalog beteiligt ist, wird der Pfad mit `default::RootPath` kombiniert und dann wie oben beschrieben verarbeitet.

Der physische Speicherort der Quelldatendateien wird normalerweise mit [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2) angegeben. Es können mehrere Werte angegeben werden, damit Quelldatendateien über mehrere Dateisysteme verteilt werden können. Der Render Server versucht jeden Pfad in der angegebenen Reihenfolge, bis die Datendatei gefunden wird.

Neue Datendateien jeder Art können jederzeit hinzugefügt werden, ohne den Server zu stoppen.
