---
description: Verwenden Sie diese Servereinstellungen, um Ihren Server zu konfigurieren.
solution: Experience Manager
title: Server
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# Server{#server}

Verwenden Sie diese Servereinstellungen, um Ihren Server zu konfigurieren.

## SV::ImageServerMode - Image-Server-Modus {#section-991b287f2dde4f77a24fc69d5b32cabd}

Sowohl eine 32- als auch eine 64-Bit-Version des Image-Servers sind für Linux verfügbar. Geben Sie ImageServer64 bei der Installation auf 64-Bit-Linux-Servern oder ImageServer32 (Standard) bei der Installation auf 32-Bit-Servern an.

>[!NOTE]
>
>Die 64-Bit-Version des Image-Servers unterstützt keine FlashPix-Quelldateien.

>[!NOTE]
>
>Der 64-Bit-Modus wird unter Windows nicht unterstützt. Es dürfen nur `ImageServer32` angegeben werden. Andernfalls wird das Image Serving nicht gestartet.

## SV::PsHeapSize - Plattform-Server-Heap-Größe {#section-fd83715948764aeda58d6b3a9f9f8be9}

Die Java-Heap-Größe für den Platform-Server. Die Standardeinstellung ist &quot; `512m`&quot; (512 MB).

## IS::TcpPort, PS::isConnection.port - Image Server Listening Port {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Gibt den Anschluss an, der für die Kommunikation zwischen dem Platform-Server und dem Image-Server verwendet wird. Stellen Sie sicher, dass Sie eine Anschlussnummer angeben, die auf dem Hostsystem sonst nicht verwendet wird.

>[!NOTE]
>
>Damit das Image Serving ordnungsgemäß funktioniert, muss derselbe Wert für `IS::TcpPort` und `PS::isConnection.port` festgelegt werden.

## IS::PhysicalMemory - Speicherlimit für Image-Server {#section-85e37aa2ac6e456eb698da716dd3247d}

Die ungefähre Grenze für Bilddaten im Arbeitsspeicher, ausgedrückt als Prozentsatz des physischen Arbeitsspeichers. Der gültige Bereich liegt zwischen 10 % und 90 %. Der Image-Server versucht, die Verwendung des Bildspeichers nach Möglichkeit auf die angegebene Menge zu beschränken. Die Höchstgrenze kann während der Aktivität der schweren Verarbeitung vorübergehend überschritten werden.

## IS::WorkerThreads - Anzahl der Image Server-Worker-Threads {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Die maximale Anzahl von Threads, die der Image-Server zur Verarbeitung von Bilddaten verwendet. Der Standardwert ist 0, was es dem Image-Server ermöglicht, die Thread-Anzahl automatisch zu optimieren.

Einige Betriebssysteme verfügen über Threading-Modelle mit einem hohen kontextbezogenen Switching-Overhead. Unter solchen Umständen kann sich die Gesamtleistung des Servers bei Auswahl einer bestimmten Thread-Anzahl (z. B. ein Thread pro CPU) verbessern. Möglicherweise sind einige Experimente erforderlich, um die optimale Einstellung zu finden. Weitere Informationen finden Sie in den Image Serving-Versionshinweisen und in der Dokumentation zum Betriebssystem.

## IS::NumberOfTextServers - Anzahl der Textserverinstanzen {#section-971e20a90c1a473598fba738ed95671a}

Die maximale Anzahl von Text-Renderern, die gleichzeitig aktiv sein können. 0 (Standard) entspricht dem 1,5-fachen der Anzahl der verfügbaren CPU-Kerne.

## IS::TextServerTcpPortRange - Text Server Communication Ports {#section-a13465de88ed4df09931e5ba840c1942}

Die für die Textserverkommunikation zu verwendenden Ports. Geben Sie die erste und letzte Portnummer, getrennt durch &#39;-&#39;, an.
