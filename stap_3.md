# Het couplet als functie

Het couplet van *Jingle bells* gaan we straks 3 keer afspelen, iedere keer gevolgd door het refrein. Om het gebruik van de code voor het couplet makkelijker te maken, gaan we die code inpakken in een zogenaamde **functie**. Een **functie** is een stuk code dat je een unieke naam geeft zodat je die code later kunt gebruiken door alleen maar de naam van de functie op te geven.

De functie voor het couplet geven we als naam `speel_couplet`. We kiezen de naam van de functie zo dat iemand anders snapt wat de functie doet zonder naar de code te hoeven kijken.

Ga naar het begin van de buffer in **Sonic Pi** en voeg een nieuwe regel toe vlak voor het eerste `play_pattern` commando met  
`define :speel_couplet do`  
Ga naar het einde van de buffer en voeg na het laatste `sleep` commando een nieuwe regel toe met  
`end`

Druk op de `Run` knop om je muziek te testen. Je hoort helemaal niets! Dit is omdat je de functie `speel_couplet` wel gedefinieerd hebt, maar nog niet aangeroepen hebt.

Blijf aan het einde van de buffer en voeg direct na de regel met `end` een lege regel toe en daarna nog een nieuwe regel met  
`speel_couplet`  
Je hebt nu een aanroep van je functie toegevoegd.

Druk weer op `Run` om te testen. Je couplet doet het weer!

[De volgende stap >>](stap_4.md)

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons-Licentie" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />Dit werk valt onder een <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/deed.nl">Creative Commons Naamsvermelding-NietCommercieel-GelijkDelen 4.0 Internationaal-licentie</a>.
