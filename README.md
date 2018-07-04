# GOB

**G**enerieke **O**ntsluiting **B**asisgegevens

_An English version of this document can be found in README.en.md_

## Achtergrond

Basisgegevens zijn de grondstof voor een groot aantal gemeentelijke processen.
Zonder deze gegevens kunnen de processen niet worden uitgevoerd.

Basisgegevens worden bijgehouden in basisregistraties (door de wet voorgeschreven) en kernregistraties (door het college van B&W voorgeschreven).
Basisinformatie is ervoor verantwoordelijk dat deze gegevens voldoen aan de wettelijke voorschriften en op de juiste manier worden gebruikt.

Voor een deel worden deze gegevens uit een eigen gemeentelijke voorzieningen (bronsysteem) gehaald en voor een deel uit landelijke voorzieningen.
Het probleem is dat al deze bronnen niet één-en-dezelfde gegevens-/berichtenstandaard gebruiken.  
De binnengemeentelijke afnemers maken weer gebruik van verschillende systemen waarin de basisgegevens worden getoond of verwerkt.

De zeven basisregistraties zijn:
1. personen (BRP)
2. adressen en gebouwen (BAG)
3. waarde onroerende zaken (BR WOZ)
4. kleinschalige topografie (BRT)
5. grootschalige topografie (BGT)
6. handelsregister (HR)
7. kadaster (BRK).

De acht kernregistraties zijn:
1. de gemeentelijke beperkingenregistratie (Wkpb)
2. het actueel hoogtebestand Nederland
3. gebieden
4. NAP
5. luchtfoto's
6. meetbouten
7. monumenten
8. panoramabeelden.

Voor het ophalen van gegevens bij de bron of de landelijke voorziening, het beheer, de vertaling en de distributie van de basisgegevens zijn drie systemen in gebruik:
- DIVA voor vastgoedgegevens
- Makelaarsuite voor persoonsgegevens 
- Handelsregister en Neuron Communicator voor BAG- en WOZ-gegevens

Niet alle systemen kunnen de verschillende aanleveringen verwerken.
Een ‘vertaling’ is daarom noodzakelijk.
Binnen GOB worden de basisgegevens uit de verschillende bronregistraties opgeslagen, verwerkt en gedistribueerd in een formaat conform gedefinieerd op [Stelselpedia](https://www.amsterdam.nl/stelselpedia/|Stelselpedia) en [RSGB](https://www.gemmaonline.nl/index.php/Informatiemodel_Basis-_en_Kerngegevens_(RSGB)).

## Doel

Het doel van het project is de levering van kwalitatief hoogwaardige basisgegevens ten behoeve van gemeentelijke processen te garanderen tegen minimale beheerinspanningen en kosten.

Met als afgeleide doelstellingen:
- Leveringen op maat

Veel afnemers hebben behoefte aan datasets die zijn samengesteld uit meerdere basisgegevens.
Er is daarom behoefte aan functionaliteit waarmee afnemers kunnen worden bediend met leveringen op maat. 

- Integraal kwaliteitsbeheer van het stelsel

Het project moet de consistentie, integriteit en kwaliteit van het gehele Amsterdamse stelsel van basisgegevens beheren,
inclusief eisen die in het kader van de archiefwet aan informatiebeheer worden gesteld.

## Globale werkwijze

Het GOB project is een modulair opgebouwd systeem.

Elke component binnen GOB heeft een welafgebakende functie en zijn eventueel ook los van GOB inzetbaar.
Voorbeelden van componenten zijn de import van Neuron data, opslag van Stelselpedia data, afleiden van mutaties op basis van een import.

Communicatie tussen de componenten loopt via een Message Broker.

Opslag van gegevens vindt plaats in een database.

Alle componenten worden gevoed vanuit een op Stelselpedia en RSGB gebaseerd data formaat.

Afhankelijkheden van specifieke message brokers of databases zijn geencapsuleerd.
De keuze voor een specifieke message broker of database kan eventueel worden aangepast.

## Gebruikers

De gebruikers van GOB zijn ambtenaren, burgers en ondernemers.

Ambtenaren binnen de gemeente Amsterdam gebruiken de data ter ondersteuning of als input voor hun werkzaamheden.

Burgers en ondernemers hebben toegang tot (het publiek beschikbare deel van) de data via een API of web applicaties.
