---
description: Eine Prioritätswarnung wird gesendet, wenn der freie Java-Heap-Speicherplatz unmittelbar nach einem Java-Garbage Collection-Zyklus unter dem angegebenen Schwellenwert liegt.
seo-description: Eine Prioritätswarnung wird gesendet, wenn der freie Java-Heap-Speicherplatz unmittelbar nach einem Java-Garbage Collection-Zyklus unter dem angegebenen Schwellenwert liegt.
seo-title: Warnung zur Priorität des Heap-Speicherplatzes
solution: Experience Manager
title: Warnung zur Priorität des Heap-Speicherplatzes
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# Warnung zur Priorität des Heap-Speichers{#heap-space-priority-alert}

Eine Prioritätswarnung wird gesendet, wenn der freie Java-Heap-Speicherplatz unmittelbar nach einem Java-Garbage Collection-Zyklus unter dem angegebenen Schwellenwert liegt.

Wiederholte Warnungen sollten durch Vergrößerung des Java-Heap-Speichers behoben werden. Nachfolgende Vorkommnisse dieser Bedingung führen erst dann zu einer E-Mail-Benachrichtigung, wenn die mit `AS::monitorAlertGenerator.heapSpaceResetInterval` angegebene Verzögerung abgelaufen ist.
