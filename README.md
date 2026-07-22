# Star Citizen Mining, Refinery és Blueprint Segéd

## Magyar leírás

Ez egy ingyenes, nem kereskedelmi Star Citizen közösségi segéd, amely egyetlen felületen rendezi a kiválasztott alapanyagok farmolásához, felismeréséhez, finomításához és blueprint alapú felhasználásához szükséges információkat.

A program egyetlen HTML-fájlból fut. Nincs szükség telepítésre, külön szerverre, adatbázisra vagy felhasználói fiókra.

A helyszínek, alapanyagok, radarjelek és finomítói adatok közvetlenül a HTML-fájlban találhatók. A blueprint receptek ellenőrzéséhez és a külső HUB-oldalak megnyitásához internetkapcsolat szükséges.

## Fő funkciók

### Alapanyag-farmkártyák

Az alapanyagok mining helyszínenként külön kártyákon jelennek meg.

Minden kártya megmutatja:

* a csillagrendszer nevét;
* a pontos mining helyszínt;
* az ott megszerezhető alapanyagokat;
* az alapanyag maximális vagy megadott előfordulási arányát;
* a mining típusát;
* a radar signature adatokat;
* a javasolt finomítót;
* az elérhető finomítási bónuszt;
* valamint az adott adathoz tartozó magyarázó megjegyzéseket.

A program külön kezeli a ship mining, ROC vagy vehicle mining, illetve FPS mining anyagokat.

### Rendszerenkénti csoportosítás

A farmhelyek csillagrendszerenként vannak csoportosítva.

A jelenlegi rendszerlista:

* Stanton;
* Pyro;
* Nyx.

Minden rendszer külön összecsukható és kinyitható.

A rendszer fejlécén látható, hogy az adott rendszerben hány farmhely szerepel.

A „Minden mutatása” gomb:

* törli a keresést;
* visszaállítja a rendszer- és állapotszűrőt;
* megszünteti a receptkijelöléseket;
* visszaállítja a teljes alapanyaglistát;
* és minden rendszert újra kinyit.

### Keresés és szűrés

A keresővel helyszínre, rendszerre, alapanyagra és finomítóra lehet keresni.

Külön rendszerszűrővel megjeleníthető:

* minden rendszer;
* csak Stanton;
* csak Pyro;
* csak Nyx.

Az állapotszűrővel megjeleníthető:

* minden farmkártya;
* csak azok, amelyeken még van feladat;
* csak a teljesen elkészült kártyák.

### Radar signature adatok

Minden támogatott alapanyag saját radarjel-információt kap.

A radarjel blokk megmutatja:

* az alap radar signature értéket;
* a mining típust;
* a hozzá tartozó színkódot;
* a lehetséges klaszterméretet;
* a klaszter minimum- és maximumjelét;
* valamint a köztes értékek számításának módját.

Kisebb ship mining klasztereknél a program az egymás után következő radarértékeket is megjeleníti.

Nagyobb FPS vagy ROC klasztereknél az egyedi alapjel, a minimális klaszterjel és a maximális klaszterjel jelenik meg.

Ha egy anyaghoz az adatforrás csak alapjelet közöl, de klaszterméretet nem, a program ezt külön jelzi. Ilyenkor nem talál ki nem ellenőrzött értékeket.

### Finomítói adatok

Minden finomítandó alapanyagnál megjelenik:

* a javasolt refinery station;
* a refinery station rendszere;
* az elérhető yield-bónusz;
* és az esetleges azonos értékű alternatív finomító.

A program külön jelzi azokat az alapanyagokat, amelyekhez a jelenlegi UEX refinery táblázat nem közöl állomásspecifikus yield-bónuszt.

Ilyen esetben a segéd nem nevez meg találomra „legjobb finomítót”.

A lap alján külön finomító-összesítő található, amely megmutatja:

* mely alapanyagokat érdemes ugyanarra a refinery stationre vinni;
* hány alapanyag tartozik az adott finomítóhoz;
* milyen bónuszok érhetők el;
* és mely esetekben van azonos értékű alternatíva.

