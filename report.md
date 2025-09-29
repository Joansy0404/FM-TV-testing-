# Auto-Alternating VPN Stream Test Report

**Last tested:** UK
**Last update:** 2025-09-29 07:40 UTC
**Test duration:** 25.4 minutes
**Sample size:** All streams
**Configuration:** VODs=No, PPV=No, FAST=No
**Total historical tests:** 3

## Latest Test Results

| Location | Working | Geo-blocked | Failed | Total | Success Rate | Timeouts | Conn Errors | Proxy Errors |
|----------|---------|-------------|--------|-------|--------------|----------|-------------|-------------|
| Direct | 116 | 330 | 116 | 562 | **20.6%** | 0 | 63 | 0 |
| UK VPN | 40 | 328 | 194 | 562 | **7.1%** | 0 | 0 | 0 |

## VPN Connection Details

- **Country:** GB
- **City:** London
- **IP:** 146.70.179.109
- **ISP:** AS9009 M247 Europe SRL

## Historical Performance

**UK VPN** (3 tests)
- Average: 2.4%
- Latest: 7.1%
- Range: 0.0% - 7.1%

**Latest VPN Impact:** -13.5% vs direct connection

## Recent Test History

| Date | Country | VPN Success | Direct Success | Impact | Duration |
|------|---------|-------------|----------------|--------|----------|
| 2025-09-29 06:24 UTC | UK | 0.0% | 18.5% | -18.5% | 18.8min |
| 2025-09-29 07:01 UTC | UK | 0.0% | 20.3% | -20.3% | 17.4min |
| 2025-09-29 07:40 UTC | UK | 7.1% | 20.6% | -13.5% | 25.4min |

## Working Streams Sample (40 total)

**UK** (12)
- 5 USA
- BBC ALBA
- BBC PARLIAMENT
- DMAX
- E4
- ... and 7 more

**USA** (28)
- ABC
- AMC (EAST)
- BIG TEN NETWORK
- BOOMERANG
- BUZZR
- ... and 23 more

## Geo-blocked Streams (328)

- QUEST+1 (UK)
- QVC (UK)
- QVC BEAUTY (UK)
- QVC EXTRA (UK)
- QVC STYLE (UK)
- RACING TV (UK)
- REALLY (UK)
- S4C (UK)
- SKY ARTS (UK)
- SKY ATLANTIC (UK)
- ... and 318 more

## Next Test

Next automatic test will use **US VPN**

---
*Report generated at 2025-09-29 07:40 UTC*
*Auto-alternates between UK and US ProtonVPN using ffprobe validation*

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
    }
  ]
}
-->
