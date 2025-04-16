# mcp_AI

# 🌤️ Weather Alert & Forecast MCP Tool

A lightweight microservice using [FastMCP](https://pypi.org/project/mcp/) that fetches weather alerts and forecasts from the [National Weather Service API](https://www.weather.gov/documentation/services-web-api). This tool provides U.S. state-level alerts and location-based forecasts.

---

## 🚀 Features

- **Get Active Alerts:** Fetch active weather alerts for any U.S. state using its two-letter abbreviation.
- **Get Forecast:** Retrieve the upcoming weather forecast for a specific latitude and longitude.
- **Asynchronous Requests:** Efficient use of `httpx` for non-blocking API calls.
- **Formatted Output:** Readable string output ideal for chatbot integration or quick CLI access.

---

## 👷️ Installation

```bash
pip install httpx
pip install fastmcp  # Or your local FastMCP package
```

---

## 📦 Usage

Make sure you have Python 3.9+ and `fastmcp` installed.

```bash
python main.py
```

The MCP server will start and listen for commands using the `stdio` transport.

---

## 🧰 Available Tools

### `get_alerts(state: str)`

Fetch active weather alerts for a U.S. state.

**Arguments:**

- `state`: Two-letter state code (e.g., `CA`, `TX`, `NY`)

**Returns:**\
A formatted string of current alerts or a message if none are available.

---

### `get_forecast(latitude: float, longitude: float)`

Fetch a detailed forecast for a specific location.

**Arguments:**

- `latitude`: Latitude of the location (e.g., `37.7749`)
- `longitude`: Longitude of the location (e.g., `-122.4194`)

**Returns:**\
Up to 5 periods of detailed forecast data (e.g., "Tonight", "Monday").

---

## 🧪 Example Output

**Alert Example:**

```
Event: Flood Warning  
Area: San Joaquin County  
Severity: Moderate  
Description: Flooding is expected in low-lying areas...  
Instructions: Turn around, don’t drown...
```

**Forecast Example:**

```
Tonight:
Temperature: 54°F
Wind: 10 mph NW
Forecast: Clear skies with calm wind.

---
Monday:
Temperature: 68°F
Wind: 5 to 10 mph W
Forecast: Sunny and warm.
```

---

## 📟 License

This project is licensed under the MIT License.




 
