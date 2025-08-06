# Gemini API Proxy
[中文](README-TW.md)

This is a proxy server designed specifically for the Google Gemini API. It allows you to securely consolidate multiple API keys into a single endpoint and randomly select one for use with each request. This is useful for managing keys, load balancing, and integrating with front-end applications without exposing your keys.

## ✨ Features

*   **Multi-Key Management**: Pass multiple Google AI API keys, separated by commas, in the `x-goog-api-key` header.
*   **Random Key Selection**: A key is randomly selected from your provided list for each request, helping to distribute the load.
*   **Request Forwarding**: Seamlessly forwards all requests to the Google Generative Language API (`https://generativelanguage.googleapis.com`).
*   **Flexible Deployment**: Optimized for Vercel, but also supports deployment using Docker.

## 🚀 Deployment Guide

We highly recommend using Vercel for a quick and easy one-click deployment.

### Vercel (Recommended)

[![Deploy to Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/spectre-pro/gemini-proxy)

1.  Click the "Deploy to Vercel" button above.
2.  Follow the instructions on Vercel to clone this repository and deploy it.
3.  Once deployed, you will receive a dedicated proxy URL.

### Docker

You can also use Docker to deploy on any supported platform, such as [Claw Cloud](https://console.run.claw.cloud/signin?link=RGXA3AIOBR4S).

```
docker run -d \
  -p 80:34562 \
  --name gemini-proxy \
  --restart unless-stopped \
  ghcr.io/spectre-pro/gemini-proxy
```

3.  Your proxy server will be running at `http://localhost:80`.  
## Star History

<picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=spectre-pro/gemini-proxy&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=spectre-pro/gemini-proxy&type=Date" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=spectre-pro/gemini-proxy&type=Date" />
</picture>