A jelenlegi HTML-változat finomítói adatai a UEX Star Citizen 4.9 adatai alapján, 2026. július 22-én lettek újraellenőrizve.

### Receptszűrő

A receptszűrő alapértelmezetten összecsukva indul.

Kinyitva a receptek egyenletes, több soros rácsban jelennek meg. Nincs vízszintes görgetősáv.

A receptgombok a képernyő szélességéhez igazodnak, ezért asztali gépen és mobilon is áttekinthetőek maradnak.

Egy receptre kattintva a program csak az adott item elkészítéséhez szükséges alapanyagokat és farmhelyeket mutatja.

Ugyanarra a receptre ismét rákattintva a kijelölés megszűnik.

Egyszerre több recept is kijelölhető.

Több recept kijelölése esetén a program az összes kiválasztott itemhez szükséges alapanyagok egyesített listáját mutatja.

A rendszer automatikusan eltávolítja a duplikált alapanyagokat. Ha több kiválasztott recepthez ugyanaz az alapanyag kell, az csak egyszer jelenik meg a farmútvonalban.

Ha minden recept kijelölése megszűnik, a teljes alapanyaglista automatikusan visszaáll.

A „Minden recept / minden alapanyag” gomb az összes receptkijelölést egyszerre törli.

### Blueprint API ellenőrzés

A receptszűrő és az alapanyag-blueprint kapcsolatok ellenőrzése a Star Citizen Wiki Blueprint API használatával történik.

A program:

* lekéri az elérhető játékverziókat;
* több API-verziót is ellenőrizhet;
* megkeresi a projektben felsorolt blueprint itemeket;
* ellenőrzi a receptek ingredient listáját;
* és az elérhető adatok közül azt a verziót használja, amelyben a legtöbb keresett item megtalálható.

Ha az API valamelyik itemet nem adja vissza, a program ezt külön jelzi.

Hiányos API-eredménynél a segéd nem állítja automatikusan, hogy az adott alapanyag biztosan egyik itemhez sem szükséges.

### Alapanyagból blueprint keresés

Az alapanyag neve külön kattintható.

Az alapanyag nevére kattintva egy felugró ablak jelenik meg, amely megmutatja:

* melyik kiválasztott blueprint itemekhez kell az adott alapanyag;
* hány valódi receptkapcsolatot talált az API;
* milyen néven szerepel az ingredient az API-ban;
* melyik API game version alapján készült az eredmény;
* és hány megadott itemet sikerült megtalálni.

Minden megtalált blueprinthez külön „BP wiki megnyitása” link tartozik.

A link új böngészőlapon nyitja meg a megfelelő Star Citizen Wiki blueprint oldalt.

### HUB-hivatkozások

Egyes receptgombok jobb felső részén külön, kattintható „HUB” felirat jelenik meg.

A HUB felirat:

* külön működik a receptgombtól;
* nem kapcsolja be vagy ki a receptszűrést;
* az adott itemhez kézzel hozzárendelt HUB-oldalt nyitja meg;
* és új böngészőlapon nyílik meg.

A HUB gomb csak azoknál az itemeknél jelenik meg, amelyekhez külön HUB-link lett megadva.

Az azonos típusú, de különálló itemek saját receptgombot és saját HUB-hivatkozást kapnak. Például az M5A Cannon és az M6A Cannon két külön itemként szerepel.

### Haladás követése

Minden alapanyagnál külön „Kitermelve” jelölőnégyzet található.

A finomítandó anyagoknál külön „Finomítóba beadva” jelölés is használható.

A helyszínkártya folyamatosan mutatja:

* az elkészült feladatok számát;
* az összes feladat számát;
* és azt, ha a teljes farmhely elkészült.

A teljesen kész kártyák külön vizuális állapotot kapnak.

A jelölések automatikusan elmentődnek a böngésző helyi tárhelyében.

Az adatok nem kerülnek külön szerverre vagy felhasználói fiókba.

A „Jelölések törlése” gomb megerősítés után törli az összes helyben elmentett haladást.

