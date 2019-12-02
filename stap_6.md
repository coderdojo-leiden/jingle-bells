# Uitdaging: Herhalen maar!

Zoals je je nog wel zult herinneren, bestaat een volledige uitvoering van *Jingle bells* uit drie coupletten, iedere keer gevolgd door het refrein. Je kunt dit op twee manieren programmeren.

## Kopieren en plakken
Het makkelijkste is om de vier regels aan het einde van de buffer te kopieren en gewoon twee keer te plakken zodat alles in totaal drie keer gedaan wordt. Dit levert 12 regels code op. Als je couplet en refrein nog vaker herhaald zouden moeten worden, dan levert dit uiteindelijk heel veel code op die steeds hetzelfde doet. Deze oplossing is dus alleen geschikt voor een klein aantal herhalingen.

## Een lus gebruiken
Als je in Sonic Pi een serie commando's een vast aantal keren wilt herhalen, dan gebruik je daarvoor de `times` functie. Drie keer het couplet en het refrein uitvoeren programmeer je dan als volgt  
`3.times do`  
`use_synth :piano`  
`speel_couplet`  
`use_synth :pretty_bell`  
`speel_refrein`  
`end`  
Meer herhalingen nodig? Vervang gewoon het getal `3` door het aantal herhalingen dat jij wilt! En het aantal regels code blijft gewoon 6.  
Het enige nadeel(tje) van deze oplossing is dat het nu lastiger is om bijvoorbeeld je couplet iedere keer met een ander geluid (bijv. eerste couplet `:piano`, tweede couplet `:hoover` en derde couplet `:prophet`) af te spelen.

Wil je nog wat meer te weten over de mogelijkheden van functies? Ga dan naar de uitleg op [de volgende pagina](stap_7.md).

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons-Licentie" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />Dit werk valt onder een <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/deed.nl">Creative Commons Naamsvermelding-NietCommercieel-GelijkDelen 4.0 Internationaal-licentie</a>.
