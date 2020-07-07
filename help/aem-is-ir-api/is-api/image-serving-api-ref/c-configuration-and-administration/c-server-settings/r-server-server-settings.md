---
description: Verwenden Sie diese Servereinstellungen, um Ihren Server zu konfigurieren.
seo-description: Verwenden Sie diese Servereinstellungen, um Ihren Server zu konfigurieren.
seo-title: Server
solution: Experience Manager
title: Server
topic: Scene7 Image Serving - Image Rendering API
uuid: 50db98cc-8354-4884-9416-00808828061b
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# Server{#server}

Verwenden Sie diese Servereinstellungen, um Ihren Server zu konfigurieren.

## SV::ImageServerMode - Image-Servermodus {#section-991b287f2dde4f77a24fc69d5b32cabd}

Sowohl eine 32- als auch eine 64-Bit-Version des Image-Servers sind für Linux verfügbar. Geben Sie ImageServer64 bei Installation auf 64-Bit-Linux-Servern oder ImageServer32 (Standard) bei Installation auf 32-Bit-Servern an.

>[!NOTE]
>
>Die 64-Bit-Version des Image-Servers unterstützt keine FlashPix-Quelldateien.

>[!NOTE]
>
>Der 64-Bit-Modus wird unter Windows nicht unterstützt. Es `ImageServer32` kann nur angegeben werden. Andernfalls wird beim Image Serving kein Beginn ausgeführt.

## SV::PsHeapSize - Heap-Größe des Platform-Servers {#section-fd83715948764aeda58d6b3a9f9f8be9}

Die Java-Heap-Größe für den Platform-Server. Der Standardwert ist &quot; `512m`&quot;(512 MB).

## IS::TcpPort, PS::isConnection.port - Image-Server-Listening-Anschluss {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Gibt den Anschluss an, der für die Kommunikation zwischen dem Platform-Server und dem Image-Server verwendet wird. Stellen Sie sicher, dass Sie eine Anschlussnummer angeben, die auf dem Host-System sonst nicht verwendet wird.

>[!NOTE]
>
>Damit Image Serving ordnungsgemäß funktioniert, muss für `IS::TcpPort` `PS::isConnection.port`und der gleiche Wert festgelegt werden.

## IS::PhysicalMemory - Speichergrenze für Image-Server {#section-85e37aa2ac6e456eb698da716dd3247d}

Die ungefähre Grenze für Bilddaten im Arbeitsspeicher, ausgedrückt als Prozentsatz des physischen Speichers. Der gültige Bereich liegt zwischen 10 % und 90 %. Der Image-Server versucht, die Verwendung des Bildspeichers möglichst auf die angegebene Menge zu beschränken. Die Höchstgrenze kann bei Aktivität der Schwerindustrie vorübergehend überschritten werden.

## IS::WorkerThreads - Anzahl der Image-Server-Threads {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Die maximale Anzahl von Threads, die der Image-Server zur Verarbeitung von Bilddaten verwendet. Der Standardwert ist 0, was es dem Image-Server ermöglicht, die Thread-Anzahl automatisch zu optimieren.

Einige Betriebssysteme haben Threadingmodelle mit hohem Kontextumschaltaufwand. In einem solchen Fall kann sich die Gesamtleistung des Servers verbessern, wenn eine bestimmte Thread-Anzahl ausgewählt wird (z. B. ein Thread pro CPU). Einige Experimente sind möglicherweise erforderlich, um die optimale Einstellung zu finden. Weitere Informationen finden Sie in den Versionshinweisen zum Image-Server und in der Dokumentation zum Betriebssystem.

## IS::NumberOfTextServers - Anzahl der Textserverinstanzen {#section-971e20a90c1a473598fba738ed95671a}

Die maximale Anzahl an gleichzeitig aktiven Textrenderern. 0 (Standard) entspricht der 1,5-fachen Anzahl verfügbarer CPU-Kerne.

## IS::TextServerTcpPortRange - Kommunikationsanschlüsse für Textserver {#section-a13465de88ed4df09931e5ba840c1942}

Die für die Textserverkommunikation zu verwendenden Anschlüsse. Geben Sie die erste und letzte Anschlussnummer mit &quot;-&quot;an.
