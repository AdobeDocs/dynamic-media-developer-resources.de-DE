---
description: Eine Prioritätswarnung wird gesendet, wenn der freie Java-Heap-Speicherplatz unmittelbar nach einem Java-Garbage Collection-Zyklus unter dem angegebenen Schwellenwert liegt.
solution: Experience Manager
title: Warnung zur Priorität des Heap-Speicherplatzes
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Warnung zur Priorität des Heap-Speichers{#heap-space-priority-alert}

Eine Prioritätswarnung wird gesendet, wenn der freie Java-Heap-Speicherplatz unmittelbar nach einem Java-Garbage Collection-Zyklus unter dem angegebenen Schwellenwert liegt.

Wiederholte Warnungen sollten durch Vergrößerung des Java-Heap-Speichers behoben werden. Nachfolgende Vorkommnisse dieser Bedingung führen erst dann zu einer E-Mail-Benachrichtigung, wenn die mit `AS::monitorAlertGenerator.heapSpaceResetInterval` angegebene Verzögerung abgelaufen ist.
