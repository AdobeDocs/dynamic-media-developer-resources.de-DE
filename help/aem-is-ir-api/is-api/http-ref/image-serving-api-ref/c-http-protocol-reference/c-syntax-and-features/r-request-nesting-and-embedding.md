---
description: Die Bildbereitstellung unterstützt die unbegrenzte Verschachtelung von Bildbereitstellungsanfragen, das Einbetten von Bildbereitstellungsanfragen sowie das Einbetten von Bildern, die von fremden Servern abgerufen wurden. Nur Ebenenbilder und Ebenenmasken unterstützen diese Mechanismen.
solution: Experience Manager
title: Verschachtelung und Einbettung anfordern
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 0%

---

# Verschachtelung und Einbettung anfordern{#request-nesting-and-embedding}

Die Bildbereitstellung unterstützt die unbegrenzte Verschachtelung von Bildbereitstellungsanfragen, das Einbetten von Bildbereitstellungsanfragen sowie das Einbetten von Bildern, die von fremden Servern abgerufen wurden. Nur Ebenenbilder und Ebenenmasken unterstützen diese Mechanismen.

>[!NOTE]
>
>Bestimmte E-Mail-Clients und Proxy-Server können die geschweiften Klammern kodieren, die für die Schachtelungs- und Einbettungssyntax verwendet werden. Anwendungen, bei denen dies ein Problem darstellt, sollten Klammern anstelle von geschweiften Klammern verwenden.

## Verschachtelte Bildbereitstellungsanfragen {#section-6954202119e0466f8ff27c79f4f039c8}

Eine gesamte Image-Serving-Anfrage kann als Ebenenquelle verwendet werden, indem sie im `src=`-Befehl (oder `mask=`-Befehl) mit der folgenden Syntax angegeben wird:

`…&src=is( nestedRequest)&…`

Beim `is`-Token wird zwischen Groß- und Kleinschreibung unterschieden.

