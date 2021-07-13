---
description: Neben der Größe (size=) und Positionierung (pos=) Ebenen relativ zu Ebene 0 und der Angabe der Komponentenreihenfolge (z-order) mit dem Befehl layer= können Ebenen gedreht (rotate=) und umgedreht (flip=) werden.
solution: Experience Manager
title: Ebenenvorgänge
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# Ebenenvorgänge{#layer-operations}

Neben der Größe (size=) und Positionierung (pos=) Ebenen relativ zu Ebene 0 und der Angabe der Komponentenreihenfolge (z-order) mit dem Befehl layer= können Ebenen gedreht (rotate=) und umgedreht (flip=) werden.

Die Attribute `origin=` und `anchor=` können verwendet werden, um die gewünschte Ausrichtung zwischen Ebenen beizubehalten, wenn Bilder oder Text in Vorlagen dynamisch geändert werden.

Der Befehl `maskUse=` ist für Bildebenen verfügbar, um auf den Hintergrundbereich von Bildern mit separaten Masken zuzugreifen.

`opac=` kann verwendet werden, um die Deckkraft der Ebene zu variieren und  `hide=` die Ebene ein- oder auszublenden.
