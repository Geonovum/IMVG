# Data content en structuur

## Inleiding
<!--IMKL 2015 bevat dit kopje extra t.o.v. template-->
[<mark>Structuur zoals in onderstaande alinea's besproken nog ter discussie</mark>]
De volgende paragrafen beschrijven de inhoud en structuur van het IMVG met behulp van UML-diagrammen en bijbehorende objectcatalogus.

De verschillende uitwisselingsprocessen BAG, WOZ, NHR en BRP worden slechts in zoverre in dit document behandelt, daar waar zij afwijken van hetgeen reeds in de betreffende eigen documentatie is opgenomen. Deze worden in aparte paragrafen behandeld. Dit resulteert in vier deelmodellen: 

- IMVG-Gebruik[<mark>werktitel</mark>]
- IMVG-BAG
- IMVG-WOZ
- IMVG-NHR
- IMVG-BRP

Als eerste geeft dit hoofdstuk een algemene beschrijving aan de hand van het referentiemodel IMVG. 

Vervolgens wordt dieper ingegaan op de gedetailleerde technische kant van het informatiemodel. 

Het eerste gedeelte van dit hoofdstuk bevat de UML-diagrammen van het referentiemodel, het volledige model en de deelmodellen. Objecten, attributen, datatypen en relaties tussen objecten beschrijven eenduidig, schematisch en *in full detail* de inhoudelijke informatie van het informatiemodel. Elke deelparagraaf geeft een toelichting op een deelmodel. De deelparagraaf bevat tevens een compleet diagram van het deelmodel. Indien een onderwerp een aparte toelichting nodig heeft, wordt dit aangeduid met de kop 'Extra toelichting'.

Het tweede gedeelte van dit hoofdstuk bevat de objectcatalogus met ain tabelvorm dezelfde infroamtie al de diagrammen, maar nu met taal beschreven. Alle informatie-elementen zijn daarbij voorzien van definities en waar nodig een toelichting. De objectcatalogus bevat de gezamenlijke informatie-inhoud van alle deelmodellen. De objectcatalogus maakt dus geen apart onderscheidt tussen de deelmodellen.

## Algemene uitgangspunten
<!--IMKL2015 bevat dit kopje niet t.o.v. template-->

## UML-diagrammen

### Beschrijving algemeen

<figure>
	<table style="width: 100%" cellpadding="10" valign="top">
		<col width="30%">
		<col width="20%">
		<col width="50%">
		<tr>
			<th>Stereotype</th>
			<th>Modelelement</th>
			<th>Beschrijving</th>
		</tr>
		<tr>
			<td>txt</td>
			<td>txt</td>
			<td>txt</td>
		<tr>
			<td>txt</td>
			<td>txt</td>
			<td>txt</td>
		<tr>
			<td>txt</td>
			<td>txt</td>
			<td>txt</td>
		<tr>
			<td>txt</td>
			<td>txt</td>
			<td>txt</td>
		<tr>
			<td>txt</td>
			<td>txt</td>
			<td>txt</td>
		<tr>
			<td>txt</td>
			<td>txt</td>
			<td>txt</td>
		<tr>
			<td>txt</td>
			<td>txt</td>
			<td>txt</td>		
	</table>
	<figcaption> - <mark>Gebruikte stereotypen vanuit het KKG UML profiel (MIM)</mark></figcaption>
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

Voeg je de uitkomsten uit de bovenstaande BAG-koppelingen samen, dan zijn er verschillende combinaties mogelijk (zie: <mark>figuur 4</mark>). Indien vanuit geen van de drie bronnen een indicatie van gebruik is, beschouwen we het object als administratief leeg (combinatie 8). In de overige gevallen gaat het informatiemodel uit van gebruik (combinatie 1-7).

<figure>
	<a target="_blank" href="images/tabel_leegstand_groot.png">
		<img src="images/tabel_leegstand_groot.png" alt="Combinaties gebruik basisregistraties" width="80%" class="img-responsive">
	</a>
	<figcaption> - Mogelijke combinaties gebruiksstatus IMVG (klik voor vergroting)</figcaption>
</figure>

### Overzicht

Onderstaande figuur toont een overzicht van het volledige Informatiemodel Vastgoedgebruik.

[<mark>Vastgoedobject in referentiemodel opnemen</mark>: pand is specialisatie van vastgoedobject] 

<figure>
	<a target="_blank" href="images/IMVG_informatiemodel.png">
		<img src="images/IMVG_informatiemodel.png" alt="Informatatiemodel IMVG" class="img-responsive">
	</a>
	<figcaption> - Informatiemodel IMVG (klik voor vergroting)</figcaption>
</figure>

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