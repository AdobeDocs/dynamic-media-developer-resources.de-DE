---
description: Zu den Quelldatendateien für das Image Rendering gehören Vignettendateien, Materialdateien (Bilder für wiederholbare Texturen und Dekore sowie Schrank- und Fensterbedeckungsdateien) und ICC-Profile.
seo-description: Zu den Quelldatendateien für das Image Rendering gehören Vignettendateien, Materialdateien (Bilder für wiederholbare Texturen und Dekore sowie Schrank- und Fensterbedeckungsdateien) und ICC-Profile.
seo-title: Quelldaten
solution: Experience Manager
title: Quelldaten
topic: Scene7 Image Serving - Image Rendering API
uuid: 76c6419c-613e-4eff-b30f-9fea2a7daf5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---


# Quelldaten{#source-data}

Zu den Quelldatendateien für das Image Rendering gehören Vignettendateien, Materialdateien (Bilder für wiederholbare Texturen und Dekore sowie Schrank- und Fensterbedeckungsdateien) und ICC-Profile.

Alle Quelldatendateien müssen für die native Codekomponente des Image Rendering (zusammen mit dem Image-Server) verfügbar sein.

Wenn ein Materialkatalog betroffen ist, wird die im Materialkatalog angegebene Datei (mit `vignette::Path`, `catalog::Path` oder `icc::ProfilePath`) vom Render-Server wie folgt nachgeschlagen:

* Wenn der Pfad absolut ist, wird er wie angegeben verwendet.
* Wenn der Pfad relativ ist, wird ihm `catalog::RootPath` (aus einem benannten Materialkatalog) vorangestellt.
* Ist der Pfad absolut, wird er verwendet. Andernfalls wird ihm das Präfix `default::RootPath` (aus dem Standardkatalog) vorangestellt.
* Ist der Pfad absolut, wird er verwendet. Andernfalls kombiniert der Server ihn mit dem unter [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2) angegebenen Pfad.
* Wenn der Pfad nun absolut ist, wird er verwendet. ansonsten wird angenommen, dass es relativ zu [!DNL *[!DNL install_folder]*] ist.

Wenn kein Bildkatalog beteiligt ist, wird der Pfad mit `default::RootPath` kombiniert und dann wie oben verarbeitet.

Der physische Speicherort der Quelldatendateien wird normalerweise mit [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2) angegeben. Es können mehrere Werte angegeben werden, damit Quelldatendateien über mehrere Dateisysteme verteilt werden können. Der Render-Server versucht jeden Pfad in der angegebenen Reihenfolge, bis die Datendatei gefunden wurde.

Neue Datendateien jeder Art können jederzeit hinzugefügt werden, ohne den Server zu beenden.
