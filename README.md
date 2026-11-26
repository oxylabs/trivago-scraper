# Trivago Scraper API

[![Oxylabs promo code](https://raw.githubusercontent.com/oxylabs/product-integrations/refs/heads/master/Affiliate-Universal-1090x275.png)](https://oxylabs.io/pages/gitoxy?utm_source=github&utm_medium=referral&utm_content=trivago-scraper&utm_campaign=banner&groupid=877)

<p align="left">
  <a href="https://dashboard.oxylabs.io"><img src="https://img.shields.io/badge/%F0%9F%9A%80_Get_Started-FF6B35?style=for-the-badge" alt="Get started"></a>
  <a href="https://developers.oxylabs.io/products/web-api"><img src="https://img.shields.io/badge/%F0%9F%93%9A_Documentation-4A90E2?style=for-the-badge" alt="Documentation"></a>
  <a href="https://dashboard.oxylabs.io"><img src="https://img.shields.io/badge/%F0%9F%93%8A_Dashboard-2EA44F?style=for-the-badge" alt="Dashboard"></a>
  <a href="https://discord.gg/Pds3gBmKMH"><img src="https://img.shields.io/badge/%F0%9F%92%AC_Discord-5865F2?style=for-the-badge" alt="Discord"></a>
  <a href="https://www.youtube.com/@oxylabs"><img src="https://img.shields.io/badge/%E2%96%B6%EF%B8%8F_YouTube-FF0000?style=for-the-badge" alt="YouTube"></a>
</p>

Oxylabs’ [Trivago Scraper](https://oxylabs.io/products/scraper-api/web/trivago?utm_source=github&utm_medium=referral&utm_content=trivago-scraper&groupid=877) is a data gathering solution allowing you to extract real-time information from an Trivago website effortlessly. This brief guide explains how an Trivago Scraper works and provides code examples to understand better how you can use it hassle-free.

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
With our Trivago Scraper, you can seamlessly extract public data from any Trivago web page. Gather essential hotel details like location, ratings, amenities, or guest reviews, to understand the hospitality industry and stay ahead in your business. If you need any assistance, our support team is just a live chat or an email away at support@oxylabs.io.
