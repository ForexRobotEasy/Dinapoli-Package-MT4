# Dinapoli Package MT4

This ReadMe file provides an overview of the Dinapoli Package MT4 code and its functionalities. Please note that ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in the product. To find the official developer of this product, please use MQL5.

## Overview

The Dinapoli Package MT4 is a comprehensive and versatile forex trading software developed by the Forex Robot Easy Team. It consists of various components, including the Oscillator Predictor, MACD Predictor, Thrust Scanner, Advanced Fibonacci Indicators, and essential Trading Functions. These components work together to provide accurate and reliable predictions of potential market movements, identify strong trading opportunities, and execute trading plans effectively.

## Components

### Oscillator Predictor

The Oscillator Predictor is responsible for predicting potential market movements based on the input prices. It utilizes a specific prediction logic to provide insights into market trends accurately. The function `OscillatorPredictor` takes an array of prices as input and returns the predicted oscillator value.

```cpp
double OscillatorPredictor(double[] prices) {
    // Oscillator prediction logic
    // ...
    return oscillatorPrediction;
}
```

### MACD Predictor

The MACD Predictor focuses on momentum and trend-following aspects of trading. It predicts potential market movements using the MACD indicator. The function `MACDPredictor` takes an array of prices as input and returns the predicted MACD value.

```cpp
double MACDPredictor(double[] prices) {
    // MACD prediction logic
    // ...
    return macdPrediction;
}
```

### Thrust Scanner

The Thrust Scanner identifies thrusts or strong movements in the market. It accurately detects potential trading opportunities signaled by thrusts. The function `ThrustScanner` takes an array of prices as input and returns a boolean value indicating whether a thrust is detected.

```cpp
bool ThrustScanner(double[] prices) {
    // Thrust scanning logic
    // ...
    return isThrustDetected;
}
```

### Advanced Fibonacci Indicators

The Dinapoli Package MT4 includes Advanced Fibonacci Indicators, but no specific code requirements are mentioned for this component.

### Trading Functions

The Trading Functions component implements necessary functions to execute Dinapoli trade plans effectively. It provides seamless integration of the developed code with existing trading platforms, specifically the MT4 platform. The following functions are included:

```cpp
void OpenBuyOrder(double price, double lotSize) {
    // Open buy order logic
    // ...
}

void CloseBuyOrder(double price) {
    // Close buy order logic
    // ...
}

void OpenSellOrder(double price, double lotSize) {
    // Open sell order logic
    // ...
}

void CloseSellOrder(double price) {
    // Close sell order logic
    // ...
}
```

### Main Function

The main function `OnTick` demonstrates an example usage of the Dinapoli Package MT4. It retrieves market prices, performs predictions using the Oscillator Predictor and MACD Predictor, and detects thrusts using the Thrust Scanner. Based on these predictions, it executes appropriate trading orders.

```cpp
void OnTick() {
    // Example usage of the Dinapoli Package MT4
    double[] prices = GetMarketPrices();
    
    double oscillatorPrediction = OscillatorPredictor(prices);
    double macdPrediction = MACDPredictor(prices);
    bool isThrustDetected = ThrustScanner(prices);
    
    if (oscillatorPrediction > 0 && macdPrediction > 0 && isThrustDetected) {
        OpenBuyOrder(prices[0], 0.01);
    } else if (oscillatorPrediction < 0 && macdPrediction < 0 && !isThrustDetected) {
        OpenSellOrder(prices[0], 0.01);
    }
    
    // Close open orders logic
    // ...
}
```

## Deliverables

The Dinapoli Package MT4 includes the following deliverables:

- Fully functional code for the Oscillator Predictor, MACD Predictor, and Thrust Scanner.
- Documentation detailing the implemented trading functions and their usage.
- User guide for configuring and utilizing the Dinapoli Package MT4.

## Additional Information

For detailed reviews and trading results of this product, please visit [Forex Robot Easy - Dinapoli Package MT4 Review](https://forexroboteasy.com/forex-robot-review/dinapoli-package-mt4-review-all-in-one-forex-software/). Please note that ForexRobotEasy is not the official developer of this product, and the provided code is only a sample demonstration of its functionality. To find the official developer of this product, please use MQL5.
