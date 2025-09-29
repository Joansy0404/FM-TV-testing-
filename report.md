# VPN Stream Test Report

**Last tested:** UK
**Test method:** ffprobe
**Last update:** 2025-09-29 10:03 UTC
**Test duration:** 30.8 minutes
**Sample size:** 200
**Configuration:** VODs=No, PPV=No, FAST=No

## Latest Test Results

| Location | Working | Geo-blocked | Failed | Total | Success Rate |
|----------|---------|-------------|--------|-------|--------------|
| Direct | 145 | 4 | 51 | 200 | **72.5%** |
| UK VPN | 149 | 4 | 47 | 200 | **74.5%** |

## VPN Connection Details

- **Country:** GB
- **City:** London
- **IP:** 146.70.179.100
- **ISP:** AS9009 M247 Europe SRL

## Error Analysis

- **Connection refused**: 33 occurrences
- **HTTP 404 Not Found**: 5 occurrences
- **HTTP 403 Forbidden**: 4 occurrences
- **Server error (5xx)**: 3 occurrences
- **Invalid stream data**: 2 occurrences
- **HTTP 406 Not Acceptable**: 1 occurrences
- **[tcp @ 0x555cfec7df40] failed to resolve hostname hls.mskycdn.online: no address associated with hos**: 1 occurrences
- **HTTP 400 Bad Request**: 1 occurrences
- **[http @ 0x55c688d96f40] stream ends prematurely at 0, should be 18446744073709551615**: 1 occurrences

**VPN Impact:** +2.0% vs direct connection

## Working Streams via VPN (149 total)

**AE** (18)
- MBC ACTION
- MAJID
- SKY NEWS ARABIA
- MBC PERSIA
- WANASAH
- ... and 13 more

**AF** (5)
- DUNYA NAW TV
- BAHAR TV
- RTA EDUCATION
- Chekad TV
- KAYHAN TV

**AM** (3)
- ARMENIA 1
- ARMENIA 2
- FIRST CHANNEL NEWS

**AO** (2)
- MUZANGALA TV
- KK TV ANGOLA

**AR** (8)
- 5TV CORRIENTES
- ARGENTINÍSIMA SATELITAL
- CADENA 103
- CANAL 11 DE LA COSTA
- CANAL 13 LA RIOJA
- ... and 3 more

**AUS** (11)
- ABC TV SYDNEY
- ABC TV MELBOURNE
- ABC TV DARWIN
- ABC TV PLUS
- FOX SPORTS 501
- ... and 6 more

**CA** (2)
- CTV 2
- Fubo sports 1

**HK** (1)
- NOW SPORTS 1

**IE** (3)
- PREMIER SPORTS 1
- RTÈ ONE
- VIRGIN MEDIA FOUR

**JP** (1)
- DISNEY CHANNEL

## Next Test

Next automatic test will use **US VPN**

---
*Report generated at 2025-09-29 10:03 UTC*
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
    },
    {
      "date": "2025-09-29 09:16 UTC",
      "country": "UK",
      "method": "ffprobe",
      "ip": "149.40.63.139",
      "city": "London",
      "isp": "AS212238 Datacamp Limited",
      "config": "S:200,V:False,P:False,F:False",
      "duration_min": 28.5,
      "results": {
        "direct": {
          "working": 151,
          "geoblocked": 5,
          "failed": 44,
          "total": 200,
          "rate": 75.5
        },
        "vpn": {
          "working": 50,
          "geoblocked": 1,
          "failed": 149,
          "total": 200,
          "rate": 25.0
        }
      }
    },
    {
      "date": "2025-09-29 10:03 UTC",
      "country": "UK",
      "method": "ffprobe",
      "ip": "146.70.179.100",
      "city": "London",
      "isp": "AS9009 M247 Europe SRL",
      "config": "S:200,V:False,P:False,F:False",
      "duration_min": 30.8,
      "results": {
        "direct": {
          "working": 145,
          "geoblocked": 4,
          "failed": 51,
          "total": 200,
          "rate": 72.5
        },
        "vpn": {
          "working": 149,
          "geoblocked": 4,
          "failed": 47,
          "total": 200,
          "rate": 74.5
        }
      }
    }
  ]
}
-->
