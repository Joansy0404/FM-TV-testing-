# 📺 Enhanced M3U Stream Status Report

**Generated on:** 2025-09-26 18:37:11 UTC  
**Duration:** 469.9 seconds  
**Runner Location:** GitHub Actions (global infrastructure)  
**Configuration:** VODs: ❌, PPV: ❌, Timeout: 10s

## 📊 Summary

| Metric | Count | Percentage |
|--------|-------|-----------|
| **Total Streams Found** | 1483 | 100% |
| **📺 M3U8 Streams** | 467 | 31.5% |
| **🎬 VOD Files** | 838 | 56.5% |
| **📡 TS Streams** | 3 | 0.2% |
| **🔗 Other Streams** | 175 | 11.8% |
| **🔍 Checked Streams** | 593 | 40.0% |
| **✅ Working Streams** | 572 | 96.5% |
| **❌ Failed Streams** | 21 | 3.5% |
| **⭕ Skipped Streams** | 890 | 60.0% |

## 📊 Stream Type Breakdown

| Type | Working | Failed | Total Checked | Success Rate |
|------|---------|--------|---------------|-------------|
| **📺 M3U8** | 395 | 21 | 416 | 95.0% |
| **📡 TS** | 2 | 0 | 2 | 100.0% |
| **🔗 Other** | 175 | 0 | 175 | 100.0% |

## 📁 Files Processed

- `channel playlist.m3u`: 1483 streams (467 M3U8, 838 VOD, 3 TS, 175 Other)

## ⭕ Skipped Streams (890 total)

### 🎬 VOD Files (838 skipped)
*Enable "Check VODs" in workflow dispatch to test these*

| Group | Count |
|-------|---------|
| AE | 5 |
| AF | 4 |
| AMC+ | 4 |
| Angel Studios | 1 |
| Apple TV+ | 7 |
| BritBox | 4 |
| CBC Gem | 1 |
| DOCPLAY | 1 |
| Disney+ | 199 |
| FMTV+ | 3 |
| HBO MAX | 107 |
| Hallmark+ | 1 |
| NETFLIX | 22 |
| Others | 83 |
| PBS | 2 |
| PRIME VIDEO | 40 |
| Paramount+ | 89 |
| Peacock TV | 132 |
| RTÈ PLAYER | 3 |
| SONY Pictures Core | 75 |
| SONY Pictures Core (Shows) | 12 |
| STARZ | 35 |
| Stan. | 2 |
| Studiocanal Presents | 3 |
| UK | 2 |
| USA FAST | 1 |

### 🥊 PPV/Event Channels (52 skipped)
*Enable "Check PPV" in workflow dispatch to test these*

| Group | Count |
|-------|---------|
| UK EVENTS | 1 |
| USA EVENTS | 50 |
| USA FAST | 1 |


## 📋 Failure Analysis (21 total failures)

### 🚫 Access Denied (14 streams)
*Geo-blocked or authentication required*

| Channel | Group | Type | Error | Code | File |
|---------|-------|------|-------|------|---------|
| BLAZE | UK | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| TV WAREHOUSE | UK | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| INSIDE CRIME | UK FAST | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| TG 4 | IE | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| AL MASHHAD | AE | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| ALARABIYA | AE | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| MBC 1 | AE | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| MBC 4 | AE | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| MBC 5 | AE | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| MBC BOLLYWOOD | AE | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| MBC DRAMA | AE | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| MBC PERSIA | AE | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| SPACETOON ARABIC | AE | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| WANASAH | AE | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |

### ⏱️ Connection Timeouts (2 streams)
*Server slow/overloaded or PPV preparing*

| Channel | Group | Type | Error | Code | File |
|---------|-------|------|-------|------|---------|
| RACER TV | USA | M3U8 | Timeout after 10s | None | channel playlist.m3u |
| ALTERNA TV | AR | M3U8 | Timeout after 10s | None | channel playlist.m3u |

### 🌐 DNS Failures (1 streams)
*Domain name resolution failed*

| Channel | Group | Type | Error | Code | File |
|---------|-------|------|-------|------|---------|
| ABC AUSTRALIA VIETNAM | AUS | M3U8 | DNS resolution failed | None | channel playlist.m3u |

### ❓ Not Found (404) (4 streams)
*Stream URL no longer exists*

| Channel | Group | Type | Error | Code | File |
|---------|-------|------|-------|------|---------|
| HALLMARK DRAMA | USA | M3U8 | Stream not found | 404 | channel playlist.m3u |
| CTB PERTH | AUS | M3U8 | Stream not found | 404 | channel playlist.m3u |
| INDO OZ TV | AUS | M3U8 | Stream not found | 404 | channel playlist.m3u |
| CANAL 3 LAS HERAS | AR | M3U8 | Stream not found | 404 | channel playlist.m3u |


## 📋 Configuration Notes

- **VOD Checking:** Disabled - VOD files with various formats were not tested
- **PPV/Event Checking:** Disabled - UK EVENTS & USA EVENTS groups were not tested
- **Timeout:** 10 seconds per stream (PPV channels get 2x timeout)
- **VOD Detection:** Enhanced to detect #.mkv, .mkv/, .mkv?, /movie/, /film/, /vod/ patterns
- **M3U8 Detection:** Matches URLs containing .m3u8 anywhere (handles tokens/parameters)
- **TS Detection:** Identifies .ts stream URLs as separate category
- **Event Groups:** Automatically detects "UK EVENTS", "USA EVENTS", and similar groups

## 📈 Geographic & Technical Notes

- Tests run from **GitHub Actions** global infrastructure
- "Access Denied" (403) errors typically indicate geo-restrictions
- PPV channels may be offline between events (normal behavior)
- VOD files are static content and should be consistently available
- M3U8 streams are adaptive bitrate live streams
- TS streams are transport stream format (often live TV)
- Timeout errors may indicate server overload or preparation time
- DNS errors suggest the streaming service domain is down

## 🔧 Technical Details

- **User-Agent:** Chrome 120 simulation for maximum compatibility
- **Method:** HEAD for direct video files, GET with stream verification for live content
- **VOD Detection:** Enhanced patterns including hash (#), slash (/), and query (?) separators
- **M3U8 Detection:** Identifies adaptive streaming URLs (.m3u8) with token support
- **TS Detection:** Recognizes transport stream URLs (.ts)
- **Headers:** Enhanced with security headers and proper content type
- **Rate Limiting:** Dynamic delays based on success rate
- **Retry Logic:** Single attempt per stream to avoid overwhelming servers

## 🎛️ Manual Testing Options

To test specific content types:
1. Go to **Actions** → **Check M3U Streams** → **Run workflow**
2. Toggle **Check VODs** to test video-on-demand content
3. Toggle **Check PPV** to test Pay-Per-View channels
4. Adjust **Timeout** for slower connections

---
*Last updated: 2025-09-26 18:37:11 UTC*
*Report generated automatically by Enhanced GitHub Actions*
