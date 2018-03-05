# Overview

Dit hoofdstuk geeft een overzicht van de <mark>[invullen]</mark>

## Naam en Acroniemen
* Dataspecificatie voor dataproduct Landelijke Informatievoorziening Vastgoedgebruik
* LIV2018 - Dataspecificatie voor vastgoedgebruiksinformatie

<!--Doelstelling
Het doel is om in februari 2018 te komen tot een nieuwe landelijke monitor leegstand 2.0, waarin de bevindingen van diverse plausibiliteitsonderzoeken zo veel mogelijk zijn verwerkt. Tevens wordt een processtandaard opgeleverd, gepubliceerd en in beheer genomen. Verder wordt de mogelijke dienstverlening aan partijen inzichtelijk gemaakt.-->

## Informele beschrijving

### Definitie

<!--
BAG
NHR
WOZ
BRP

*[LIV]: Landelijke Informatievoorziening Vastgoedgebruik
*[BAG]: Basisregistratie Adressen en Gebouwen
*[NHR]: Nationaal Handelsregister (basisregistratie)
*[WOZ]: Waardering Onroerende Zaken (basisregistratie)
*[BRP]: Basisregistratie Personen
-->


**Vastgoedobject**
*bag pand/vbo*

**Administratief gebruik en niet-gebruik (leegstand)**
*Er is niet een algemene concensus over wat de definitie van leegstand is*

**Vastgoedgebruik**
*het (administratief?) in gebruik zijn van een pand o.i.d.*

