# 📺 Enhanced M3U Stream Status Report

**Generated on:** 2025-09-26 07:54:10 UTC  
**Duration:** 511.1 seconds  
**Runner Location:** GitHub Actions (global infrastructure)  
**Configuration:** VODs: ❌, PPV: ❌, Timeout: 10s

## 📊 Summary

| Metric | Count | Percentage |
|--------|-------|-----------|
| **Total Streams Found** | 1349 | 100% |
| **📺 M3U8/Live Streams** | 656 | 48.6% |
| **🎬 VOD Files** | 693 | 51.4% |
| **🔍 Checked Streams** | 604 | 44.8% |
| **✅ Working Streams** | 583 | 96.5% |
| **❌ Failed Streams** | 21 | 3.5% |
| **⭐ Skipped Streams** | 745 | 55.2% |

## 📊 Stream Type Breakdown

| Type | Working | Failed | Total Checked | Success Rate |
|------|---------|--------|---------------|-------------|
| **📺 M3U8/Live** | 583 | 21 | 604 | 96.5% |
| **🎬 VOD Files** | 0 | 0 | 0 | 0.0% |

## 📁 Files Processed

- `channel playlist.m3u`: 1349 streams (479 M3U8, 693 VOD)

## ⭐ Skipped Streams (745 total)

### 🎬 VOD Files (693 skipped)
*Enable "Check VODs" in workflow dispatch to test these*

| Group | Count |
|-------|---------|
| AMC+ | 3 |
| Angel Studios | 1 |
| Apple TV+ | 5 |
| BritBox | 3 |
| DOCPLAY | 1 |
| Disney+ | 178 |
| FMTV+ | 1 |
| HBO MAX | 94 |
| Hallmark+ | 1 |
| NETFLIX | 20 |
| Others | 51 |
| PBS | 1 |
| PRIME VIDEO | 29 |
| Paramount+ | 84 |
| Peacock TV | 104 |
| RTÈ PLAYER | 3 |
| SONY Pictures Core | 65 |
| SONY Pictures Core (Shows) | 12 |
| STARZ | 33 |
| Stan. | 2 |
| Studiocanal Presents | 2 |

### 🥊 PPV/Event Channels (52 skipped)
*Enable "Check PPV" in workflow dispatch to test these*

| Group | Count |
|-------|---------|
| UK EVENTS | 1 |
| USA EVENTS | 50 |
| USA FAST | 1 |


## 📋 Failure Analysis (21 total failures)

### 🚫 Access Denied (15 streams)
*Geo-blocked or authentication required*

| Channel | Group | Type | Error | Code | File |
|---------|-------|------|-------|------|---------|
| BLAZE | UK | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| TV WAREHOUSE | UK | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| INSIDE CRIME | UK FAST | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| TG 4 | IE | M3U8 | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
| FOX SPORTS 506 | AUS | Other | Access denied (geo-blocked/auth required | 403 | channel playlist.m3u |
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

### ⏱️ Connection Timeouts (1 streams)
*Server slow/overloaded or PPV preparing*

| Channel | Group | Type | Error | Code | File |
|---------|-------|------|-------|------|---------|
| QVC | USA | M3U8 | Timeout after 10s | None | channel playlist.m3u |

### 🌐 DNS Failures (1 streams)
*Domain name resolution failed*

| Channel | Group | Type | Error | Code | File |
|---------|-------|------|-------|------|---------|
| ABC AUSTRALIA VIETNAM | AUS | M3U8 | DNS resolution failed | None | channel playlist.m3u |

### ❓ Not Found (404) (3 streams)
*Stream URL no longer exists*

| Channel | Group | Type | Error | Code | File |
|---------|-------|------|-------|------|---------|
| BIG TEN NETWORK | USA | M3U8 | Stream not found | 404 | channel playlist.m3u |
| USA Network | CA | Other | Stream not found | 404 | channel playlist.m3u |
| CANAL 4 SAN JUAN | AR | M3U8 | Stream not found | 404 | channel playlist.m3u |

### 💥 Server Errors (5xx) (1 streams)
*Server-side technical issues*

| Channel | Group | Type | Error | Code | File |
|---------|-------|------|-------|------|---------|
| SKY SPORT 1 | NZ | Other | Server error (502) | 502 | channel playlist.m3u |


## 📋 Configuration Notes

- **VOD Checking:** Disabled - URLs with .m3u8/#.mkv format were not tested
- **PPV/Event Checking:** Disabled - UK EVENTS & USA EVENTS groups were not tested
- **Timeout:** 10 seconds per stream (PPV channels get 2x timeout)
- **VOD Detection:** Matches URLs ending with .m3u8/#.mkv, .m3u8/#.mp4, etc.
- **M3U8 Detection:** Matches URLs containing .m3u8 (excluding VOD formats)
- **Event Groups:** Automatically detects "UK EVENTS", "USA EVENTS", and similar groups

## 📈 Geographic & Technical Notes

- Tests run from **GitHub Actions** global infrastructure
- "Access Denied" (403) errors typically indicate geo-restrictions
- PPV channels may be offline between events (normal behavior)
- VOD files are static content and should be consistently available
- M3U8 streams are adaptive bitrate live streams
- Timeout errors may indicate server overload or preparation time
- DNS errors suggest the streaming service domain is down

## 🔧 Technical Details

- **User-Agent:** Chrome 120 simulation for maximum compatibility
- **Method:** HEAD for direct video files, GET with stream verification for live content
- **VOD Detection:** Specifically matches .m3u8/#.mkv, .m3u8/#.mp4 format URLs
- **M3U8 Detection:** Identifies adaptive streaming URLs (.m3u8)
- **Headers:** Enhanced with security headers and proper content type
- **Rate Limiting:** Dynamic delays based on success rate
- **Retry Logic:** Single attempt per stream to avoid overwhelming servers

## 🎛️ Manual Testing Options

To test specific content types:
1. Go to **Actions** → **Check M3U Streams** → **Run workflow**
2. Toggle **Check VODs** to test .m3u8/#.mkv files (video-on-demand)
3. Toggle **Check PPV** to test Pay-Per-View channels
4. Adjust **Timeout** for slower connections

---
*Last updated: 2025-09-26 07:54:10 UTC*
*Report generated automatically by Enhanced GitHub Actions*
