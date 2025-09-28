# FFmpeg-Enhanced IPTV Stream Validation Report

**Generated:** 2025-09-28 20:26 UTC  
**Duration:** 1105.0s (18.4m)  
**Method:** Two-pass validation (HTTP + FFmpeg verification)  
**Sample:** 500 streams tested  

## Executive Summary

- **✅ Verified Working:** 0 streams (0.0%)
- **🔒 Geo-blocked:** 269 streams (53.8%)
- **❌ HTTP Failed:** 183 streams (36.6%)
- **⚠️ FFmpeg Failed:** 48 streams (9.6%)
- **📊 Total Tested:** 500 streams

## Validation Pipeline Analysis

| Stage | Passed | Failed | Success Rate | Notes |
|-------|--------|--------|-------------|--------|
| HTTP Validation | 48 | 452 | 9.6% | Content download + type validation |
| FFmpeg Verification | 0 | 48 | 0.0% | Actual video stream validation |
| **Overall Pipeline** | **0** | **500** | **0.0%** | **End-to-end accuracy** |

**Performance:** 0.45 streams/sec HTTP validation, 0.04 streams/sec FFmpeg verification

## Stream Type Analysis

| Type | Verified Working | Geo-blocked | HTTP Failed | FFmpeg Failed | Total | Success Rate |
|------|-----------------|-------------|-------------|---------------|-------|-------------|
| Channel | 0 | 269 | 183 | 48 | 500 | 0.0% |

## FFmpeg Verification Failures

*These streams passed HTTP validation but failed FFmpeg verification (false positives)*

| Channel | Type | Group | Error Reason |
|---------|------|-------|---------------|
| E4 | Channel | UK | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |
| TNT SPORTS 5 | Channel | UK | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |
| TNT SPORTS ULTIMATE | Channel | UK | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |
| ALTITUDE SPORTS | Channel | USA | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |
| NATIONAL GEOGRAPHIC WILD | Channel | UK | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |
| CTV 2 | Channel | CA | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |
| HUB PREMIER 2 | Channel | INT | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |
| SPECTRUM SPORTSNET | Channel | USA | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |
| TOGETHER TV | Channel | UK | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |
| MUTV | Channel | UK | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |
| SUPERSPORT RUGBY | Channel | ZA | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |
| LFCTV | Channel | UK | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |
| TSN 4 | Channel | CA | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |
| U&ALIBI | Channel | UK | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |
| FOX SPORTS 501 | Channel | AUS | FFmpeg failed: ffmpeg version 6.1.1-3ubuntu5 Copyr |

**Total FFmpeg failures:** 48 streams
**Timeout failures:** 0 streams
**Error failures:** 48 streams

## Geo-blocked Streams

| Channel | Type | Group | HTTP Status |
|---------|------|-------|-------------|
| BLAZE | Channel | UK | 403 |
| FOX SPORTS 506 | Channel | AUS | 403 |
| TV WAREHOUSE | Channel | UK | 403 |
| DISNEY JR. | Channel | JP | 403 |
| NESN | Channel | USA | 403 |
| RACING TV | Channel | UK | 403 |
| REPORT TV | Channel | AL | 403 |
| SKY NEWS EXTRA 2 | Channel | AUS | 403 |
| TV BRICS AFRICA | Channel | ZA | 403 |
| SKY SPORT 4 | Channel | NZ | 403 |

## Technical Analysis & Recommendations

**False Positive Analysis:**
- HTTP validation passed: 48 streams
- FFmpeg verification failed: 48 streams
- False positive rate: 100.0%

**High False Positive Rate Detected (100.0%)**
- Many streams are returning non-video content (HTML pages, errors, etc.)
- HTTP validation needs stricter content analysis
- FFmpeg verification is essential for accuracy

**Low Success Rate Analysis (0.0%)**
- Most streams appear to be offline or problematic
- Consider testing different stream sources
- Check if proxy/geo-unblocking is needed

**Optimization Recommendations:**
- Implement stricter HTTP content validation to reduce false positives
- Consider adding proxy support for geo-blocked content

## Validation Methodology

**Two-Pass Validation Process:**

1. **HTTP Validation (Phase 1):**
   - Downloads 500KB of stream data
   - Validates IPTV-specific content types
   - Detects HTML error pages and non-video content
   - Identifies geo-blocking (HTTP 403, 451, 426)
   - 10s initial, 15s extended timeout

2. **FFmpeg Verification (Phase 2):**
   - Only tests streams that passed HTTP validation
   - Attempts to decode actual video stream for 5 seconds
   - Eliminates false positives from HTTP validation
   - Extracts detailed video/audio information
   - 15 second timeout per verification

**Key Improvements Over Basic Methods:**
- Eliminates false positives from error pages
- Provides actual video codec and resolution information
- Confirms streams contain decodable video data
- Two-tier approach balances speed with accuracy

## Configuration Details

- **Content Types:** Channels only
- **HTTP Timeouts:** 10s initial, 15s extended
- **FFmpeg Timeout:** 15s per verification
- **Sample Size:** 500
- **Data Threshold:** 500KB minimum for HTTP validation
- **FFmpeg Version:** 6.1.1-3ubuntu5

## Debugging Information

**For further optimization, consider:**
- **Proxy Integration:** Add proxy support for 269 geo-blocked streams
- **Content Analysis:** Enhance HTTP validation to reduce 48 false positives
- **Provider Grouping:** Group by actual stream providers for targeted testing
- **Timeout Optimization:** Current FFmpeg timeout may be too conservative
- **Batch Processing:** Parallel FFmpeg verification could improve speed

**FFmpeg Error Patterns:**
- Other: 48 streams

---
*FFmpeg-enhanced validation completed in 1105.0 seconds*  
*Two-pass methodology ensures high accuracy with detailed stream analysis*  
*False positive rate: 100.0% (HTTP pass, FFmpeg fail)*
