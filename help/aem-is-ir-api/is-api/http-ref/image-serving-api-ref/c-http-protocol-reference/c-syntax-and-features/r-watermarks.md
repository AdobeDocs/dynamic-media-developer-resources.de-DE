---
description: Image Serving implementiert eine einfache visuelle Wasserzeichenfunktion.
solution: Experience Manager
title: Wasserzeichen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Wasserzeichen{#watermarks}

Image Serving implementiert eine einfache visuelle Wasserzeichenfunktion.

Ein Wasserzeichen ist normalerweise ein halbtransparentes Bild, kann jedoch Text oder ein komplexeres, mehrschichtiges zusammengesetztes Bild sein. Der Server legt das Wasserzeichen über das Antwortbild, nachdem alle Ansichtsattribute ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) angewendet wurden.

Wasserzeichen werden aktiviert, indem `attribute::Watermark` auf einen gültigen Katalogeintrag gesetzt wird, der das Wasserzeichenbild oder die Vorlage enthalten würde. Wenn `attribute::Watermark` in einem benannten Katalog festgelegt ist, fügt der Server das Wasserzeichen zu allen Bildanforderungen hinzu, die in der Anfrage-URL auf die Katalog-ID verweisen. Wenn `default::Watermark` festgelegt ist (im Standardkatalog [!DNL default.ini]), wird das Wasserzeichen auf alle Bildanforderungen angewendet, unabhängig davon, ob sie auf einen Katalog verweisen oder nicht.

Wasserzeichen werden nicht auf Bilder angewendet, die als Antwort auf Miniaturansichts-Anfragen (`req=tmb`) und bestimmte Anfragen von Dynamic Media-Viewern zurückgegeben werden.

## Skalierung und Ausrichtung {#section-89ef9e5926ae438abbd8e70332749b76}

Wenn ein Wasserzeichen angegeben wird, generiert der Server zunächst das zusammengesetzte Bild (das *Zielbild*), auf das das Wasserzeichen angewendet werden muss (bevor die Ansicht transformiert wird). Der Server generiert dann das zusammengesetzte Bild für das Wasserzeichen genau wie jedes andere Bild (das *Wasserzeichenbild*).

Im Gegensatz zu Standardbildern können `sizeN=` für Ebene=0 oder Ebene=Komp des Wasserzeichenbildes angegeben werden. Dies ermöglicht die Skalierung des Wasserzeichenbildes relativ zum Zielbild. Wenn `sizeN=` nicht angegeben ist, behält das Wasserzeichenbild seine Pixelgröße bei, wenn es mit dem Zielbild zusammengeführt wird.

Anforderungsbefehle (z. B. `fmt=`) und Anzeigebefehle (z. B. `wid=`) werden in Wasserzeicheneinträgen ignoriert, mit Ausnahme von `align=`. `align=` können verwendet werden, um das Wasserzeichenbild relativ zum Wasserzeichenbild relativ zum Zielbild zu positionieren. Dies ermöglicht die Positionierung des Wasserzeichens relativ zu einer Ecke oder Kante des Zielbilds.

Nach dem Skalieren und Ausrichten legt der Server das Wasserzeichenbild mithilfe der für die `blendMode=` oder `opac=` des Wasserzeichenbildes angegebenen `layer=0`- und `layer=comp` über das Zielbild. Schließlich werden die für das Zielbild angegebenen Anforderungs- und Ansichtsbefehle angewendet, um das Antwortbild zu erstellen.

Beachten Sie, dass sich das Wasserzeichenbild niemals über Leerzeichen erstreckt, die dem Antwortbild durch die Befehle `wid=` und `hei=` hinzugefügt werden.

## Beispiel {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Ein typisches Wasserzeichen kann aus einem einfachen RGBA-Bild bestehen, das ein Logo oder einen Copyright-Hinweis enthält. Wir erstellen einen Datensatz im Bildkatalog (oder Standardkatalog), wobei `catalog::Id` auf `watermark` gesetzt ist, und geben die Wasserzeichenbilddatei in `catalog::Path` an. Wir möchten das Wasserzeichen dehnen, damit es in das Ansichtsbild passt (ohne das Wasserzeichen zu verzerren), während wir einen kleinen zusätzlichen Rand lassen, und die Deckkraft auf 20 % des ursprünglichen Wasserzeichens reduzieren, sodass wir `catalog::Modifier` auf `sizeN=0.9,0.9&opac=20` setzen. Um das Wasserzeichen zu aktivieren, setzen Sie `attribute::Watermark` auf die ID des Wasserzeichenkatalogeintrags, in diesem Beispiel „Wasserzeichen“. Vielleicht möchten wir mit verschiedenen `blendMode=` experimentieren, um verschiedene Wasserzeicheneffekte zu erzielen.

## Verwandte Themen {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
