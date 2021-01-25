---
description: Direkten Zugriff auf pfadbasierte Assets zulassen.
seo-description: Direkten Zugriff auf pfadbasierte Assets zulassen.
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# AllowDirectAccess{#allowdirectaccess}

Direkten Zugriff auf pfadbasierte Assets zulassen.

Wenn dieses Attribut definiert ist, ist pfadbasierter Zugriff für die angegebenen Objekttypen zulässig oder eingeschränkt, je nachdem, ob das `include`- oder `exclude`-Schlüsselwort verwendet wird.

>[!NOTE]
>
>Wenn das Attribut `AllowDirectAccess` nicht angegeben ist, lautet der Standardwert `exclude`.

* `include` erlaubt den Zugriff auf die angegebenen Objektarten und beschränkt den Zugriff auf alle anderen.
* `exclude` beschränkt den Zugriff auf die angegebenen Objektarten und erlaubt den Zugriff auf alle anderen.

Wenn weder `include` noch `exclude` angegeben ist, wird `include` angenommen.

Folgende Typen können gesteuert werden:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Beispiele {#section-4c3765ebaa4245a799b454fc196f9237}

* Direkten Zugriff nur für die Objekttypen `IS` und `STATIC` zulassen

   `AllowDirectAccess=include:IS,STATIC`

* Direkten Zugriff auf alle Objekttypen mit Ausnahme von `IS` und `STATIC``AllowDirectAccess=exclude:IS,STATIC` zulassen

* Direkten Zugriff für *no*-Objekttypen zulassen (d.h. keine einschließen)

   `AllowDirectAccess=include:`

* Direkten Zugriff für *alle* Objekttypen zulassen (d.h. keine ausschließen)

   `AllowDirectAccess=exclude:`

* Entspricht `include:IS,STATIC` (wenn `include`/ `exclude` nicht vorhanden ist, wird `include` angenommen)

   `AllowDirectAccess=IS,STATIC`

   Beachten Sie, dass dies der Standardwert ist, der verwendet wird, wenn das `AllowDirectAccess`-Attribut für diese Firma nicht angegeben ist.

* Keine einschließen, entspricht `include:` (wenn `include`/ `exclude` nicht vorhanden ist, wird `include` angenommen)

   `AllowDirectAccess=`

