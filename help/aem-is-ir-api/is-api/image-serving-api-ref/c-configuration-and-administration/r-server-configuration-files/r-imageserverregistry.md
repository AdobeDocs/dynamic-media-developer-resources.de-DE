---
description: Enthält Image-Server-Konfigurationseinstellungen.
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
TQID: 'https://experienceleague.adobe.com/UdMACutToNmpsXnhU0jAaItCZJ8r0RTxirjaqXSpa0c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

Enthält Image-Server-Konfigurationseinstellungen.

Beim Ändern dieser XML-Datei muss darauf geachtet werden, dass die gültige XML-Syntax beibehalten wird. Andernfalls kann es vorkommen, dass der Image-Server nicht gestartet wird.

Damit die Änderungen wirksam werden, starten Sie den Bildserver neu, nachdem Sie diese Datei bearbeitet haben. Nur die unten aufgeführten Elementwerte werden zur Änderung unterstützt. Bearbeiten Sie alle anderen Inhalte dieser Datei nur, wenn Sie vom technischen Support für Dynamic Media dazu aufgefordert werden.

>[!NOTE]
>
>Ändern Sie nicht die Struktur von `<imageserverregistry>`, einschließlich der Reihenfolge der Elemente. Gehen Sie beim Bearbeiten dieser Datei umsichtig vor, da der Bildserver sonst möglicherweise nicht gestartet wird.

Die folgende Abbildung zeigt, welche Elemente geändert werden können. Es sind andere Elemente vorhanden, die nicht geändert werden dürfen. Die Reihenfolge der Elemente unten spiegelt nicht die Reihenfolge wider, in der sie in der Datei vorhanden sein müssen.

```
<imageserverregistry>
    <TcpPort> 27345 </TcpPort>    
    <RootPath ./images </RootPath>
    <TempDirectory ./temp </TempDirectory>
    <Log> ./logs/ImageServer.log </Log>
    <TraceClient> 2 </TraceClient>
    <TraceStatsInterval> 600 </TraceStatsInterval>
    <PhysicalMemory> 20 </PhysicalMemory>
    <WorkerThreads> 0 </WorkerThreads>
    <SVGTcpPort> 27346 </SVGTcpPort>
    <MaxRenderRgnPixels> 16 </MaxRenderRgnPixels>
    <MaxSavePixels> 100 </MaxSavePixels>
    <MaxMessageSize> 16 </MaxMessageSize>
    <CacheServerUrl> http://localhost:8080/is/cache/secondary </CacheServerUrl>
    <NumberOfTextServers> 0 </NumberOfTextServers>
    <TextServerTcpPortRange> 27347-27380 </TextServerTcpPortRange>
    <SaveDirectory> ./ </SaveDirectory>
    <RemoteUrlDefaultExpiration> 36000 </RemoteUrlDefaultExpiration>
    <RemoteUrlTimeout> 60 </RemoteUrlTimeout>
    <MaxNonDsfSize> 4 </MaxNonDsfSize>
</imageserverregistry>
```

## Anmerkungen {#section-7217f011f69f41e7af4f3983d7776d6f}

Es können mehrere `<RootPath>` vorhanden sein (eines für jeden Ordner der Quelldatendatei). Bild-Server durchsucht die Stammpfade in der angegebenen Reihenfolge, um eine bestimmte Quelldatei zu finden.