### Szöveg kijelölése és másolása

Az oldal szövegei kijelölhetők és vágólapra másolhatók.

Ez vonatkozik többek között:

* az itemnevekre;
* az alapanyagokra;
* a helyszínekre;
* a radarértékekre;
* a finomítókra;
* a bónuszokra;
* és a megjegyzésekre.

A receptgombokon és más kezelőfelületi elemeken megjelenő szöveg is kijelölhető, ahol azt a böngésző működése lehetővé teszi.

### Reszponzív felület

A felület asztali számítógépen, laptopon, tableten és mobiltelefonon is használható.

Kisebb kijelzőn:

* a szűrők egymás alá rendeződnek;
* a receptgombok kevesebb oszlopban jelennek meg;
* a farmkártyák egyoszlopos elrendezésre váltanak;
* a blueprint találati ablak mobilbarát formát kap.

## Felhasznált adatforrások

### SCMDB

Az eredeti mining adatbázis alapjául szolgáló információk az SCMDB PTU Mining Database alapján kerültek a projektbe.

Ide tartoznak:

* mining helyszínek;
* alapanyag-előfordulási arányok;
* radar signature alapértékek;
* radarértékekhez tartozó színkódok;
* mining típusok és klaszteradatok.

Forrás:

SCMDB PTU Mining Database

A jelenlegi HTML-fájl nem tartalmaz SCMDB-ről átvett képeket.

### UEX Corporation

A finomítói helyszínek és yield-bónuszok a UEX Corporation refinery adatbázisa alapján kerültek meghatározásra.

Ahol a UEX nem közöl külön állomásspecifikus bónuszt, a program ezt egyértelműen jelzi, és nem ad meg feltételezett legjobb finomítót.

Forrás:

