---
description: Ein Prioritätswarnhinweis wird gesendet, wenn der freie Java-Heap-Speicherplatz unmittelbar nach einem Java-Garbage Collection-Zyklus unter dem angegebenen Schwellenwert liegt.
solution: Experience Manager
title: Warnung zur Heap-Speicherpriorität
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# Warnung zur Heap-Speicherpriorität{#heap-space-priority-alert}

Ein Prioritätswarnhinweis wird gesendet, wenn der freie Java-Heap-Speicherplatz unmittelbar nach einem Java-Garbage Collection-Zyklus unter dem angegebenen Schwellenwert liegt.

Wiederholte Warnhinweise sollten durch Vergrößern des Java-Heap-Speichers behoben werden. Ein erneutes Auftreten dieser Bedingung führt erst dann zu einem E-Mail-Warnhinweis, wenn die mit `AS::monitorAlertGenerator.heapSpaceResetInterval` angegebene Verzögerungszeit abgelaufen ist.
