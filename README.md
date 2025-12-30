You’re not asking to *change meaning* — you want to **change signal quality**:
same facts, but presented with **intentional structure, visual rhythm, and professional tone**, not “abandoned dump”.

Below is a **clean, non-childish, non-emoji**, **badge-driven**, well-organized rewrite.
You can paste this directly as your README.

---
# GOAT Stock Screener (Deprecated)

![Status](https://img.shields.io/badge/status-deprecated-red.svg)
![Language](https://img.shields.io/badge/python-3.7%2B-blue.svg)
![Library](https://img.shields.io/badge/pandas-required-brightgreen.svg)
![Market](https://img.shields.io/badge/markets-equities-lightgrey.svg)

> **Project Status Notice**  
> This repository is **deprecated** and no longer under active development.  
> The actively maintained, GUI-based successor is available here:  
> **https://github.com/th-efool/Quant-Kernel**

---

## Overview

**GOAT Stock Screener** is a Python-based stock analysis and signal-generation framework focused on **technical indicators** and **rule-driven strategies**.

The project was designed as a **modular research and experimentation base**, enabling rapid prototyping of trading logic across both **global** and **Indian equity markets**.

It integrates:
- **Yahoo Finance** for historical market data
- **Dhan HQ API** for intraday Indian market data

Although deprecated, the repository remains useful as a **reference implementation** for indicator pipelines, strategy structure, and backtesting workflows.

---

## Core Features

- **Multiple Technical Strategies**
  - Moving Average Crossover
  - McGinley Dynamic–based signals

- **Dual Market Data Sources**
  - Yahoo Finance (global markets)
  - Dhan HQ API (Indian equities)

- **Flexible Timeframes**
  - Daily analysis
  - Intraday (minute-level) analysis

- **Parameter-Driven Design**
  - Adjustable indicator periods
  - Configurable frequency multipliers

- **Deterministic Signal Output**
  - Clear buy / sell signal identification

- **Modular Architecture**
  - Separation of data ingestion, indicators, and strategies
  - Designed for extension rather than monolithic execution

---

## Project Structure

```
goat/
├── Good_Functions.py        # Data fetching (Yahoo Finance & Dhan HQ) + backtesting
├── Indicators.py            # Technical indicator implementations
├── Initialization.py        # Ticker configuration and source initialization
├── **init**.py

├── MA Cross Buy.py          # Moving Average crossover buy strategy
├── MA Cross Sell.py         # Moving Average crossover sell strategy
├── McG Buy.py               # McGinley-based buy strategy
├── McG Sell.py              # McGinley-based sell strategy
├── Template.py              # Strategy development template
└── **init**.py
````

---

## Configuration

### Dhan HQ API Credentials
In `Good_Functions.py`, replace the placeholder values with your credentials:

- `client_id`
- `access_token`

### Ticker Initialization
Edit `Initialization.py` to configure:
- Yahoo Finance tickers
- Dhan HQ security ID mappings

---

## Strategy Customization

Each strategy file exposes tunable parameters:

- `day_trading` — intraday vs daily mode
- `frequency` — interval scaling factor
- `short`, `long`, `period` — indicator-specific windows

---

## Creating New Strategies

1. Use `Template.py` as a base
2. Implement indicator logic (or reuse from `Indicators.py`)
3. Define buy/sell conditions
4. Run and validate against historical data

---

## Usage

### Running a Strategy

Example: McGinley Sell strategy

```bash
python "McG Sell.py"
````

This will:

1. Fetch market data
2. Compute the McGinley Dynamic indicator
3. Generate and print sell signals

### Backtesting

The backtesting utilities in `Good_Functions.py` allow evaluation of strategies over historical datasets.

---

## Installation

### Prerequisites

* Python 3.7+

### Dependencies

```bash
pip install pandas numpy yfinance dhanhq
```

### Clone

```bash
git clone https://github.com/yourusername/goat-stock-screener.git
cd goat-stock-screener
```

(Optional) Virtual environment:

```bash
python -m venv env
source env/bin/activate   # Windows: env\Scripts\activate
```

---

## Disclaimer

This project is provided **strictly for educational and research purposes**.
No financial advice is given.
The author assumes no responsibility for financial outcomes resulting from its use.



