# Website-Image Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Website-Image Scraper](https://oxylabs.io/products/scraper-api/web/website-image-scraper?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Website-Image website effortlessly. This brief guide explains how an Website-Image Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Website-Image results by providing your own URLs to our service. We can return the HTML for any Website-Image page you like.

#### Python code example

The example below illustrates how you can get HTML of Website-Image page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://oxylabs.io/blog'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/website-image-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta charSet=\"utf-8\" /><meta name=\"viewport\" content=\"width=de ... </html>",
      "created_at": "2023-12-18 11:32:02",
      "updated_at": "2023-12-18 11:32:03",
      "page": 1,
      "url": "https://oxylabs.io/blog",
      "job_id": "7142476600309768193",
      "status_code": 200
    }
  ]
}
```
With our Website-Image Scraper, you can seamlessly extract public data from any of the chosen Website-Image web pages. Gather essential details pertinent to your interests, say, intricate artwork details, photographer's information, or image descriptions, to understand the prevailing trends and stay one step ahead in your field. For any queries or concerns, our support team is at your service through live chat or you can also reach out to us at hello@oxylabs.io.