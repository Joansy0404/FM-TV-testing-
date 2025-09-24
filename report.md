# 📺 M3U Stream Status Report with Hot-Swap

**Generated on:** 2025-09-24 18:27:01 UTC
**GitHub Actions Runner Location:** GitHub's infrastructure (global)

## 📊 Summary

| Metric | Count | Percentage |
|--------|-------|------------|
| **Total Streams** | 1232 | 100% |
| **✅ Working Streams** | 1218 | 98.9% |
| **🔄 Hot-Swapped Streams** | 0 | 0.0% |
| **❌ Failed Streams** | 14 | 1.1% |

## 📁 Files Processed

- `vod playlist.m3u`: 495 streams
- `channel playlist.m3u`: 737 streams **(Hot-swap enabled)**

## 🔍 Hot-Swap Attempt Details (14 channels)

*Detailed breakdown of what was tried for channels that couldn't be fixed:*

### AL MASHHAD

- **Exact matches found:** 0
- **Fuzzy matches found:** 0
- **Total candidates tested:** 0

*No backup streams found for this channel name.*

### ALARABIYA

- **Exact matches found:** 0
- **Fuzzy matches found:** 0
- **Total candidates tested:** 0

*No backup streams found for this channel name.*

### MBC 1

- **Exact matches found:** 0
- **Fuzzy matches found:** 0
- **Total candidates tested:** 0

*No backup streams found for this channel name.*

### MBC 4

- **Exact matches found:** 0
- **Fuzzy matches found:** 0
- **Total candidates tested:** 0

*No backup streams found for this channel name.*

### MBC 5

- **Exact matches found:** 0
- **Fuzzy matches found:** 0
- **Total candidates tested:** 0

*No backup streams found for this channel name.*

### MBC BOLLYWOOD

- **Exact matches found:** 0
- **Fuzzy matches found:** 0
- **Total candidates tested:** 0

*No backup streams found for this channel name.*

### MBC DRAMA

- **Exact matches found:** 0
- **Fuzzy matches found:** 0
- **Total candidates tested:** 0

*No backup streams found for this channel name.*

### MBC PERSIA

- **Exact matches found:** 0
- **Fuzzy matches found:** 0
- **Total candidates tested:** 0

*No backup streams found for this channel name.*

### SPACETOON ARABIC

- **Exact matches found:** 0
- **Fuzzy matches found:** 0
- **Total candidates tested:** 0

*No backup streams found for this channel name.*

### WANASAH

- **Exact matches found:** 0
- **Fuzzy matches found:** 0
- **Total candidates tested:** 0

*No backup streams found for this channel name.*

### BLAZE

- **Exact matches found:** 0
- **Fuzzy matches found:** 0
- **Total candidates tested:** 0

*No backup streams found for this channel name.*

### TG 4

- **Exact matches found:** 0
- **Fuzzy matches found:** 0
- **Total candidates tested:** 0

*No backup streams found for this channel name.*

### TG 4+1

- **Exact matches found:** 0
- **Fuzzy matches found:** 0
- **Total candidates tested:** 0

*No backup streams found for this channel name.*

### TV WAREHOUSE

- **Exact matches found:** 0
- **Fuzzy matches found:** 0
- **Total candidates tested:** 0

*No backup streams found for this channel name.*


## 📋 Remaining Failures (14 streams)

*These streams failed and no working backup was found.*

### 🚫 Access Denied (13 streams)
*Likely geo-blocked or requires authentication*

| Channel Name | Group | File | Error Details | Code |
|-------------|-------|------|---------------|------|
| AL MASHHAD | AE | channel playlist.m3u | Access denied (possibly geo-blocked) | 403 |
| ALARABIYA | AE | channel playlist.m3u | Access denied (possibly geo-blocked) | 403 |
| MBC 1 | AE | channel playlist.m3u | Access denied (possibly geo-blocked) | 403 |
| MBC 4 | AE | channel playlist.m3u | Access denied (possibly geo-blocked) | 403 |
| MBC 5 | AE | channel playlist.m3u | Access denied (possibly geo-blocked) | 403 |
| MBC BOLLYWOOD | AE | channel playlist.m3u | Access denied (possibly geo-blocked) | 403 |
| MBC DRAMA | AE | channel playlist.m3u | Access denied (possibly geo-blocked) | 403 |
| MBC PERSIA | AE | channel playlist.m3u | Access denied (possibly geo-blocked) | 403 |
| SPACETOON ARABIC | AE | channel playlist.m3u | Access denied (possibly geo-blocked) | 403 |
| WANASAH | AE | channel playlist.m3u | Access denied (possibly geo-blocked) | 403 |
| BLAZE | UK | channel playlist.m3u | Access denied (possibly geo-blocked) | 403 |
| TG 4 | UK | channel playlist.m3u | Access denied (possibly geo-blocked) | 403 |
| TV WAREHOUSE | UK | channel playlist.m3u | Access denied (possibly geo-blocked) | 403 |

### ⏱️ Connection Timeouts (1 streams)
*Server too slow to respond or overloaded*

| Channel Name | Group | File | Error Details | Code |
|-------------|-------|------|---------------|------|
| TG 4+1 | UK | channel playlist.m3u | Connection timeout | N/A |


## 📈 Hot-Swap Technology

- **Priority Order:** Original `channel playlist.m3u` → moj → dlive
- **Target File:** `channel playlist.m3u` (only this file gets modified)
- **Backup Sources:** 2 external M3U files with priority system
- **Testing Strategy:** Backup streams are only tested when needed (during swap attempts)
- **Matching Strategy:** Exact name match first, then fuzzy matching
- **Verification:** Each backup URL is tested in priority order before replacement
- **Prevention:** Same backup URL won't be used twice

## 📈 Geographic Notes

- Tests run from **GitHub Actions infrastructure** (multiple global locations)
- "Access Denied" errors may indicate geo-restrictions
- Hot-swap uses alternative sources that may have different geographic availability
- DNS errors suggest the streaming service may be down entirely
- Timeout errors often indicate server overload or slow response

## 📝 Technical Details

- **User-Agent:** Modern browser simulation for better compatibility
- **Timeout:** 15 seconds per stream, 10 seconds for backup verification
- **Method:** HEAD request first, then GET with stream verification
- **Hot-Swap Logic:** Download backup sources → Match channel names → Test alternatives → Replace URLs
- **File Modification:** Only `channel playlist.m3u` is modified with working alternatives

---
*Last updated: 2025-09-24 18:27:01 UTC*
*Report generated automatically by GitHub Actions*
*Hot-swap technology: Automatically maintaining stream availability*
