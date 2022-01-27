# Case-API-Visualisering

***

Case modul 4 API

## Introduktion
I caset ska ni arbeta individuellt och skapa en webbsida som visualiserar data från API:er. Det ska vara en applikation som visualiserar data för restauranger i USA.

## API

### Documenu
https://documenu.com

Tjänsten är gratis att använda (upp till en viss gräns). Men den kan vi komma åt över 600000 Restauranger begränsat till USA. Ni behöver registrera er, och vi rekommenderar att ni gör det med GitHub. 

När du registrerat dig så finns din API-nyckel tillgänglig.

Gå sedan in på https://documenu.com/dashboard/apipreview för att se hur en request kan se ut. 

Exempel på *endpoints*:

#### GET Search Restaurang Geo
https://documenu.com/docs#get_search_restaurants_geo

Här hämtar API:et information om närliggande restauranger från en angiven punkt (longitud, latitud).

#### GET Search Restaurants
https://documenu.com/docs#get_search_restaurants

Här hämtar API:et information om restauranger från en ex stat, eller en zip code.


#### Tips
EFtersom man kan göra ett begränsat antal förfrågningar så bör ni spara ner en json respons och spara det som en lokal fil i er utvecklingsmiljö. När ni utvecklar kan ni ibland hämta verkliga data, och ibland data från en lokal fil. Ex:

```javascript
 let url; 
 // url = "https://api.documenu.com/v2/restaurants/search/geo?lat ...;
 url = "data.json";
```

## Wireframes - LoFi & HiFi -> Prototyp
Även om denna produkten ni skall skapa antagligen kommer vara enbart en vy så kommer det säkert finnas ett flöde (t ex filtrering).

Att ta fram:
- En LoFi-wireframe som förklarar strukturen och flödet (Valfritt)
- En HiFi-wireframe som förklarar strukturen och flödet (Figma)
- Prototyp i Figma med ett interaktivt flöde
- Ni får använda er av befintliga UI-kits, men sätt gärna er egen touch på det.

## Namngivningsprinciper när du kodar
- använd latinska tecken för variabelnamn och funktioner namngivna camelCase 
- skriv kommentarer i din kod
- skriv kod med indrag (indentation)

## Om koden i applikationen 
Applikationen får inte använda externa ramverk, utan det är "vanilla" JavaScript och CSS som gäller.
Dela upp struktur, innehåll, design och logik. Använd externa filer för CSS och JavaScript.


## Så börjar du
Skapa ett privat repo på GitHub och koppla det till din lokala utvecklingsmiljö. 
Under projektet - senast 1 februari bjuder du in dina lärare. Se Settings -> Manage access -> Add people

*Lägg till:*

- frozenbanana (Henry)
- andsju (Anders)
- addkolon (Mattias)


## Grundläggande krav

- I applikation ska en besökare kunna navigera efter närliggande resturanger. I API:et finns olika endpoints som gör det möjligt att söka, utifrån latidude och logitude
- Ett resultat ska presenteras och kunna filtreras efter någon valbar egenskap
- Appen ska utgå från mobile first. Dvs när ni utvecklar så antag viewport likt en iPhone 10


Utvecklingen av applikationen ska finnas dokumenterad på GitHub. Du ska ha gjort minst 10 commits under projektet.


## Utmaningar
(Förutom att applikationen uppfyller de grundläggande kraven ovan)

Här finns följande utmaningar. Anta en eller flera!

- Skapa en hjälpklass för en metod som fetch()
- Sidan ska även ha anpassad vy för skärm
- Skapa en extra vy  
- Spara ngn form av data i Local Storage
- Beräkna avstånd mellan två punkter baserade på latitude | longitude (se länk under resurser)
- En användare ska kunna klicka på en karta för att ange en utgångspunkt för närliggande restauranger
- Integrera en klickbar karta som ex **mapbox** https://www.mapbox.com. I dokumentationen över API:et kommer du kunna se hur kartan kan integreras på webbsidan.


![mapbox](/mapbox.png)


## Inlämning och redovisning
- Caset "lämnas in" (Gihub repo) den 14 februari. Ditt  räknas som inlämning
- Redovisning av caset är den 15 februari.

Vi vill den här gången att alla får ta del av varandras redovisning. Det innebär att ni behöver förbereda er på att redovisningen är kort - ca 5 minuter per person. Då visar ni (demonstrerar) er applikation genom att dela skärm. 

Förbered 5 minuters redovisning enligt följande mall:

I reovisningen ska du:
- demonstrera applikationen
- visa exempel på annan funktionalitet (ex ngn av utmaningarna)
- berätta vad du är mest nöjd med (design, kod, struktur...)
- berätta vad du skulle vilja att applikationen kan göra, men inte hunnit att koda
- Redovisningen sker i bokstavordning (efternamn)

## Handledning
Det kommer givetvis finnas möjlighet till handledning fram tills den 15 februari. I första hand är det under vanlig lektionstid.

## Resurser
- Kom igång med Documenu: https://documenu.com/docs#get_started
- Geocoding API playground: https://docs.mapbox.com/playground/geocoding/
- Dokumentation och genomgångar: https://glimnet.sharepoint.com/sites/Webbutvecklare2021/SitePages/Modul-4.aspx
- Fetch: https://github.com/thejsway/thejsway/blob/master/manuscript/chapter21.md
- Beräkna avstånd mellan två punkter baserade på latitude / longitude: https://www.movable-type.co.uk/scripts/latlong.html
