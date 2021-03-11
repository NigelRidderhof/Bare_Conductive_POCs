# Bare_Conductive_POCs

_Inbegrepen: Arduino code en mp3 files.
De code is grotendeels afkomstig van de [Bare Conductive GitHub](https://github.com/BareConductive)
[Bare Conductive website](https://www.bareconductive.com/)_

Plaats deze repository direct in je Arduino map. 

Binnen deze repository zijn de projecten opgedeeld in [`Touch`](/Touch) en [`Proximity`](/Proximity). In ieder van deze is een mapje voor de mp3 files om op je SD kaart te zetten middels de SD kaart reader. Alleen het MIDI keys project heeft geen mp3 files nodig. 

In Arduino zelf kun je bij de projecten komen middels `Bestand > Schetsboek > Bare Conductive POCs`.

##### Specifieke benoemswaardigheden:
- MIDI Keys: voor de viool in plaats van de piano uit de video, pas in het [`MIDI_keys.ino`](/Touch/MIDI_keys/MIDI_keys.ino) bestand de [`INSTRUMENT`](https://github.com/NigelRidderhof/Bare_Conductive_POCs/blob/ac8a690fec910acc2db3ca0ab798f44c5d9c2c40/Touch/MIDI_keys/MIDI_keys.ino#L80) waarde aan van 16 naar 40.
  Voor de drumgeluiden, pas de [`MELODIC_INSTRUMENT`](https://github.com/NigelRidderhof/Bare_Conductive_POCs/blob/ac8a690fec910acc2db3ca0ab798f44c5d9c2c40/Touch/MIDI_keys/MIDI_keys.ino#L64) waarde aan van `true` naar `false`.
- Het bestand voor `Proximity > Geluid_trigger` is bijna hetzelfde als die voor `Touch > Pratende_objecten`. Het verschil is dat er hogere thresholds ingesteld zijn, waardoor de gevoeligheid is toegenomen en daarom bij nabijheid al getriggerd wordt i.p.v. pas bij aanraking.
- Het bestand voor `Proximity > Grapher` is ook bijna hetzelfde als die voor `Touch > Pratende_objecten`. De waarde van `MPR121_DATASTREAM_ENABLE` is echter naar `true` gezet, zodat de data doorgegeven kan worden naar het Processing project dat je ook nodig hebt. Zie voor dit, de 2 nodige Processing libraries en verdere uitleg de hiervoor bestemde Bare Conductive pagina, [Grapher](https://www.bareconductive.com/blogs/resources/touch-board-grapher).
