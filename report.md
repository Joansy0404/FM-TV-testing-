# IPTV Stream Validation Report

**Generated:** 2025-09-28 18:15 UTC  
**Duration:** 537.1s (9.0m)  
**Method:** Robust content validation (IPTV Checker methodology)  
**Sample:** 100 streams tested  

## Summary

- **✅ Working:** 13 streams (13.0%)
- **🔒 Geo-blocked:** 4 streams (4.0%)
- **❌ Failed:** 83 streams (83.0%)
- **📊 Total tested:** 100 streams

**Performance:** 0.2 streams/second with content validation

## Stream Type Analysis

| Type | Working | Geo-blocked | Failed | Total | Success Rate |
|------|---------|-------------|--------|-------|-------------|
| Channel | 13 | 4 | 83 | 100 | 13.0% |

## Sample Working Streams

| Channel | Type | Group |
|---------|------|---------|
| HUB PREMIER 2 | Channel | INT |
| BBC ALBA | Channel | UK |
| SKY SCI-FI | Channel | UK |
| U&ALIBI | Channel | UK |
| NATIONAL GEOGRAPHIC | Channel | UK |
| SUPERSPORT FOOTBALL | Channel | ZA |
| SKY SPORTS MAIN EVENT UHD | Channel | UK |
| U&GOLD | Channel | UK |
| TSN 4 | Channel | CA |
| ITV QUIZ | Channel | UK |
| VIRGIN MEDIA FOUR | Channel | IE |
| Global TV | Channel | CA |
| ALTITUDE SPORTS | Channel | USA |

## Geo-blocked Streams

| Channel | Type | Group |
|---------|------|---------|
| BLAZE | Channel | UK |
| TG 4 | Channel | IE |
| TV WAREHOUSE | Channel | UK |
| ORA NEWS | Channel | AL |

## Sample Failed Streams

| Channel | Type | Group |
|---------|------|---------|
| SKY CINEMA ACTION | Channel | UK |
| GAME SHOW NETWORK (EAST) | Channel | USA |
| RTÈ NEWS | Channel | IE |
| DISCOVERY KIDS | Channel | IN |
| AL ARABIYA | Channel | AE |
| CHARGE! | Channel | USA |
| HORSE & COUNTRY | Channel | UK |
| NOUR TV | Channel | AE |
| NICK JR. | Channel | USA |
| ITV 4 | Channel | UK |

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
*IPTV validation completed in 537.1 seconds*  
*Uses proven IPTV Checker methodology for accurate results*