Die verschachtelte Anfrage darf nicht den Stammverzeichnis des Servers enthalten (normalerweise ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>Die Trennzeichen für verschachtelte Anfragen (`'(',')'`) und die Befehlstrennzeichen (`'?'`, `'&'`, `'='`) in verschachtelten Anfragen dürfen nicht HTTP-kodiert sein. In der Tat müssen verschachtelte Anfragen genauso codiert werden wie die äußere (verschachtelte) Anfrage.

Vorverarbeitungsregeln werden auf verschachtelte Anfragen angewendet.

Die folgenden Befehle werden ignoriert, wenn sie in verschachtelten Anfragen angegeben werden (entweder in der Anfrage-URL oder in `catalog::Modifier` oder `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Wenn das Ergebnisbild der verschachtelten Anfragen Maskendaten (Alpha) enthält, werden diese als Ebenenmaske an die Einbettungsebene übergeben.

Ignoriert werden auch `attribute::MaxPix` und `attribute::DefaultPix` des Bildkatalogs, der für die verschachtelte Anfrage gilt.

Das Bildergebnis einer verschachtelten IS-Anfrage kann optional zwischengespeichert werden, indem `cache=on` eingeschlossen wird. Standardmäßig ist das Zwischenspeichern von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn erwartet wird, dass das Zwischenbild in einer anderen Anfrage innerhalb eines angemessenen Zeitraums wiederverwendet wird. Es gilt die standardmäßige Server-seitige Cache-Verwaltung. Daten werden in einem verlustfreien Format zwischengespeichert.

## Render-Anfragen für eingebettete Bilder {#section-69c5548db930412b9b90d9b2951a6969}

Wenn das Dynamic Media-Bild-Rendering auf dem Server aktiviert ist, können Render-Anforderungen als Ebenenquellen verwendet werden, indem sie im Befehl src= (oder mask=) angegeben werden. Verwenden Sie die folgende Syntax:

` …&src=ir( *[!DNL renderRequest]*)&…`

Beim `ir`-Token wird zwischen Groß- und Kleinschreibung unterschieden.

*[!DNL renderRequest]* ist die übliche Bildwiedergabeanfrage, mit Ausnahme des HTTP-Stammpfads ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>Die Trennzeichen für verschachtelte Anfragen (`'(',')'`) und die Befehlstrennzeichen (`'?'`, `'&'`, `'='`) in verschachtelten Anfragen dürfen nicht HTTP-kodiert sein. Effektiv müssen eingebettete Anfragen genauso codiert werden wie die äußere (einbettende) Anfrage.

Die folgenden Image-Rendering-Befehle werden ignoriert, wenn sie in verschachtelten Anfragen angegeben werden:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Ignoriert werden auch die `attribute::MaxPix` und `attribute::DefaultPix` des Materialkatalogs, der für die verschachtelte Render-Anfrage gilt.

Das Bildergebnis einer verschachtelten IR-Anfrage kann optional zwischengespeichert werden, indem `cache=on` eingeschlossen wird. Standardmäßig ist das Zwischenspeichern von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn erwartet wird, dass das Zwischenbild in einer anderen Anfrage innerhalb eines angemessenen Zeitraums wiederverwendet wird. Es gilt die standardmäßige Server-seitige Cache-Verwaltung. Daten werden in einem verlustfreien Format zwischengespeichert.

## Eingebettete FXG-Render-Anfragen {#section-c817e4b4f7da414ea5a51252ca7e120a}

Wenn der FXG Graphics Renderer (auch als [!DNL AGMServer] bezeichnet) installiert und mit Image Serving aktiviert ist, können FXG-Anfragen als Ebenenquellen verwendet werden, indem sie in `src=` (oder `mask=`) Befehlen angegeben werden. Verwenden Sie die folgende Syntax:

`…&src=fxg( renderRequest)&…`

Beim `fxg`-Token wird zwischen Groß- und Kleinschreibung unterschieden.

>[!NOTE]
>
>Das FXG-Grafik-Rendering ist nur in der gehosteten Dynamic Media-Umgebung verfügbar und erfordert möglicherweise zusätzliche Lizenzen. Wenden Sie sich an den technischen Support für Dynamic Media, um weitere Informationen zu erhalten.

*[!DNL renderRequest]* ist die übliche FXG-Render-Anfrage, mit Ausnahme des HTTP-Stammpfads ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>Die Trennzeichen ( `'(',')'`) und die Befehlstrennzeichen ( `'?'`, `'&'`, `'='`) in verschachtelten Anfragen dürfen nicht HTTP-kodiert sein. Effektiv müssen eingebettete Anfragen genauso codiert werden wie die äußere (einbettende) Anfrage.

Die folgenden FXG-Befehle werden ignoriert, wenn sie in verschachtelten Anfragen angegeben werden:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Fremdbildquellen {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

Image Serving unterstützt den Zugriff auf Quellbilder auf fremden HTTP-Servern.

>[!NOTE]
>
>Für Remote-URLs wird nur das HTTP-Protokoll unterstützt.

Um eine Fremd-URL für einen `src=` oder einen `mask=`-Befehl anzugeben, trennen Sie die Fremd-URL oder das URL-Fragment mit Klammern ab:

`…&src=( foreignUrl)&…`

Wichtig Die Trennzeichen ( `'(',')'`) und Befehlstrennzeichen ( `'?'`, `'&'`, `'='`) in verschachtelten Anfragen dürfen nicht HTTP-kodiert sein. Effektiv müssen eingebettete Anfragen genauso codiert werden wie die äußere (einbettende) Anfrage.

Vollständige absolute URLs (sofern `attribute::AllowDirectUrls` festgelegt ist) und URLs relativ zu `attribute::RootUrl` sind zulässig. Ein Fehler tritt auf, wenn eine absolute URL eingebettet ist und das Attribut: `AllowDirectUrls` gleich 0 ist oder wenn eine relative URL angegeben und `attribute::RootUrl` leer ist.

Während fremde URLs nicht direkt in der Pfadkomponente der Anfrage-URL angegeben werden können, ist es möglich, eine Vorverarbeitungsregel einzurichten, um die Konvertierung relativer Pfade in absolute URLs zu ermöglichen (siehe folgendes Beispiel).

Fremdbilder werden vom Server entsprechend den in der HTTP-Antwort enthaltenen Caching-Kopfzeilen zwischengespeichert. Wenn weder ein `ETag` noch ein HTTP-Antwort-Header für die letzte Änderung vorhanden ist, wird die Antwort nicht zwischengespeichert. Dies kann bei wiederholten Zugriffen auf dasselbe Fremdbild zu Leistungseinbußen führen, da die Bildbereitstellung das Bild bei jedem Zugriff erneut abrufen und überprüfen muss.

Dieser Mechanismus unterstützt dieselben Bilddateiformate, die vom Dienstprogramm „Image Convert“ (IC) unterstützt werden, mit Ausnahme von Quellbildern mit 16 Bit pro Komponente.

>[!NOTE]
>
>Die Bildbereitstellung führt automatisch das Validierungsprogramm aus, wenn ein fremdes Bild zum ersten Mal verwendet wird, um sicherzustellen, dass das Bild gültig ist und während der Übertragung nicht beschädigt wurde. Dies kann zu einer leichten Verzögerung beim ersten Zugriff führen. Um eine optimale Leistung zu erzielen, wird empfohlen, die Größe solcher Bilder zu begrenzen und/oder ein Bilddateiformat zu verwenden, das gut komprimiert ist.

## Einschränkungen {#section-fb68e3f0d40947feb94d7bf183b64929}

Die Größe des Bildes, das durch verschachtelte/eingebettete Anfragen generiert wird, wird normalerweise automatisch optimiert. Wenn das Caching verschachtelter Anfragebilder aktiviert ist, können Sie die Leistung inkrementell steigern, indem Sie die genaue Größe des verschachtelten Bildes angeben, sodass keine weitere Skalierung erforderlich ist, wenn der Cache-Eintrag wiederverwendet wird.

Wichtige Bildbereitstellung unterstützt keine Doppelkodierung von verschachtelten oder eingebetteten Anforderungen. Verschachtelte und eingebettete Anfragen müssen genauso wie einfache Anfragen HTTP-kodiert sein.

## Beispiele {#section-d800cfc31abe46d2a964f8e7929231f1}

**Schichtvorlage mit Zwischenspeicherung:**

Verwenden Sie Verschachtelung, um einer Ebenenvorlage eine Zwischenspeicherung hinzuzufügen. Eine begrenzte Anzahl von Hintergrundbildern wird mit stark variablem Text überlagert. Die anfängliche Vorlagenzeichenfolge könnte wie folgt aussehen:

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Mit geringfügigen Änderungen können wir das Bild der Ebene 0 vorab skalieren und dauerhaft zwischenspeichern, wodurch die Server-Last reduziert wird:

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Einbetten von Anfragen für das Dynamic Media-Bild-Rendering**

Verwenden einer in [!DNL myCatalog/myTemplate] gespeicherten Vorlage; Generieren des Bildes für Ebene2 der Vorlage mithilfe von Dynamic Media Image Rendering:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Beachten Sie die verschachtelten geschweiften Klammern. Die Anfrage zum Rendern von Bildern bettet einen Rückruf an Image Serving ein, um eine wiederholbare Textur abzurufen.

## Verwandte Themen {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Request PreProcessing](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Image Rendering Reference, [templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Image Serving Utilities](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
