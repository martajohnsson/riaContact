Menage your artists and albums applikation
------------------------------------------------------------

Detta är en enkel javascript applikation byggd inom ramar för kursen RIA. 
Applikationen använder sig av följande bibliotek ()dessa fins i 
 js/lib/ katalogen):

-Backbone
   BackboneRelational
   Backbone.localStorage
- Underscore
- Require
   Order

------------------------------------------------------------
huvud filer
------------------------------------------------------------
index.html 
Laddar alla bibliotek som behövs genom att anropa js/main genom Require (bootstrap). Alla templates som behövs för applikatione finns i denna fil.

router.js
Denna filen ansvarar för att skapa initella vyer och grund funktionalitet.

main.js
Skapar alla förkortningar för använda bibliotek med hjälp av Require.js

app.js
Initierar applikationen och tillåter att: *When all of your Routers have been created, and all of the routes are set up properly, call Backbone.history.start() to begin monitoring hashchange events, and dispatching routes. *

------------------------------------------------------------
modeler:
------------------------------------------------------------

models/AlbumModel.js
Ett album objekt innehåller information om ett särskild album. 
Det är nördvändigt att ha en model av sina objekt.Filen innehåller validering för modelen.

models/ArtistModel.js
Ett artist objekt innehåller information om en särskild artist samt innehåller information om vilka relationer som finns mot album objektet samt validering av objektet.

------------------------------------------------------------
collections:
------------------------------------------------------------

collections/AlbumCollection.js
En collection/samling av alla album objekt

collections/ArtistCollection.js
En collection/samling av alla artist objekt
------------------------------------------------------------
vyer:
------------------------------------------------------------

views/main/index.js
Start view för hela applikationen. Innehåller referenser till artist och model collectioner.
Renderar artistCollection och tillhörande albums.
Filen använder sig av underscore för att utnyttja templating funktionalitet och gör möjligt att skapa formen för en ny album samt länkar till möjligheten för att lägga till en ny artist.

views/main/ArtistCollectionView.js
För varje artist som finns i artist collectionen skapar den en ny artistView (artist.js) vy

views/main/artist.js
Visar artistens namn och en lista med dess albums genom att skapa en ny vy: LibraryItemView (libraryItem.js). Används av ArtistCollectionView.js.

views/main/libraryItem.js
Ansvarar för att presentera ett enskilt album objekt för artisten. Används av artist.js

views/user/newArtist.js
Denna vy tillåter att skapa en ny Artist i vår collection

------------------------------------------------------------
Förslag för vidare utveckling
------------------------------------------------------------

1. Ta bort en artist (DONE)

2. Ta bort en album (DONE)

3. Uppdatera artist (DONE)

4. Uppdatera album (DONE)
------------------------------------------------------------
