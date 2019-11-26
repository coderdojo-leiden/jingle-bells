# Het refrein als functie

Net als voor het couplet gaan we de code voor het refrein in een functie stoppen. De functie voor het refrein geven we als naam `speel_refrein`.

Ga naar het einde van de buffer in **Sonic Pi** en voeg na de regel met `end` het volgende toe  
`define :speel_refrein do`  
`end`
Ga naar het begin van de buffer en voeg direct na het `speel_couplet` commando een nieuwe regel toe met  
`speel_refrein`

Druk op de `Run` knop om je muziek te testen. Je hoort alleen de muziek van het couplet en nog geen refrein. Dat is omdat je functie `speel_refrein` nog leeg is.

Dit is de muziek voor het refrein: <a href="resources/refrein.txt" target="_blank">resources/refrein.txt</a>.  
Kopieer deze code en plak ze aan het einde van de buffer in de functie `speel_refrein`, dus na de regel met  
`define :speel_refrein do`  
en voor de regel met  
`end`

Druk weer op `Run` om te testen. Je couplet wordt nu gevolgd door het refrein!
