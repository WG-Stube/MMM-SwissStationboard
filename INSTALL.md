# Installation SBB Fahrplan

## Manuelle Installation

1. In den Modul Ordner wechseln
`cd ~/MagicMirror/modules`

2. Erweiterung herunterladen und installieren
`git clone https://github.com/WG-Stube/MMM-SwissStationboard`

3. Modul einrichten
`nano ~/MagicMirror/config/config.js`
In der Datei ganz am Ende der Liste (nach dem letzten `},` ) einfügen
```js
{
	module: 'MMM-SwissStationboard',
	position: 'bottom_bar',
	header: 'Zugverbindungen',
	config: {
		stop: 'Marthalen', // Bahnhof
		maximumEntries: 4, // Anzahl Abfahrten die angezeigt werden
		minWalkingTime: 10, // Zeit bis zum Bahnhof
		hideNotReachable: 0, // Nicht erreichbare Verbindungen nicht anzeigen
	}
},
```

4. Nano schliessen mit `CTRL+O` und `CTRL+X`

5. Mirror starten zum testen 
- `cd ~/MagicMirror`
- `npm run start`
