# Auto-Alternating VPN Stream Test Report

**Last tested:** UK
**Last update:** 2025-09-29 07:01 UTC
**Test duration:** 17.4 minutes
**Sample size:** All streams
**Configuration:** VODs=No, PPV=No, FAST=No
**Total historical tests:** 2

## Latest Test Results

| Location | Working | Geo-blocked | Failed | Total | Success Rate | Timeouts | Conn Errors |
|----------|---------|-------------|--------|-------|--------------|----------|-------------|
| Direct | 114 | 330 | 118 | 562 | **20.3%** | 0 | 61 |
| UK VPN | 0 | 0 | 562 | 562 | **0.0%** | 0 | 0 |

## VPN Connection Details

- **Country:** GB
- **City:** London
- **IP:** 154.47.24.199
- **ISP:** AS212238 Datacamp Limited

## Historical Performance

**UK VPN** (2 tests)
- Average: 0.0%
- Latest: 0.0%
- Range: 0.0% - 0.0%

**Latest VPN Impact:** -20.3% vs direct connection

## Recent Test History

| Date | Country | VPN Success | Direct Success | Impact | Duration |
|------|---------|-------------|----------------|--------|----------|
| 2025-09-29 06:24 UTC | UK | 0.0% | 18.5% | -18.5% | 18.8min |
| 2025-09-29 07:01 UTC | UK | 0.0% | 20.3% | -20.3% | 17.4min |

## Next Test

Next automatic test will use **US VPN**

---
*Report generated at 2025-09-29 07:01 UTC*
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
    }
  ]
}
-->
