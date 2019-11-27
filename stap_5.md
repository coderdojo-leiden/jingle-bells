# Uitdaging: De geluiden aanpassen

Laten we het standaard piepje van **Sonic Pi** eens vervangen door een leuker geluid. Voor het couplet gaan we een piano-geluid gebruiken en voor het refrein een bel-geluid. (Het toch niet voor niets *Jingle bells*?)

Ga naar het einde van de buffer en voeg vlak voor de regel met de **aanroep** van functie `speel_couplet` een nieuwe regel toe met  
`use_synth :piano`

Druk op de `Run` knop om je muziek te testen. Niet alleen je couplet, maar ook je refrein wordt nu met piano-geluid afgespeeld.  
Voeg daarom vlak voor de regel met de **aanroep** van functie `speel_refrein` een nieuwe regel toe met  
`use_synth :pretty_bell`

Aan het einde van de buffer staan als het goed is nu de volgende vier regels code:  
`use_synth :piano`  
`speel_couplet`  
`use_synth :pretty_bell`  
`speel_refrein`

Druk weer op `Run` om te testen. Je couplet met piano-geluid wordt nu gevolgd door het refrein met bel-geluid.

Probeer eens andere synths om te horen welk geluid het beste bij jouw uitvoering van *Jingle bells* past.