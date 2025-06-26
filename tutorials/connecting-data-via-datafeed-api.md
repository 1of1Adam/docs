---
title: "How to connect data via datafeed API | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/"
extracted_at: "2025-06-22T09:16:26.609Z"
---

# How to connect data via datafeed APIThis tutorial explains how to implement real-time data streaming to Advanced Charts / [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/) step-by-step.
As an example, the tutorial describes connection via free CryptoCompare API
that [provides data](#use-external-data-source) from several crypto exchanges.
After completing this tutorial, you will learn how to implement datafeed using Datafeed API, display historical data using ordinary
HTTP requests, and stream real-time data via WebSocket.
The tutorial is divided into three parts:

- [Widget Constructor set-up](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/Widget-Setup)
- [Datafeed implementation](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/Datafeed-Implementation)
- [Streaming implementation](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/Streaming-Implementation)

> **Tip:** 
- You can find the final code for this tutorial on the [GitHub repository](https://github.com/tradingview/charting-library-tutorial).
- At the end of each section, you will find the complete code blocks related to a specific step.
- Before proceeding with the tutorial, we recommend checking the [Prerequisites](#prerequisites) section.

## Prerequisites
### Get repository access
The [Advanced Charts repository](https://github.com/tradingview/charting_library) is private.
Refer to the [Getting Access](https://www.tradingview.com/charting-library-docs/latest/getting_started/quick-start#getting-access) section for more information.
### Use external data source
The library is used to display financial data but it does not contain or provide any data.
You need to implement your own data source to display data in the library.
It can be a web API, a database, or a CSV file.
This tutorial uses the [CryptoCompare API](https://min-api.cryptocompare.com/), which has a wide range of market data.
Note that CryptoCompare requires an API key to request their stream data.
You need to get such key to complete the tutorial. Refer to the [CryptoCompare documentation](https://www.cryptocompare.com/coins/guides/how-to-use-our-api/) for more information.

> **Warning:** We cannot guarantee that CryptoCompare works in your region.
If you see the `ERR_CONNECTION_REFUSED` error when running the tutorial, try to use a proxy or VPN.

### See results on the fly
If you want to see the results of this tutorial right away, take the following steps:

Clone the [tutorial repository](https://github.com/tradingview/charting-library-tutorial).
Note that for the real project, it is better to use this repository as a submodule in yours.
```
git clone https://github.com/tradingview/charting-library-tutorial.git

```

Go to the repository folder and initialize the Git submodule with the library:

```
git submodule update --init --recursive

```
Alternatively, you can [download](https://docs.github.com/en/repositories/working-with-files/using-files/downloading-source-code-archives) the library repository from a ZIP file or [clone](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) it using Git.

Run the following command to serve static files:

```
npx serve

```