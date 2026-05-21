---
description: Verwenden Sie diese Server-Einstellungen, um Ihren Server zu konfigurieren.
solution: Experience Manager
title: Server
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
TQID: 'https://experienceleague.adobe.com/403CInOL4425Gv35Njb69WSo-QRyvTuDUZEBtNRsvj0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 357
ht-degree: 0%

---

# Server{#server}

Verwenden Sie diese Server-Einstellungen, um Ihren Server zu konfigurieren.

## SV::ImageServerMode - Image-Server-Modus {#section-991b287f2dde4f77a24fc69d5b32cabd}

Sowohl eine 32- als auch eine 64-Bit-Version des Image-Servers sind für Linux verfügbar. Geben Sie ImageServer64 an, wenn es auf 64-Bit-Linux-Servern installiert ist, oder ImageServer32 (Standard), wenn es auf 32-Bit-Servern installiert ist.

>[!NOTE]
>
>Die 64-Bit-Version des Image-Servers unterstützt keine FlashPix-Quelldateien.

>[!NOTE]
>
>Der 64-Bit-Modus wird unter Windows nicht unterstützt. Es können nur `ImageServer32` angegeben werden. Andernfalls wird die Bildbereitstellung nicht gestartet.

## SV::PsHeapSize - [!DNL Platform Server] Heap-Größe {#section-fd83715948764aeda58d6b3a9f9f8be9}

Die Java-Heap-Größe für die [!DNL Platform Server]. Die Standardeinstellung ist &quot;`512m`&quot; (512 MB).

## IS::TcpPort, PS::isConnection.port - Lauschender Port des Bild-Servers {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Gibt den Port an, der für die Kommunikation zwischen dem [!DNL Platform Server] und dem Bildserver verwendet wird. Stellen Sie sicher, dass Sie eine Port-Nummer angeben, die sonst auf dem Host-System nicht verwendet wird.

>[!NOTE]
>
>Damit die Bildbereitstellung ordnungsgemäß funktioniert, muss für `IS::TcpPort` und `PS::isConnection.port` derselbe Wert festgelegt werden.

## IS::Physikalischer Speicher - Speicherlimit des Bild-Servers {#section-85e37aa2ac6e456eb698da716dd3247d}

Der ungefähre Grenzwert für speicherinterne Bilddaten, ausgedrückt als Prozentsatz des physischen Speichers. Gültiger Bereich ist 10 % bis 90 %. Der Bildserver versucht, die Verwendung des Bildspeichers nach Möglichkeit auf den angegebenen Wert zu beschränken. Diese Grenze kann bei starker Verarbeitungsaktivität vorübergehend überschritten werden.

## IS::WorkerThreads - Anzahl der Image-Server-Worker Threads {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Die maximale Anzahl von Threads, die der Bild-Server für die Verarbeitung von Bilddaten verwendet. Der Standardwert ist 0, wodurch der Bild-Server die Thread-Anzahl automatisch optimieren kann.

Einige Betriebssysteme verfügen über Threading-Modelle mit einem hohen Overhead bei der Kontextumschaltung. In einem solchen Fall kann sich die Gesamtleistung des Servers verbessern, wenn eine bestimmte Thread-Anzahl ausgewählt wird (z. B. ein Thread pro CPU). Möglicherweise sind einige Experimente erforderlich, um die optimale Einstellung zu finden. Weitere Informationen finden Sie in den Versionshinweisen zu Image-Serving und in der Dokumentation zum Betriebssystem.

## IS::NumberOfTextServers - Anzahl der Text-Server-Instanzen {#section-971e20a90c1a473598fba738ed95671a}

Die maximale Anzahl von Text-Renderern, die gleichzeitig aktiv sein sollen. 0 (Standard) entspricht der 1,5-fachen Anzahl der verfügbaren CPU-Kerne.

## IS::TextServerTcpPortRange - Text-Server-Kommunikations-Ports {#section-a13465de88ed4df09931e5ba840c1942}

Die Ports, die für die Text-Server-Kommunikation verwendet werden sollen. Angabe der ersten und letzten Portnummer, getrennt durch &quot;-&quot;.
