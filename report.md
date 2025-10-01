# Stream Test Report

**Last update:** 2025-10-01 20:30 UTC
**Test method:** ffprobe
**Test scope:** vpn_only
**Test location:** US VPN

## Development Status & Key Findings

**Report Generated:** 2025-10-01 20:30 UTC
**Workflow Version:** 2.0 (Optimized FFprobe)

### Current Performance:
- **VPN Test (US)**: 223/609 working (36.6%)

### What We Know Works:
- **FFprobe method**: 58% success rate on direct connection (validated 2025-09-30)
- **Optimal Configuration**: 3MB probe (direct) / 5MB probe (VPN), 3-5s analyze, 30-45s timeout
- **Test delay**: 0.3s between streams (fast without overwhelming servers)
- **Browser method**: Only 14% success - NOT suitable for these streams
- **Root cause**: Browser gets `manifestIncompatibleCodecsError` (48.8%) - HLS.js cannot transmux stream codecs

### Critical Lessons Learned:
1. **Too aggressive FFprobe settings FAIL**: 32K probe + 0s analyze = 0% success
2. **Balanced settings WORK**: 3-5MB probe + 3-5s analyze = 58% success
3. **Browser testing is wrong tool**: Streams use MPEG-TS or codecs HLS.js can't handle
4. **Main failure patterns**: Connection refused (33%), timeouts (5%), geo-blocking (2%)
5. **Speed vs accuracy**: Balanced settings complete 50 streams in ~1.5 minutes

### Known Issues & Next Steps:
- [ ] **Connection Refused (33% of failures)**: Servers offline, blocking, or rate-limiting
- [ ] **Test VPN performance**: Compare geo-blocking patterns US vs UK
- [ ] **Layer 2 validation**: Consider adding manifest parser (hls-monitor/pyhls)
- [ ] **Retry strategy**: Test failed streams with higher timeouts (60s)
- [ ] **Hybrid mode**: Test if browser can rescue specific FFprobe failure types
- [ ] **Expand testing**: Move from 50-stream sample to full 600+ playlist

## Technical Configuration

### Test Parameters
- **Sample size:** 0
- **VODs enabled:** false
- **PPV enabled:** false
- **FAST enabled:** false
- **Test delay:** 0.3 seconds between streams

### Environment
- **Runner:** ubuntu-latest (GitHub Actions)
- **Python:** 3.x
- **FFmpeg/FFprobe:** Latest (apt-get)
- **VPN Provider:** ProtonVPN via Gluetun
- **VPN Country:** US
- **VPN City:** New York
- **Connected IP:** 185.98.169.37
- **Verified Location:** San Jose
- **ISP:** AS212238 Datacamp Limited
- **Container:** python:3.11-slim (Docker)
- **Network:** Shared namespace with Gluetun container

### FFprobe Settings
**VPN Configuration:**
- Connection timeout: 45 seconds (`-timeout 45000000`)
- Probe size: 5MB (`-probesize 5000000`)
- Analyze duration: 5 seconds (`-analyzeduration 5000000`)
- Subprocess timeout: 60 seconds (Python wrapper)
- Stream selection: Video stream 0 only (`-select_streams v:0`)
- Output format: JSON (`-of json`)
- Verbosity: Errors only (`-v error`)
- User-Agent: Chrome 131 on Windows
- Headers: Referer set to google.com

**Rationale:**
- Balanced settings proven to work (58% success rate)
- VPN gets higher timeouts/probe due to latency
- Avoids aggressive optimization that caused 0% success

## Playlist & Stream Information

### Source File
- **Filename:** `channel playlist.m3u`
- **Format:** Extended M3U with metadata
- **Total streams:** ~1776 (before filtering)
- **Location:** Repository root

### Stream Composition
- **Live TV Channels:** Majority of content
- **VOD Files:** URLs ending with `#.mkv`
- **PPV Events:** Boxing, UFC, WWE, special events
- **FAST Channels:** Free Ad-Supported TV

### Geographic Distribution
Streams from 20+ countries including:
- **North America:** USA (largest), CA
- **Europe:** UK, FR, DE, NL, IT, ES
- **Oceania:** AUS, NZ
- **Middle East:** AE, SA, YE
- **Africa:** ZA
- **South America:** BR, AR
- **Asia:** AL

