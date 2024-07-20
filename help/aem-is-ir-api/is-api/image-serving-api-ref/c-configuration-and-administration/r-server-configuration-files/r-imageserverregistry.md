---
description: Enthält Image-Server-Konfigurationseinstellungen.
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

Enthält Image-Server-Konfigurationseinstellungen.

Beim Ändern dieser XML-Datei muss darauf geachtet werden, dass die gültige XML-Syntax beibehalten wird. Andernfalls kann der Image-Server möglicherweise nicht gestartet werden.

Damit Änderungen wirksam werden, starten Sie den Image-Server nach der Bearbeitung dieser Datei neu. Nur die unten aufgeführten Elementwerte werden für Änderungen unterstützt. Bearbeiten Sie alle anderen Inhalte dieser Datei nur auf Empfehlung des technischen Kundendienstes von Dynamic Media.

>[!NOTE]
>
>Ändern Sie nicht die Struktur von `<imageserverregistry>`, einschließlich der Reihenfolge der Elemente. Gehen Sie beim Bearbeiten dieser Datei vorsichtig vor. Andernfalls kann der Image-Server möglicherweise nicht gestartet werden.

Die folgende Abbildung zeigt, welche Elemente geändert werden können. Andere Elemente sind vorhanden, die nicht geändert werden dürfen. Die folgende Reihenfolge der Elemente spiegelt nicht die Reihenfolge wider, in der sie in der Datei vorhanden sein müssen.

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

Es können mehrere `<RootPath>` -Elemente vorhanden sein (eines für jeden Ordner mit den Quelldatendateien). Image Server durchsucht die Stammpfade in der angegebenen Reihenfolge, um eine bestimmte Quelldatei zu finden.
