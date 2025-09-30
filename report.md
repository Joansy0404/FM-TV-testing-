# Stream Test Report

**Last update:** 2025-09-30 21:51 UTC
**Test method:** ffprobe
**Test scope:** vpn_only
**Test location:** Direct Connection

## Development Status & Key Findings

**Report Generated:** 2025-09-30 21:51 UTC
**Workflow Version:** 2.0 (Optimized FFprobe)

### Current Performance:

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
- **Connection:** Direct (no VPN)
- **Location:** GitHub Actions datacenter

### FFprobe Settings
**Direct Connection Configuration:**
- Connection timeout: 30 seconds (`-timeout 30000000`)
- Probe size: 3MB (`-probesize 3000000`)
- Analyze duration: 3 seconds (`-analyzeduration 3000000`)
- Subprocess timeout: 45 seconds (Python wrapper)
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

## Testing Methodology

**FFprobe Configuration:**
- Timeout: 30 seconds, Probe: 3MB, Analyze: 3s (Direct optimized)
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
| 2025-09-30 16:08 UTC | browser | Direct | 7 | 0 | 43 | 50 | 14.0% | HLS.js codec errors (48%) |
| 2025-09-30 16:40 UTC | ffprobe | Direct | 0 | 0 | 50 | 50 | 0.0% | Too aggressive settings |
| 2025-09-30 16:59 UTC | ffprobe | Direct | 29 | 1 | 20 | 50 | 58.0% | Balanced config working |
| 2025-09-30 18:01 UTC | ffprobe | UK VPN | 53 | 3 | 19 | 75 | 70.7% | Balanced config working |
| 2025-09-30 18:25 UTC | ffprobe | US VPN | 54 | 2 | 19 | 75 | 72.0% | Balanced config working |
| 2025-09-30 20:02 UTC | ffprobe | UK VPN | 136 | 378 | 95 | 609 | 22.3% |  |
| 2025-09-30 21:20 UTC | ffprobe | US VPN | 130 | 377 | 102 | 609 | 21.3% |  |

**Performance Insights:**
- FFprobe with balanced settings consistently outperforms browser (58% vs 14%)
- Overly aggressive optimization causes complete failure (0% success rate)
- Browser method limited by JavaScript codec support in HLS.js library
- Connection refused is dominant error (33% of failures) regardless of method


---
*Generated at 2025-09-30 21:51 UTC*

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
    }
  ]
}
-->
