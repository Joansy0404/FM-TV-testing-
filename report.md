# Stream Test Report

**Test method:** ffprobe
**Test scope:** direct_only
**Last update:** 2025-09-29 11:12 UTC
**Test duration:** 14.8 minutes

## Latest Test Results

| Location | Working | Geo-blocked | Failed | Total | Success Rate |
|----------|---------|-------------|--------|-------|--------------|
| Direct | 113 | 332 | 117 | 562 | **20.1%** |

## Error Analysis

- **HTTP 403 Forbidden**: 332 occurrences
- **Connection refused**: 60 occurrences
- **Server error (5xx)**: 31 occurrences
- **HTTP 404 Not Found**: 9 occurrences
- **http://alt.xtream-ie.org/abn1j1otrse/vvtbgggms/1eyj1cmwioiaiahr0chm6ly9jdnr2lmn2ywxszxkubmv0l2hscy9l**: 8 occurrences
- **http://alt.xtream-ie.org/abn1j1otrse/vvtbgggms/1eyj1cmwioiaiahr0cdovlzizljizny4xmdqumta2ojgwodavvvnb**: 3 occurrences
- **http://alt.xtream-ie.org/abn1j1otrse/vvtbgggms/1eyj1cmwioiaiahr0chm6ly9hmxhzlnzpcc8zmdawmdkilcaiawqi**: 1 occurrences
- **http://alt.xtream-ie.org/abn1j1otrse/vvtbgggms/1eyj1cmwioiaiahr0chm6ly9jdnr2lmn2ywxszxkubmv0l2hscy9x**: 1 occurrences
- **http://alt.xtream-ie.org/abn1j1otrse/vvtbgggms/1eyj1cmwioiaiahr0chm6ly9hmxhzlnzpcc80mdawmda0myisicjp**: 1 occurrences
- **http://alt.xtream-ie.org/abn1j1otrse/vvtbgggms/1eyj1cmwioiaiahr0chm6ly9hmxhzlnzpcc80mdawmda0miisicjp**: 1 occurrences

---
*Generated at 2025-09-29 11:12 UTC*

<!-- HISTORY
{
  "tests": [
    {
      "date": "2025-09-29 06:24 UTC",
      "country": "UK",
      "ip": "149.40.48.73",
      "city": "London",
      "isp": "AS212238 Datacamp Limited",
      "config": "S:All,V:False,P:False,F:False",
      "duration_min": 18.8,
      "results": {
        "direct": {
          "working": 104,
          "geoblocked": 331,
          "failed": 127,
          "total": 562,
          "rate": 18.505338078291814
        },
        "vpn": {
          "working": 0,
          "geoblocked": 0,
          "failed": 562,
          "total": 562,
          "rate": 0.0
        }
      }
    },
    {
      "date": "2025-09-29 07:01 UTC",
      "country": "UK",
      "ip": "154.47.24.199",
      "city": "London",
      "isp": "AS212238 Datacamp Limited",
      "config": "S:All,V:False,P:False,F:False",
      "duration_min": 17.4,
      "results": {
        "direct": {
          "working": 114,
          "geoblocked": 330,
          "failed": 118,
          "total": 562,
          "rate": 20.284697508896798,
          "timeouts": 0,
          "connection_errors": 61
        },
        "vpn": {
          "working": 0,
          "geoblocked": 0,
          "failed": 562,
          "total": 562,
          "rate": 0.0,
          "timeouts": 0,
          "connection_errors": 0
        }
      }
    },
    {
      "date": "2025-09-29 07:40 UTC",
      "country": "UK",
      "ip": "146.70.179.109",
      "city": "London",
      "isp": "AS9009 M247 Europe SRL",
      "config": "S:All,V:False,P:False,F:False",
      "duration_min": 25.4,
      "results": {
        "direct": {
          "working": 116,
          "geoblocked": 330,
          "failed": 116,
          "total": 562,
          "rate": 20.640569395017792,
          "timeouts": 0,
          "connection_errors": 63,
          "proxy_errors": 0
        },
        "vpn": {
          "working": 40,
          "geoblocked": 328,
          "failed": 194,
          "total": 562,
          "rate": 7.11743772241993,
          "timeouts": 0,
          "connection_errors": 0,
          "proxy_errors": 0
        }
      }
    },
    {
      "date": "2025-09-29 08:42 UTC",
      "country": "UK",
      "method": "ffprobe",
      "ip": "149.50.209.148",
      "city": "London",
      "isp": "AS212238 Datacamp Limited",
      "config": "S:100,V:False,P:False,F:False",
      "duration_min": 12.0,
      "results": {
        "direct": {
          "working": 73,
          "geoblocked": 2,
          "failed": 25,
          "total": 100,
          "rate": 73.0
        },
        "vpn": {
          "working": 25,
          "geoblocked": 0,
          "failed": 75,
          "total": 100,
          "rate": 25.0
        }
      }
    },
    {
      "date": "2025-09-29 09:16 UTC",
      "country": "UK",
      "method": "ffprobe",
      "ip": "149.40.63.139",
      "city": "London",
      "isp": "AS212238 Datacamp Limited",
      "config": "S:200,V:False,P:False,F:False",
      "duration_min": 28.5,
      "results": {
        "direct": {
          "working": 151,
          "geoblocked": 5,
          "failed": 44,
          "total": 200,
          "rate": 75.5
        },
        "vpn": {
          "working": 50,
          "geoblocked": 1,
          "failed": 149,
          "total": 200,
          "rate": 25.0
        }
      }
    },
    {
      "date": "2025-09-29 10:03 UTC",
      "country": "UK",
      "method": "ffprobe",
      "ip": "146.70.179.100",
      "city": "London",
      "isp": "AS9009 M247 Europe SRL",
      "config": "S:200,V:False,P:False,F:False",
      "duration_min": 30.8,
      "results": {
        "direct": {
          "working": 145,
          "geoblocked": 4,
          "failed": 51,
          "total": 200,
          "rate": 72.5
        },
        "vpn": {
          "working": 149,
          "geoblocked": 4,
          "failed": 47,
          "total": 200,
          "rate": 74.5
        }
      }
    },
    {
      "date": "2025-09-29 11:12 UTC",
      "country": "US",
      "method": "ffprobe",
      "scope": "direct_only",
      "duration_min": 14.8,
      "results": {
        "direct": {
          "working": 113,
          "geoblocked": 332,
          "failed": 117,
          "total": 562,
          "rate": 20.106761565836297
        }
      }
    }
  ]
}
-->
