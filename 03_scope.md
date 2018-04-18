# Scope

<mark>[Inleidende tekst ... ]</mark>

## Scope
Dit document beschrijft de dataspecificatie van de Landelijke Informatievoorziening Vastgoedgebruik. Hierin worden de structuur, inhoud, data-inwinning en datakwaliteit van de Landelijke Informatievoorziening Vastgoedgebruik gedetailleerd uiteengezet. De dataspecificatie dient daarmee als basis voor de realisatie en ontsluiting van verschillende dataservices.

De Landelijke Informatievoorziening Vastgoedgebruik beschrijft het *gebruik* van al het *formeel geregistreerde vastgoed* op het Nederlandse grondgebied (vasteland) op een uniforme manier.

De kern van de LIV bestaat uit de koppeling van een viertal basisregistraties 

* Basisregistratie Adressen en Gebouwen (BAG);
* Basisregistratie Waardering Onderoerende Zaken (WOZ);
* Nationaal Handelsregister (NHR);
* Basisregistratie Personen (BRP);

Een toelichting op de koppeling vindt plaats in [<mark>paragraaf 3.1.6</mark>].

#### Gebruik
De informatievoorziening richt zich in eerste instantie op het vaststellen en classificeren van administratief gebruik. In de eerste versie van de voorziening gaat de aandacht uit naar dat deel van de gebouwenvoorraad dat administratief *niet* in gebruik is, ofwel: administratieve leegstand.

De koppeling tussen basisregistraties geeft inzicht in het administratieve gebruik op het niveau van een verblijfsobject (BAG). Een afgeleide hiervan is administratieve leegstand. Hiervan is volgens de methodiek sprake als er op een adres in de BAG *geen gebruiker* (WOZ), *geen vestiging* (NHR) en/of *geen persoon* (BRP) geregistreerd staat ([<mark>zie ook: 3.1.6</mark>]).

De LIV bevat informatie over de gebruiksstatus van verblijfsobjecten en voor een deel van panden zonder verblijfsobjecten (bijv. schuren en stallen in het geval van agrarisch vastgoed). Stand- en ligplaatsen vallen buiten de scope van de informatievoorziening.

#### Formele registratie
Formeel geregistreerd betekent in dit geval de registratie van informatie over (het gebruik van) vastgoedobjecten zoals die is vastgelegd in de basisregistraties BAG, WOZ, NHR en BRP.

#### Vastgoed
Het vastgoed omvat in deze voorziening alle panden met verblijfsobjecten, <mark>aangevuld met een subselectie van panden die op een agrarisch erf vallen</mark>. <mark>Paragraaf 4.2 licht dit verder toe</mark>.

#### Integrale benadering
Een belangrijk onderdeel van deze aanpak is de nadruk op het integrale karakter van de voorziening. Dat wil zeggen dat de volledige vastgoedpopulatie wordt meegenomen. Bestaande informatievoorzieningen richten zich vaak op een specifiek deel van het vastgoed, bijvoorbeeld kantoren of winkels. Ondanks de voordelen die deze voorziening hebben voor de marktspecifieke informatiebehoefte, zijn er ook nadelen. Het blijkt lastig om informatie tussen deze voorziening uit te wisselen. En bovendien bestaat niet voor alle typen vastgoed een informatievoorziening.

Om verschillende redenen is het relevant gebleken om informatie over verschillende vastgoedtypen in een bepaald gebied aan elkaar te kunnen relateren <mark>[link naar eerdere rapport(en)]</mark>. Gemeenten en provincies zijn bijvoorbeeld verplicht de Ladder Duurzame Verstedelijking toe te passen in hun in ruimtelijke ordeningsvraagstukken. Hiermee ligt de behoefte aan integraal inzicht feitelijk verankerd in een wettelijk basis.

Het gebruik van een pand (zowel vergund als feitelijk) zegt respectievelijk iets over het oorspronkelijke gebruiksdoel en het huidige gebruik. Als iets leegstaat kan het zijn dat het object leegstaat als gevolg van bijvoorbeeld overaanbod voor die specifieke functie, terwijl er aan andere functies misschien een tekort is. In zulke gevallen is het relevant om vraag en aanbod van ruimte integraal aan elkaar te relateren.

#### Uniformering van de werkwijze
In het verlengde van een integrale benadering, ligt een uniforme benadering. Hoewel er verschillende partijen zijn die naar het gebruik van vastgoed kijken en daarover publiceren, is er onderling geen consensus over de methode en de definities. Daarom heeft een brede groep partijen de wens geuit om hierover afspraken te maken. Een informatiestanddaard is zo'n afspraak. Daarom leggen we hierin de beginselen van de LIV vast.

#### Referentiemodel
De LIV koppelt verschillende basisregistraties aan elkaar om een indiciatie van het vastgoedgebruik op een locatie te kunnen geven. In [<mark>paragraaf 3.1.1 **gebruik**</mark>] werd die methodiek al kort toegelicht. De leegstand die volgt uit deze aanpak, noemen we administratieve leegstand. Deze paragraaf licht de methode verder toe. 

