---
description: Image Serving implementiert eine einfache visuelle Wasserzeichenfunktion.
seo-description: Image Serving implementiert eine einfache visuelle Wasserzeichenfunktion.
seo-title: Wasserzeichen
solution: Experience Manager
title: Wasserzeichen
topic: Scene7 Image Serving - Image Rendering API
uuid: b2bbaa59-dad9-4be3-bb92-142ed44f6d65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 1%

---


# Wasserzeichen{#watermarks}

Image Serving implementiert eine einfache visuelle Wasserzeichenfunktion.

Bei einem Wasserzeichen handelt es sich in der Regel um ein halbtransparentes Bild, es kann sich jedoch um Text oder ein komplexeres Composite-Bild mit Ebenen handeln. Der Server legt das Wasserzeichen über dem Antwortbild, nachdem alle Attribute der Ansicht ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) angewendet wurden.

Die Wasserzeichen-Funktion wird aktiviert, indem `attribute::Watermark` auf einen gültigen Katalogeintrag gesetzt wird, der das Wasserzeichenbild oder die Vorlage enthalten würde. Wenn `attribute::Watermark` in einem benannten Katalog eingestellt ist, fügt der Server das Wasserzeichen allen Bildanforderungen hinzu, die auf die Katalog-ID in der Anforderungs-URL verweisen. Wenn `default::Watermark` eingestellt ist (im Standardkatalog, [!DNL default.ini]), wird das Wasserzeichen auf alle Bildanforderungen angewendet, unabhängig davon, ob sie auf einen Katalog verweisen oder nicht.

Wasserzeichen werden nicht auf Bilder angewendet, die aufgrund von Miniaturansichtsanforderungen ( `req=tmb`) und bestimmten Anforderungen von Scene7-Viewern zurückgegeben werden.

## Skalierung und Ausrichtung {#section-89ef9e5926ae438abbd8e70332749b76}

Wenn ein Wasserzeichen angegeben wird, generiert der Server zunächst das Composite-Bild (das *Zielgruppe-Bild*), auf das das Wasserzeichen angewendet werden muss (bevor die Ansicht transformiert wird). Der Server generiert dann das Composite-Bild für das Wasserzeichen wie jedes andere Bild (das *Wasserzeichenbild*).

Im Gegensatz zu Standardbildern kann `sizeN=` für layer=0 oder layer=comp des Wasserzeichenbilds angegeben werden. Dies ermöglicht die Skalierung des Wasserzeichenbilds relativ zum Bild der Zielgruppe. Wenn `sizeN=` nicht angegeben ist, behält das Wasserzeichenbild seine Pixelgröße bei, wenn es mit der Zielgruppe zusammengeführt wird.

Anforderungsbefehle (z. B. `fmt=`) und Ansichten (z. B. `wid=`) werden in Wasserzeichenaufzeichnungen ignoriert, mit Ausnahme von `align=`. `align=` kann verwendet werden, um das Wasserzeichenbild relativ zum Wasserzeichenbild relativ zum Zielgruppe-Bild zu positionieren. Dadurch kann das Wasserzeichen relativ zu einer Zielgruppe oder Kante des Bilds positioniert werden.

Nach dem Skalieren und Ausrichten legt der Server das Wasserzeichenbild mithilfe der `blendMode=`- und `opac=`-Werte, die für `layer=0` oder `layer=comp` des Wasserzeichenbilds angegeben sind, auf das Zielgruppe-Image. Schließlich werden die für das Zielgruppe-Image angegebenen Anforderungs- und Ansichten-Befehle angewendet, um das Antwortbild zu erstellen.

Beachten Sie, dass das Wasserzeichenbild nie über einen Leerraum hinausgeht, der dem Antwortbild durch die Befehle `wid=` und `hei=` hinzugefügt wird.

## Beispiel {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Ein typisches Wasserzeichen kann aus einem einfachen RGBA-Bild bestehen, das ein Logo oder einen Copyright-Hinweis enthält. Wir erstellen einen Datensatz im Bildkatalog (oder im Standardkatalog) mit `catalog::Id` auf `watermark` und geben die Wasserzeichenbilddatei in `catalog::Path` an. Wir möchten das Wasserzeichen so dehnen, dass es in das Bild der Ansicht passt (ohne das Wasserzeichen zu verzerren), während ein wenig zusätzlicher Rand bleibt, und die Deckkraft auf 20 % des ursprünglichen Wasserzeichens reduzieren. Daher setzen wir `catalog::Modifier` auf `sizeN=0.9,0.9&opac=20`. Um Wasserzeichen zu aktivieren, setzen Sie `attribute::Watermark` in diesem Beispiel auf die ID des Wasserzeichenkatalogeintrags &quot;Wasserzeichen&quot;. Wir sollten mit verschiedenen `blendMode=`-Auswahlmöglichkeiten experimentieren, um unterschiedliche Wasserzeicheneffekte zu erzielen.

## Verwandte Themen {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
