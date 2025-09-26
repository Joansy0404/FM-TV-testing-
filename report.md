# 📺 Enhanced M3U Stream Status Report

**Generated on:** 2025-09-26 20:44:53 UTC  
**Duration:** 523.9 seconds  
**Runner Location:** GitHub Actions (global infrastructure)  
**Configuration:** VODs: ❌, PPV: ❌, Timeout: 10s

## 📊 Summary

| Metric | Count | Percentage |
|--------|-------|-----------|
| **Total Streams Found** | 1488 | 100% |
| **Total Channel Streams** | 663 | 44.6% |
| **Total VOD Streams** | 825 | 55.4% |
| **🔍 Checked Streams** | 611 | 41.1% |
| **✅ Working Streams** | 504 | 82.5% |
| **❌ Failed Streams** | 107 | 17.5% |
| **⭕ Skipped Streams** | 877 | 58.9% |

## 📊 Stream Type Breakdown

| Type | Working | Failed | Total Checked | Success Rate |
|------|---------|--------|---------------|-------------|
| **📺 .M3U8** | 334 | 100 | 434 | 77.0% |
| **📡 .TS** | 2 | 0 | 2 | 100.0% |
| **⚙️ Profile URLs** | 35 | 0 | 35 | 100.0% |
| **🔗 Other** | 133 | 7 | 140 | 95.0% |

## 📁 Files Processed

- `channel playlist.m3u`: 1488 streams (485 M3U8, 825 VOD, 3 TS, 0 Token, 35 Profile, 140 Other)

## ⭕ Skipped Streams (877 total)

### 🎬 VOD Files (825 skipped)
*Enable "Check VODs" in workflow dispatch to test these*

| Group | Count |
|-------|---------|
| AMC+ | 4 |
| Angel Studios | 1 |
| Apple TV+ | 7 |
| BritBox | 4 |
| CBC Gem | 1 |
| DOCPLAY | 1 |
| Disney+ | 199 |
| FMTV+ | 3 |
| HBO MAX | 106 |
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

### 🥊 PPV/Event Channels (52 skipped)
*Enable "Check PPV" in workflow dispatch to test these*

| Group | Count |
|-------|---------|
| UK EVENTS | 1 |
| USA EVENTS | 50 |
| USA FAST | 1 |


## 📋 Failure Analysis (107 total failures)

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

### ⏱️ Connection Timeouts (5 streams)
*Server slow/overloaded or PPV preparing*

| Channel | Group | Type | Error | Code | File |
|---------|-------|------|-------|------|---------|
| SKY SPORTS CRICKET | UK | Other | Timeout after 10s | None | channel playlist.m3u |
| SKY SPORTS NFL | UK | Other | Timeout after 10s | None | channel playlist.m3u |
| ESPN | USA | Other | Timeout after 10s | None | channel playlist.m3u |
| REVOLT | USA | M3U8 | Timeout after 10s | None | channel playlist.m3u |
| PEACOCK PREMIER LEAGUE TV | USA | Other | Timeout after 10s | None | channel playlist.m3u |

### 🌐 DNS Failures (1 streams)
*Domain name resolution failed*

| Channel | Group | Type | Error | Code | File |
|---------|-------|------|-------|------|---------|
| ABC AUSTRALIA VIETNAM | AUS | M3U8 | DNS resolution failed | None | channel playlist.m3u |

### ❓ Not Found (404) (4 streams)
*Stream URL no longer exists*

| Channel | Group | Type | Error | Code | File |
|---------|-------|------|-------|------|---------|
| CTB PERTH | AUS | M3U8 | Stream not found | 404 | channel playlist.m3u |
| INDO OZ TV | AUS | M3U8 | Stream not found | 404 | channel playlist.m3u |
| BEATS RADIO | AR | M3U8 | Stream not found | 404 | channel playlist.m3u |
| CANAL 3 LAS HERAS | AR | M3U8 | Stream not found | 404 | channel playlist.m3u |

### 💥 Server Errors (5xx) (2 streams)
*Server-side technical issues*

| Channel | Group | Type | Error | Code | File |
|---------|-------|------|-------|------|---------|
| SKY SPORT 1 | NZ | Other | Server error (502) | 502 | channel playlist.m3u |
| Fubo sports 1 | CA | Other | Server error (502) | 502 | channel playlist.m3u |

### ❓ Unknown Errors (81 streams)
*Unexpected errors*

