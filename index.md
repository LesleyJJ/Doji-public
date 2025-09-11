# Doji Indicator for MetaTrader 5

A custom MetaTrader 5 indicator that identifies and marks Doji candlestick patterns on price charts. Doji candles are important reversal signals in technical analysis, representing market indecision.

## Overview

The Doji indicator automatically scans historical price data to identify Doji candlestick patterns and marks them with blue dots on the chart. A Doji candle is characterized by having a very small body relative to its total range, indicating that the opening and closing prices are nearly equal.

## Features

- **Automatic Doji Detection**: Scans up to 1500 historical candles (configurable)
- **Visual Markers**: Marks Doji patterns with blue dots below the candle
- **Customizable Threshold**: Adjustable sensitivity for Doji detection
- **Real-time Updates**: Automatically updates when new candles form
- **Chart Integration**: Seamlessly integrates with MetaTrader 5 charts

## Installation

1. Copy the `Doji.mq5` file to your MetaTrader 5 `Indicators` folder:
   ```
   MetaTrader 5/MQL5/Indicators/
   ```

2. Compile the indicator in MetaEditor or restart MetaTrader 5

3. Add the indicator to your chart from the Navigator panel

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `Lookback_Candles` | int | 1500 | Number of historical candles to analyze |
| `Doji_Threshhold` | double | 0.1 | Maximum body-to-range ratio for Doji detection (0.1 = 10%) |
| `Enable_Drawing` | bool | true | Enable/disable visual markers on chart |

## How It Works

The indicator calculates the Doji pattern using the following logic:

1. **Range Calculation**: `range = high - low`
2. **Body Calculation**: `body = |open - close|`
3. **Doji Condition**: `body / range ≤ Doji_Threshhold`

When a Doji is detected, a blue dot is placed below the candle at a distance of 20% of the candle's range.

## Usage

1. **Add to Chart**: Drag the indicator from the Navigator to your chart
2. **Configure Settings**: Adjust parameters in the indicator settings dialog
3. **Monitor Signals**: Watch for blue dots marking Doji patterns
4. **Combine with Analysis**: Use Doji signals in conjunction with other technical analysis tools

## Trading Applications

Doji candles are significant in technical analysis because they indicate:

- **Market Indecision**: Buyers and sellers are in equilibrium
- **Potential Reversal**: Often signals trend exhaustion
- **Support/Resistance**: Can act as key levels for future price action

### Common Trading Strategies

- **Reversal Signals**: Look for Doji at trend extremes
- **Breakout Confirmation**: Doji at support/resistance levels
- **Trend Continuation**: Doji in trending markets may indicate pause before continuation

## Technical Details

- **Platform**: MetaTrader 5
- **Language**: MQL5
- **Type**: Custom Indicator
- **Buffers**: 2 (Doji detection and price levels)
- **Drawing**: Chart objects (labels with dots)

## File Structure

```
Doji/
├── Doji.mq5          # Main indicator source code
├── Doji.mqproj       # MetaEditor project file
├── .gitignore        # Git ignore file
└── README.md         # This documentation
```

## Requirements

- MetaTrader 5 platform
- MQL5 compiler (included with MetaTrader 5)

## Version History

- **v1.00** - Initial release with basic Doji detection and visualization

## License

Copyright © 2025 LesleyJJ. All rights reserved.

## Support

For issues, questions, or feature requests, please refer to the MQL5.com community forums or contact the developer.

## Disclaimer

This indicator is for educational and informational purposes only. Trading involves risk, and past performance does not guarantee future results. Always conduct your own analysis and consider your risk tolerance before making trading decisions.

---

**Note:** The full source code is not publicly available. If you are interested in accessing the source code or collaborating, please [contact me](mailto:jacobjohnlesley@gmail.com).
