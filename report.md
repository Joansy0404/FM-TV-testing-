# Improved IPTV Stream Validation Report

**Generated:** 2025-09-28 21:24 UTC  
**Duration:** 2464.4s (41.1m)  
**Method:** Multi-method validation (connectivity + HTTP + ffprobe)  
**Sample:** 500 streams tested  
**Debug Mode:** Enabled  

## Executive Summary

- **✅ Working Streams:** 216 (43.2%)
- **🔒 Geo-blocked:** 6 (1.2%)
- **❌ Failed Streams:** 278 (55.6%)
- **📊 Total Tested:** 500 streams

## Validation Method Analysis

- **HTTP:** 61 streams (28.2%)
- **FFPROBE:** 155 streams (71.8%)

**FFprobe Confirmation:** 57/216 streams (26.4%)

## Working Streams Sample

| Channel | Type | Method | FFprobe | User Agent | Group |
|---------|------|--------|---------|------------|--------|
| FOX SPORTS 501 | Channel | http | ✓ | VLC/3.0.12 LibV | AUS |
| ARTN TV | Channel | ffprobe | ✗ | Unknown | AM |
| TV BRICS AFRICA | Channel | ffprobe | ✗ | Unknown | ZA |
| QUEST+1 | Channel | http | ✓ | VLC/3.0.12 LibV | UK |
| LIFETIME MOVIE NETWORK (E | Channel | ffprobe | ✗ | Unknown | USA |
| NATIONAL GEOGRAPHIC (EAST | Channel | ffprobe | ✗ | Unknown | USA |
| Chekad TV | Channel | ffprobe | ✗ | Unknown | AF |
| DUBAI TV | Channel | ffprobe | ✗ | Unknown | AE |
| SKY NEWS | Channel | ffprobe | ✗ | Unknown | UK |
| VIRGIN MEDIA TWO | Channel | http | ✓ | VLC/3.0.12 LibV | IE |
| STARZ CINEMA | Channel | ffprobe | ✗ | Unknown | USA |
| CANAL 3 LA PAMPA | Channel | ffprobe | ✗ | Unknown | AR |
| NFL NETWORK | Channel | ffprobe | ✗ | Unknown | USA |
| AKAAL CHANNEL | Channel | ffprobe | ✗ | Unknown | UK INT |
| EXPO CHANNEL | Channel | ffprobe | ✗ | Unknown | AUS |

## Failed Streams Analysis

**Failure Reasons:**
- All validation methods failed: 278 streams

**Sample Failed Streams:**

| Channel | Type | Reason | Group |
|---------|------|--------|--------|
| TRAVEL CHANNEL | Channel | All validation methods failed | USA |
| BEATS RADIO | Channel | All validation methods failed | AR |
| BET SOUL | Channel | All validation methods failed | USA |
| DUBAI RACING 3 | Channel | All validation methods failed | AE |
| TNT SPORTS 3 | Channel | All validation methods failed | UK |
| NEWS 24 | Channel | All validation methods failed | AL |
| ABC KIDS | Channel | All validation methods failed | AUS |
| WARNER TV | Channel | All validation methods failed | IT |
| COURT TV | Channel | All validation methods failed | USA |
| SUPERSPORT RUGBY | Channel | All validation methods failed | ZA |

## Geo-blocked Streams

| Channel | Type | Group |
|---------|------|---------|
| AL MASHHAD | Channel | AE |
| TV WAREHOUSE | Channel | UK |
| CNA | Channel | AL |
| RTÈ 2 | Channel | IE |
| TG 4 | Channel | IE |
| FOX SPORTS 506 | Channel | AUS |

## Debug Information

### TRAVEL CHANNEL

- **curl:** ✓
- **wget:** ✗
  - Return code: 4
  - Error: Spider mode enabled. Check if remote file exists.
--2025-09-28 21:24:55--  http://alt.xtream-ie.org/
- **ffprobe_basic:** ✗
  - Return code: 1
  - Error: http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9mbDcubW92ZW9uam95LmNvbS9UcmF2
- **ffprobe_streams:** ✗
  - Return code: 1
  - Error: http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9mbDcubW92ZW9uam95LmNvbS9UcmF2

### BEATS RADIO

- **curl:** ✓
- **wget:** ✗
  - Return code: 8
  - Error: Spider mode enabled. Check if remote file exists.
--2025-09-28 21:24:56--  http://alt.xtream-ie.org/
- **ffprobe_basic:** ✗
  - Return code: 1
  - Error: http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly92aWRlb3N0cmVhbS5zaG9ja21lZGlh
- **ffprobe_streams:** ✗
  - Return code: 1
  - Error: http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly92aWRlb3N0cmVhbS5zaG9ja21lZGlh

### BET SOUL

- **curl:** ✓
- **wget:** ✗
  - Return code: 8
  - Error: Spider mode enabled. Check if remote file exists.
--2025-09-28 21:24:58--  http://alt.xtream-ie.org/
- **ffprobe_basic:** ✗
  - Return code: 1
  - Error: http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9mbDcubW92ZW9uam95LmNvbS9CRVRf
- **ffprobe_streams:** ✗
  - Return code: 1
  - Error: http://alt.xtream-ie.org/aBn1J1oTRSe/VVtbggGMS/1eyJ1cmwiOiAiaHR0cHM6Ly9mbDcubW92ZW9uam95LmNvbS9CRVRf

## Recommendations

**Performance:**
- Testing rate: 0.20 streams/second
- Average time per stream: 4.93s

## Methodology Improvements

This validation uses a more permissive approach:
- Tests connectivity before HTTP validation
- Uses multiple User-Agent strings for better compatibility
- Accepts various content types (binary data, m3u8 playlists)
- Uses ffprobe for additional stream verification
- Provides detailed debugging when enabled
- Reduced false negatives compared to strict validation

---
*Improved validation completed in 2464.4 seconds*
