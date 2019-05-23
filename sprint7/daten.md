# API Formate

Alle Daten werden im JSON Format kommuniziert.

## Geräte

Typespec:

```ts
type Device = {
	"id": string,
	"name": string,
	"description": string,
	"attributes": { 
		[key: string]: string 
	},
	"location": {
		"name": string,
		"description": string
	}
}
```

Beispiel:

```json
{
	"id": "2356354556",
	"name": "Notenrechner Lehrer"
	"description": "Zentraler Notenrechner im Lehrerzimmer"
	"attributes": {
		"Nur Lehrer": "Ja",
		"Passwortgeschützt": "Ja",
		"Betriebssystem": "Windows 2000"
	},
	"location": {
		"name": "Lehrerzimmer",
		"description": "Keine Schüler (offiziell) erlaubt!"
	}
}
```

### `GET /api/devices`

Gibt alle Geräte im System zurück.

Die ID eines Gerätes ist dessen Barcode als String.

Rückgabe: `Status 200`

```ts
Device[]
```

### `GET /api/devices/:id`

Gibt das Gerät mit der angegebenen ID zurück.

Die ID eines Gerätes ist dessen Barcode als String.

#### Fall: Das Gerät existiert

Rückgabe: `Status 200`

```ts
Device
```

#### Fall: Das Gerät existiert nicht

Rückgabe: `Status 404`

### `POST /api/devices`

Legt ein neues Gerät an.

```ts
Device
```

### Fall: Gerät erfolgreich angelegt

Rückgabe: `Status: 201`

```ts
Device
```

### Fall: JSON Fehlerhaft oder unvollständig

Rückgabe: `Status: 400`

### `PUT /api/devices/:id`

Aktualisiert die Daten eines Gerätes.

```ts
Device
```

### Fall: Gerät erfolgreich aktualisiert

Rückgabe: `Status: 200`

```ts
Device
```

### Fall: Gerät existiert nicht

Rückgabe: `Status: 404`

### Fall: JSON Fehlerhaft oder unvollständig

Rückgabe: `Status: 400`

### `DELETE /api/devices/:id`

Löscht ein Gerät und alle damit verknüpften Daten(z.B. Tickets).

### Fall: Gerät erfolgreich gelöscht

Rückgabe: `Status: 200`

```ts
Device
```

### Fall: Gerät existiert nicht

Rückgabe: `Status: 404`
