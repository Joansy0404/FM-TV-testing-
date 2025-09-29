# VPN Stream Test Report

**Last tested:** UK
**Test method:** ffprobe
**Last update:** 2025-09-29 08:42 UTC
**Test duration:** 12.0 minutes
**Sample size:** 100
**Configuration:** VODs=No, PPV=No, FAST=No

## Latest Test Results

| Location | Working | Geo-blocked | Failed | Total | Success Rate |
|----------|---------|-------------|--------|-------|--------------|
| Direct | 73 | 2 | 25 | 100 | **73.0%** |
| UK VPN | 25 | 0 | 75 | 100 | **25.0%** |

## VPN Connection Details

- **Country:** GB
- **City:** London
- **IP:** 149.50.209.148
- **ISP:** AS212238 Datacamp Limited

## Error Analysis

- **SSL/TLS error**: 39 occurrences
- **Unknown error**: 29 occurrences
- **HTTP 404 Not Found**: 3 occurrences
- **http://alt.xtream-ie.org/abn1j1otrse/vvtbgggms/1eyj1cmwioiaiahr0cdovlzg0lje3lju1lje4ntoxnda3mi8ilcai**: 1 occurrences
- **Connection timeout**: 1 occurrences
- **http://alt.xtream-ie.org/abn1j1otrse/vvtbgggms/1eyj1cmwioiaiahr0chm6ly9obhmubxnrewnkbi5vbmxpbmuvdhyv**: 1 occurrences
- **http://alt.xtream-ie.org/abn1j1otrse/vvtbgggms/1eyj1cmwioiaiahr0cdovlze4ns45os4xmzyunta6otk4ms9zdhjl**: 1 occurrences

**VPN Impact:** -48.0% vs direct connection

## Working Streams via VPN (25 total)

**AE** (1)
- MBC ACTION

**AR** (2)
- 5TV CORRIENTES
- CADENA 103

**AUS** (1)
- FOX SPORTS 501

**IE** (2)
- PREMIER SPORTS 1
- RTÈ ONE

**NZ** (1)
- SKY SPORT 9

**UK** (6)
- SKY CINEMA SCI-FI HORROR
- NATIONAL GEOGRAPHIC
- E4
- TOGETHER TV
- SKY WITNESS
- ... and 1 more

**USA** (10)
- CINEMAX HITS
- AMC (EAST)
- LIFETIME MOVIE NETWORK (EAST)
- IFC
- MSG
- ... and 5 more

**ZA** (2)
- SUPERSPORT GRANDSTAND
- SUPERSPORT VARIETY 1

## Next Test

Next automatic test will use **US VPN**

---
*Report generated at 2025-09-29 08:42 UTC*
*Test method: ffprobe | Auto-alternates between UK and US ProtonVPN*

<!-- HISTORY
{
  "tests": [
    {
      "date": "2025-09-29 06:24 UTC",
      "country": "UK",
      "ip": "149.40.48.73",
      "city": "London",
      "isp": "AS212238 Datacamp Limited",
      "config": "S:All,V:False,P:False,F:False",
      "duration_min": 18.8,
      "results": {
        "direct": {
          "working": 104,
          "geoblocked": 331,
          "failed": 127,
          "total": 562,
          "rate": 18.505338078291814
        },
        "vpn": {
          "working": 0,
          "geoblocked": 0,
          "failed": 562,
          "total": 562,
          "rate": 0.0
        }
      }
    },
    {
      "date": "2025-09-29 07:01 UTC",
      "country": "UK",
      "ip": "154.47.24.199",
      "city": "London",
      "isp": "AS212238 Datacamp Limited",
      "config": "S:All,V:False,P:False,F:False",
      "duration_min": 17.4,
      "results": {
        "direct": {
          "working": 114,
          "geoblocked": 330,
          "failed": 118,
          "total": 562,
          "rate": 20.284697508896798,
          "timeouts": 0,
          "connection_errors": 61
        },
        "vpn": {
          "working": 0,
          "geoblocked": 0,
          "failed": 562,
          "total": 562,
          "rate": 0.0,
          "timeouts": 0,
          "connection_errors": 0
        }
      }
    },
    {
      "date": "2025-09-29 07:40 UTC",
      "country": "UK",
      "ip": "146.70.179.109",
      "city": "London",
      "isp": "AS9009 M247 Europe SRL",
      "config": "S:All,V:False,P:False,F:False",
      "duration_min": 25.4,
      "results": {
        "direct": {
          "working": 116,
          "geoblocked": 330,
          "failed": 116,
          "total": 562,
          "rate": 20.640569395017792,
          "timeouts": 0,
          "connection_errors": 63,
          "proxy_errors": 0
        },
        "vpn": {
          "working": 40,
          "geoblocked": 328,
          "failed": 194,
          "total": 562,
          "rate": 7.11743772241993,
          "timeouts": 0,
          "connection_errors": 0,
          "proxy_errors": 0
        }
      }
    },
    {
      "date": "2025-09-29 08:42 UTC",
      "country": "UK",
      "method": "ffprobe",
      "ip": "149.50.209.148",
      "city": "London",
      "isp": "AS212238 Datacamp Limited",
      "config": "S:100,V:False,P:False,F:False",
      "duration_min": 12.0,
      "results": {
        "direct": {
          "working": 73,
          "geoblocked": 2,
          "failed": 25,
          "total": 100,
          "rate": 73.0
        },
        "vpn": {
          "working": 25,
          "geoblocked": 0,
          "failed": 75,
          "total": 100,
          "rate": 25.0
        }
      }
    }
  ]
}
-->
