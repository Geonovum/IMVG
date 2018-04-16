# Scope

<mark>[Inleidende tekst ... ]</mark>

<mark>TEST AFBEELDING</mark>

![figure 1-1](image_tabel_leegstand.png?raw=true)

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

De LIV bevat informatie over de gebruiksstatus van verblijfsobjecten en voor een deel van panden zonder verblijfsobjecten (bijv. schuren en stallen in het geval van agrarisch vastgoed). Stand- en ligplaatsen vallen buiten de scope van de informatievoorziening.

#### Formele registratie
Formeel geregistreerd betekent in dit geval de registratie van informatie over (het gebruik van) vastgoedobjecten zoals die is vastgelegd in de basisregistraties BAG, WOZ, NHR en BRP.

#### Vastgoed
Het vastgoed omvat in deze voorziening alle panden met verblijfsobjecten, aangevuld met een subselectie van panden die op een <mark>agrarisch erf</mark> vallen. <mark>Paragraaf 4.2 licht dit verder toe.</mark>

#### Integrale benadering
Een belangrijk onderdeel van deze aanpak is de nadruk op het integrale karakter van de voorziening. Dat wil zeggen dat de volledige vastgoedpopulatie wordt meegenomen. Bestaande informatievoorzieningen richten zich vaak op een specifiek deel van het vastgoed, bijvoorbeeld kantoren of winkels. Ondanks de voordelen die deze voorziening hebben voor de marktspecifieke informatiebehoefte, zijn er ook nadelen. Het blijkt lastig om informatie tussen deze voorziening uit te wisselen. En bovendien bestaat niet voor alle typen vastgoed een informatievoorziening.

Om verschillende redenen is het relevant gebleken om informatie over verschillende vastgoedtypen in een bepaald gebied aan elkaar te kunnen relateren <mark>[link naar eerdere rapport(en)]</mark>. Gemeenten en provincies zijn bijvoorbeeld verplicht de Ladder Duurzame Verstedelijking toe te passen in hun in ruimtelijke ordeningsvraagstukken. Hiermee ligt de behoefte aan integraal inzicht feitelijk verankerd in een wettelijk basis.

Het gebruik van een pand (vergund en feitelijk) zegt iets over (respectievelijk) het oorspronkelijke gebruiksdoel en het huidige gebruik. Als iets leegstaat kan het zijn dat het object leegstaat als gevolg van bijvoorbeeld overaanbod voro die specifieke functie, terwijl er aan andere functies misschien een tekort is. In zulke gevallen is het relevant om vraag en aanbod van ruimte integraal aan elkaar te relateren.

#### Uniformering van de werkwijze
In het  verlengde van een integrale benadering, ligt een uniforme benadering. Hoewel er verschillende partijen zijn die naar het gebruik van vastgoed kijken en daarover publiceren, is er onderling geen consensus over de methode en de definities. Daarom heeft  een brede groep partijen de wens geuit om hierover afspraken te maken. <mark>Wat verstaan we onder leegstand? Welke categorieën onderscheiden we? Volgens welke methodiek stellen we gebruik vast? Op basis van welke bronnen? etc. </mark>.

#### Dataproducten <!-- andere titel: ~functionaliteiten? -->
Al deze informatie wordt vervolgens door verschillende dataproducten aangeroepen. 
* Jaarlijkse statistiek CBS
* Tussenproduct
* Objectniveau gemeenten
* Remote Access CBS
