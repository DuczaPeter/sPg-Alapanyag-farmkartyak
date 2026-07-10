## Star Citizen alapanyag-farm és blueprint segéd

Ez egy egyfájlos HTML-segéd, amely a kiválasztott Star Citizen alapanyagok farmolását, finomítását és blueprint-felhasználását rendezi egy helyre.

### Mire használható?

A program helyszínenként külön kártyákon mutatja:

* melyik alapanyag hol található,
* az adott helyszínen mekkora a legjobb előfordulási arány,
* milyen radar signature értékek alapján lehet felismerni,
* melyik finomítóba érdemes vinni,
* mekkora finomítási bónusz jár,
* melyik blueprint itemekhez szükséges az adott anyag.

Az anyag nevére kattintva megnyílik a hozzá tartozó blueprint-lista, ahonnan egy kattintással elérhető az adott Star Citizen Wiki blueprintoldala.

### Milyen adatokat használtunk?

A lelőhelyadatok egy Star Citizen 4.9 PTU adatcsomagból származnak.

A finomítók és finomítási bónuszok ellenőrzéséhez a UEX refinery adatbázisát használtuk.

A blueprintok és az alapanyag-kapcsolatok lekéréséhez a Star Citizen Wiki API szolgáltatását használjuk:

[https://api.star-citizen.wiki/blueprints](https://api.star-citizen.wiki/blueprints)

A radar signature értékek a külön megadott ship mining és FPS mining signature táblázat alapján kerültek be.

### Hogyan működik?

A teljes program egyetlen HTML-fájlban fut.

Nincs szükség telepítésre vagy külön szerverre. A fájlt meg kell nyitni egy modern böngészőben.

A blueprint-adatok internetkapcsolattal, közvetlenül a Star Citizen Wiki API-ból töltődnek be.

A pipálható állapotok, például a „Kitermelve” és a „Finomítóba beadva” jelölések a böngésző helyi tárhelyében kerülnek mentésre.

### Miért készült?

A cél az volt, hogy ne kelljen több külön weboldalt, táblázatot és képet egyszerre nézni.

Egyetlen felületen látható:

* hova kell menni,
* mit kell ott összeszedni,
* milyen radarértéket kell keresni,
* hova kell vinni finomítani,
* és melyik item elkészítéséhez szükséges az adott alapanyag.

A felület mobilon és asztali gépen is használható, és a kártyás kialakítás miatt gyorsan átlátható.
