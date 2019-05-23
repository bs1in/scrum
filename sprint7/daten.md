# API Formate

Alle Daten werden im JSON Format kommuniziert.

## Geräte

Typespec:

```ts
type Device = {
	/**
	 * Die ID des Gerätes, in unserem Fall der Barcode.
	 */
	"id": string, // PK
	/**
	 * Der Name des Gerätes.
	 */
	"name": string,
	/**
	 * Der Beschreibung des Gerätes.
	 */
	"description": string,
	/**
	 * Zusätzliche Userdefinierte Attribute als Key-Value-Pairs (=Map).
	 */
	"attributes": { 
		[key: string]: string 
	},
	/**
	 * Wo ist das Gerät?
	 */
	"location": {
		/**
		 * Name des Ortes.
		 */
		"name": string,
		/**
		 * Beschreibung des Ortes.
		 */
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

## Tickets

Typespec:

```ts
type Ticket = {
	/**
	 * Die ID des Tickets.
	 */
	"id": string, // PK
	/**
	 * Die ID des verknüpften Gerätes. Leer wenn mit keinem Gerät verknüpft.
	 */
	"device": string, // FK -> Device
	/**
	 * Eine User angegebene Beschreibung des Tickets, leer wenn keine Beschreibung.
	 */
	"description": string,
	/**
	 * Ist das Ticket erledigt?
	 */
	"done": boolean
}
```

Beispiel:

```json
{
	"id": "790",
	"device": "2356354556"
	"description": "Es sind zu viele schlechte Noten gespeichert - Bitte Festplatte neu formatieren.",
	"done": false
}
```

### `GET /api/tickets`

Gibt alle Tickets im System zurück.

Rückgabe: `Status 200`

```ts
Ticket[]
```

### `GET /api/tickets/:id`

Gibt das Ticket mit der angegebenen ID zurück.

#### Fall: Das Ticket existiert

Rückgabe: `Status 200`

```ts
Ticket
```

#### Fall: Das Ticket existiert nicht

Rückgabe: `Status 404`

### `POST /api/tickets`

Legt ein neues Ticket an.

```ts
Ticket
```

### Fall: Ticket erfolgreich angelegt

Rückgabe: `Status: 201`

```ts
Ticket
```

### Fall: JSON Fehlerhaft oder unvollständig

Rückgabe: `Status: 400`

### `PUT /api/ticket/:id`

Aktualisiert die Daten eines Ticket.

```ts
Ticket
```

### Fall: Ticket erfolgreich aktualisiert

Rückgabe: `Status: 200`

```ts
Ticket
```

### Fall: Ticket existiert nicht

Rückgabe: `Status: 404`

### Fall: JSON Fehlerhaft oder unvollständig

Rückgabe: `Status: 400`

### `DELETE /api/tickets/:id`

Löscht ein Ticket.

### Fall: Ticket erfolgreich gelöscht

Rückgabe: `Status: 200`

```ts
Ticket
```

### Fall: Ticket existiert nicht

Rückgabe: `Status: 404`

