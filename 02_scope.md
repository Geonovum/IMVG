# Scope

<mark>[Inleidende tekst ... ]</mark>

## Scope
Dit document beschrijft de dataspecificatie van de Landelijke Informatievoorziening Vastgoedgebruik. Hierin worden de structuur, inhoud, data-inwinning en datakwaliteit van de Landelijke Informatievoorziening Vastgoedgebruik gedetailleerd uiteen gezet. De dataspecificatie dient daarmee als basis voor de realisatie en ontsluiting van verschillende dataservices.

De Landelijke Informatievoorziening Vastgoedgebruik beschrijft het gebruik van al het formeel geregistreerde vastgoed op het Nederlandse grondgebied (vasteland) op een uniforme manier.

De kern van de LIV bestaat uit de koppeling van een viertal basisregistraties <mark>[verder toelichten]</mark>
* Basisregistratie Adressen en Gebouwen (BAG);
* Basisregistratie Waardering Onderoerende Zaken (WOZ);
* Nationaal Handelsregister (NHR);
* Basisregistratie Personen (BRP);

#### Gebruik
De informatievoorziening richt zich in eerste instantie op het vaststellen en classificeren van administratief gebruik. In de eerste versie van de voorziening gaat de aandachti uit naar administratief niet-in-gebruik, ofwel: leegstand.

Gaat om verblijfsobjecten en panden, maar lig- en standplaatsen worden buiten beschouwing gelaten.

De koppeling tussen bovenstaande registraties geeft inzicht in het administratieve gebruik op het niveau van een verblijfsobject (BAG). Als er op een adres in de BAG geen gebruiker, geen vestiging en/of geen persoon geregistreerd staat, is er sprake van administratieve leegstand. 

#### Formele registratie
Met formeel geregistreerd bedoelen we in dit geval de informatie over het gebruik van vastgoedobjecten zoals die is vastgelegd in de eerdergenoemde basisregistraties.

#### Integrale benadering
Een speerpunt van deze aanpak is de aandacht voor een integraal inzicht in leegstand en gebruik. Dat wil zeggen dat de volledige vastgoedpopulatie wordt meegenomen. Bestaande inforamtievoorzieningen richten zich vaak op een specifiek deel van het vastgoed, bijvoorbeeld kantoren of winkels. Met name vanuit het perspectief van (administratieve) leegstand is het relevant om de problematiek vanuit een integraal oogpunt te beschouwen. Namelijk: een object is niet in gebruik in de functie waarvoor het een vergunning heeft (BAG), of waarvoor het het laatst gebruikt is. Dit kan mede de reden zijn dat het leegstaat. Bovendien zijn vastgoedobjecten onderling aan elkaar gerelateerd en niet slechts binnen een categorie. <!-- Dit kan een stuk duidelijker geformuleerd worden-->

#### Uniformering van de werkwijze
In het  verlengde van een integrale benadering, ligt een uniforme benadering. Hoewel er verschillende partijen zijn die naar het gebruik van vastgoed kijken en daarover publiceren, is er onderling geen consencus over de belangrijkste <!-- inzichten/afspraken/uitkomsten/opvattingen-->. Daarom is er vanuit een brede groep partijen de wens geuit om hierover afspraken te maken. Welke categorieën onderscheiden we? Volgens welke methodiek stellen we gebruik vast? Op basis van welke bronnen? etc.

#### Dataproducten <!-- andere titel: ~functionaliteiten? -->
Al deze informatie wordt vervolgens door verschillende dataproducten aangeroepen. 
* Jaarlijkse statistiek CBS
* Tussenproduct
* Objectniveau gemeenten
* Remote Access CBS

<!-- Dit document beschrijft de dataspecificatie, IMKL2015, van het door KLIC ontsloten dataproduct
Utiliteitsnetten.

IMKL2015 geeft de gedetailleerde beschrijving van structuur, inhoud en datakwaliteit van utiliteitsnetten
en dient als basis voor de realisatie en ontsluiting van KLIC services.

De gebruikstoepassing waar de semantiek van IMKL2015 door wordt bepaald komt voort uit verschillende
wetgevingen, regelingen en processen. <hier iets vergelijkbaars opnemen over basisregistraties en kaders m.b.t. gebruik?

Deze zijn:
WION: Wet Informatie-uitwisseling Ondergrondse Netten. Uitwisseling van kabel en leiding
informatie ter voorkoming van graafschade voor de netten: telecom, riolering, water, elektriciteit,
gas en warmte

INSPIRE: Europese richtlijn voor uitwisseling van digitale gegevens gerelateerd aan milieu. Voor
deze specificatie in het bijzonder het thema Utilities en Governmental Services en daarin de Utility
Networks. Dataspecificaties voor uitwisseling kabel en leidingen informatie voor de netten:
datatransport, riolering, water, elektriciteit, gas, warmte en andere kabels & leidingen.

Besluit externe veiligheid buisleidingen (BevB): Besluit houdende milieukwaliteitseisen
externe veiligheid voor het vervoer van gevaarlijke stoffen door buisleidingen. Onder andere
opname van buisleidingen met gevaarlijke inhoud (Bgi) (en beperkingen op ruimtegebruik) in een
bestemmings- of inpassingsplan.

Register risicosituaties gevaarlijke stoffen (RRGS) Verplichting tot invoeren risico’s van
gevaarlijke stoffen in een landelijk risicoregister.

De volgende gebruikstoepassing is nog niet operationeel in IMKL2015 verwerkt.
Er is voor nu nog een onvoldoende beschreven toepassing. Er is wel al een experimenteel diagram toegevoegd om de gedachte
te bepalen.

EC61 (COM 147) EU richtlijn voor een Verordening van het Europees Parlement en Raad over
maatregelen om de kosten van de aanleg van elektronische hogesnelheidscommunicatienetwerken
te verlagen.-->