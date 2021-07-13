---
description: In der Befehlssequenz URL- oder Katalogmodifikator beginnt eine Ebenendefinitionssequenz mit dem Befehl layer= und endet mit einem anderen Befehl layer=, einem Befehl Effect= oder dem Ende der URL.
solution: Experience Manager
title: Festlegen von Ebenen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# Festlegen von Ebenen{#specifying-layers}

In der Befehlssequenz URL oder Katalog::Modifier beginnt eine Ebenendefinitionssequenz mit dem Befehl layer= und endet mit einem anderen Befehl layer=, einem Befehl Effect= oder dem Ende der URL.

Alle Befehle innerhalb der Ebenendefinitionssequenz sind mit der Ebene verknüpft.

Der Befehl `layer=` gibt eine Ebenennummer an, die eine Ganzzahl von 0 oder größer sein muss. Alle Befehle in Ebenendefinitionssequenzen mit derselben Ebenennummer werden auf dieselbe Ebene angewendet. Wenn derselbe Befehl mehrmals auftritt, hat die letzte Instanz Vorrang.
