# Realistic IPTV Stream Validation Report

**Generated:** 2025-09-28 21:53 UTC  
**Duration:** 88.2s (1.5m)  
**Validation Mode:** Permissive  
**Sample Size:** 200 streams  

## Validation Results

- **✅ Definitely Working:** 29 (14.5%)
- **⚠️ Likely Working:** 0 (0.0%)
- **🔒 Geo-blocked:** 1 (0.5%)
- **❌ Definitely Failed:** 170 (85.0%)

**Conservative Success Rate:** 14.5% (definitely working only)  
**Optimistic Success Rate:** 14.5% (including likely working)  

## Stream URL Analysis

- **Unknown:** 115 streams (57.5%)
- **Http Stream:** 85 streams (42.5%)

## Success Rate by Stream Type

| Stream Type | Definitely Working | Likely Working | Total | Success Rate |
|-------------|-------------------|----------------|-------|-------------|
| Http Stream | 29 | 0 | 85 | 34.1% |
| Unknown | 0 | 0 | 115 | 0.0% |

## Definitely Working Streams (Sample)

- **DC League of Super-Pets** (Http Stream) - Unknown
- **Wash My Soul in the River's Flow** (Http Stream) - Unknown
- **Chevalier** (Http Stream) - Unknown
- **The 15:17 to Paris** (Http Stream) - Unknown
- **The Grand Budapest Hotel** (Http Stream) - Unknown
- **Fountain of Youth** (Http Stream) - Unknown
- **U&THE PAST** (Http Stream) - Unknown
- **Chaos Walking** (Http Stream) - Unknown
- **Faster** (Http Stream) - Unknown
- **Breaking Bad S01 E02 The Cat's in the Ba** (Http Stream) - Unknown

## Actionable Recommendations for Reducing False Negatives

### High Failure Rate Detected (85.0%)

**Top Failure Reasons:**
- HTTP 404: 115 streams
- HTTP 500: 55 streams

**Recommended Actions:**

### Validation Mode Analysis

**Current Mode: Permissive**
- Minimizes false negatives, may include some questionable streams
- Good for discovering maximum working stream count

### Next Steps to Improve Validation

2. **Geo-blocking Mitigation** (1 blocked streams)
   - Test with proxy services
   - Implement VPN rotation
   - Use residential IP addresses

4. **Alternative Validation Methods**
   - Test with actual media players (VLC, ffmpeg)
   - Implement playlist analysis for HLS streams
   - Use deep packet inspection
   - Consider crowd-sourced validation

## Validation Accuracy Analysis

This validation prioritizes **reducing false negatives** over perfect accuracy.

**Result: Poor (14.5% likely working)**
- Stream source may have issues
- Implement multiple recommendations above

**Key Insight:** The difference between 'definitely working' (14.5%) and 'likely working' (14.5%) suggests 0.0% of streams might work with different validation approaches.

---
*Realistic validation completed in 88.2 seconds*
