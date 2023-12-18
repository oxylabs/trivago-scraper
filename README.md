# Trivago Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Trivago Scraper](https://oxylabs.io/products/scraper-api/web/trivago?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Trivago website effortlessly. This brief guide explains how an Trivago Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Trivago results by providing your own URLs to our service. We can return the HTML for any Trivago page you like.

#### Python code example

The example below illustrates how you can get HTML of Trivago page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.trivago.com/en-us/odr/hotels-chicago-illinois?search=200-14411&_gl=1*1u91udd*_up*mq..&gclid=trivago'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/trivago-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en-US\" dir=\"ltr\"><head><meta charSet=\"utf-8\"/><meta name=\"viewport\" conte ... </html>",
      "created_at": "2023-12-18 11:07:45",
      "updated_at": "2023-12-18 11:07:47",
      "page": 1,
      "url": "https://www.trivago.com/en-us/odr/hotels-chicago-illinois?search=200-14411&_gl=1*1u91udd*_up*mq..&gclid=trivago",
      "job_id": "7142470490890738689",
      "status_code": 200
    }
  ]
}
```
With our Trivago Scraper, you can seamlessly extract public data from any Trivago web page. Gather essential hotel details like location, ratings, amenities, or guest reviews, to understand the hospitality industry and stay ahead in your business. If you need any assistance, our support team is just a live chat or an email away at hello@oxylabs.io.