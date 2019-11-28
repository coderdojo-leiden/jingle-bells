# Het couplet programmeren

We beginnen met het programmeren van het couplet. Een liedje bestaat vaak uit een couplet gevolgd door een refrein en dat een paar keer herhaald. De tekst van het refrein is iedere keer hetzelfde, maar de tekst van het couplet wijzigt meestal per herhaling, maar de muziek blijft wel hetzelfde.

*Jingle bells* bestaat uit 3 coupletten. De tekst van het eerste couplet staat onder de eerste vier notenbalken van de muziek en onder de resterende drie notenbalken staat de tekst van het refrein. De tekst van het tweede en het derde couplet staan helemaal onderaan (zonder notenbalken).

Ondanks dat we 3 coupletten hebben gaan we de muziek voor de coupletten maar 1 keer programmeren.

Dit is de muziek voor het couplet: <a href="resources/couplet.txt" target="_blank">resources/couplet.txt</a>.  
Kopieer deze code en plak ze in een lege buffer in **Sonic Pi**. Ga helemaal naar het begin van de buffer en voeg hier de volgende regel toe  
`use_bpm 240`  
en voeg hierna nog een lege regel toe.

Druk op de `Run` knop om je muziek te testen. Je hoort nu de muziek van het eerste couplet.

Als je naar de code van het eerste couplet kijkt, zie je dat er behalve het `play` commando (dat een enkele noot speelt) nog twee commando's worden gebruikt: `play_pattern` en `play_pattern_timed`. Het leuke van deze 2 commando's is dat je meerdere noten achter elkaar af kunt spelen met maar 1 commando!

Als je meer wilt weten over de `play_pattern` en `play_pattern_timed` commando's, lees dan vooral verder, ander ga je meteen door naar [de volgende stap >>](stap_3.md)

Aan het `play_pattern` commando geef je een lijst met noten, waarna het commando deze noten achter elkaar afspeelt, waarbij iedere noot 1 tel duurt.  
Het commando  
`play_pattern [:d4, :b4, :a4, :g4]`  
doet dus precies hetzelde als  
`play :d4`  
`sleep 1`  
`play :b4`  
`sleep 1`  
`play :a4`  
`sleep 1`  
`play :g4`  
`sleep 1`  
maar dan in 1 regel in plaats van in 8 regels!

Het `play_pattern` commando, maar ook het `play_pattern_timed` commando wat we zo meteen behandelen, maakt gebruik van lijsten. Een lijst begint met een openblokhaak `[`, eindigt met een sluitblokhaak `]` en daartussen zet je de elementen gescheiden door komma’s. De elementen kunnen noten zijn (zoals hierboven), maar ook bijvoorbeeld getallen. Voorbeelden van lijsten met noten zijn:  
`[:d4, :b4]` is een lijst met 2 noten: `:b4` gevolgd door `:d4`,  
`[:b4]` is een lijst met maar 1 noot: `:b4`.

Aan het `play_pattern_timed` commando geef je een lijst met noten gevolgd door een even lange lijst met getallen. Het getal geeft aan hoe lang de noot (in tellen) moet duren. Dit commando is handig als je noten niet allemaal 1 tel duren.  
Het commando  
`play_pattern_timed [:d4, :d4, :d4, :b4, :a4, :g4], [0.5, 0.5, 1, 1, 1, 1]`  
doet precies hetzelde als  
`play :d4`  
`sleep 0.5`  
`play :d4`  
`sleep 0.5`  
`play :d4`  
`sleep 1`  
`play :b4`  
`sleep 1`  
`play :a4`  
`sleep 1`  
`play :g4`  
`sleep 1`  
maar dan in 1 regel in plaats van in 12 regels!

Hierboven zie je naast een lijst met noten een voorbeeld van een lijst met getallen.

[De volgende stap >>](stap_3.md)



