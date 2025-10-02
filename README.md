# google-trends-scraper

![Google Trends Scraper Actor Logo](https://images.apifyusercontent.com/oYyezynONTeIZJZbuoM0mrzdKFbdCiB-8HkdYEaJ_Ew/rs:fill:250:250/cb:1/aHR0cHM6Ly9hcGlmeS1pbWFnZS11cGxvYWRzLXByb2QuczMudXMtZWFzdC0xLmFtYXpvbmF3cy5jb20vM1ByZFpVREtZWFVYWkxXTTMtYWN0b3ItcXA2bUtTU2NZb3V0WXFDT2EtN21NQXoyNUMxaS1nb29nbGVfdHJlbmRzX2FjdG9yLmpwZw.webp Google Trends Scraper**  
Fetch real-time trending searches, interest over time, interest by region, and related queries/topics with a single, configurable Apify actor.

***

## Overview

Struggling to scrape data from Google Trends? This easy-to-use, reliable scraper gives you access to all the data you need. Try it free for 1 day—with no credit card required—and only pay if you love it.

`google-trends-scraper` wraps the [Google Trends Scraper actor on Apify](https://apify.com/scraperpro/google-trends-scraper), providing:

- **Trending Now** (realtime hot searches)  
- **Interest Over Time** (time series for keywords)  
- **Interest By Region** (geographic breakdown)  
- **Related Queries & Topics** (top & rising searches)  

***

## Quickstart

### Apify CLI

```bash
npx apify run scraperpro/google-trends-scraper \
  --input '{"scrape_type":"trending_now","common_geo":"US","trending_hours":24}'
```

### HTTP API

```bash
curl -X POST https://api.apify.com/v2/acts/scraperpro~google-trends-scraper/runs \
     -H "Content-Type: application/json" \
     -d '{"scrape_type":"trending_now","common_geo":"US","trending_hours":24}'
```

***

## Detailed Usage

### Node.js

```javascript
import Apify from 'apify';

(async () => {
    const run = await Apify.call('scraperpro/google-trends-scraper', {
        scrape_type: 'interest_over_time',
        keywords: ['data science', 'machine learning'],
        predefined_timeframe: 'today 12-m',
        common_geo: 'US',
    });
    console.log(run.output[0].data);
})();
```

### Python

```python
from apify_client import ApifyClient

client = ApifyClient('<APIFY_TOKEN>')
run = client.actor("scraperpro/google-trends-scraper").call(run_input={
    "scrape_type": "related_queries",
    "keywords": ["python"],
    "predefined_timeframe": "today 12-m"
})
print(run["output"][0]["data"])
```

***

## Example Inputs & Outputs

| Use Case                               | Input JSON                                                                                                   |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Realtime trending (US, 24h)            | `{"scrape_type":"trending_now","common_geo":"US","trending_hours":24}`                                       |
| Interest over time (US)                | `{"scrape_type":"interest_over_time","keywords":["data science"],"predefined_timeframe":"today 12-m"}`       |
| Related queries (global)               | `{"scrape_type":"related_queries","keywords":["python"],"predefined_timeframe":"today 12-m"}`                |

Each run writes one dataset item containing:
- `scrape_type`  
- `data` (results array or object)  
- `input_summary` (geo, timeframe, resolution, etc.)  
- `error` & `error_message`  

***

## Best Practices

- **Rate Limits:** Use shorter timeframes or proxies to avoid `429` errors.  
- **Data Volume:** Limit `geo_resolution` to `COUNTRY` or `REGION` before scaling to `CITY`/`DMA`.  
- **Time Range:** The `trending_now` type supports 1–191 hours.  
- **Empty Results:** Ensure keywords have sufficient search volume in chosen geo/timeframe.  

***

## Contributing

Contributions are welcome! Please open issues or submit pull requests for:

- Bug fixes  
- New examples (Node.js, Python, shell)  
- Improved documentation or tutorials  

Refer to [CONTRIBUTING.md](./CONTRIBUTING.md) for details.

***

## License & Support

This project is licensed under the MIT License.  
For actor support, visit the [Apify Store listing](https://apify.com/scraperpro/google-trends-scraper) or contact [radwanfaris13@gmail.com](mailto:radwanfaris13@gmail.com).

*Happy scraping!*