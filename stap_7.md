# Extraatje: Functieparameters

Je hebt nu 2 eigen functies gemaakt: `speel_couplet` en `speel_refrein`. Maar bij het programmeren van *Jingle bells* heb je ook gebruik gemaakt van een flink aantal functies die in **Sonic Pi** zijn ingebouwd.

`play` is een voorbeeld van zo'n functie. De `play` functie roep je altijd aan met tenminste 1 waarde: het symbool voor de noot die je gespeeld wilt hebben (bijvoorbeeld `:c4`) of de MIDI-waarde van die noot (bijvoorbeeld `60`).

`sleep` is een andere functie die je veel gebruikt. Deze roep je altijd aan met het aantal tellen dat gewacht moet worden. Als je in de helpdocumentatie van **Sonic Pi** onder de **Taal** tab zoekt naar de `sleep` functie, dan zie je daar de definitie van de `sleep` functie: `sleep beats (number)`. `sleep` is de naam van de functie en `beats` (Engels voor tellen) is de naam van de (enige) parameter van de functie. `(number)` geeft aan dat de waarde van de parameter een getal moet zijn, dus `sleep 60` is goed, maar `sleep :c4` is fout.

Een functie kan dus 0 parameters hebben (zoals jouw `speel_couplet` en `speel_refrein`), maar ook 1 of meer parameters (zoals `play` en `sleep`).

Op dit moment gebruik je een `use_synth` commando vlak voor een aanroep van `speel_couplet` of `speel_refrein` om te bepalen met welk instrument het couplet of refrein gespeeld moet worden. Zou het niet handiger zijn als je gewoon aan de functies `speel_couplet` en `speel_refrein` kunt vertellen welk instrument ze moeten gebruiken? Dus dat je schrijft  
`speel_couplet :piano`  
`speel_refrein :pretty_bell`.

We beginnen met het aanpassen van de `speel_couplet` functie. De definitie van deze functie moeten we uitbreiden met een parameter waarin we het gewenste instrument aan de functie doorgeven. Deze parameter noemen we `instrument`. Net als bij functies, gebruiken we bij parameters ook namen die goed aangeven wat de bedoeling van de parameter is. De eerste regel van functie `speel_couplet` moet veranderd worden in  
`define :speel_couplet do |instrument|`  
De lijst van parameters van de functie komt dus na de `do` en staat tussen verticale strepen (`|`). Als je functie geen parameters heeft, dan kun je de lijst weglaten (zoals nu nog bij functie `speel_refrein`) en als je functie meer dan 1 parameter nodig heeft, dan zet je alle parameternamen tussen de verticale strepen gescheiden door komma's.

Vanaf nu kunnen we in de code van functie `speel_couplet` (alles tot aan de `end`) gebruik maken van parameter `instrument`. We willen dat alle noten van het couplet gespeeld worden met de waarde van `instrument`, dus voegen we  
`use_synth instrument`  
toe direct voor het eerste `play_pattern` commando.

Druk op de `Run` knop om je muziek te testen. **Sonic Pi** geeft nu een foutmelding omdat je functie `speel_couplet` 1 parameter verwacht, maar je aanroep geen waarde voor deze parameter geeft!

Vervang daarom de regels  
`use_synth :piano`  
`speel_couplet`  
door  
`speel_couplet :piano`  
en druk weer op `Run` om te testen. Nu wordt *Jingle bells* weer netjes uitgevoerd, met het piano-geluid voor het couplet.

Doe hetzelfde voor het refrein:
* Voeg een parameter `instrument` toe aan de definitie van functie `speel_refrein`.
* Voeg een `use_synth` commando toe aan de definitie van functie `speel_refrein`.
* Verwijder het `use_synth` commando vlak voor de aanroep van functie `speel_refrein`.
* Voeg `:pretty_bell` toe aan de aanroep van functie `speel_refrein`.

Druk weer op `Run` om te testen. *Jingle bells* zou weer normaal uitgevoerd moeten worden.

We sluiten af met nog een leuk weetje over parameters. Als je de eerste regel van de definitie van functie `speel_refrein`  
vervangt door  
`define :speel_refrein do |instrument = :pretty_bell|`  
dan kun je de aanroep  
`speel_refrein :pretty_bell`  
vervangen door  
`speel_refrein`  
Dus als je `speel_refrein` aanroept zonder parameter, dan weet de functie dat je `:pretty_bell` wilt gebruiken omdat je parameter door `instrument = :pretty_bell` is gedefinieerd.  
En je kunt het refrein nog altijd afspelen met een ander geluid, bijvoorbeeld  
`speel_refrein :dull_bell`  
Uiteraard kun je dit ook voor het couplet doen.
