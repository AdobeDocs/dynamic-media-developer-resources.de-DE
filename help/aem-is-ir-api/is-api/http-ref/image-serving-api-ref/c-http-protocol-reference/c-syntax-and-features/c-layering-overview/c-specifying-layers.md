---
description: In der URL- oder Katalog-Modifizierer-Befehlssequenz wird eine Ebenendefinitionssequenz mit dem Befehl layer= ausgeführt und mit einem anderen Befehl layer=, einem Befehl effect= oder dem Ende der URL beendet.
seo-description: In der URL- oder Katalog-Modifizierer-Befehlssequenz wird eine Ebenendefinitionssequenz mit dem Befehl layer= ausgeführt und mit einem anderen Befehl layer=, einem Befehl effect= oder dem Ende der URL beendet.
seo-title: Festlegen von Ebenen
solution: Experience Manager
title: Festlegen von Ebenen
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# Festlegen von Ebenen{#specifying-layers}

In der Befehlssequenz URL oder Katalog::Modifier wird eine Ebenendefinitionssequenz mit dem Befehl layer= Beginn und mit einem anderen Befehl layer=, einem Befehl effect= oder dem Ende der URL beendet.

Alle Befehle innerhalb der Ebenendefinitionssequenz sind mit der Ebene verknüpft.

Der Befehl `layer=` gibt eine Ebenennummer an, bei der es sich um eine Ganzzahl von 0 oder größer handeln muss. Alle Befehle in Ebenendefinitionssequenzen mit derselben Ebenenzahl werden auf dieselbe Ebene angewendet. Wenn derselbe Befehl mehrmals auftritt, ist die letzte Instanz gültig.
