# Leads Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Leads Scraper](https://oxylabs.io/products/scraper-api/web/leads-scraper?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Leads website effortlessly. This brief guide explains how an Leads Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Leads results by providing your own URLs to our service. We can return the HTML for any Leads page you like.

#### Python code example

The example below illustrates how you can get HTML of Leads page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.explorium.ai/blog/business-data/b2b-leads-data/#'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/leads-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!doctype html>\n<html lang=\"en\">\n<head><meta charset=\"UTF-8\"><script>if(navigator.userAgent.match(/M ... </html>",
      "created_at": "2023-12-18 11:33:25",
      "updated_at": "2023-12-18 11:33:30",
      "page": 1,
      "url": "https://www.explorium.ai/blog/business-data/b2b-leads-data/#",
      "job_id": "7142476947208057857",
      "status_code": 200
    }
  ]
}
```
With our Leads Scraper, you can effectively gather personalized data from any Leads web page. Obtain the necessary client information, such as demographic data, contact details, or preference patterns, to understand your target audience and stay one step ahead of your competitors. If you need any help, get in touch with our support team through live chat or send us an email at hello@oxylabs.io.