# 🎯 Free Public APIs

Collection of **currently working** free public APIs that don't require authentication, API keys, or have extremely generous free tiers (updated January 2026).

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
