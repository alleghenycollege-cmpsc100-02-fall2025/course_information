## Data Structures Overview for Lab 08

Each program uses **dictionaries with nested dictionaries** to organize sensor data and alert information. Understanding these structures is essential for completing the lab.

### temperature_monitor.py - Temperature Database

**Structure:** Dictionary with string keys (location IDs) and nested dictionary values

```python
readings = {
    "LAB_A": {
        "location": "Lab Room A",      # String: Location name
        "temp": 22.5,                  # Float: Temperature in Celsius
        "humidity": 45.0,              # Float: Humidity percentage
        "comfort": "Good"              # String: Comfort level category
    },
    "CLASSROOM": {
        "location": "Classroom B",
        "temp": 26.3,
        "humidity": 52.0,
        "comfort": "Warm"
    }
}
```

**Key Operations:**
- Access temperature: `readings["LAB_A"]["temp"]`
- Iterate through all: `for loc_id, data in readings.items()`
- Check threshold: `if data["temp"] > 25`

---

### light_monitor.py - Light Level Database

**Structure:** Dictionary with string keys (location IDs) and nested dictionary values

```python
readings = {
    "WINDOW": {
        "location": "Window Area",     # String: Location name
        "light_level": 680,            # Integer: Light level (0-1000)
        "brightness": "Bright"         # String: Brightness category
    },
    "CORNER": {
        "location": "Back Corner",
        "light_level": 150,
        "brightness": "Dark"
    }
}
```

**Key Operations:**
- Access light level: `readings["WINDOW"]["light_level"]`
- Build list of levels: `levels = [data["light_level"] for data in readings.values()]`
- Check threshold: `if data["light_level"] < 200`

---

### buzzer_manager.py - Alert Tracking Database

**Structure:** Dictionary with string keys (location IDs) and nested dictionary values

```python
alerts = {
    "LAB_A": {
        "location": "Lab Room A",      # String: Location name
        "buzzer_on": False,            # Boolean: Current buzzer state
        "alert_count": 0,              # Integer: Total alerts triggered
        "last_reason": "None"          # String: Reason for last alert
    },
    "CLASSROOM": {
        "location": "Classroom B",
        "buzzer_on": True,
        "alert_count": 2,
        "last_reason": "High temperature"
    }
}
```

**Key Operations:**
- Update buzzer state: `alerts["LAB_A"]["buzzer_on"] = True`
- Increment count: `alerts[loc_id]["alert_count"] = alerts[loc_id]["alert_count"] + 1`
- Check active alerts: `if data["buzzer_on"]`

---

### main.py - Integration Variables

**Structure:** Three separate dictionaries (one for each module)

```python
# Created in main()
temp_data = {}      # Holds temperature_monitor readings
light_data = {}     # Holds light_monitor readings
alert_data = {}     # Holds buzzer_manager alerts

# Passed between modules:
check_all_alerts(temp_data, light_data, alert_data)
```

**Integration Flow:**
1. `temp.check_temp_alerts(temp_data)` → Returns list of alert strings
2. `light.check_light_alerts(light_data)` → Returns list of alert strings
3. Alert strings parsed to extract location IDs
4. `buzzer.trigger_buzzer(alert_data, loc_id, reason)` → Updates alert dictionary and sounds buzzer

---

### Alert Functions Return Type: Lists of Strings

Both `check_temp_alerts()` and `check_light_alerts()` return **lists of formatted strings**:

```python
# Example return values:
temp_alerts = [
    "CLASSROOM: Temperature 26.3C is too warm",
    "LAB_A: Humidity 65.0% is too high"
]

light_alerts = [
    "CORNER: Light level 150 is too dark (min 200)"
]
```

**Why lists?** Multiple locations can have alerts simultaneously, so functions return all alerts at once.

---

### Summary of Data Structures Used

| Program | Main Structure | Value Type | Purpose |
|---------|---------------|------------|---------|
| `temperature_monitor.py` | Dictionary | Nested Dictionary | Store temp/humidity readings per location |
| `light_monitor.py` | Dictionary | Nested Dictionary | Store light levels per location |
| `buzzer_manager.py` | Dictionary | Nested Dictionary | Track buzzer state and alert history |
| `check_*_alerts()` | List | Strings | Return multiple alert messages |
| `main.py` | Three separate Dictionaries | Nested Dictionary | Coordinate all modules |

**Nested Dictionary Pattern:** All three modules use `outer_dict[key] = inner_dict` where:
- **Outer key:** Location ID (string like "LAB_A")
- **Inner dictionary:** Contains multiple properties (location name, sensor values, status)

This pattern allows you to store multiple pieces of related information for each location!
