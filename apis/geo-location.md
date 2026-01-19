# 🌍 Geo-location / IP to Location APIs

(Last checked: January 2026)

| # | Service                  | URL / Endpoint                            | Sample Response fields                              | Rate Limit              | Status     | Remark                                  |
|---|--------------------------|-------------------------------------------|-----------------------------------------------------|-------------------------|------------|-----------------------------------------|
| 1 | InMobi CMP GeoIP         | `https://cmp.inmobi.com/geoip`            | country, region, city                               | ? (very generous)       | ✅ Working | Very minimal & fast                     |
| 2 | ipapi.co                 | `https://ipapi.co/json/`                  | ip, city, region, country, latitude, timezone...   | 30,000 req/month        | ✅         | Very popular & reliable                 |
| 3 | ipinfo.io (no key)       | `https://ipinfo.io/json`                  | ip, city, region, country, loc, org...             | 50,000/month            | ✅         | Good data quality                       |
| 4 | freeipapi.com            | `https://freeipapi.com/api/json`          | ip, city, regionName, countryCode, lat, lon...     | Unlimited? (2025)       | ✅         | Includes currency & languages           |
| 5 | ipwhois.app              | `https://ipwhois.app/json/`               | ip, country, city, latitude, isp, timezone...      | 10,000/month            | ✅         | Nice response                           |
| 6 | ip.sb                    | `https://api.ip.sb/geoip`                 | country, region, city, latitude, longitude...      | Very generous           | ✅         | Simple & fast                           |

### Quick test snippet (fetch + JSON)

```js
fetch('https://cmp.inmobi.com/geoip')
  .then(r => r.json())
  .then(data => console.log(data))
// {
//   "country": "bgd",
//   "region": "c",
//   "city": "dhaka"
// }
