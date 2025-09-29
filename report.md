# Auto-Alternating VPN Stream Test Report

**Last tested:** UK
**Last update:** 2025-09-29 06:24 UTC
**Test duration:** 18.8 minutes
**Sample size:** All streams
**Configuration:** VODs=No, PPV=No, FAST=No
**Total historical tests:** 1

## Latest Test Results

| Location | Working | Geo-blocked | Failed | Total | Success Rate |
|----------|---------|-------------|--------|-------|-------------|
| Direct | 104 | 331 | 127 | 562 | **18.5%** |
| UK VPN | 0 | 0 | 562 | 562 | **0.0%** |

## VPN Connection Details

- **Country:** GB
- **City:** London
- **IP:** 149.40.48.73
- **ISP:** AS212238 Datacamp Limited

## Historical Performance

**UK VPN** (1 tests)
- Average: 0.0%
- Latest: 0.0%
- Range: 0.0% - 0.0%

**Latest VPN Impact:** -18.5% vs direct connection

## Recent Test History

| Date | Country | VPN Success | Direct Success | Impact | Duration |
|------|---------|-------------|----------------|--------|----------|
| 2025-09-29 06:24 UTC | UK | 0.0% | 18.5% | -18.5% | 18.8min |

## Next Test

Next automatic test will use **US VPN**

---
*Report generated at 2025-09-29 06:24 UTC*
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
    }
  ]
}
-->
