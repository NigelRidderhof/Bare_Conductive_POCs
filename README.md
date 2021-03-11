# Bare_Conductive_POCs

Plaats deze repository direct in je Arduino map. 

Binnen deze repository zijn de projecten opgedeeld in `Touch` en `Proximity`. In ieder van deze is een mapje voor de mp3 files om op je SD kaart te zetten middels de reader. Alleen het MIDI keys project heeft geen mp3 files nodig. 

In Arduino zelf kun je bij de projecten komen middels `Bestand > Schetsboek > Bare Conductive POCs`.

##### Specifieke benoemswaardigheden:
- MIDI Keys: voor de viool in plaats van de piano uit de video, pas in het `.ino` bestand de `INSTRUMENT` waarde aan van 16 naar 40.
  Voor de drumgeluiden, pas de `MELODIC_INSTRUMENT` waarde aan van `true` naar `false`.
- Het bestand voor `Proximity > Geluid_trigger` is bijna hetzelfde als die voor `Touch > Pratende_objecten`. Het verschil is dat er hogere thresholds ingesteld zijn, waardoor de gevoeligheid is toegenomen en daarom bij nabijheid al getriggerd wordt i.p.v. pas bij aanraking.
- Het bestand voor `Proximity > Grapher` is ook bijna hetzelfde als die voor `Touch > Pratende_objecten`. De waarde van `MPR121_DATASTREAM_ENABLE` is echter naar `true` gezet, zodat de data doorgegeven kan worden naar het Processing project dat je ook nodig hebt. Zie voor dit, de 2 nodige Processing libraries en verdere uitleg de hiervoor bestemde pagina [Grapher](https://www.bareconductive.com/blogs/resources/touch-board-grapher).
