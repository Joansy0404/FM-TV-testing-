# IPTV Stream Validation Report

**Generated:** 2025-09-28 18:33 UTC  
**Duration:** 409.8s (6.8m)  
**Method:** Robust content validation (IPTV Checker methodology)  
**Sample:** 100 streams tested  

## Summary

- **✅ Working:** 19 streams (19.0%)
- **🔒 Geo-blocked:** 4 streams (4.0%)
- **❌ Failed:** 77 streams (77.0%)
- **📊 Total tested:** 100 streams

**Performance:** 0.2 streams/second with content validation

## Stream Type Analysis

| Type | Working | Geo-blocked | Failed | Total | Success Rate |
|------|---------|-------------|--------|-------|-------------|
| Channel | 19 | 4 | 77 | 100 | 19.0% |

## Sample Working Streams

| Channel | Type | Group |
|---------|------|---------|
| SUPERSPORT FOOTBALL | Channel | ZA |
| VIRGIN MEDIA TWO | Channel | IE |
| LALIGA TV | Channel | UK |
| SKY SCI-FI | Channel | UK |
| QUEST+1 | Channel | UK |
| SPECTRUM SPORTSNET | Channel | USA |
| DISCOVERY | Channel | UK |
| SKY SPORT 6 | Channel | NZ |
| SKY SPORTS MAIN EVENT UHD | Channel | UK |
| NOW SPORTS 1 | Channel | HK |
| HUB PREMIER 2 | Channel | INT |
| SKY SPORT 5 | Channel | NZ |
| SKY SPORTS MAIN EVENT | Channel | UK |
| SKY WITNESS | Channel | UK |
| MSNBC | Channel | USA |

## Geo-blocked Streams

| Channel | Type | Group |
|---------|------|---------|
| BLAZE | Channel | UK |
| FOX SPORTS 506 | Channel | AUS |
| ORA NEWS | Channel | AL |
| RTÈ 2 | Channel | IE |

## Sample Failed Streams

| Channel | Type | Group |
|---------|------|---------|
| MTV 2 | Channel | USA |
| 5 USA | Channel | UK |
| U&DAVE | Channel | UK |
| PEACE TV ENGLISH | Channel | AE |
| SKY SPORTS CRICKET | Channel | UK |
| LOVE NATURE | Channel | USA |
| AL SHARQIYA MIN KABLA | Channel | AE |
| METV | Channel | USA |
| MAGNOLIA NETWORK | Channel | USA |
| NATIONAL GEOGRAPHIC (EAST) | Channel | USA |

## Validation Methodology

This checker uses robust IPTV validation techniques:

- **Content Validation:** Downloads 500KB of actual stream data
- **Content-Type Checking:** Validates IPTV-specific MIME types
- **Retry Logic:** 10s initial timeout, 15s extended
- **Geo-blocking Detection:** Identifies HTTP 403, 451, 426 status codes
- **Rate Limit Handling:** Automatic retry with delays
- **Streaming Verification:** Tests actual data flow, not just HTTP responses

## Configuration

- **Content Types:** Channels only
- **Timeouts:** 10s initial, 15s extended
- **Sample Size:** 100
- **Validation Threshold:** 500KB minimum data

---
*IPTV validation completed in 409.8 seconds*  
*Uses proven IPTV Checker methodology for accurate results*