De LIV maakt gebruik van het [<mark>bron:[stelsel van basisregistraties](https://www.digitaleoverheid.nl/voorzieningen/gegevens/inhoud-basisregistraties/stelselplaat/)</mark>]. Voor het bepalen van gebruik van vastgoed komen de BAG, WOZ, NHR en BRP in aanmerking. Deze registraties kunnen een indicatie geven over de gebruiksstatus van een vastgoedobject. In de LIV staat de BAG centraal. Deze basisregistratie bevat alle adressen en geometrieën van gebouwen in Nederland en voorziet ze van een unieke identificatiecode.

**Figuur x.x: Referentiemodel LIV**
![referentiemodel](images/referentiemodel.png?raw=true)

De andere drie basisregsistraties verwijzen voor locatiegegevens naar de BAG op basis van die identificatiecode. Hierdoor is het mogelijk om informatie uit de andere bronnen rechtstreeks aan een BAG-locatie te koppelen. Dat geeft inzicht in de gebeurtenissen op een locatie. Bovendien voorziet de BAG het gebouwen van aanvullende informatie, zoals: bouwjaar (pand), gebruiksdoel en oppervlakte (verblijfsobject). [<mark>zie gedetailleerdere uitleg onder 4.2</mark>]

Woningen vormen het belangrijkste deel van de gebouwenvoorraad, [<mark>namelijk 80%</mark>]. De BRP legt van alle inwoners van Nederland het woonadres vast [<mark>bron: [Rijksoverheid BRP](https://www.rijksoverheid.nl/onderwerpen/privacy-en-persoonsgegevens/basisregistratie-personen-brp)</mark>]. Hiermee is het mogelijk om te zien of een woning in gebruik is: heeft een woning een tenminste één bewoner, dan staat deze ingeschreven in het BRP. Het BRP verwijst voor het adres naar de BAG. Met andere woorden: koppelt de BAG aan de BRP, dan heeft het BAG-object een gebruiker.

De [<mark>overige 20%</mark>] van de gebouwenvoorraad bestaat uit niet-woningen (kantoren, winkels, scholen, etc.). Het Handelsregister registreert alle bedrijven, rechtspersonen en andere organisaties die deelnemen aan het economisch verkeer in Nederland [<mark>bron: [KvK](https://www.kvk.nl/over-de-kvk/over-het-handelsregister/)</mark>]. Op een vergelijkbare manier als met het BRP is voor de niet-woningen na te gaan of er op een locatie gebruik is: vindt er op een locatie tenminste één economische activiteit plaats, dan staat deze ingeschreven in het NHR. Voor de adresgegevens maakt het register een verwijzing naar de BAG. Daarom is de aanname: koppelt de BAG aan het NHR, dan heeft het BAG-object een gebruiker.

Alle gegevens die nodig zijn om de WOZ-waarde te relateren aan zowel een onroerende zaak als aan een belanghebende zijn opgenomen in de basisregistratie WOZ [<mark>bron: [DigitaleOverheid](https://www.digitaleoverheid.nl/voorzieningen/gegevens/inhoud-basisregistraties/woz/)</mark>]. Voor de adressering van een onroerende zaak maakt de WOZ een koppeling met de BAG.
Grofweg kent de WOZ twee typen belanghebbenden: een *eigenaar* of een *gebruiker*. Een WOZ-object kan meerdere eigenaren en meerdere gebruikers hebben. Een WOZ-object heeft tenminste één eigenaar. Soms is die eigenaar zelf gebruiker. Maar, het komt ook voor dat eigenaar en gebruiker verschillende personen zijn. In dat geval kan het voorkomen dat een WOZ-object wel een eigenaar, maar geen gebruiker heeft omdat de eigenaar op dat moment geen huurder heeft. De basisregistratie WOZ beslaat de totale vastgoedvoorraad. Daardoor geeft het extra inzicht in het gebruik van zowel woningen [<mark>kanttekening?</mark>] als niet-woningen. het afleiden van gebruik uit de WOZ, verschilt dus van de manier waarop dat met de BRP en het NHR gebeurt, want daar is de koppeling zelf de indicatie voor gebruik. 

Voeg je de uitkomsten uit de bovenstaande BAG-koppelingen samen, dan zijn er verschillende combinaties mogelijk [<mark>verwijzing tabel onder 3.1.1</mark>]. Indien vanuit geen van de drie bronnen een indicatie van gebruik is, beschouwen we het object als administratief leeg [<mark>tabel</mark>].

**Tabel x.x: Mogelijke combinaties LIV**
![LIV-combinaties](images/table_leegstand_large.png?raw=true)

#### Dataproducten/Functionaliteiten <!-- andere titel: ~functionaliteiten? -->
Al deze informatie wordt vervolgens door verschillende dataproducten aangeroepen: 
* Jaarlijkse statistiek CBS
* Tussenproduct
* Objectniveau gemeenten
* Remote Access CBS