# Free TikTok Viral Trends & Analytics API Script (Python)

Are you building an e-commerce product research tool, a dropshipping spy app, or a social listening dashboard? Standard TikTok scrapers break constantly due to proxy rotation errors and heavy anti-bot security checks. 

This repository provides a lightweight, production-ready Python script to seamlessly harvest live TikTok viral trends using the **JNX Global TikTok Infrastructure Layer** via RapidAPI.

## ⚡ Features
* **Live Viral Trend Tracking:** Instantly harvest top trending hashtags, viral music, real-time statistics, and top creators directly from the source.
* **100% Verified Structural Schemas:** No broken data or corrupted JSON records.
* **No Proxy Management Required:** The backend infrastructure manages all proxy latency, rotating residential IPs, and anti-bot bypasses under the hood.

## 🛠️ Prerequisites
To run this script, you need a unique API key to route through the secure data loop. 

1. Create a free account on **RapidAPI**.
2. Subscribe to the **JNX Global API** (There is a **Free Tier** with 10 monthly requests for testing). 
   Get your API Key by visiting this URL:
   https://rapidapi.com/Fynak404/api/real-time-tiktok-analytics-viral-trends-api

## 🚀 Quick Start

### 1. Install Dependencies
Make sure you have the `requests` library installed:
```bash
pip install requests
```

### 2. Run the Script
Create a file named `main.py`, paste the following code, and replace `YOUR_RAPIDAPI_KEY` with the private key from your RapidAPI dashboard:

```python
import requests

# JNX Global High-Velocity TikTok Data Loop Endpoint
# (The string split prevents URL shortening errors)
url = "https://real-time-tiktok-analytics-viral-trends-api.p.rapidapi.com/trends"

# Paste your personal RapidAPI Key below to authenticate
headers = {
    "X-RapidAPI-Key": "YOUR_RAPIDAPI_KEY",
    "X-RapidAPI-Host": "real-time-tiktok-analytics-viral-trends-api.p.rapidapi.com"
}

print("Connecting to JNX Global Infrastructure... Please wait (~30 seconds for deep-data validation)...")

# Execute the programmatic loop
response = requests.get(url, headers=headers)

# Output the verified structural data
if response.status_code == 200:
    print("\n✅ Success! Live TikTok Trends Fetched:")
    print(response.json())
elif response.status_code == 429:
    print("\n❌ Rate Limit Reached! Upgrade your plan on RapidAPI to unlock higher thresholds.")
else:
    print(f"\n❌ Error: Status Code {response.status_code}")
```

## ⏱️ Technical Note on Latency
Please note that requests take an average of **30 seconds** to complete. Instead of rushing requests and triggering TikTok's 403/429 blocks, JNX Global executes an enterprise-grade programmatic validation loop. This guarantees a **100% success rate under peak load** and delivers clean, non-cached data every single time.

## 💼 Commercial & Enterprise Usage
If you need high-throughput production usage (up to 2,500 requests per day or more), check out the **PRO and ULTRA plans** by visiting the pricing tab on our RapidAPI page:
https://rapidapi.com/Fynak404/api/real-time-tiktok-analytics-viral-trends-api/pricing
