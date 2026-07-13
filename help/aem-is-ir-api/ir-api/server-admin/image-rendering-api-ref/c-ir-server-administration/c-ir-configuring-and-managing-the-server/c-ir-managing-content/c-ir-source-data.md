---
description: Zu den Quelldatendateien für das Rendern von Bildern gehören Vignettendateien, Materialdateien (Bilder für wiederholbare Texturen und Abziehbilder sowie Schrank- und Fensterabdeckungsstildateien) und ICC-Profile.
solution: Experience Manager
title: Source-Daten
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
TQID: 'https://experienceleague.adobe.com/lvrZxGOZbo6ORttqcBhCTuYPzbiD9xei5qkRwnapIh8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 0%

---

# Source-Daten{#source-data}

Zu den Quelldatendateien für das Rendern von Bildern gehören Vignettendateien, Materialdateien (Bilder für wiederholbare Texturen und Abziehbilder sowie Schrank- und Fensterabdeckungsstildateien) und ICC-Profile.

Alle Quelldatendateien müssen für die native Code-Komponente von Image Rendering (zusammen mit dem Image-Server) zugänglich sein.

Wenn es sich um einen Materialkatalog handelt, wird die im Materialkatalog angegebene Datei (mit `vignette::Path`, `catalog::Path` oder `icc::ProfilePath`) wie folgt vom Render-Server nachgeschlagen:

* Wenn der Pfad absolut ist, wird er unverändert verwendet.
* Wenn der Pfad relativ ist, wird ihm das Präfix `catalog::RootPath` (aus einem benannten Materialkatalog) vorangestellt.
* Wenn der Pfad absolut ist, wird er verwendet. Andernfalls wird ihm das Präfix `default::RootPath` (aus dem Standardkatalog) vorangestellt.
* Wenn der Pfad absolut ist, wird er verwendet. Andernfalls wird er vom Server mit dem in „ir.resourceRootPaths[ angegebenen Pfad ](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Wenn der Pfad jetzt absolut ist, wird er verwendet. Andernfalls wird er als relativ zu [!DNL *[!DNL install_folder]*] angenommen.

Wenn kein Bildkatalog involviert ist, wird der Pfad mit `default::RootPath` kombiniert und dann wie oben beschrieben verarbeitet.

Der physische Speicherort von Quelldatendateien wird normalerweise mit [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2) angegeben. Es können mehrere Werte angegeben werden, damit Quelldatendateien über mehrere Dateisysteme verteilt werden können. Der Render-Server versucht jeden Pfad in der angegebenen Reihenfolge, bis die Datendatei gefunden wird.

Neue Datendateien jeglicher Art können jederzeit hinzugefügt werden, ohne den Server anzuhalten.

