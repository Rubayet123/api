# 🎯 Free Public APIs

Collection of **currently working** free public APIs that don't require authentication, API keys, or have extremely generous free tiers.

> ⚠️ **Important**: Free APIs can die or add restrictions suddenly.  
> Last major update: January 19, 2026  
> Feel free to open issues/PRs when something stops working!

## 🌍 Geo-location / IP to Location

| Service          | Endpoint                              | Main fields                        | Rate Limit              | Status |
|------------------|---------------------------------------|------------------------------------|-------------------------|--------|
| InMobi           | `https://cmp.inmobi.com/geoip`        | country, region, city              | Very generous (?)       | ✅     |
| ipapi.co         | `https://ipapi.co/json/`              | city, country, lat/lon, timezone…  | 30,000/mo               | ✅     |
| ipinfo.io        | `https://ipinfo.io/json`              | city, country, loc, org…           | 50,000/mo               | ✅     |
| freeipapi.com    | `https://freeipapi.com/api/json`      | city, country, currency, lat/lon…  | Very generous           | ✅     |
| ipwhois.app      | `https://ipwhois.app/json/`           | city, country, isp, timezone…      | 10,000/mo               | ✅     |

**Quick test** (Dhaka example):
```js
fetch('https://cmp.inmobi.com/geoip').then(r => r.json()).then(console.log);
```




## ☀️ Weather – No API Key Required

| Service       | Endpoint Example (shortened)                              | Main features                        | Rate Limit / Notes              | Status     |
|---------------|-----------------------------------------------------------|--------------------------------------|---------------------------------|------------|
| Open-Meteo    | `api.open-meteo.com/v1/forecast?...`                      | Current + hourly + 16-day forecast   | Free, non-commercial, excellent | ✅ Best     |
| wttr.in       | `wttr.in/Dhaka?format=j1`                                 | Current + 3-day, nice JSON/terminal  | Very generous, no key           | ✅ Popular |
| 7Timer!       | `www.7timer.info/bin/api.pl?...&output=json`              | Simple civil/astro forecast          | Unlimited?, no key              | ✅ Working |


**Open-Meteo** (current weather + forecast – Dhaka):
```js
fetch('https://api.open-meteo.com/v1/forecast?latitude=23.81&longitude=90.41&current=temperature_2m,weather_code&daily=temperature_2m_max,temperature_2m_min&timezone=Asia%2FDhaka')
  .then(r => r.json())
  .then(console.log);
```

**wttr.in (simple one-liner):**
```js
curl "wttr.in/Dhaka?format=3"
# → Dhaka: ☁️ +24°C
```





---

⭐ If this list helps you – give it a star!  