[UEX Refinery Database](https://uexcorp.space/mining/refineries)

### Star Citizen Wiki API

A blueprintok, craftolható itemek, ingredient kapcsolatok, API game versionök és közvetlen blueprint hivatkozások ellenőrzéséhez a Star Citizen Wiki API szolgáltatását használjuk.

Forrás:

[Star Citizen Wiki Blueprints](https://api.star-citizen.wiki/blueprints)

### Közösségi HUB-oldalak

Egyes itemekhez külön közösségi HUB assignment link tartozik.

Ezek a hivatkozások manuálisan vannak az itemnevekhez rendelve. Nem a Star Citizen Wiki API generálja őket.

## Használat

1. Töltsd le a HTML-fájlt.

2. Nyisd meg egy modern böngészőben, például Chrome, Edge vagy Firefox alatt.

3. Használd a keresőt, ha egy konkrét helyszínt, alapanyagot vagy finomítót keresel.

4. A rendszerszűrővel válaszd ki Stantont, Pyrót vagy Nyxet.

5. A rendszer fejlécére kattintva csukd össze vagy nyisd ki az adott rendszer farmhelyeit.

6. Nyisd ki a „Mit szeretnél legyártani?” receptszűrőt.

7. Jelölj ki egy vagy több receptet.

8. A program csak a kijelölt receptekhez szükséges alapanyagokat és farmhelyeket fogja megjeleníteni.

9. Egy kijelölt receptre újra kattintva eltávolíthatod azt a szűrésből.

10. Az alapanyag nevére kattintva ellenőrizheted, mely kiválasztott blueprint itemekhez szükséges.

11. A „BP wiki megnyitása” gombbal közvetlenül megnyithatod az adott blueprint Wiki-oldalát.

12. A külön HUB felirattal rendelkező itemeknél a HUB-oldal új böngészőlapon nyitható meg.

13. A „Kitermelve” és „Finomítóba beadva” jelölésekkel kövesd a haladást.

14. A „Minden mutatása” gombbal állítsd vissza a teljes listát.

15. A „Jelölések törlése” gombbal törölheted az összes elmentett haladást.

A blueprintadatok betöltéséhez és a külső HUB-oldalak megnyitásához internetkapcsolat szükséges.

## Miért készült?

A cél az volt, hogy ne kelljen egyszerre több külön weboldalt, képet, táblázatot és jegyzetet nézni.

A segéd egyetlen felületen mutatja meg:

* hova kell menni;
* milyen alapanyag található ott;
* milyen előfordulási arányra lehet számítani;
* milyen radarjelet kell keresni;
* mekkora klaszter tartozhat a jelhez;
* hova érdemes vinni finomítani;
* milyen finomítási bónusz érhető el;
* mely blueprint itemekhez szükséges az anyag;
* mely receptek alapanyagait kell együtt összegyűjteni;
* és mely közösségi HUB-oldal tartozik az adott itemhez.

## Korlátozások

A segéd csak a projektben előre megadott itemeket és alapanyagokat ellenőrzi.

A blueprint kapcsolatokat a Star Citizen Wiki API aktuálisan elérhető adatai alapján állapítja meg.

Ha egy item vagy recept hiányzik az API-ból, az eredmény hiányos lehet.

A mining helyszínek, előfordulási arányok, radarjelek, receptek és finomítói bónuszok Star Citizen frissítései során megváltozhatnak.

A statikus adatok nem frissülnek automatikusan a HTML-fájlban. Ezeket új patch vagy adatváltozás után kézzel kell ellenőrizni és frissíteni.

## Jogi és forrásmegjelölési nyilatkozat

Ez egy rajongói, közösségi projekt.

A projekt nem áll hivatalos kapcsolatban a Cloud Imperium Games, a Roberts Space Industries, az SCMDB, a UEX Corporation vagy a Star Citizen Wiki üzemeltetőivel.

A Star Citizen név, a játékhoz tartozó védjegyek, játékadatok és grafikai elemek a megfelelő jogtulajdonosok tulajdonát képezik.

A projekt nem állítja, hogy az SCMDB, a UEX Corporation vagy a Star Citizen Wiki adatai a projekt saját tulajdonát képeznék.

A repository saját forráskódjára vonatkozó licenc nem terjed ki automatikusan a külső forrásból származó:

* játékadatokra;
* adatbázis-tartalmakra;
* API-adatokra;
* képekre;
* logókra;
* védjegyekre;
* vagy külső weboldalak tartalmára.

A projektben szereplő HUB-hivatkozások kizárólag külső oldalakra mutató linkek. A linkelt oldal tartalmát és elérhetőségét a segéd nem kezeli és nem garantálja.

Az adatok a Star Citizen frissítései miatt megváltozhatnak. A projekt ezért nem garantálja, hogy minden információ mindig teljesen aktuális, teljes vagy hibamentes.

Szerzői jogi, eltávolítási vagy adatjavítási kérés esetén kérlek, nyiss egy GitHub issue-t.

---

# Star Citizen Mining, Refinery and Blueprint Helper

## English description

This is a free, non-commercial Star Citizen community helper that brings together the information required for locating, identifying, refining, and using selected mining resources in blueprint recipes.

The application runs as a single HTML file. It does not require installation, a separate server, a database, or a user account.

Mining locations, resources, radar signatures, and refinery data are stored directly in the HTML file. An internet connection is required to check blueprint recipes and open external HUB pages.

## Main features

### Resource farming cards

Resources are displayed on separate cards grouped by mining location.

Each location card displays:

* the star system;
* the exact mining location;
* the resources available there;
* the maximum or listed occurrence rate;
* the mining type;
* radar signature information;
* the recommended refinery;
* the available refinery yield bonus;
* and explanatory notes related to the data.

The tool distinguishes between ship mining, ROC or vehicle mining, and FPS mining resources.

### Grouping by star system

Farming locations are grouped by star system.

The current system list includes:

* Stanton;
* Pyro;
* Nyx.

Each system section can be collapsed and expanded independently.

The system header also shows how many farming locations are currently displayed in that system.

The “Show all” button:

* clears the search field;
* resets the system and progress filters;
* clears all recipe selections;
* restores the complete resource list;
* and expands every system section.

### Search and filtering

The search field can match mining locations, star systems, resource names, and refinery names.

The system filter can display:

* all systems;
* Stanton only;
* Pyro only;
* Nyx only.

The progress filter can display:

* all farming cards;
* only cards with unfinished tasks;
* only fully completed cards.

### Radar signature data

Every supported resource has its own radar signature information.

The radar section displays:

* the base radar signature;
* the mining type;
* the related color code;
* the possible cluster size;
* the minimum and maximum cluster signature;
* and information about how intermediate values are calculated.

For smaller ship-mining clusters, the tool can display the consecutive radar values.

For larger FPS or ROC clusters, it displays the individual base signature, the minimum cluster signature, and the maximum cluster signature.

If the source provides only a base signature but no cluster size, the interface explicitly states that the cluster value is not listed. The tool does not invent unverified values.

### Refinery information

Each refinable resource displays:

* the recommended refinery station;
* the system containing that refinery;
* the available yield bonus;
* and any equal-value alternatives.

Resources without a station-specific yield bonus in the current UEX refinery data are clearly marked.

In these cases, the tool does not invent a “best refinery.”

A separate refinery summary is shown at the bottom of the page. It displays:

* which resources should be taken to the same refinery;
* how many resources are assigned to each refinery;
* the available yield bonuses;
* and cases where another refinery provides an equal bonus.

The refinery data in the current HTML version was rechecked against UEX Star Citizen 4.9 data on July 22, 2026.

### Recipe filter

The recipe filter starts collapsed by default.

When expanded, recipes are displayed in an evenly arranged multi-row grid. The interface does not use a horizontal scrollbar.

Recipe buttons adapt to the available screen width and remain readable on desktop and mobile devices.

Clicking a recipe displays only the resources and farming locations required for that item.

Clicking the same selected recipe again removes the selection.

Multiple recipes can be selected at the same time.

When several recipes are selected, the tool displays the combined list of resources required for all selected items.

Duplicate resources are automatically merged. If several selected recipes require the same resource, that resource appears only once in the farming route.

When every recipe is deselected, the complete resource list is restored automatically.

The “All recipes / all resources” button clears every recipe selection at once.

### Blueprint API checks

Recipe filtering and resource-to-blueprint relationships are checked through the Star Citizen Wiki Blueprint API.

The application:

* retrieves available game versions;
* can check several API versions;
* searches for the blueprint items listed in the project;
* checks their ingredient lists;
* and uses the available version that contains the highest number of requested items.

If the API does not return one or more items, the interface clearly reports that the result may be incomplete.

An incomplete API result is not treated as proof that a resource is not required by any item.

### Finding blueprints from a resource

Resource names are clickable.

Clicking a resource opens a modal window showing:

* which selected blueprint items require that resource;
* how many confirmed recipe relationships were found;
* the ingredient name returned by the API;
* the API game version used for the result;
* and how many requested items were successfully found.

Each matching blueprint includes a separate “Open BP wiki” link.

The related Star Citizen Wiki blueprint page opens in a new browser tab.

### HUB links

Some recipe buttons contain a separate clickable “HUB” label in their upper-right corner.

The HUB label:

* works independently from the recipe button;
* does not enable or disable recipe filtering;
* opens the manually assigned HUB page for that item;
* and opens it in a new browser tab.

The HUB label is only shown for items that have an assigned HUB URL.

Similar but separate items receive their own recipe buttons and their own HUB links. For example, the M5A Cannon and M6A Cannon are handled as two separate items.

### Progress tracking

Each resource has a separate “Mined” checkbox.

Refinable resources also include a separate “Submitted to refinery” checkbox.

Each location card continuously displays:

* the number of completed tasks;
* the total number of tasks;
* and whether the entire location is complete.

Completed cards receive a separate visual state.

Progress is automatically stored in the browser’s local storage.

The progress data is not uploaded to a server or user account.

The “Clear progress” button removes all locally stored progress after confirmation.

### Text selection and copying

Text displayed on the page can be selected and copied to the clipboard.

This includes:

* item names;
* resource names;
* locations;
* radar signature values;
* refinery names;
* bonuses;
* and notes.

Text shown on recipe buttons and other interface elements can also be selected where permitted by normal browser behavior.

### Responsive interface

The interface works on desktop computers, laptops, tablets, and mobile phones.

On smaller screens:

* filters are arranged vertically;
* recipe buttons use fewer columns;
* farming cards switch to a single-column layout;
* the blueprint result window receives a mobile-friendly layout.

## Data sources

### SCMDB

The original mining dataset used by the project is based on the SCMDB PTU Mining Database.

This includes:

* mining locations;
* resource occurrence rates;
* base radar signatures;
* radar signature color coding;
* mining types and cluster information.

Source:

SCMDB PTU Mining Database

The current HTML file does not contain images copied from SCMDB.

### UEX Corporation

Refinery locations and yield bonuses are based on the UEX Corporation refinery database.

When UEX does not list a station-specific bonus for a resource, the application explicitly reports this instead of assigning an assumed best refinery.

Source:

[UEX Refinery Database](https://uexcorp.space/mining/refineries)

### Star Citizen Wiki API

Blueprints, craftable items, ingredient relationships, API game versions, and direct blueprint links are checked through the Star Citizen Wiki API.

Source:

[Star Citizen Wiki Blueprints](https://api.star-citizen.wiki/blueprints)

### Community HUB pages

Some items have manually assigned community HUB assignment links.

These links are matched to item names manually. They are not generated by the Star Citizen Wiki API.

## Usage

1. Download the HTML file.

2. Open it in a modern browser such as Chrome, Edge, or Firefox.

3. Use the search field to find a specific location, resource, or refinery.

4. Use the system filter to select Stanton, Pyro, or Nyx.

5. Click a system header to collapse or expand its farming locations.

6. Expand the “What do you want to craft?” recipe filter.

7. Select one or more recipes.

8. The application will display only the resources and farming locations required for the selected recipes.

9. Click a selected recipe again to remove it from the filter.

10. Click a resource name to check which selected blueprint items require it.

11. Use the “Open BP wiki” button to open the relevant blueprint Wiki page.

12. Items with a separate HUB label can open their assigned HUB page in a new browser tab.

13. Use the “Mined” and “Submitted to refinery” checkboxes to track progress.

14. Use “Show all” to restore the complete list.

15. Use “Clear progress” to remove all locally saved progress.

An internet connection is required to load blueprint data and open external HUB pages.

## Why was it created?

The goal was to avoid having to check several different websites, images, spreadsheets, and notes at the same time.

The tool shows in one place:

* where to go;
* which resources are available there;
* what occurrence rate can be expected;
* which radar signature to search for;
* what cluster size may belong to that signature;
* where the material should be refined;
* which refinery yield bonus is available;
* which blueprint items require the resource;
* which recipe resources should be collected together;
* and which community HUB page belongs to an item.

## Limitations

The helper checks only the items and resources predefined in the project.

Blueprint relationships are determined using the currently available Star Citizen Wiki API data.

If an item or recipe is missing from the API, the result may be incomplete.

Mining locations, occurrence rates, radar signatures, recipes, and refinery bonuses may change between Star Citizen updates.

Static data stored in the HTML file is not updated automatically. It must be manually reviewed and updated after relevant game patches or data changes.

## Legal and attribution notice

This is a fan-made community project.

This project is not officially affiliated with Cloud Imperium Games, Roberts Space Industries, SCMDB, UEX Corporation, or the Star Citizen Wiki team.

The Star Citizen name, game-related trademarks, game data, and graphical assets belong to their respective owners.

The project does not claim ownership of data originating from SCMDB, UEX Corporation, or Star Citizen Wiki.

Any license applied to the original source code of this repository does not automatically cover externally sourced:

* game data;
* database content;
* API data;
* images;
* logos;
* trademarks;
* or external website content.

HUB links included in the project are links to external pages only. The helper does not control or guarantee the content or availability of linked pages.

Star Citizen data may change between game updates. The project therefore cannot guarantee that all information will always remain current, complete, or error-free.

For copyright, removal, or data correction requests, please open a GitHub issue.
