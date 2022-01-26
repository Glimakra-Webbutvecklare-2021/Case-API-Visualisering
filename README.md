# Case-API-Visualisering

***

Case modul 4 API

## Introduktion
I caset ska ni arbeta individuellt och skapa en webbsida som visualiserar data från API:er. Det ska vara en applikation som visualiserar data för restauranger i USA.

## API:er

### Documenu
https://documenu.com

Tjänsten är gratis att använda (upp till en viss gräns). Men den kan vi komma åt över 600000 Restauranger begränsat till USA. Ni behöver registrera er, och vi rekommenderar att ni gör det med GitHub.
Gå sedan in på https://documenu.com/dashboard/apipreview för att se hur en request kan se ut. 

En bra *endpoint*  är **GET Search Restaurang Geo** för er restaurang vy.

https://documenu.com/docs#get_search_restaurants_geo

Under era kontouppgifter hittar ni er API-nyckel.

API:et kan hämta närmaste restauranger från en angiven punkt (longitud, latitud).

#### Tips
EFtersom man kan göra ett begränsat antal förfrågningar så bör ni spara ner en json respons och spara det som en lokal fil i er utvecklingsmiljö. När ni utvecklar kan ni ibland hämta verkliga data, och ibland data från en lokal fil. Ex:

```javascript
 let url; 
 // url = "https://api.documenu.com/v2/restaurants/search/geo?lat ...;
 url = "data.json";
```

### mapbox
https://www.mapbox.com

![mapbox](/mapbox.png)

Tjänsten kan användas efter att man registrerar sig på https://account.mapbox.com/auth/signup/
https://account.mapbox.com/auth/signup/

I dokumentationen över API:et kommer du kunna se hur kartan kan integreras på webbsidan.


## Utforma en designskiss
Genom papper eller annat medium beskriv hur restaurangvyn ska se ut. Desginvalen inkluderar men är inte begränsade till:
- font
- färgpalett
- ikoner och bilder

## Namngivningsprinciper när du kodar
- använd latinska tecken för variabelnamn och funktioner
- använd förklarande namn, namngivna camelCase
- skriv kommentarer i din kod
- skriv kod med indrag (indentation)

## Om koden i applikationen 
Applikationen får inte använda externa ramverk, utan det är vanilla JavaScript och CSS som gäller.
Dela upp struktur, innehåll, design och logik. Använd externa filer för CSS och JavaScript.


## Så börjar du
Skapa ett privat repo på GitHub och koppla det till din lokala utvecklingsmiljö (Visual Studio Code). Under projektet - senast 1 februari bjuder du in dina lärare. Se Settings -> Manage access -> Add people

*Lägg till:*

- frozenbanana (Henry)
- andsju (Anders)
- addkolon (Mattias)


## Grundläggande krav

- I applikation ska en besökare kunna navigera efter närliggande resturanger 
- Ett resultat ska presenteras och kunna filtreras efter någon valbar egenskap
- Appen ska utgå från mobile first. Dvs när ni utvecklar så antag viewport likt en iPhone 10
- En bild av en karta (ej klickbar för koordinater) 

Utvecklingen av applikationen ska finnas dokumenterad på GitHub. Du ska ha gjort minst 10 commits under projektet.


## Utmaningar
(Förutom att applikationen uppfyller de grundläggande kraven ovan)

Här finns följande utmaningar. Anta en eller flera!

- Skapa en hjälpklass för en metod som fetch()
- Sidan ska även ha anpassad vy för skärm
- En användare ska kunna klicka på kartan för att ange en utgångspunkt för närliggande restauranger 
- Spara ngn form av data i Local Storage
- Beräkna avstånd mellan två punkter baserade på latitude | longitude (se länk under resurser)
- ..ngt som du tycker 

## Inlämning och redovisning
- Caset lämnas in den 14 februari
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
