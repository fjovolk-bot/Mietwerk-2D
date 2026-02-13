# Savegame-Datenstruktur (Mietwerk 2D)

Der komplette Spielzustand wird als JSON gespeichert (`localStorage`, Export/Import).

## Top-Level

```json
{
  "version": 2,
  "week": 12,
  "month": 4,
  "cash": 134500,
  "reserveBalance": 5400,
  "monthlyRentCollected": 3810,
  "creditPaidThisMonth": true,
  "lastMonthSummary": {
    "income": 11430,
    "expenses": 9100,
    "net": 2330
  },
  "monthsWinningStreak": 1,
  "selectedPropertyId": 100,
  "selectedUnitId": 101,
  "nextId": 140,
  "properties": [],
  "tasks": [],
  "marketOffers": [],
  "log": [],
  "gameOver": false,
  "victory": false
}
```

## Property (`properties[]`)

```json
{
  "id": 100,
  "name": "Wohnblock Nord",
  "x": 1,
  "y": 1,
  "value": 350000,
  "condition": 74,
  "fixedCosts": 1800,
  "reserveMonthly": 700,
  "opsDiscountWeeks": 2,
  "credit": {
    "remaining": 240000,
    "rate": 1900,
    "termMonths": 180
  },
  "units": []
}
```

## Unit (`properties[].units[]`)

```json
{
  "id": 101,
  "label": "1A",
  "rent": 950,
  "deposit": 1900,
  "wear": 32,
  "isAdvertised": false,
  "tenant": {
    "name": "Meier",
    "satisfaction": 73,
    "reliability": 89
  }
}
```

`tenant` kann `null` sein.

## Task (`tasks[]`)

```json
{
  "id": 120,
  "propertyId": 100,
  "unitId": 101,
  "type": "Reparatur",
  "cost": 1400,
  "duration": 2,
  "remainingWeeks": 1,
  "priority": "Hoch",
  "status": "in_arbeit",
  "createdWeek": 9,
  "effect": {
    "conditionPlus": 8,
    "satisfactionPlus": 3,
    "wearMinus": 10
  }
}
```

`status`: `offen` | `in_arbeit` | `erledigt`

## Gebrauchtmarkt (`marketOffers[]`)

```json
{
  "id": 133,
  "name": "Restposten Bodenbelag",
  "type": "renovation",
  "price": 1700,
  "effect": {
    "wearMinus": 12
  },
  "risk": 0.2,
  "hint": "-Abnutzung, mittleres Risiko",
  "sold": false
}
```

## Log (`log[]`)

```json
{
  "week": 12,
  "text": "Wohnung 2A ausgewählt.",
  "type": "muted"
}
```
