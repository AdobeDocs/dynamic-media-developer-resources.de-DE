---
description: Verwenden Sie diese Servereinstellungen für Inhaltsdatenordner.
seo-description: Verwenden Sie diese Servereinstellungen für Inhaltsdatenordner.
seo-title: Inhaltsdatenordner
solution: Experience Manager
title: Inhaltsdatenordner
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# Inhaltsdatenordner{#content-data-folders}

Verwenden Sie diese Servereinstellungen für Inhaltsdatenordner.

## IS::RootPath - Stammordner für Bilddaten {#section-5c57569514bb4d00b19de31d2e137e3b}

Der Speicherort aller Quelldaten, einschließlich Bildern, Schriftarten und ICC-Profilen. Dabei kann es sich um einen oder mehrere absolute Dateipfade oder Pfade im Verhältnis zu *[!DNL install_folder]* handeln, die durch Semikolons getrennt sind. Wenn leer, ist *[!DNL install_folder]* der Standardstamm. Es können mehrere Werte angegeben werden, um Bilddaten über mehrere Dateisysteme zu verteilen. Der Image-Server versucht die Stammpfade in der angegebenen Reihenfolge, bis die angeforderte Datei gefunden wurde.

## PS::staticContent.rootPath - Static Content Data Root Folders {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

Der Speicherort der Quelldaten für statischen Inhalt, die über den [!DNL /is/static]-Kontext bereitgestellt werden sollen. Kann ein oder mehrere absolute Dateipfade oder Pfade relativ zu *[!DNL install_folder]* sein, durch Semikolons getrennt. Wenn leer, ist *[!DNL install_folder]* der Standardstamm.

Mehrere Werte können durch Semikolons getrennt angegeben werden, um statische Inhalte über mehrere Dateisysteme zu verteilen. Normalerweise werden dieselben Werte wie `IS::RootPath` festgelegt.

Der Plattformserver versucht die Stammpfade in der angegebenen Reihenfolge, bis die angeforderte Datei gefunden wurde.

>[!NOTE]
>
>Standardmäßig ist dieses Feld absichtlich auf einen nicht vorhandenen Speicherort ( [!DNL *[!DNL install_folder]*/static]) eingestellt, wodurch der statische Inhaltsdienst effektiv deaktiviert wird.

## IS::SaveDirectory - File Save Root Folder {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Der Stammpfad für `attribute::SavePath` (wird von `req=saveToFile` verwendet). Der Image-Server muss über Zugriffsberechtigungen für den Unterordner verfügen, in dem er Bilddateien erstellen wird.
