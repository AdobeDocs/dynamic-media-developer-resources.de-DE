---
description: Der Abschnitt "Abfrage"von Anforderungen und Vignettenmodifizierer-Zeichenfolgen kann benutzerdefinierte Variablen enthalten.
seo-description: Der Abschnitt "Abfrage"von Anforderungen und Vignettenmodifizierer-Zeichenfolgen kann benutzerdefinierte Variablen enthalten.
seo-title: Benutzerdefinierte Variablen
solution: Experience Manager
title: Benutzerdefinierte Variablen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# Benutzerspezifische Variablen{#custom-variables}

Der Abschnitt &quot;Abfrage&quot;von Anforderungen und die Zeichenfolgen &quot;vignette::Modifier&quot;können benutzerdefinierte Variablen enthalten.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Variablenname. Kann aus einer beliebigen Kombination aus Alpha-, Ziffernzeichen- und sicheren Zeichen bestehen, mit Ausnahme von &#39;$&#39;.

** *[!DNL value]* ** Wert, auf den die Variable gesetzt werden soll (Zeichenfolge).

Variablen werden ähnlich wie andere Serverbefehle definiert, wobei die obige Syntax verwendet wird. Variablen müssen definiert werden, bevor auf sie verwiesen werden kann. Variablen, die in `vignette::Modifier` definiert sind, können in der URL-Anforderung referenziert werden und umgekehrt.

>[!NOTE]
>
>*[!DNL value]* muss für eine sichere HTTP-Übertragung mit einem Pass URL-kodiert sein. Dublette-Codierung ist erforderlich, wenn *[!DNL value]* über HTTP erneut übertragen wird. Dies ist der Fall, wenn *[!DNL value]* in eine verschachtelte ausländische Anforderung ersetzt wird.

Variablen werden referenziert, indem der Variablenname (durch einen vorangestellten und einen nachfolgenden $) an einer beliebigen Stelle in Befehlswerte eingebettet wird. Beispiel: zwischen dem &#39;=&#39; hinter dem Befehlsnamen und dem nachfolgenden &#39;&amp;&#39; oder dem Ende der Anforderung. Der Server ersetzt jedes dieser Vorkommen von $ *[!DNL name]*$ durch *[!DNL string]*. Bei Vorkommen von $ *[!DNL name]*$ in Befehlsnamen (vor dem Gleichheitszeichen eines Befehls) und im Pfadteil der Anforderung werden keine Ersetzungen vorgenommen.

Benutzerdefinierte Variablen werden möglicherweise nicht verschachtelt. Alle Vorkommen von $ *[!DNL name]*$ innerhalb von *[!DNL string]* werden nicht ersetzt. Beispielsweise wird das Anforderungsfragment `$var2=apple&$var1=my$var2$tree&text=$var1$` in `text=my$var2$tree` aufgelöst.

$ ist kein reserviertes Zeichen; es kann andernfalls in der Anforderung auftreten. Beispiel: `src=my$texture$file.tif` ist ein gültiger Befehl (vorausgesetzt, dass ein Materialkatalogeintrag oder eine Texturdatei mit dem Namen [!DNL my$texture$file.tif] vorhanden ist), während `wid=$number$` nicht vorhanden ist, da `wid=` ein numerisches Argument erfordert.