### Common Stream Characteristics
- **Protocol:** HLS (HTTP Live Streaming)
- **Container:** Mix of MPEG-TS and fMP4
- **Codecs:** H.264, H.265, various audio codecs
- **URL Pattern:** Proxy URLs to alt.xtream-ie.org
- **Authentication:** Some require tokens/headers

### Typical Failure Patterns
Based on historical testing:
1. **Connection Refused (30-35%)**: Servers offline, blocking automation, or overloaded
2. **Geo-blocking (2-5%)**: HTTP 403/401, varies by test location
3. **Not Found (5-10%)**: HTTP 404, moved or deleted content
4. **Timeouts (5-15%)**: Slow/unresponsive servers, network issues
5. **Invalid Data**: Malformed streams, codec issues

## Latest Test Results

| Location | Working | Geo-blocked | Failed | Total | Success Rate |
|----------|---------|-------------|--------|-------|--------------|
| US VPN | 223 | 356 | 30 | 609 | **36.6%** |

## Error Analysis

**Total failed streams:** 30

### Error Categories

- **Timeouts:** 1 (0.3%)
- **Authentication/Permission:** 356 (91.8%)
- **Not Found (404):** 26 (6.7%)
- **Connection Errors:** 1 (0.3%)

### Top 10 Error Messages

1. **HTTP 403/401 (all UAs failed)** - 356 occurrences (91.8%)
2. **HTTP 404 Not Found** - 26 occurrences (6.7%)
3. **FFprobe timeout (60s, all UAs)** - 1 occurrences (0.3%)
4. **Connection refused (all UAs)** - 1 occurrences (0.3%)
5. ** (UA2: ExoPlayer)** - 1 occurrences (0.3%)
6. ** (UA5: Mozilla)** - 1 occurrences (0.3%)
7. **Invalid stream data (all UAs)** - 1 occurrences (0.3%)
8. **http://alt.xtream-ie.org/abn1j1otrse/vvtbgggms/1eyj1cmwioiaiahr0chm6ly9ha216zwqu** - 1 occurrences (0.3%)

## Failed Streams Details

Streams that failed testing (for investigation):

