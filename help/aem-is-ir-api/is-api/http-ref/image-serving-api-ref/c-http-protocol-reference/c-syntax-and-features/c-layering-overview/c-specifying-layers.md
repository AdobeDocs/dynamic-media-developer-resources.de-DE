---
description: In der URL- oder Katalog-Modifizierer-Befehlssequenz wird eine Ebenendefinitionssequenz mit dem Befehl layer= ausgeführt und mit einem anderen Befehl layer=, einem Befehl effect= oder dem Ende der URL beendet.
solution: Experience Manager
title: Festlegen von Ebenen
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# Festlegen von Ebenen{#specifying-layers}

In der Befehlssequenz URL oder Katalog::Modifier wird eine Ebenendefinitionssequenz mit dem Befehl layer= Beginn und mit einem anderen Befehl layer=, einem Befehl effect= oder dem Ende der URL beendet.

Alle Befehle innerhalb der Ebenendefinitionssequenz sind mit der Ebene verknüpft.

Der Befehl `layer=` gibt eine Ebenennummer an, bei der es sich um eine Ganzzahl von 0 oder größer handeln muss. Alle Befehle in Ebenendefinitionssequenzen mit derselben Ebenenzahl werden auf dieselbe Ebene angewendet. Wenn derselbe Befehl mehrmals auftritt, ist die letzte Instanz gültig.
