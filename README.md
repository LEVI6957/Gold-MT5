# XAUUSD Trading Bot - MetaTrader 5 (MT5)

This repository contains an Expert Advisor (EA) for MetaTrader 5 (MT5) designed for trading XAUUSD on the M15 timeframe. The bot uses the **Average True Range (ATR)** as one of its indicators to make trading decisions. The EA was developed using the **EA Studio**.

## Features

- **Symbol**: XAUUSD
- **Timeframe**: M15 (15-Minute chart)
- **Strategy**: Uses ATR for volatility-based trading decisions.
- **Risk Management**: Includes configurable stop-loss and take-profit levels.
- **Fully Automated**: Executes trades based on market conditions and strategy rules.
- **Customization**: Easily customizable for different symbols or timeframes.

## Requirements

1. **MetaTrader 5** (MT5) Platform
   - Download [MetaTrader 5](https://www.metatrader5.com/en/download) if you haven’t already installed it.
2. **MQL5 Source File**: You will need the `.mq5` file from this repository.
3. Basic knowledge of MetaTrader 5 and how to install Expert Advisors (EA) is recommended.

## Installation

1. **Download the Trading Bot**
   - Clone or download this repository.
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   ```

2. **Move the `.mq5` file** to your MetaTrader 5 folder.
   - Copy the `.mq5` file to the `Experts` directory of your MetaTrader 5 installation. 
   - Usually, this folder is located at:  
     `C:\Users\<Your Username>\AppData\Roaming\MetaQuotes\Terminal\<MT5 Instance>\MQL5\Experts`

3. **Compile the EA** in MetaEditor.
   - Open MetaEditor (from MT5 platform), navigate to the file, and press **Compile** (or press F7).
   - Ensure there are no errors in the code.

4. **Run the EA on MT5**:
   - Open MetaTrader 5.
   - Drag and drop the compiled EA onto a chart of the **XAUUSD M15** timeframe.
   - Configure the EA’s input settings according to your preferences.

## How It Works

The Expert Advisor uses the **ATR (Average True Range)** to evaluate market volatility and adjusts trading conditions accordingly. Key elements include:

- **Buy/Sell Signals**: The EA opens buy or sell orders based on the ATR value.
- **Risk Management**: Customizable stop-loss and take-profit settings to control risk.
- **Trailing Stop**: Optionally adjusts the stop-loss level as the trade moves in your favor.

## Usage

1. **Timeframe**: Ensure you are running the EA on the **M15** timeframe.
2. **Symbol**: This EA is designed for **XAUUSD** but can be customized for other symbols.
3. **Parameters**: 
   - You can adjust the trading parameters in the EA’s settings.
   - Modify the **ATR period**, **stop-loss**, and **take-profit** values based on your risk tolerance.

## Parameters

- **ATR Period**: Default is 14. This defines the period for calculating ATR.
- **Stop Loss**: Configurable stop-loss level.
- **Take Profit**: Configurable take-profit level.
- **Risk Management Settings**: You can set the lot size, risk percentage, and more.

## Troubleshooting

- **iATR Parameter Error**: If you encounter an error such as `'iATR' - wrong parameters count`, make sure the **iATR** function is called correctly in the `.mq5` file.
  ```cpp
  double atrValue = iATR("XAUUSD", PERIOD_M15, 14);
  ```
- Make sure all required parameters (symbol, timeframe, and ATR period) are correctly specified in your code.
