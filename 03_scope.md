# Scope

<mark>[Inleidende tekst ... ]</mark>

## Scope
Dit document beschrijft de dataspecificatie van de Landelijke Informatievoorziening Vastgoedgebruik. Hierin worden de structuur, inhoud, data-inwinning en datakwaliteit van de Landelijke Informatievoorziening Vastgoedgebruik gedetailleerd uiteengezet. De dataspecificatie dient daarmee als basis voor de realisatie en ontsluiting van verschillende dataservices.

De Landelijke Informatievoorziening Vastgoedgebruik beschrijft het *gebruik* van al het *formeel geregistreerde vastgoed* op het Nederlandse grondgebied (vasteland) op een uniforme manier.

De kern van de LIV bestaat uit de koppeling van een viertal basisregistraties <mark>[verder toelichten]</mark>
* Basisregistratie Adressen en Gebouwen (BAG);
* Basisregistratie Waardering Onderoerende Zaken (WOZ);
* Nationaal Handelsregister (NHR);
* Basisregistratie Personen (BRP);

#### Gebruik
De informatievoorziening richt zich in eerste instantie op het vaststellen en classificeren van administratief gebruik. In de eerste versie van de voorziening gaat de aandacht uit naar dat deel van de gebouwenvoorraad dat administratief *niet* in gebruik is, ofwel: leegstaat.

De koppeling tussen basisregistraties geeft inzicht in het administratieve gebruik op het niveau van een verblijfsobject (BAG). Een afgeleide hiervan is administratieve leegstand. Hiervan is volgens de methodiek sprake als er op een adres in de BAG *geen gebruiker* (WOZ), *geen vestiging* (NHR) en/of *geen persoon* (BRP) geregistreerd staat, is er sprake van administratieve leegstand.

[<mark>Verwijzing opnemen - voor verdere uitleg zie: referentiemodel (onderstaande tabel daar naartoe verplaatsen)</mark>]

![LIV-combinaties](images/table_leegstand_large.png?raw=true)

De LIV bevat informatie over de gebruiksstatus van verblijfsobjecten en voor een deel van panden zonder verblijfsobjecten (bijv. schuren en stallen in het geval van agrarisch vastgoed). Stand- en ligplaatsen vallen buiten de scope van de informatievoorziening.

#### Formele registratie
Formeel geregistreerd betekent in dit geval de registratie van informatie over (het gebruik van) vastgoedobjecten zoals die is vastgelegd in de basisregistraties BAG, WOZ, NHR en BRP.

#### Vastgoed
Het vastgoed omvat in deze voorziening alle panden met verblijfsobjecten, aangevuld met een subselectie van panden die op een <mark>agrarisch erf</mark> vallen. <mark>Paragraaf 4.2 licht dit verder toe.</mark>

#### Integrale benadering
Een belangrijk onderdeel van deze aanpak is de nadruk op het integrale karakter van de voorziening. Dat wil zeggen dat de volledige vastgoedpopulatie wordt meegenomen. Bestaande informatievoorzieningen richten zich vaak op een specifiek deel van het vastgoed, bijvoorbeeld kantoren of winkels. Ondanks de voordelen die deze voorziening hebben voor de marktspecifieke informatiebehoefte, zijn er ook nadelen. Het blijkt lastig om informatie tussen deze voorziening uit te wisselen. En bovendien bestaat niet voor alle typen vastgoed een informatievoorziening.

Om verschillende redenen is het relevant gebleken om informatie over verschillende vastgoedtypen in een bepaald gebied aan elkaar te kunnen relateren <mark>[link naar eerdere rapport(en)]</mark>. Gemeenten en provincies zijn bijvoorbeeld verplicht de Ladder Duurzame Verstedelijking toe te passen in hun in ruimtelijke ordeningsvraagstukken. Hiermee ligt de behoefte aan integraal inzicht feitelijk verankerd in een wettelijk basis.

Het gebruik van een pand (vergund en feitelijk) zegt respectievelijk iets over het oorspronkelijke gebruiksdoel en het huidige gebruik. Als iets leegstaat kan het zijn dat het object leegstaat als gevolg van bijvoorbeeld overaanbod voor die specifieke functie, terwijl er aan andere functies misschien een tekort is. In zulke gevallen is het relevant om vraag en aanbod van ruimte integraal aan elkaar te relateren.

#### Uniformering van de werkwijze
In het  verlengde van een integrale benadering, ligt een uniforme benadering. Hoewel er verschillende partijen zijn die naar het gebruik van vastgoed kijken en daarover publiceren, is er onderling geen consensus over de methode en de definities. Daarom heeft een brede groep partijen de wens geuit om hierover afspraken te maken.

