# Savegame-Datenstruktur (Mietwerk 2D v3)

```json
{
  "version": 3,
  "difficulty": "normal",
  "week": 8,
  "month": 2,
  "cash": 112340,
  "reserveBalance": 2100,
  "monthlyRentCollected": 2840,
  "creditPaidThisMonth": false,
  "lastMonthSummary": { "income": 9800, "expenses": 8700, "net": 1100 },
  "monthsWinningStreak": 0,
  "selectedPropertyId": 100,
  "selectedUnitId": 101,
  "selectedApplicantId": 140,
  "nextId": 165,
  "properties": [],
  "tasks": [],
  "tenantPool": [],
  "houseMarket": [],
  "usedMarket": [],
  "log": [],
  "gameOver": false,
  "victory": false
}
```

## properties[]
```json
{
  "id": 100,
  "name": "Wohnblock Nord",
  "x": 1,
  "y": 1,
  "value": 340000,
  "condition": 74,
  "fixedCosts": 1700,
  "reserveMonthly": 700,
  "opsDiscountWeeks": 0,
  "credit": {
    "remaining": 230000,
    "rate": 1850,
    "termMonths": 180
  },
  "units": []
}
```

## properties[].units[]
```json
{
  "id": 101,
  "label": "1A",
  "rent": 930,
  "deposit": 1860,
  "wear": 34,
  "isAdvertised": true,
  "tenant": {
    "name": "Meier",
    "satisfaction": 74,
    "reliability": 87
  }
}
```

## tenantPool[]
```json
{
  "id": 140,
  "name": "Nguyen",
  "budget": 1050,
  "reliability": 82,
  "expectation": 68,
  "patienceWeeks": 4
}
```

## houseMarket[]
```json
{
  "id": 150,
  "name": "Haus H",
  "price": 395000,
  "condition": 79,
  "units": [],
  "fixedCosts": 1750,
  "reserveMonthly": 680,
  "creditTemplate": {
    "part": 0.65,
    "rate": 2560,
    "termMonths": 180
  }
}
```

## usedMarket[]
```json
{
  "id": 160,
  "name": "Boden-Restposten",
  "price": 1500,
  "effect": { "wearMinus": 10 },
  "risk": 0.22,
  "hint": "-Abnutzung",
  "sold": false
}
```

## tasks[]
```json
{
  "id": 170,
  "propertyId": 100,
  "unitId": 101,
  "type": "Reparatur",
  "cost": 1200,
  "duration": 2,
  "remainingWeeks": 1,
  "priority": "Mittel",
  "status": "in_arbeit",
  "createdWeek": 7,
  "effect": { "conditionPlus": 7, "satisfactionPlus": 3 }
}
```
