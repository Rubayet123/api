# 🎯 Awesome APIs Collection (Free Public APIs)

Collection of **currently working free public APIs** that **don't require authentication**, API keys or have very generous free tiers (updated 2025–2026).

> ⚠️ **Important**: Free APIs die or add restrictions very often.  
> Last major update: January 2026  
> Feel free to open issue / PR when something stops working!

## Categories

- 🌍 [Geo-location / IP Geolocation](./apis/geo-location.md)
- ☀️ Weather
- 🖼️ Free Image APIs / Generators
- 📝 Free Text / AI endpoints
- 🎵 Music / Lyrics
- 💰 Finance / Crypto
- ⚡ Others / Utilities


## Updated API List (January 2026)

### Geo / IP Location

| # | Service                  | URL / Endpoint                            | Sample Response fields                              | Rate Limit              | Status     | Remark                                  |
|---|--------------------------|-------------------------------------------|-----------------------------------------------------|-------------------------|------------|-----------------------------------------|
| 1 | InMobi CMP GeoIP         | `https://cmp.inmobi.com/geoip`            | country, region, city                               | ? (very generous)       | ✅ Working | Very minimal & fast                     |
| 2 | ipapi.co                 | `https://ipapi.co/json/`                  | ip, city, region, country, latitude, timezone...   | 30,000 req/month        | ✅         | Very popular & reliable                 |
| 3 | ipinfo.io (no key)       | `https://ipinfo.io/json`                  | ip, city, region, country, loc, org...             | 50,000/month            | ✅         | Good data quality                       |
| 4 | freeipapi.com            | `https://freeipapi.com/api/json`          | ip, city, regionName, countryCode, lat, lon...     | Unlimited? (2025)       | ✅         | Includes currency & languages           |
| 5 | ipwhois.app              | `https://ipwhois.app/json/`               | ip, country, city, latitude, isp, timezone...      | 10,000/month            | ✅         | Nice response                           |
| 6 | ip.sb                    | `https://api.ip.sb/geoip`                 | country, region, city, latitude, longitude...      | Very generous           | ✅         | Simple & fast                           |

#### Quick test snippet (fetch + JSON)

```js
fetch('https://cmp.inmobi.com/geoip')
  .then(r => r.json())
  .then(data => console.log(data))
// {
//   "country": "bgd",
//   "region": "c",
//   "city": "dhaka"
// }
```



### ☀️ Weather APIs – Free / No API Key Required

(Last checked: January 19, 2026)

These APIs provide current weather, forecasts, and sometimes historical data without forcing you to register or use an API key.

| # | Service              | Endpoint / Example URL                                                                 | Response type     | Main Features                              | Rate Limit / Notes                              | Status     |
|---|----------------------|----------------------------------------------------------------------------------------|-------------------|--------------------------------------------|-------------------------------------------------|------------|
| 1 | Open-Meteo           | `https://api.open-meteo.com/v1/forecast?latitude=23.81&longitude=90.41&current=temperature_2m,relative_humidity_2m,weather_code&daily=temperature_2m_max,temperature_2m_min` | JSON              | Current + hourly + daily forecast (up to 16 days), many models, very accurate | Free for non-commercial, generous limits, no key | ✅ Excellent |
| 2 | wttr.in              | `https://wttr.in/Dhaka?format=j1` <br> `curl wttr.in/Dhaka`                           | JSON / ANSI / HTML / PNG | Beautiful console output, current + 3-day forecast | Very generous, no key, mostly for fun & scripts | ✅ Very popular |
| 3 | 7Timer!              | `https://www.7timer.info/bin/api.pl?lon=90.41&lat=23.81&product=civ&output=json`     | JSON              | Astro/civil weather forecast, simple & old-school | Unlimited?, no key                              | ✅ Working  |
| 4 | Open-Meteo (Historical) | `https://archive-api.open-meteo.com/v1/archive?latitude=23.81&longitude=90.41&start_date=2025-01-01&end_date=2025-01-19&daily=temperature_2m_max` | JSON              | Historical data (back to ~1940 in many places) | Free non-commercial, no key                     | ✅ Great for data projects |

#### Quick test snippets (JavaScript fetch)

**1. Open-Meteo – Current weather + forecast (Dhaka example)**

```js
fetch('https://api.open-meteo.com/v1/forecast?latitude=23.8103&longitude=90.4125&current=temperature_2m,apparent_temperature,weather_code,wind_speed_10m&daily=temperature_2m_max,temperature_2m_min,sunrise,sunset&timezone=Asia%2FDhaka')
  .then(r => r.json())
  .then(data => console.log(data));


---

⭐ If this list helps you – give it a star!  
Last checked: January 19, 2026
