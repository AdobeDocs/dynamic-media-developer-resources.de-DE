---
description: Image Serving implementiert eine einfache visuelle Wasserzeichenfunktion.
solution: Experience Manager
title: Wasserzeichen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Wasserzeichen{#watermarks}

Image Serving implementiert eine einfache visuelle Wasserzeichenfunktion.

Ein Wasserzeichen ist normalerweise ein halbtransparentes Bild, es kann sich jedoch um Text oder ein komplexeres, mehrschichtiges Composite-Bild handeln. Der Server legt das Wasserzeichen nach allen Ansichtsattributen ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) angewendet wurden.

Wasserzeichen wird durch die Einstellung `attribute::Watermark` zu einem gültigen Katalogeintrag, der das Wasserzeichenbild oder die Vorlage enthalten würde. Wenn `attribute::Watermark` in einem benannten Katalog festgelegt ist, fügt der Server das Wasserzeichen zu allen Bildanforderungen hinzu, die auf die Katalog-ID in der Anfrage-URL verweisen. Wenn `default::Watermark` festgelegt ist (im Standardkatalog, [!DNL default.ini]), wird das Wasserzeichen auf alle Bildanforderungen angewendet, unabhängig davon, ob sie auf einen Katalog verweisen oder nicht.

Wasserzeichen werden nicht auf Bilder angewendet, die als Antwort auf Miniaturanfragen ( `req=tmb`) und bestimmte Anfragen von Dynamic Media-Viewern.

## Skalierung und Ausrichtung {#section-89ef9e5926ae438abbd8e70332749b76}

Wenn ein Wasserzeichen angegeben wird, generiert der Server zunächst das zusammengesetzte Bild (das *Zielbild*), auf die das Wasserzeichen angewendet werden muss (bevor die Ansicht angewendet wird). Der Server generiert dann das zusammengesetzte Bild für das Wasserzeichen wie jedes andere Bild (das *Wasserzeichenbild*).

Im Gegensatz zu Standardbildern, `sizeN=` kann für layer=0 oder layer=comp des Wasserzeichenbilds angegeben werden. Dies ermöglicht die Skalierung des Wasserzeichenbilds relativ zum Zielbild. Wenn `sizeN=` nicht angegeben ist, behält das Wasserzeichenbild seine Pixelgröße bei, wenn es mit dem Zielbild zusammengeführt wird.

Anforderungsbefehle (z. B. `fmt=`) und Anzeigen von Befehlen (z. B. `wid=`) werden in Wasserzeichendatensätzen ignoriert, mit Ausnahme von `align=`. `align=` kann verwendet werden, um das Wasserzeichenbild relativ zum Wasserzeichenbild relativ zum Zielbild zu positionieren. Dadurch kann das Wasserzeichen relativ zu einer Ecke oder Kante des Zielbilds positioniert werden.

Nach der Skalierung und Ausrichtung legt der Server das Wasserzeichenbild mithilfe der `blendMode=` und `opac=` Werte, die für `layer=0` oder `layer=comp` des Wasserzeichenbilds. Schließlich werden die für das Zielbild angegebenen Anforderungs- und Ansichtsbefehle angewendet, um das Antwortbild zu erstellen.

Beachten Sie, dass sich das Wasserzeichenbild nie über einen leeren Bereich erstreckt, der dem Antwortbild vom `wid=` und `hei=` Befehle.

## Beispiel {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Ein typisches Wasserzeichen kann aus einem einfachen RGBA-Bild bestehen, das ein Logo oder einen Copyright-Hinweis enthält. Wir erstellen einen Datensatz im Bildkatalog (oder im Standardkatalog) mit `catalog::Id` auf `watermark` und geben Sie die Bilddatei des Wasserzeichens in `catalog::Path`. Wir möchten das Wasserzeichen so ausdehnen, dass es an das Ansichtsbild angepasst wird (ohne das Wasserzeichen zu verzerren), während ein wenig zusätzlicher Rand verbleibt, und die Deckkraft auf 20 % des ursprünglichen Wasserzeichens reduzieren, sodass wir `catalog::Modifier` nach `sizeN=0.9,0.9&opac=20`. Um Wasserzeichen zu aktivieren, legen Sie `attribute::Watermark` an die ID des Wasserzeichenkatalogeintrags, in diesem Beispiel &quot;Wasserzeichen&quot;. Vielleicht möchten wir mit verschiedenen `blendMode=` Auswahl verschiedener Wasserzeicheneffekte.

## Verwandte Themen {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