#### Referentiemodel
Een informatiestanddaard is zo'n afspraak. Daarom leggen we hierin de beginselen van de LIV vast. In [<mark>referentie naar paragraaf</mark>] werd de methodiek al kort toegelicht. De LIV koppelt verschillende basisregistraties aan elkaar om een indiciatie van het gebruik op een locatie te kunnen geven. Hieronder lichten we die methodiek verder toe. 

De leegstand die volgt uit die koppeling, noemen we administratieve leegstand. 

De LIV maakt gebruik van het stelsel van basisregistraties. Dit is [<mark>beschrijving stelsel, bron zoeken</mark>]. Voor het bepalen van gebruik van vastgoed komen de BAG, WOZ, NHR en BRP in aanmerking.

In de LIV staat de BAG centraal. Deze basisadministratie bevat alle adressen en geometrieën van gebouwen in Nederland en voorziet ze van een unieke identificatiecode. Ook bevat deze registratie aanvullende informatie over het object, zoals: bouwjaar, gebruiksdoel en oppervlakte.

<mark>nog iets over verblijfsobjecten en panden</mark>

De andere drie basisregsistraties verwijzen voor locatiegegevens naar de BAG op basis van de identificatiecode. Dit biedt de mogelijkheid om informatie uit de andere bronnen rechtstreeks aan een BAG-locatie te koppelen. Dat geeft inzicht in de gebeurtenissen op die locatie. 

Woningen vormen het belangrijkste deel van de gebouwenvoorraad, [<mark>namelijk 80%</mark>]. De BRP legt van alle inwoners van Nederland het woonadres vast (https://www.rijksoverheid.nl/onderwerpen/privacy-en-persoonsgegevens/basisregistratie-personen-brp). Hiermee is het mogelijk om te zien of een woning in gebruik is: heeft een woning een tenminste één bewoner, dan staat deze ingeschreven in het BRP. Het BRP verwijst voor het adres naar de BAG. Met andere woorden: koppelt de BAG aan de BRP, dan heeft het BAG-object een gebruiker.

De [<mark>overige 20%</mark>] van de gebouwenvoorraad bestaat uit niet-woningen (kantoren, winkels, scholen, etc.). Het Handelsregister registreert alle bedrijven, rechtspersonen en andere organisaties die deelnemen aan het economisch verkeer in Nederland (https://www.kvk.nl/over-de-kvk/over-het-handelsregister/). Op een vergelijkbare manier als met het BRP is voor de niet-woningen na te gaan of er op een locatie gebruik is: vindt er op een locatie tenminste één economische activiteit plaats, dan staat deze ingeschreven in het NHR. Voor de adresgegevens maakt het register een verwijzing naar de BAG. Daarom is de aanname: koppelt de BAG aan het NHR, dan heeft het BAG-object een gebruiker.

Alle gegeven sdie nodig zijn om de WOZ-waarde te relateren aan zowel een onroerende zaak als aan een belanghebende zijn opgenomen in de basisregistratie WOZ. Voor de onroerende zaak met de WOZ een koppeling met de BAG. 
Grofweg kent de WOZ twee typen belanghebbenden: een eigenaar of een gebruiker. Een WOZ-object kan meerdere eigenaren en meerdere gebruikers hebben. Een WOZ-object heeft altijd een eigenaar. Soms is die eigenaar zelf gebruiker. Maar het komt ook voor dat eigenaar en gebruiker verschillende personen zijn. In dat geval kan het voorkomen dat een WOZ-object wel een eigenaar, maar geen gebruiker heeft, omdat de eigenaar op dat moment gene huurder heeft. De WOZ beslaat de totale vastgoedvoorraad. Op deze manier geeft de WOZ extra inzicht in gebruik van zowel woningen als niet-woningen [<mark>hier kanttekening maken?</mark>]. Deze methode is verschilt dus van BRP en NHR: daar de koppeling de indicatie voor gebruik; de WOZ bevat zelf een gegeven over gebruik. 

Voeg je de uitkomsten uit de bovenstaande BAG-koppelingen samen, dan zijn er verschillende combinaties mogelijk [<mark>verwijzing tabel</mark>]. Indien vanuit geen van de drie bronnen een indicatie van gebruik is, beschouwen we het object als administratief leeg [<mark>tabel</mark>].

![referentiemodel](images/referentiemodel.png?raw=true)

##### Wat verstaan we onder leegstand? 
(zie 3.1.1 Gebruik)
##### Welke categorieën onderscheiden we?
(zie: afbeelding)
##### Volgens welke methodiek stellen we gebruik vast?
(zie: combinatie van voorgenoemde)
##### Op basis van welke bronnen? etc.
(zie afbeelding)

#### Dataproducten <!-- andere titel: ~functionaliteiten? -->
Al deze informatie wordt vervolgens door verschillende dataproducten aangeroepen. 
* Jaarlijkse statistiek CBS
* Tussenproduct
* Objectniveau gemeenten
* Remote Access CBS