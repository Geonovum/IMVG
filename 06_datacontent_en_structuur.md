# Data content en structuur

## Inleiding
<!--IMKL 2015 bevat dit kopje extra t.o.v. template-->
[<mark>Structuur zoals in onderstaande alinea's besproken nog ter discussie</mark>]
De volgende paragrafen beschrijven de inhoud en structuur van het IMVG met behulp van UML-diagrammen en bijbehorende objectcatalogus.

De verschillende uitwisselingsprocessen BAG, WOZ, NHR en BRP worden slechts in zoverre in dit document behandelt, daar waar zij afwijken van hetgeen reeds in de betreffende eigen documentatie is opgenomen. Deze worden in aparte paragrafen behandeld. Dit resulteert in vier deelmodellen: 

- IMVG-Gebruik [<mark>werktitel</mark>]
- IMVG-BAG
- IMVG-WOZ
- IMVG-NHR
- IMVG-BRP

Als eerste geeft dit hoofdstuk een algemene beschrijving aan de hand van het referentiemodel IMVG. 

Vervolgens gaat het hoofdstuk dieper in op de technische details van het informatiemodel. 

Het eerste gedeelte van dit hoofdstuk bevat de UML-diagrammen van het referentiemodel, het volledige model en de deelmodellen. Objecten, attributen, datatypen en relaties tussen objecten beschrijven eenduidig, schematisch en *in full detail* de inhoudelijke informatie van het informatiemodel. Elke deelparagraaf geeft een toelichting op een deelmodel. De deelparagraaf bevat tevens een compleet diagram van het deelmodel. Indien een onderwerp een aparte toelichting nodig heeft, wordt dit aangeduid met de kop 'Extra toelichting'.

Het tweede gedeelte van dit hoofdstuk bevat de objectcatalogus met ain tabelvorm dezelfde infroamtie al de diagrammen, maar nu met taal beschreven. Alle informatie-elementen zijn daarbij voorzien van definities en waar nodig een toelichting. De objectcatalogus bevat de gezamenlijke informatie-inhoud van alle deelmodellen. De objectcatalogus maakt dus geen apart onderscheidt tussen de deelmodellen.

## Algemene uitgangspunten
<!--IMKL2015 bevat dit kopje niet t.o.v. template-->

## UML-diagrammen

### Beschrijving algemeen

[<mark>Volgende zinnen plek geven in deze paragraaf</mark>]
> Het IMVG neemt van elk deelmodel (basisregistraties) slecht een deel van de inhoud over en voegt daar de spedifieke informatie an toe die nodig is vor de realisatie van de in de scope genoemde processen.

> "Met IMKL2015 kan daardoor een dataset geleverd worden of dataservice worden ingericht die
INSPIRE conform is en voorziet in het detail van de eisen van de genoemde processen."

[<mark>Onderstaande figuur invullen vanuit KKG/MIM</mark>]. Link naar document:
https://docs.geostandaarden.nl/mim/def-st-mim10-20170614

<!--use cellpadding="10" for more space around cell content-->
<figure>
	<table style="width: 100%" valign="top" border="1">
		<col width="20%">
		<col width="20%">
		<col width="60%">
		<tr>
			<th>Stereotype</th>
			<th>Modelelement</th>
			<th>Beschrijving</th>
		</tr>
		<tr>
			<td>Objecttype</td>
			<td>UML-Class</td>
			<td>De typering van een groep objecten (in de werkelijkheid) die binnen een domein relevant zijn en als gelijksoortig worden beschouwd.</td>
		</tr>
		<tr>
			<td>Attribuutsoort</td>
			<td>UML-Property</td>
			<td>De typering van gelijksoortige gegevens die voor een objecttype van toepassing is.</td>
		</tr>
		<tr>
			<td>Gegevensgroep</td>
			<td>UML-Property</td>
			<td>Een typering van een groep van gelijksoortige gegevens die voor een objecttype van toepassing is.</td>
		</tr>
		<tr>
			<td>Gegevensgroeptype</td>
			<td>UML-Class</td>
			<td>Een groep van met elkaar samenhangende attribuutsoorten. Een gegevensgroeptype is altijd een type van een gegevensgroep.</td>
		</tr>
		<tr>
			<td>Generalisatie</td>
			<td>UML-generalization</td>
			<td>De typering van het hiërarchische verband tussen een meer generiek object van een objecttype en een meer specifiek object van een ander objecttype waarbij het laatstgenoemde object eigenschappen van het eerstgenoemde object overerft.</td>
		</tr>
		<tr>
			<td>Relatiesoort</td>
			<td>UML-association</td>
			<td>De typering van het structurele verband tussen een object van een objecttype en een (ander) object van een ander (of hetzelfde) objecttype.</td>
		</tr>
		<tr>
			<td>Relatieklasse</td>
			<td>UML-associationClass</td>
			<td>Een relatiesoort met eigenschappen.</td>
		</tr>
		<tr>
			<td>Externe koppeling</td>
			<td>UML-association</td>
			<td>Een associatie waarmee vanuit het perspectief van het eigen informatiemodel een objecttype uit het ‘eigen’ informatiemodel gekoppeld wordt aan een objecttype van een extern informatiemodel. De relatie zelf hoort bij het ‘eigen’ objecttype.</td>
		</tr>
		<tr>
			<td>Relatierol</td>
			<td>UML-Property</td>
			<td>De benaming van de manier waarop een object deelneemt aan een relatie met een ander object.</td>
		</tr>
		<tr>
			<td>Referentielijst</td>
			<td>UML-Datatype</td>
			<td>Een lijst met een opsomming van de mogelijke domeinwaarden van een attribuutsoort, die buiten het model in een externe waardenlijst worden beheerd. De domeinwaarden in de lijst kunnen in de loop van de tijd aangepast, uitgebreid, of verwijderd worden, zonder dat het informatiemodel aangepast wordt (in tegenstelling tot bij een enumeratie).</td>
		</tr>		
		<tr>
			<td>Referentie element</td>
			<td>UML-Property</td>
			<td>Een eigenschap van een object in een referentielijst in de vorm van een gegeven.</td>
		</tr>
		<tr>
			<td>Enumeratie</td>
			<td>UML-enumeration</td>
			<td>Een datatype waarvan de mogelijke waarden limitatief zijn opgesomd in een statische lijst.</td>
		</tr>
		<tr>
			<td>Enumeratiewaarde</td>
			<td>UML-enumerationLiteral</td>
			<td>Een gedefinieerde waarde, in de vorm van een eenmalig vastgesteld constant gegeven.</td>
		</tr>
		<tr>
			<td>Stereotype «Codelist»</td>
			<td>UML-datatype</td>
			<td>De definitie van een codelist is gelijk aan de definitie van een referentielijst.</td>
		</tr>
		<tr>
			<td>Primitief datatype</td>
			<td>UML-PrimitiveType</td>
			<td>Een in het eigen model gedefinieerd primitieve datatype. Deze worden wel door de modelleur gecreëerd, met een eigen naam en een eigen definitie (en eigen metagegevens).</td>
		</tr>
		<tr>
			<td>Gestructureerd datatype</td>
			<td>UML-property</td>
			<td>Specifiek benoemd gestructureerd datatype dat de structuur van een gegeven beschrijft, samengesteld uit minimaal twee elementen.</td>
		</tr>
		<tr>
			<td>Data element</td>
			<td>UML-property</td>
			<td>Een onderdeel/element van een Gestructureerd datatype die als type een datatype heeft.</td>
		</tr>
		<tr>
			<td>Union</td>
			<td>UML-datatype</td>
			<td>Gestructureerd datatype, waarmee wordt aangegeven dat er meer dan één mogelijkheid is voor het datatype van een attribuut. Het attribuut zelf krijgt als datatype de union. De union biedt een keuze uit verschillende datatypes, elk afzonderlijk beschreven in een union element.</td>
		</tr>		
		<tr>
			<td>Union element</td>
			<td>UML-property</td>
			<td>Een type dat gebruikt kan worden voor het attribuut zoals beschreven in de definitie van Union. Het union element is een onderdeel van een Union, uitgedrukt in een eigenschap (attribute) van een union, die als keuze binnen de Union is gerepresenteerd.</td>
		</tr>
		<tr>
			<td>Extern</td>
			<td>UML-package</td>
			<td>Een groepering van constructies die een externe instantie beheert en beschikbaar stelt aan een informatiemodel en die in het informatiemodel ongewijzigd gebruikt worden.</td>
		</tr>		
		<tr>
			<td>View</td>
			<td>UML-package</td>
			<td>Een groepering van objecttypen die gespecificeerd zijn in een extern informatiemodel en vanuit het perspectief van het eigen informatiemodel inzicht geeft welke gegevens van deze objecttypen relevant zijn binnen het eigen informatiemodel.</td>
		</tr>
		<tr>
			<td>Id</td>
			<td>UML-property</td>
			<td>Aanduiding dat de relatiesoort waarop de «id» is gedefinieerd een onderdeel is van de unieke aanduiding van een objecttype.</td>
		</tr>		
		<tr>
			<td>Constraint</td>
			<td>UML-Constraint</td>
			<td>Een constraint is een conditie of een beperking, die over een of meerdere modelelementen uit het informatiemodel geldt.</td>
		</tr>			
	</table>
	<figcaption> - <mark>Gebruikte stereotypen vanuit het KKG UML-profiel (MIM)</mark></figcaption>
</figure>

Het IMVG maakt gebruik van het <a target="_blank" href="https://www.digitaleoverheid.nl/voorzieningen/gegevens/inhoud-basisregistraties/stelselplaat/">stelsel van basisregistraties</a> (zie: <mark>figuur 4</mark>). IMVG is gemodelleerd als de koppeling van de modellen van de basisregistraties WOZ, NHR, BRP aan het model van de BAG. Door deze koppeling ontstaat extra informatie over het administratieve gebruik en andere eigenschappen van een verblijfsobject in de BAG. De volgende paragrafen geven een verdere uiwerking van de verschillende elementen van het IMVG. Eerst volgt een uiteenzetting van de globale structuur aan de hand van het referentiemodel IMVG.

<figure>
	<a target="_blank" href="https://upload.wikimedia.org/wikipedia/commons/8/8f/Stelsel_van_Basisregistraties.png">
		<img src="https://upload.wikimedia.org/wikipedia/commons/8/8f/Stelsel_van_Basisregistraties.png" alt="Stelselplaat" class="img-responsive">
	</a>
	<figcaption> - Stelsel van Basisregistraties: stelselplaat (klik voor vergroting)</figcaption>
</figure>

**Referentiemodel**

Het Informatiemodel Vastgoedgebruik (IMVG) koppelt verschillende basisregistraties aan elkaar (zie: <mark>figuur 5</mark>). Het doel en de structuur van deze bronnen bepalen in belangrijke mate de afbakening van het begrip *vastgoedgebruik*. Met andere woorden: het model geeft informatie over de *administratieve* gebruiksstatus van een verblijfsobject (zie: <a href="#informeleBeschrijving" title="Ga naar: Informele beschrijving">paragraaf 4.2</a>). Per bron leggen we hieronder kort uit wat de rol is in het informatiemodel. Tot slot wordt het object *LV-gebruik* kort uitgelegd.

[<mark>Vastgoedobject in referentiemodel opnemen</mark>: pand is specialisatie van vastgoedobject]  

<figure>
	<a target="_blank" href="images/IMVG_referentiemodel.png">
		<img src="images/IMVG_referentiemodel.png" alt="Referentiemodel IMVG" class="img-responsive">
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

Voeg je de uitkomsten uit de bovenstaande BAG-koppelingen samen, dan zijn er verschillende combinaties mogelijk (zie: <mark>figuur 4</mark>). Indien vanuit geen van de drie bronnen een indicatie van gebruik is, geldt het object als administratief leeg (combinatie 8). In de overige gevallen gaat het informatiemodel uit van gebruik (combinatie 1-7).

<figure>
	<a target="_blank" href="images/tabel_leegstand_groot.png">
		<img src="images/tabel_leegstand_groot.png" alt="Combinaties gebruik basisregistraties" width="80%" class="img-responsive">
	</a>
	<figcaption> - Mogelijke combinaties gebruiksstatus IMVG (klik voor vergroting)</figcaption>
</figure>

### Overzicht

<mark>Onderstaande figuur toont een overzicht van het volledige Informatiemodel Vastgoedgebruik.</mark>

Het onderstaand UML diagram bevat het complete IMVG, inclusief de relatie met de basisregistraties BAG, WOZ, NHR en BRP. De volgende paragrafen lichten telkens een deel van het diagram toe.

<figure>
	<a target="_blank" href="images/IMVG_informatiemodel.png">
		<img src="images/IMVG_informatiemodel.png" alt="Informatatiemodel IMVG" class="img-responsive">
	</a>
	<figcaption> - Informatiemodel IMVG (klik voor vergroting)</figcaption>
</figure>

[<mark>Vastgoedobject in referentiemodel opnemen</mark>: pand is specialisatie van vastgoedobject] 

<figure>
	<table style="width: 100%" cellpadding="10" border="1">
	<col width="15%">
	<col width="85%">
		<tr>
			<th>Kleur</th>
			<th>Uitleg</th>
		</tr>
		<tr>
			<td>Groen</td>
			<td>Landelijke Voorziening Waarde Onroerende Zaken</td>
		</tr>		
		<tr>
			<td>Blauw</td>
			<td>Informatiemodel Vastgoedgebruik</td>
		</tr>
		<tr>
			<td>Oranje</td>
			<td>Landelijke Voorziening Basisregistratie Adressen en Gebouwen</td>
		</tr>
		<tr>
			<td>Paars</td>
			<td>Basisregistratie Nationaal Handelsregister</td>
		</tr>
		<tr>
			<td>Roze</td>
			<td>Basisregistratie Personen/Gemeentelijke Basisadministratie</td>
		</tr>
	</table>
	<figcaption> - Kleurgebruik in UML diagrammen</figcaption>
</figure>

Dataverkeer [<mark>Nog opnemen? Lijkt nu (nog) niet relevant.</mark>]

Het UML-diagram toont de informatie die nodig is voor de indicatie van administratief vastgoedgebruik. Ook bevat het model alle gegevens uit de basisregistraties BAG, WOZ, NHR en BRP die vastgoedobject van relevante extra kenmerken voorziet (bijv. aantal vierkante meters in gebruik of leegstaand). Daarom zijn in het model ook de relaties met (delen van) deze basisregistraties opgenomen in het model. Aan de linkerkant bevindt zich de IMVG view op het informatiemodel van de LV WOZ (groen). Het deelmodel rechtsboven geeft in de IMVG view op de LV BAG weer (oranje). Rechtsonder toont de IMVG view op de NHR (paars). Het deelmodel middenboven geeft gestalte aan de IMVG view op het BRP/GBA. <mark>De kern van het model is het object in het midden (blauw): Vastgoedgebruik, dat wordt gegenereerd op het koppelvlak van de vier basisregistraties</mark>. Het IMVG objecttype Vastgoedgebruik koppelt de verschillende basisregistraties aan elkaar op basis van het objecttype Verblijfsobject dat in alle basisregistraties aanwezig is. Met andere woorden: het verblijfsobject fungeert als koppelsleutel. <mark>Voor de leesbaarheid zijn datatypen, gegevensgroepen en waardelijsten niet het overzicht opgenomen (waar wel?)</mark>.

De objecten in de koppelingslaag (Vastgoedgebruik, Verblijfsobject en Pand) vormen gezamenlijk de centrale objecten van de IMVG dataset. Via overwerving en relaties worden alle voor het model relevantie eigenschappen toegevoegd vanuit de basisregistraties. Vastgoedgebruik is een specialisatie van Verblijfsobject. Het verblijfsobject heeft weer een relatie met een pand. Een pand bevat de geometrie van een gebouw. Hierdoor is het mogelijk administratief gebruik (en dus ook leegstand) van de tot een pand behorende verblijfsobjecten op gebouwniveau weer te geven op een kaart.

**Waardelijsten**

De als datatype «codeList» opgenomen waardelijsten in de IMVG-view op de basisregistraties worden niet in het UML beheerd, maar in externe waardelijsten. Deze waardelijsten behoren toe aan andere bronhouders en worden derhalve niet binnen het IMVG en vallen daarmee buiten de scope van dit model.

### Verschillende onderdelen uit het UML-diagram
<!--### Consistentie tussen datasets (<mark>optioneel</mark>)-->
### Identifier management
<!--### Modellering van objectreferenties (<mark>optioneel</mark>)-->
<!--### Geometrie representatie (<mark>optioneel</mark>)-->
<!--### Tijdrepresentatie (<mark>optioneel</mark>)-->
## Objectcatalogus
### Objectencatalogus metadata
### Elementen die in de objectencatalogus gedefinieerd zijn (alfabetisch ordenen)
### Objecttypen
### Datatypen