- **BET SOUL** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9mbDcubW92ZW9uam95LmNvbS9CRVRf...`
- **CNBC** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9hMXhzLnZpcC8zMDAwMDkiLCAiaWQi...`
- **DISNEY JR.** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9mbDcubW92ZW9uam95LmNvbS9ESVNO...`
- **ESPN** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9hMXhzLnZpcC80MDAwMDAxMSIsICJp...`
- **ESPN 2** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly93b3JsZC1wcm94aWZpZXIueHl6L2Rh...`
- **ESPNEWS** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9hMXhzLnZpcC80MDAwMDAxNCIsICJp...`
- **FOX SOUL** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9mbDcubW92ZW9uam95LmNvbS9GT1hf...`
- **FS2** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9hMXhzLnZpcC80MDAwMDAyMiIsICJp...`
- **HALLMARK MOVIES & MYSTERY** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9mbDcubW92ZW9uam95LmNvbS9IQUxM...`
- **HGTV** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9mbDcubW92ZW9uam95LmNvbS9IR1RW...`
- **MSNBC** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9hMXhzLnZpcC8zMDAwMDgiLCAiaWQi...`
- **SHOWTIME NEXT** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9mbDcubW92ZW9uam95LmNvbS9TSE9X...`
- **SHOWTIME WOMEN** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9mbDcubW92ZW9uam95LmNvbS9TSE9X...`
- **START TV** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9mbDcubW92ZW9uam95LmNvbS9TdGFy...`
- **STARZ ENCORE CLASSIC** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9mbDcubW92ZW9uam95LmNvbS9TVEFS...`
- **TLC** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9mbDcubW92ZW9uam95LmNvbS9UTEMv...`
- **WILLOW 2** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9hMXhzLnZpcC80MDAwMDA0MyIsICJp...`
- **THE MOVIE CHANNEL** (Group: USA)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9lMi50aGV0dmFwcC50by9obHMvVGhl...`
- **AL JAZEERA ENGLISH** (Group: UK)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cDovLzE4NS45OS4xMzYuNTA6OTk4MS9zdHJl...`
- **BBC SCOTLAND** (Group: UK)
  - URL: `http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cDovLzE4NS45OS4xMzYuNTA6OTk4MS9zdHJl...`

*...and 10 more failed streams*

## Geo-blocked Streams (Sample)

Total geo-blocked: 356

- ESPN U (Group: USA)
- NESN UHD (Group: USA)
- BLAZE (Group: UK)
- QUEST RED (Group: UK)
- QUEST+1 (Group: UK)
- QVC (Group: UK)
- QVC BEAUTY (Group: UK)
- QVC EXTRA (Group: UK)
- QVC STYLE (Group: UK)
- RACING TV (Group: UK)

*...and 346 more*

## Testing Methodology

**FFprobe Configuration:**
- Timeout: 45 seconds, Probe: 5MB, Analyze: 5s (VPN optimized)
- Validates: Stream accessibility and codec detection
- Trade-off: Balanced between speed and compatibility

**Why These Settings:**
- Too aggressive (32K probe, 0s analyze) = 0% success (tested 2025-09-30 16:40 UTC)
- Balanced (3-5MB probe, 3-5s analyze) = 58% success (tested 2025-09-30 16:59 UTC)
- Streams need analysis time to recognize MPEG-TS format and extract codecs
- Browser method averages 14% due to HLS.js codec transmuxing limitations

### Historical Performance Analysis

| Date & Time | Method | Location | Working | Geo-blocked | Failed | Total | Rate | Configuration Notes |
|-------------|--------|----------|---------|-------------|--------|-------|------|---------------------|
| 2025-09-30 20:02 UTC | ffprobe | UK VPN | 136 | 378 | 95 | 609 | 22.3% |  |
| 2025-09-30 21:20 UTC | ffprobe | US VPN | 130 | 377 | 102 | 609 | 21.3% |  |
| 2025-09-30 22:58 UTC | ffprobe | US VPN | 130 | 377 | 102 | 609 | 21.3% |  |
| 2025-10-01 03:48 UTC | ffprobe | UK VPN | 137 | 376 | 96 | 609 | 22.5% |  |
| 2025-10-01 08:41 UTC | ffprobe | US VPN | 167 | 338 | 104 | 609 | 27.4% |  |
| 2025-10-01 14:47 UTC | ffprobe | UK VPN | 137 | 377 | 95 | 609 | 22.5% |  |
| 2025-10-01 20:30 UTC | ffprobe | US VPN | 223 | 356 | 30 | 609 | 36.6% |  |

**Performance Insights:**
- FFprobe with balanced settings consistently outperforms browser (58% vs 14%)
- Overly aggressive optimization causes complete failure (0% success rate)
- Browser method limited by JavaScript codec support in HLS.js library
- Connection refused is dominant error (33% of failures) regardless of method

## Recommendations

- High geo-blocking rate from this location
- Consider testing from alternative VPN regions

---
*Generated at 2025-10-01 20:30 UTC*

<!-- HISTORY
{
  "tests": [
    {
      "date": "2025-09-30 10:41 UTC",
      "country": "UK",
      "scope": "unknown"
    },
    {
      "date": "2025-09-30 11:19 UTC",
      "country": "US",
      "scope": "unknown",
      "vpn": {
        "working": 138,
        "geoblocked": 377,
        "failed": 94,
        "rate": 22.660098522167488
      }
    },
    {
      "date": "2025-09-30 13:24 UTC",
      "country": "UK",
      "scope": "unknown",
      "vpn": {
        "working": 114,
        "geoblocked": 3,
        "failed": 33,
        "rate": 76.0
      }
    },
    {
      "date": "2025-09-30 14:02 UTC",
      "country": "US",
      "scope": "unknown"
    },
    {
      "date": "2025-09-30 15:08 UTC",
      "country": "UK",
      "method": "unknown",
      "scope": "unknown",
      "vpn": {
        "working": 21,
        "geoblocked": 0,
        "failed": 129,
        "rate": 14.000000000000002
      }
    },
    {
      "date": "2025-09-30 15:39 UTC",
      "country": "US",
      "method": "browser",
      "scope": "vpn_only"
    },
    {
      "date": "2025-09-30 15:46 UTC",
      "country": "UK",
      "method": "browser",
      "scope": "vpn_only"
    },
    {
      "date": "2025-09-30 15:53 UTC",
      "country": "US",
      "method": "browser",
      "scope": "direct_only"
    },
    {
      "date": "2025-09-30 16:08 UTC",
      "country": "UK",
      "method": "browser",
      "scope": "direct_only",
      "direct": {
        "working": 7,
        "geoblocked": 0,
        "failed": 43,
        "rate": 14.000000000000002
      }
    },
    {
      "date": "2025-09-30 16:37 UTC",
      "country": "US",
      "method": "ffprobe",
      "scope": "vpn_only"
    },
    {
      "date": "2025-09-30 16:40 UTC",
      "country": "UK",
      "method": "ffprobe",
      "scope": "direct_only",
      "direct": {
        "working": 0,
        "geoblocked": 0,
        "failed": 50,
        "rate": 0.0
      }
    },
    {
      "date": "2025-09-30 16:59 UTC",
      "country": "US",
      "method": "ffprobe",
      "scope": "direct_only",
      "direct": {
        "working": 29,
        "geoblocked": 1,
        "failed": 20,
        "rate": 57.99999999999999
      }
    },
    {
      "date": "2025-09-30 18:01 UTC",
      "country": "UK",
      "method": "ffprobe",
      "scope": "vpn_only",
      "vpn": {
        "working": 53,
        "geoblocked": 3,
        "failed": 19,
        "rate": 70.66666666666667
      }
    },
    {
      "date": "2025-09-30 18:25 UTC",
      "country": "US",
      "method": "ffprobe",
      "scope": "direct_and_vpn",
      "vpn": {
        "working": 54,
        "geoblocked": 2,
        "failed": 19,
        "rate": 72.0
      }
    },
    {
      "date": "2025-09-30 20:02 UTC",
      "country": "UK",
      "method": "ffprobe",
      "scope": "vpn_only",
      "vpn": {
        "working": 136,
        "geoblocked": 378,
        "failed": 95,
        "rate": 22.33169129720854
      }
    },
    {
      "date": "2025-09-30 21:20 UTC",
      "country": "US",
      "method": "ffprobe",
      "scope": "vpn_only",
      "vpn": {
        "working": 130,
        "geoblocked": 377,
        "failed": 102,
        "rate": 21.34646962233169
      }
    },
    {
      "date": "2025-09-30 21:51 UTC",
      "country": "UK",
      "method": "ffprobe",
      "scope": "vpn_only"
    },
    {
      "date": "2025-09-30 22:01 UTC",
      "country": "US",
      "method": "ffprobe",
      "scope": "vpn_only"
    },
    {
      "date": "2025-09-30 22:03 UTC",
      "country": "UK",
      "method": "ffprobe",
      "scope": "vpn_only"
    },
    {
      "date": "2025-09-30 22:58 UTC",
      "country": "US",
      "method": "ffprobe",
      "scope": "vpn_only",
      "vpn": {
        "working": 130,
        "geoblocked": 377,
        "failed": 102,
        "rate": 21.34646962233169
      }
    },
    {
      "date": "2025-10-01 03:48 UTC",
      "country": "UK",
      "method": "ffprobe",
      "scope": "vpn_only",
      "vpn": {
        "working": 137,
        "geoblocked": 376,
        "failed": 96,
        "rate": 22.495894909688012
      }
    },
    {
      "date": "2025-10-01 08:41 UTC",
      "country": "US",
      "method": "ffprobe",
      "scope": "vpn_only",
      "vpn": {
        "working": 167,
        "geoblocked": 338,
        "failed": 104,
        "rate": 27.42200328407225
      }
    },
    {
      "date": "2025-10-01 14:47 UTC",
      "country": "UK",
      "method": "ffprobe",
      "scope": "vpn_only",
      "vpn": {
        "working": 137,
        "geoblocked": 377,
        "failed": 95,
        "rate": 22.495894909688012
      }
    },
    {
      "date": "2025-10-01 20:30 UTC",
      "country": "US",
      "method": "ffprobe",
      "scope": "vpn_only",
      "vpn": {
        "working": 223,
        "geoblocked": 356,
        "failed": 30,
        "rate": 36.61740558292282
      }
    }
  ]
}
-->