**Verblijfsobject**
*de kleinste binnen één of meer panden gelegen en voor woon-, bedrijfsmatige, of recreatieve doeleinden geschikte eenheid van gebruik die ontsloten wordt via een eigen afsluitbare toegang vanaf de openbare weg, een erf of een gedeelde verkeersruimte, onderwerp kan zijn van goederenrechtelijke rechtshandelingen en in functioneel opzicht zelfstandig is*
<mark>Verwijzing</mark> [link](http://example.com).<!--(Wet basisregistraties adressen en gebouwen, artikel 1, lid q)-->

**Pand**
*de kleinste bij de totstandkoming functioneel en bouwkundig-constructief zelfstandige eenheid die direct en duurzaam met de aarde is verbonden en betreedbaar en afsluitbaar is* 
<!-- (Wet basisregistraties adressen en gebouwen, artikel 1, lid o)-->
**Adresseerbaar object**
*(ligplaats, standplaats of verblijfsobject)*

**BAG-object**
*De BAG is op­ge­bouwd uit de vol­gen­de soor­ten ob­ject­ty­pen: woon­plaats, open­ba­re ruim­te, num­mer­aan­dui­ding, stand­plaats, lig­plaats, ver­blijfs­ob­ject, pand* <!-- bron: https://www.amsterdam.nl/stelselpedia/woordenboek/ -->

 > **<mark>Note:</mark>** definities aanvullen en fine-tunen
 

### Beschrijving
LIV2018 vormt het gemeenschappelijke begrippenkader voor de uitwisseling van informatie over vastgoedobjecten. De totale verzameling van vastgoedobjecten in Nederland vormt de gebouwenvoorraad. Deze bestaat onder andere uit woningen, winkels, kantoren, scholen, ziekenhuizen, fabrieken, winkels en sportfaciliteiten. 

In Nederland registreert de overheid "*alle met "gebouwen" samenhangende objecten*" in de Basisregistratie Adressen en Gebouwen (BAG). Deze objecten zijn afgebakend en voorzien van een unieke aanduiding. De BAG onderscheidt de volgende vier objecten en legt hiervan de gegevens vast. 
- Panden
- Verblijfsobjecten
- Standplaatsen
- Ligplaatsen

<!-- BAG-2009-2014_objectenhandboek -->

<!-- **Note:** hierop aanvullen dat voor LIV *standplaatsen* en *ligplaatsten* niet meegenomen worden. Is het logisch dat we deze niet meenemen? Ja: want geen gebruiksfunctie? Nee, want soms wel gebruiksfunctie
Uit: BAG_2009-2014_objectenhandboek - *Daarnaast bevat de basisregistratie gebouwen (permanente) ligplaatsen van woonboten en (permanente) standplaatsen van woonwagens.* -->

<!--Op een rij:
elke stand- en ligplaats is een pand in de BAG
verblijfsobjecten, stand- en ligplaatsen zijn adresseerbare objecten -->

<!-- alinea herschrijven -->
Opvallend is dat het object "gebouw" in deze registratie niet voorkomt. De definitie sloot onvoldoende aan op de gewenste toepassing van een gebouwenregistratie. In plaats daarvan is het object **pand** gedefinieerd.
<!-- BAG-2009-2014_objectenhandboek -->



<!-- alinea herschrijven -->
"*Binnen het gegevensmodel van de basisregistratie gebouwen wordt onderscheid gemaakt tussen (kleinste) bouwkundige eenheden en (kleinste) gebruikseenheden. **Panden** zijn gedefinieerd als de **(kleinste) bouwkundige eenheden**; **verblijfsobjecten** als de **(kleinste) gebruikseenheden**. Bij de afbakening van panden en verblijfsobjecten wordt aan dit onderscheid vastgehouden: de afbakening van een pand vindt plaats **onafhankelijk** van de afbakening van verblijfsobjecten. Dit neemt natuurlijk niet weg dat er wel **relaties** bestaan tussen beide objecten. Verblijfsobjecten maken altijd deel uit van een pand  of van meerdere panden). **Panden hoeven geen verblijfsobjecten te bevatten***".<!-- BAG-2009-2014_objectenhandboek --> 

**Vastgoed- en verblijfsobjecten**
Voor de definitie van een **vastgoedobject**, maakt de LIV gebruik van de definitie van een pand in de BAG. Een **pand** is daarin omschreven als de "*kleinste bij de totstandkoming functioneel en bouwkundig-constructief zelfstandige eenheid die direct en duurzaam met de aarde is verbonden en betreedbaar en afsluitbaar is*"<!-- bron BAG_2009_catalogus_grondslagen -->.

Een pand kan geen of meerdere verblijfsobjecten bevatten. Een **verblijfsobject** is:
*"kleinste binnen één of meer panden gelegen en voor woon-, bedrijfsmatige, of recreatieve doeleinden geschikte eenheid van gebruik die ontsloten wordt via een eigen afsluitbare toegang vanaf de openbare weg, een erf of een gedeelde verkeersruimte, onderwerp kan zijn van goederenrechtelijke rechtshandelingen en in functioneel opzicht zelfstandig is"*<!-- bron BAG_2009_catalogus_grondslagen -->. 

Met name het criterium van **functionele zelfstandigheid** heeft belangrijke consequenties voor informatie over vastgoedgebruik. Niet elk pand heeft één (of meerdere) verblijfsobject(en); sommige gebouwen hebben namelijk een ondersteunende functie voor een ander gebouw [<mark>ondersteunendeFuncties</mark>] <!-- BAG-2009-2014_objectenhandboek -->. Deze *ongeadreseerde* gebouwen of *bij*gebouwen zijn in een aantal gevallen eveneens relevant voor het in kaart brengen van vastgoedgebruik [<mark>bijgebouwen</mark>].

[<mark>ondersteunendeFuncties</mark>] Voorbeelden zijn: vrijstaande garageboxen, schuren, silo's, stallen, schaapskooien of toiletgebouwen op campings <!-- BAG-2009-2014_objectenhandboek -->.

[<mark>bijgebouwen</mark>] Bijvoorbeeld in het geval van agrarische bedrijven. Die bestaan vaak uit meerdere vastgoedobjecten. Sommige van deze objecten hebben een verblijfsobject (boerderij) maar anderen niet (schuren, stallen, silo's etc.). Steeds meer agrarische bedrijven stoppen<!-- bron -->. Vaak komen de bijgebouwen dan leeg te staan, terwijl de boerderij bewoond blijft. Omdat de bijgebouwen niet (apart) geadresseerd zijn, is op basis van de BAG niet vast te stellen wat de gebruiksstatus van elk afzonderlijk object is.

Een verblijfsobject in de BAG heeft een **gebruiksfunctie**: "*Het gebruiksdoel zal initieel worden afgeleid uit de bouwkundige gebruiksfunctie conform de categorisering van het Bouwbesluit 2003 zoals deze in de bouwvergunning als zodanig is aangemerkt. Op een later moment kunnen ook door de gemeente geformaliseerde gebruiswijzigingen als basis dienen voor opnamen van een aanvulend gebruiksdoel. Het gebruiksdoel dient niet te worden verward met de **planologische bestemming** en het **feitelijk gebruik**"*.<!-- bron BAG_2009_catalogus_grondslagen --> Met andere woorden, de gebruiksfunctie in de BAG betreft het **vergunde gebruik**. Zo is voor elk verblijfsobject tenminste één gebruiksdoel vastgesteld[<mark>dubbelfunctie</mark>]. Het gebruiksdoel is daarom geschikt voor een rudimentaire classificatie[<mark>gebruiksdoelen</mark>] van verblijfsobjecten. 

[<mark>dubbelfunctie</mark>] In sommige gevallen kan de bronhouder (gemeente) ervoor kiezen om een zogenaamde dubbelfunctie toe te kennen, bijvoorbeeld: woon-/winkelfunctie.

[<mark>gebruiksdoelen</mark>] De BAG onderscheidt 11 gebruiksdoelen: woon-, bijeekomst-, cel-, gezondheid-, industrie-, kantoor-, logies-, onderwijs-, sport-, winkel- en overige gebruiksfunctie. Deze indeling sluit niet altijd goed aan bij de praktijk. Agrarisch vastgoed wordt in deze classificatie bijvoorbeeld niet apart onderscheiden, maar valt onder industriefunctie.

Kortom, het onderscheid naar verblijfsobjecten is op twee manieren relevant voor de LIV: 
1. om het gebruik van een (deel van) een vastgoedobject (pand) vast te stellen, en; 
2. om binnen een vastgoedobject (pand) het type gebruik per eenheid te kunnen onderscheiden.

**Koppeling**

Om administratief gebruik vast te stellen, koppelt de LIV de WOZ, NHR en BRP aan de BAG. Deze registraties bevatten aanvullende vastgoedgegevens, of gegevens die iets zeggen over of het verblijfsobject in gebruik gebruik is of niet. In de LIV is er sprake van *administratieve leegstand* op het moment dat er op een verblijfsobject geen registratie is van: 

* een gebruiker in de WOZ[<mark>wozOnderscheid</mark>]
* een vestiging in het NHR
* een persoon in de BRP


[<mark>wozOnderscheid</mark>] Voor woningen wordt niet meer apart onderscheid gemaakt tussen een *eigenaar* en een *gebruiker*. In de praktijk is de WOZ-registratie voornamelijk relevantie voor alle typen *niet-woningen*. Woningen zitten al goed in de registratie op basis van de BRP. De aanname is dat het effect van het ontbreken van WOZ-informatie voor de categorie *woningen* beperkt is. Doordat deze informatie ontbreekt, is het exacte effect ervan onbekend.
Indien een situatie niet aan één van deze drie criteria voldoet, is er geen sprake van *administratieve leegstand* volgens de LIV. In alle andere gevallen wordt aangenomen dat er sprake is van gebruik.

#### Figuur: LIV_dataspec_bronnen_en_producten

Deze figuur beschrijft de basisopzet van de LIV. Hierin worden (delen van) de gegevens uit vier bronbestanden (LV BAG, LV WOZ, ***HR-dataservice?*** en ***BRP-...?*** ) opgehaald en aan elkaar gekoppeld op basis van de verblijfsobjectidentificatie (vbo-ID) uit de BAG. Het vbo-ID is één van de authentieke gegevens[<mark>authentiekGegeven</mark>] uit de BAG, die de andere bronnen vanuit de stelselverplichting gebruiken [<mark>stelselVerplichting</mark>]. 

[<mark>authentiekGegeven</mark>] Authentieke gegevens zijn gegevens die de Nederlandse overheden verplicht zijn te gebruiken *(bron zoeken, **of** directe URL naar bron (geldt mogelijk deels ook voor andere voetnoten))*

[<mark>stelselVerplichting</mark>] Bron: stelselverplichting?

De BAG vormt daarmee het middelpunt van de informatievoorziening. De koppeling vind plaats op vbo-id (kleinste gebruikseenheid). Daarbij is het pand is als de (kleinste) bouwkundige eenheid een belangrijk object.  De wens van gebruikers van de informatievoorziening is om op verblijfsobjectniveau te kunnen zien wat de administratieve gebruiksstatus is binnen het pand. Bovendien blijkt uit een [pilot](https://www.geonovum.nl/sites/default/files/methodiek_stappenplan_leegstand.pdf) dat bij [visualisatie van leegstand op objectniveau](http://maps.objectvision.nl/hoornleegstand/?layers=OPENBASISKAART,Hoorn_GEBRUIKSDOEL_ALLE,&zoom=9&lat=518900&lon=133200&language=nl) het hoge detailniveau en het type geometrie ("Point") van verblijfsobjecten de leesbaarheid bemoeilijkt, waardoor [aggregatie naar pandniveau](http://maps.objectvision.nl/hoornleegstand/?layers=OPENBASISKAART,Hoorn_GEBRUIKSDOEL_ALLE,&zoom=9&lat=518900&lon=133200&language=nl) (geometrie: "Polygon") wenselijk is.

**Uitgangspunten**
* beschrijft totaalpakket aan informatie dat voorzien in een aantal datafunctionaliteiten: **1** ... , **2** ... , en **3** ... .
* bevat ***geen*** specificatie van de datafunctionaliteiten zelf 
* semantische afstemming (in hoeverre en op welke manier relevant?)
* beschrijft de informatievoorziening. Het bevat geen beschrijving van de 'eindproducten', danwel (data)functionaliteiten waarvoor de LIV als basis dient.
* voorzien in een objectgerichte, gevectoriseerde data-uitwisseling
* <mark>weglaten?</mark> Afhaneklijke van type informatieproduct kan LIV toegepast worden in *view service* (WMS) of *download service* (WFS of Atom feeds [csv, excel?]). 
* geen 3D-geometrie toegepast (voor lange termijn wel relevant, dus nog rekening houden met aanknopingspunten??)
* voegt geen nieuwe geometrie toe? (wel nieuwe info, zeker naar verloop van tijd)
* bevat ook temporele informatie? (waarschijnlijk niet, tenzij datum/tijd geldigheid object of de historie die weopbouwen daaronder vallen)
* differentiatie van informatie: hoe en waar geregeld?
* integraal
* uniform
* eenduidige definitie van leegstand (administratief, structureel, tijdelijk, gedeeltelijk, verborgen) en van vastgoedcategorieën, maar (nog) geen andere definities)
* historie opbouwen zodat je over periodes (in eerste instantie jaren) heen kunt vergelijken
* landsdekkend
* [ *etc.*]