---
description: Verwenden Sie diese Servereinstellungen für Ordner mit Inhaltsdaten.
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

Verwenden Sie diese Servereinstellungen für Ordner mit Inhaltsdaten.

## IS::RootPath - Stammordner für Bilddaten {#section-5c57569514bb4d00b19de31d2e137e3b}

Der Speicherort aller Quelldaten, einschließlich Bildern, Schriftarten und ICC-Profilen. Dabei kann es sich um einen oder mehrere absolute Dateipfade oder Pfade handeln, die relativ zu *[!DNL install_folder]* sind und durch Semikolons getrennt sind. Wenn leer, ist *[!DNL install_folder]* der Standardstamm. Es können mehrere Werte angegeben werden, um Bilddaten über mehrere Dateisysteme zu verteilen. Der Image-Server versucht die Stammpfade in der angegebenen Reihenfolge, bis die angeforderte Datei gefunden wurde.

## PS::staticContent.rootPath - Statische Stammordner für Inhaltsdaten {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

Der Speicherort der statischen Inhaltsquellendaten, die über den [!DNL /is/static] -Kontext bereitgestellt werden sollen. Kann ein oder mehrere absolute Dateipfade oder Pfade sein, die relativ zu *[!DNL install_folder]* sind und durch Semikolons getrennt sind. Wenn leer, ist *[!DNL install_folder]* der Standardstamm.

Mehrere Werte können durch Semikolons getrennt angegeben werden, um statische Inhalte über mehrere Dateisysteme zu verteilen. Wird normalerweise auf dieselben Werte wie `IS::RootPath` gesetzt.

Der [!DNL Platform Server] versucht die Stammpfade in der angegebenen Reihenfolge, bis die angeforderte Datei gefunden wurde.

>[!NOTE]
>
>Standardmäßig ist dieses Feld absichtlich auf einen nicht vorhandenen Speicherort ( [!DNL *[!DNL install_folder]*/static]) gesetzt, wodurch der statische Inhaltsdienst effektiv deaktiviert wird.

## IS::SaveDirectory - File Save Root Folder {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Der Stammpfad für `attribute::SavePath` (verwendet von `req=saveToFile`). Der Image-Server muss über Zugriffsberechtigungen für den Unterordner verfügen, in dem er Bilddateien erstellt.
