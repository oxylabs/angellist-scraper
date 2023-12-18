# Angellist Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Angellist Scraper](https://oxylabs.io/products/scraper-api/web/angellist?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Angellist website effortlessly. This brief guide explains how an Angellist Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Angellist results by providing your own URLs to our service. We can return the HTML for any Angellist page you like.

#### Python code example

The example below illustrates how you can get HTML of Angellist page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.angellist.com/'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/angellist-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta charSet=\"utf-8\"/><meta name=\"viewport\" content=\"width=dev ... </html>",
      "created_at": "2023-12-18 11:17:23",
      "updated_at": "2023-12-18 11:17:25",
      "page": 1,
      "url": "https://www.angellist.com/",
      "job_id": "7142472915118785537",
      "status_code": 200
    }
  ]
}
```
Using our Angellist Scraper, you can seamlessly harvest public data from all Angellist web pages. Gather essential startup details including names, sizes, founders, funding details, or company information to understand trends and to stay competitive in the entrepreneurial landscape. Should you encounter any issues, our support team is ready to assist through live chat or feel free to email us at hello@oxylabs.io.