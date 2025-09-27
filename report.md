# M3U Stream Status Report (Enhanced with Proxies)

**Generated on:** 2025-09-27 19:49:05 UTC
**Configuration:** VODs: Disabled, PPV: Disabled, FAST: Disabled
**Proxy Performance:** 0 working proxies found
**Timeout:** 5 seconds per stream

## Summary

| Metric | Count | Percentage |
|--------|-------|------------|
| **Total Streams Found** | 1634 | 100.0% |
| **Checked Streams** | 588 | 36.0% |
| **Working Streams** | 159 | 27.0% |
| **Failed Streams** | 429 | 73.0% |
| **Skipped Streams** | 1046 | 64.0% |

## Performance Breakdown

- **Regular Streams:** 159/465 working (34.2%)
- **Geo-blocked Streams:** 0/123 working (0.0%)

## Failure Analysis (429 total failures)

### Client Errors (4xx) (305 streams)
*Too many failures to list individually (305 total)*

### Not Found (404) (1 streams)
*Connection issues*

| Channel | Group | Error | Code |
|---------|-------|-------|------|
| DISNEY JR. | JP | failed | 404 |

### Other Errors (123 streams)
*Too many failures to list individually (123 total)*

## Skipped Streams (1046 total)

### FAST (120 skipped)
*Enable "Check FAST" in workflow dispatch to test these*

### PPV (53 skipped)
*Enable "Check PPV" in workflow dispatch to test these*

### VOD (873 skipped)
*Enable "Check VOD" in workflow dispatch to test these*

## Enhanced Configuration Notes

- **VOD Checking:** Disabled - URLs ending with #.mkv are VOD files
- **PPV/Event Checking:** Disabled - UK EVENTS & USA EVENTS groups automatically detected
- **FAST Checking:** Disabled - Groups containing 'FAST' automatically detected
- **Proxy Support:** Enabled - Enhanced geo-blocking bypass
- **Timeout:** 5 seconds per stream
- **Proxy Sources:** 2 sources tested
- **Proxy Testing:** Up to 50 proxies tested to find 15 working

## Manual Testing Options

To test specific content types:
1. Go to **Actions** → **Check M3U Streams with Enhanced Proxies** → **Run workflow**
2. Toggle **Check VODs** to test video-on-demand content
3. Toggle **Check PPV** to test Pay-Per-View channels
4. Toggle **Check FAST** to test Free Ad-Supported TV channels
5. Adjust **Target Working Proxies** (15-50 recommended for geo-blocked content)
6. Toggle **Use Proxies** to enable/disable proxy support
7. Toggle **Setup Tor** for additional anonymity

## Enhanced Features

- **Multi-Source Proxy Collection:** 2 different proxy sources
- **Fast Proxy Testing:** Optimized concurrent validation
- **Geo-blocking Detection:** Automatic identification of region-locked content
- **Smart Proxy Distribution:** Random proxy selection for each geo-blocked stream
- **Tor Integration:** Optional Tor SOCKS5 proxy support
- **Enhanced Error Analysis:** Better categorization of failure types
- **Adaptive Processing:** Configurable timeouts and limits
- **Unified Reporting:** All results in single report.md file

---
*Last updated: 2025-09-27 19:49:05 UTC*
*Enhanced report with proxy support*