| Channel | Group | Type | Error | Code | File |
|---------|-------|------|-------|------|---------|
| ASPIRE | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| AXS TV | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| BBC NEWS | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| BEIN SPORTS | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| BET (EAST) | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| BET GOSPEL | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| BET HER (EAST) | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| BET JAMS | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| BET SOUL | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| BRAVO (EAST) | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| CBS SPORTS NETWORK | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| CLEO TV | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| CMT | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| CNBC WORLD | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| COMET | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| COZI TV | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| C•SPAN | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| DISCOVERY FAMILY | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| DISCOVERY LIFE | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| DISCOVERY SCIENCE | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| DISNEY CHANNEL (EAST) | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| DISNEY JR. | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| FOOD NETWORK | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| FOX BUSINESS NETWORK | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| FOX NEWS CHANNEL | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| FOX SOUL | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| FREE FORM | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| FUSE | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| FYI | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| GET TV | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| GRIT TV | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| HALLMARK DRAMA | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| HALLMARK MOVIES & MYSTERY | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| HBO FAMILY | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| HBO MOVIES | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| HGTV | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| HSN | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| INSP | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| INVESTIGATION DISCOVERY (ID) | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| ION PLUS (EAST) | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| LIFETIME (EAST) | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| LOVE NATURE | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| MAGNOLIA NETWORK | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| MGM+ | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| MGM+ MARQUEE | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| MOTOR TREND | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| MTV 2 | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| MTV CLASSIC | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| NEWS NATION | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| NFL RED ZONE | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| NICK JR. | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| NICKTOONS (EAST) | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| OUTDOOR CHANNEL | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| OUTSIDE TV | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| OVATION | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| OWN | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| OXYGEN TRUE CRIME | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| PURSUIT CHANNEL | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| QVC | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| REELZ | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| SHOWTIME 2 | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| SHOWTIME (WEST) | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| SHOWTIME NEXT | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| SHOWTIME WOMEN | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| SMITHSONIAN CHANNEL | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| SNY | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| SPORTSMAN CHANNEL | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| START TV | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| STARZ ENCORE CLASSIC | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| SUNDANCE TV | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| TENNIS CHANNEL | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| THE WEATHER CHANNEL | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| TLC | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| TRAVEL CHANNEL | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| TV LAND | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| TV ONE | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| UP TV | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| USA NETWORK | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| WILLOW 2 | USA | Other | Connection refused | None | channel playlist.m3u |
| ANTENNA TV | USA | M3U8 | Connection refused | None | channel playlist.m3u |
| FANDUEL SPORTS NETWORK ARIZONA | USA | M3U8 | Connection refused | None | channel playlist.m3u |


## 🔗 Other Stream Examples (20 shown)

*These URLs don't match standard patterns (M3U8, TS, Token, Profile, VOD)*

| Channel | Group | URL |
|---------|-------|-----|
| ITV 3 | UK | https://a1xs.vip/1000013 |
| NICK JR. | UK | https://a1xs.vip/1000052 |
| SKY SPORTS CRICKET | UK | https://a1xs.vip/2000006 |
| SKY SPORTS GOLF | UK | https://a1xs.vip/2000009 |
| SKY SPORTS MAIN EVENT | UK | https://a1xs.vip/2000001 |
| SKY SPORTS MAIN EVENT UHD | UK | https://a1xs.vip/2000015 |
| SKY SPORTS NFL | UK | https://a1xs.vip/2000011 |
| SKY SPORTS PREMIER LEAGUE | UK | https://a1xs.vip/2000002 |
| SKY SPORTS RACING | UK | https://a1xs.vip/2000010 |
| SKY SPORTS TENNIS | UK | https://a1xs.vip/2000013 |
| SKY SPORTS+ | UK | https://a1xs.vip/2000012 |
| TNT SPORTS 1 | UK | https://a1xs.vip/2000021 |
| TNT SPORTS 2 | UK | https://a1xs.vip/2000022 |
| TNT SPORTS 3 | UK | https://a1xs.vip/2000023 |
| TNT SPORTS 4 | UK | https://a1xs.vip/2000024 |
| NOW 90'S & 00'S | UK | https://jmp2.uk/stvp-GB300033HI |
| TNT SPORTS ULTIMATE | UK | https://a1xs.vip/2000031 |
| DISCOVERY | UK | https://a1xs.vip/1000033 |
| MTV | UK | https://a1xs.vip/1000037 |
| &TV | UK FAST | https://jmp2.uk/stvp-GB3700007OZ |


## 📋 Configuration Notes

- **VOD Checking:** Disabled - Only URLs ending with /#.mkv are considered VOD files
- **PPV/Event Checking:** Disabled - UK EVENTS & USA EVENTS groups were not tested
- **Timeout:** 10 seconds per stream (PPV channels get 2x timeout)
- **VOD Detection:** Simple pattern matching - only URLs ending exactly with /#.mkv
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
- **VOD Detection:** Only URLs ending with /#.mkv are classified as VOD files
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
*Last updated: 2025-09-26 20:44:53 UTC*
*Report generated automatically by Enhanced GitHub Actions*
