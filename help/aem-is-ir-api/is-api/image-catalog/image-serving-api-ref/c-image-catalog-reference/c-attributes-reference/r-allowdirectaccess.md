---
description: Direkten Zugriff auf pfadbasierte Assets zulassen.
seo-description: Direkten Zugriff auf pfadbasierte Assets zulassen.
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AllowDirectAccess{#allowdirectaccess}

Direkten Zugriff auf pfadbasierte Assets zulassen.

Wenn dieses Attribut definiert ist, ist pfadbasierter Zugriff für die angegebenen Objekttypen zulässig oder eingeschränkt, je nachdem, ob das `include` oder das `exclude` Schlüsselwort verwendet wird.

>[!NOTE]
>
>Wenn das `AllowDirectAccess` Attribut nicht angegeben ist, lautet der Standardwert `exclude`.

* `include` erlaubt den Zugriff auf die angegebenen Objektarten und beschränkt den Zugriff auf alle anderen.
* `exclude` beschränkt den Zugriff auf die angegebenen Objektarten und erlaubt den Zugriff auf alle anderen.

Wenn weder `include` noch `exclude` angegeben, wird angenommen `include` .

Folgende Typen können gesteuert werden:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Beispiele {#section-4c3765ebaa4245a799b454fc196f9237}

* Direkten Zugriff nur für `IS` und `STATIC` Objekttypen zulassen

   `AllowDirectAccess=include:IS,STATIC`

* Direkten Zugriff auf alle Objektarten mit Ausnahme von `IS` und `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Direkten Zugriff für *keine* Objekttypen zulassen (d. h. keine einschließen)

   `AllowDirectAccess=include:`

* Direkten Zugriff für *alle* Objekttypen zulassen (d. h. keine ausschließen)

   `AllowDirectAccess=exclude:`

* Äquivalent zu `include:IS,STATIC` (wenn `include`/ `exclude` nicht vorhanden ist, wird angenommen, `include` )

   `AllowDirectAccess=IS,STATIC`

   Beachten Sie, dass dies der Standardwert ist, der verwendet wird, wenn das `AllowDirectAccess` Attribut für diese Firma nicht angegeben wurde.

* Keine einschließen, entsprechend `include:` (wenn `include`/ `exclude` nicht vorhanden ist, wird angenommen, `include` )

   `AllowDirectAccess=`

