---
description: Verwenden Sie diese Server-Einstellungen für Inhaltsdatenordner.
solution: Experience Manager
title: Inhaltsdatenordner
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Inhaltsdatenordner{#content-data-folders}

Verwenden Sie diese Server-Einstellungen für Inhaltsdatenordner.

## IS::rootPath - Stammordner für Bilddaten {#section-5c57569514bb4d00b19de31d2e137e3b}

Der Speicherort aller Quelldaten, einschließlich Bilder, Schriftarten und ICC-Profile. Dabei kann es sich um einen oder mehrere absolute Dateipfade oder Pfade relativ zu *[!DNL install_folder]* handeln, die durch Semikolons getrennt sind. Wenn leer, ist *[!DNL install_folder]* der Standardstamm. Es können mehrere Werte angegeben werden, um Bilddaten über mehrere Dateisysteme zu verteilen. Der Bild-Server versucht, die Stammpfade in der angegebenen Reihenfolge auszuführen, bis die angeforderte Datei gefunden wird.

## PS:staticContent.rootPath - Stammordner für statische Inhaltsdaten {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

Der Speicherort der Daten aus statischen Inhaltsquellen, die über den [!DNL /is/static]-Kontext bereitgestellt werden sollen. Kann ein oder mehrere absolute Dateipfade oder Pfade relativ zu *[!DNL install_folder]* sein, getrennt durch Semikolons. Wenn leer, ist *[!DNL install_folder]* der Standardstamm.

Mehrere Werte können durch Semikolons getrennt angegeben werden, um statische Inhalte über mehrere Dateisysteme zu verteilen. Wird normalerweise auf dieselben Werte wie `IS::RootPath` festgelegt.

Der [!DNL Platform Server] versucht die Stammpfade in der angegebenen Reihenfolge, bis die angeforderte Datei gefunden wird.

>[!NOTE]
>
>Standardmäßig wird dieses Feld absichtlich auf einen nicht vorhandenen Speicherort ( [!DNL *[!DNL install_folder]*/static]) festgelegt, sodass der statische Content-Service deaktiviert wird.

## IS::saveDirectory - Datei Stammordner speichern {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Der Stammpfad für `attribute::SavePath` (von `req=saveToFile` verwendet). Der Bildserver muss über Erstellungszugriffsberechtigungen für den Unterordner verfügen, in dem er Bilddateien erstellt.
