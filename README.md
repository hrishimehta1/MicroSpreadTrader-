

# MicroSpreadTrader

## Overview

MicroSpreadTrader is an advanced trading algorithm designed to capitalize on minute, one-cent moves in the bid/ask spread of high-volume stocks. Leveraging order book imbalance, this strategy aims to execute a high frequency of trades daily, targeting stocks that exhibit frequent minimal price variations. This approach is inspired by and seeks to implement findings from Darryl Shen's 2015 research, among other resources.

## Features

- **Real-Time Bid/Ask Spread Analysis:** Monitors live spread changes to detect eligible trading opportunities.
- **High-Volume Stock Focus:** Optimized for securities with substantial trading volume and frequent, small-scale price movements.
- **Ensemble Trading Strategy:** Incorporates principles of order book imbalance to inform trade decisions.
- **Compliance with PDT Rules:** Designed for accounts maintaining a balance above $25,000 to comply with Pattern Day Trader regulations.
- **Framework for Streaming-Based Algorithms:** Offers a foundational codebase for developing strategies based on real-time market data.

## How It Works

The algorithm uses `Quote` objects to track the bid/ask spread, initiating trades when a change of exactly one penny is detected. This precise movement threshold is chosen to exclude larger price jumps that may indicate significant news impacting the stock. The algorithm also features a `Position` object to manage the current investment stance, ensuring that the trading activity remains within the set risk parameters.

## Requirements

- Alpaca Trade API: For executing trades and receiving market data.
- Pandas & NumPy: For data manipulation and numerical calculations.

## Setup

1. Ensure you have Python 3.x installed.
2. Install necessary Python libraries
