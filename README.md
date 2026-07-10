# Star Citizen Mining és Blueprint Segéd

## Magyar leírás

Ez egy ingyenes, nem kereskedelmi Star Citizen közösségi segéd, amely egy helyre rendezi a kiválasztott alapanyagok farmolásához, felismeréséhez, finomításához és felhasználásához szükséges információkat.

A program egyetlen HTML-fájlból fut, ezért nincs szükség telepítésre vagy külön szerverre.

## Fő funkciók

* Az alapanyagok helyszínenként külön kártyákon jelennek meg.
* Megmutatja az adott rendszer és mining helyszín nevét.
* Kijelzi az alapanyag előfordulási arányát.
* Megjeleníti a hozzá tartozó radar signature értékeket és színkódokat.
* Megmutatja a javasolt finomítót és az elérhető finomítási bónuszt.
* Az anyag nevére kattintva kilistázza, mely kiválasztott blueprint itemekhez szükséges.
* Közvetlen linket ad az adott blueprint Star Citizen Wiki oldalához.
* A „Kitermelve” és „Finomítóba beadva” jelölések segítségével követhető a haladás.
* A jelölések a böngésző helyi tárhelyében automatikusan elmentődnek.
* A felület asztali gépen és mobilon is használható.

## Felhasznált adatforrások

### SCMDB

Az alábbi adatok és képek az SCMDB PTU Mining Database alapján kerültek a projektbe:

* mining helyszínek,
* alapanyag-előfordulási arányok,
* radar signature értékek,
* radarértékekhez tartozó színkódok,
* mining helyszíneket és alapanyagokat bemutató képek.

Forrás:

[SCMDB PTU Mining Database](https://scmdb.net/?page=mine&channel=ptu)

### UEX Corporation

A finomítói helyszínek és finomítási bónuszok a UEX Corporation refinery adatbázisa alapján kerültek meghatározásra.

Forrás:

[UEX Refinery Database](https://uexcorp.space/mining/refineries)

### Star Citizen Wiki API

A blueprintok, craftolható itemek és ingredient kapcsolatok ellenőrzéséhez a Star Citizen Wiki Blueprint API szolgáltatását használjuk.

Forrás:

[Star Citizen Wiki Blueprints](https://api.star-citizen.wiki/blueprints)

## Használat

1. Töltsd le a HTML-fájlt.
2. Nyisd meg egy modern böngészőben.
3. Keress rá egy alapanyagra, vagy válassz rendszert.
4. Kattints az alapanyag nevére a hozzá tartozó blueprintok megjelenítéséhez.
5. A „Kitermelve” és „Finomítóba beadva” pipákkal jelöld az elkészült feladatokat.

A blueprintadatok betöltéséhez internetkapcsolat szükséges.

## Miért készült?

A cél az volt, hogy ne kelljen egyszerre több külön oldalt, képet és táblázatot nézni.

A segéd egyetlen felületen mutatja meg:

* hova kell menni,
* mit lehet ott megszerezni,
* milyen radarértéket kell keresni,
* hova érdemes vinni finomítani,
* és melyik item elkészítéséhez szükséges az adott alapanyag.

## Jogi és forrásmegjelölési nyilatkozat

Ez egy rajongói, közösségi projekt.

A projekt nem áll hivatalos kapcsolatban a Cloud Imperium Games, a Roberts Space Industries, az SCMDB, a UEX Corporation vagy a Star Citizen Wiki üzemeltetőivel.

A Star Citizen név, a játékhoz tartozó védjegyek, játékadatok és grafikai elemek a megfelelő jogtulajdonosok tulajdonát képezik.

A projekt nem állítja, hogy az SCMDB, a UEX vagy a Star Citizen Wiki adatai és képei a projekt saját tulajdonát képeznék.

A repository saját forráskódjára vonatkozó licenc nem terjed ki automatikusan a külső forrásból származó:

* képekre,
* játékadatokra,
* adatbázis-tartalmakra,
* logókra,
* védjegyekre.

Az adatok a Star Citizen frissítései miatt megváltozhatnak, ezért a projekt nem garantálja, hogy minden információ mindig teljesen aktuális vagy hibamentes.

Jogtulajdonosi vagy adatjavítási kérés esetén kérlek, nyiss egy GitHub issue-t.

---

# Star Citizen Mining and Blueprint Helper

## English description

This is a free, non-commercial Star Citizen community tool that brings together the information required for locating, identifying, refining, and using selected mining resources.

The application runs as a single HTML file, so no installation or separate server is required.

## Main features

* Resources are grouped into separate cards by mining location.
* Displays the star system and exact mining location.
* Shows the resource occurrence percentage.
* Displays the corresponding radar signature values and color coding.
* Shows the recommended refinery and available refinery bonus.
* Clicking a resource name displays which selected blueprint items require that resource.
* Provides a direct link to the related Star Citizen Wiki blueprint page.
* Includes “Mined” and “Submitted to refinery” checkboxes for progress tracking.
* Progress is automatically stored in the browser’s local storage.
* The interface works on both desktop and mobile devices.

## Data sources

### SCMDB

The following information and images are based on the SCMDB PTU Mining Database:

* mining locations,
* resource occurrence percentages,
* radar signature values,
* radar signature color coding,
* images showing mining locations and resources.

Source:

[SCMDB PTU Mining Database](https://scmdb.net/?page=mine&channel=ptu)

### UEX Corporation

Refinery locations and refinery bonuses are based on the UEX Corporation refinery database.

Source:

[UEX Refinery Database](https://uexcorp.space/mining/refineries)

### Star Citizen Wiki API

Blueprints, craftable items, and ingredient relationships are checked through the Star Citizen Wiki Blueprint API.

Source:

[Star Citizen Wiki Blueprints](https://api.star-citizen.wiki/blueprints)

## Usage

1. Download the HTML file.
2. Open it in a modern web browser.
3. Search for a resource or select a star system.
4. Click a resource name to display the related blueprints.
5. Use the “Mined” and “Submitted to refinery” checkboxes to track completed tasks.

An internet connection is required to load blueprint information.

## Why was it created?

The goal was to avoid having to check several different websites, images, and spreadsheets at the same time.

The tool shows in one place:

* where to go,
* which resources can be found there,
* which radar signatures to look for,
* where the materials should be refined,
* and which crafted items require each resource.

## Legal and attribution notice

This is a fan-made community project.

This project is not officially affiliated with Cloud Imperium Games, Roberts Space Industries, SCMDB, UEX Corporation, or the Star Citizen Wiki team.

The Star Citizen name, game-related trademarks, game data, and graphical assets belong to their respective owners.

The project does not claim ownership of data or images originating from SCMDB, UEX Corporation, or Star Citizen Wiki.

Any license applied to the original source code of this repository does not automatically cover externally sourced:

* images,
* game data,
* database content,
* logos,
* trademarks.

Star Citizen data may change between game updates. The project therefore cannot guarantee that all information will always remain current, complete, or error-free.

For copyright, removal, or data correction requests, please open a GitHub issue.
