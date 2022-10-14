# Library
 
 Gas verbruik CV en Tap vs weergegevens van knmi
 
ruwe data is beschikbaar op SQL
De RPI is niet capable om alle data telkens weer te mergen
Dus merge alleen de data waarom gevraagd wordt. 

Op een volwassen systeem kan wel merge van alle rijen gedaan worden. 
In geval van nieuw algorithme zullen alle dagen opnieuw geplot moeten worden
Maak algorithme versie beschikbaar op graph.



To Test : Kan RPI bubble chart weergeven met alle dag data tot op heden?


# Sources:
readings temperature sensor tap, minute granularity
readings temperature sensor CV in,minute granularity
readings temperature sensor CV out,minute granularity
readings gas P1, 15 min granularity

weather readings knmi, usually updated early in the morning, but sometimes not updated at all for multiple days.


# Workflow: 
Onderscheid: 
  proces ontbrekende dagen 
  proces ontbrekende knmi data dagen
  proces periode
  proces vandaag
  proces gisteren
  
Hoe snel is SQL minute data  van een dag: antwoord: binnen de seconde.
Dus voor dagelijkse update hoeft niet een grote file te openen, echter zou je wel dagelijks verbruik willen gebruiken als referentie.
Maar... wellicht kan na berekenen dagdata ge-upload worden naar SQL database en die geraadpleegd worden.







