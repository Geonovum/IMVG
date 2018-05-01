# Data content en structuur
## Algemene uitgangspunten
## UML-diagrammen

### Beschrijving algemeen
Het IMVG maakt gebruik van het [<mark>bron:[stelsel van basisregistraties](https://www.digitaleoverheid.nl/voorzieningen/gegevens/inhoud-basisregistraties/stelselplaat/)</mark>]. Door de de WOZ, het NHR en de BRP aan de BAG te koppelen, is het mogelijk om een indicatie te geven adminstratieve gebruiksstatus van een vastgoedobject. De volgende paragraven geven een verdere uiwerking van de verschillende elementen van het IMVG. Eerst volgt een uiteenzetting van de globale structuur aan de hand van het referentiemodel IMVG.

#### Referentiemodel
Het Informatiemodel Vastgoedgebruik (IMVG) koppelt verschillende basisregistraties aan elkaar. Het doel en de structuur van deze bronnen bepalen in belangrijke mate de afbakening van het begrip *vastgoedgebruik*. Met andere woorden: het model geeft informatie over de *administratieve* gebruiksstatus van een verblijfsobject (zie: <a href="#informeleBeschrijving" title="Ga naar: Informele beschrijving">paragraaf 4.2</a>). Per bron leggen we hieronder kort uit wat de rol is in het informatiemodel. Tot slot wordt het object *LV-gebruik* kort uitgelegd.  

<figure>
	<a target="_blank" href="images/referentiemodel.png">
		<img src="images/referentiemodel.png" alt="Referentiemodel" class="img-responsive">
	</a>
	<figcaption> - Referentiemodel IMVG (klik voor vergroting)</figcaption>
</figure>

**BAG**
Het Informatiemodel Vastgoedgebruik stelt de BAG centraal. Deze basisregistratie bevat alle adressen en geometrieën van gebouwen in Nederland en voorziet ze van een unieke identificatiecode. De andere drie basisregsistraties verwijzen voor locatiegegevens naar de BAG op basis van die identificatiecode. Hierdoor is het mogelijk om informatie uit de andere bronnen rechtstreeks aan een BAG-locatie te koppelen. Dat geeft inzicht in de gebeurtenissen op een locatie; in dit geval het gebruik. Bovendien voorziet de BAG gebouwen van aanvullende informatie, zoals: bouwjaar (pand), gebruiksdoel en oppervlakte (verblijfsobject).

**BRP**

Woningen vormen het belangrijkste deel van de gebouwenvoorraad, [<mark>namelijk 80%</mark>]. De BRP legt van alle inwoners van Nederland het woonadres vast [<mark>bron: [Rijksoverheid BRP](https://www.rijksoverheid.nl/onderwerpen/privacy-en-persoonsgegevens/basisregistratie-personen-brp)</mark>]. Hiermee is het mogelijk om te zien of een woning in gebruik is. Heeft een woning tenminste één bewoner, dan bevat het BRP op die locatie een inschrijving. Het BRP verwijst voor het adres naar de BAG. Met andere woorden: koppelt de BAG aan de BRP, dan heeft het BAG-object een gebruiker.

**NHR**

De [<mark>overige 20%</mark>] van de gebouwenvoorraad bestaat uit niet-woningen (kantoren, winkels, scholen, etc.). Voor de aanwezigheid van activiteiten op deze locaties kan het Handelsregister geraadpleegd worden. Het Handelsregister registreert alle bedrijven, rechtspersonen en andere organisaties die deelnemen aan het economisch verkeer in Nederland [<mark>bron: [KvK](https://www.kvk.nl/over-de-kvk/over-het-handelsregister/)</mark>]. Op een vergelijkbare manier als met het BRP is voor de niet-woningen na te gaan of er op een locatie gebruik is. Vindt er op een locatie tenminste één economische activiteit plaats, dan bevat het NHR op die locatie tenminste één inschrijving. Voor de adresgegevens maakt het register een verwijzing naar de BAG. Daarom is de aanname: koppelt de BAG aan het NHR, dan heeft het BAG-object een gebruiker.

**WOZ**

Alle gegevens die nodig zijn om de WOZ-waarde te relateren aan zowel een onroerende zaak als aan een belanghebende, zijn ondergebracht in de basisregistratie WOZ [<mark>bron: [DigitaleOverheid](https://www.digitaleoverheid.nl/voorzieningen/gegevens/inhoud-basisregistraties/woz/)</mark>]. Voor de adressering van een onroerende zaak maakt de WOZ een koppeling met de BAG. Grofweg kent de WOZ twee typen belanghebbenden: een *eigenaar* of een *gebruiker*. Een WOZ-object heeft tenminste één eigenaar en geen of meerdere gebruikers. Soms is de eigenaar zelf gebruiker. Maar, als dat niet het geval is, kan het voorkomen dat een WOZ-object wel een eigenaar, maar geen gebruiker heeft.

De basisregistratie WOZ beslaat de totale vastgoedvoorraad (woningen en niet-woningen). Daardoor geeft het extra inzicht in het gebruik van zowel woningen [<mark>kanttekening?</mark>] als niet-woningen. Het afleiden van gebruik uit de WOZ, verschilt dus van de manier waarop dat met de BRP en het NHR gebeurt, want daar is de koppeling *an sich* de indicatie voor gebruik. <!-- WEGLATEN: dit heeft geen betrekking op de het informatieproduct, maar op de voorziening (LIV)-->Overigens komt het ook voor dat de WOZ geen uitsluitsel geeft óf dat de WOZ niet koppelt aan de BAG. Hier houdt de huidige versie van het IMVG nog geen rekening mee.

**Vastgoedgebruik**

Voeg je de uitkomsten uit de bovenstaande BAG-koppelingen samen, dan zijn er verschillende combinaties mogelijk (zie: figuur <mark>4</mark>). Indien vanuit geen van de drie bronnen een indicatie van gebruik is, beschouwen we het object als administratief leeg (combinatie 8). In de overige gevallen gaat het informatiemodel uit van gebruik (combinatie 1-7).

<figure>
	<a target="_blank" href="images/table_leegstand_large.png">
		<img src="images/table_leegstand_large.png" alt="Combinaties gebruik basisregistraties" width="80%" class="img-responsive">
	</a>
	<figcaption> - Mogelijke combinaties gebruiksstatus IMVG (klik voor vergroting)</figcaption>
</figure>

### Overzicht
### Verschillende onderdelen uit het UML-diagram
### Consistentie tussen datasets (<mark>optioneel</mark>)
### Identifier management
### Modellering van objectreferenties (<mark>optioneel</mark>)
### Geometrie representatie (<mark>optioneel</mark>)
### Tijdrepresentatie (<mark>optioneel</mark>)
## Objectcatalogus
### Objectencatalogus metadata
### Elementen die in de objectencatalogus gedefinieerd zijn (alfabetisch ordenen)
### Objecttypen
### Datatypen