# ABM_financial_bubble
Agent Based Model representing a financial bubble

## Requirements
- NetLogo 6.4.0 or later


# WHAT IS IT?

This Agent-Based Model (ABM) simulates the formation and bursting of financial bubbles, specifically in the technology sector, driven by market hype, social influence, investor sentiment, and fundamental economic factors. It demonstrates how individual behaviors and interactions among investors (agents) can lead to complex macro-level phenomena such as market crashes.


# HOW IT WORKS

Agents represent individual investors who decide whether or not to invest in a speculative technology asset based on two main factors:

1. Market Expectations (expected returns): Each agent evaluates investment returns based on recent price growth.

2. Social Influence: Agents observe and are influenced by the sentiment of nearby peers (neighbors within a radius of 3 patches).

Each investor also has a personal risk tolerance based on their current wealth, influencing their likelihood of investing.

The technology price (tech-price) evolves each tick based on:

- Fundamental growth (real-growth-rate)

- Market momentum (tech-growth-rate)

- Investor hype (percentage of investors)

- Random volatility (tech-volatility)

A financial crash is triggered when the technology price exceeds a fundamental price threshold (real-growth-rate combined with a buffer). After the crash, the market experiences negative growth until a stabilization threshold is reached.

## AGENT COLORS

Green: Agent has not yet made a strong investment decision (neutral sentiment).

Red: Agent is actively invested in the speculative technology asset (positive sentiment).

Blue: Agent has chosen to avoid or exit investment (negative sentiment).


# HOW TO USE IT

- Setup Button: Initializes the simulation, creating agents and resetting all parameters.

- Go Button: Starts and runs the simulation continuously.

## Sliders

- tech-growth-rate: Baseline monthly growth rate of technology price influenced by market sentiment.

- real-growth-rate: Fundamental monthly growth rate representing true technological or economic growth.

- tech-volatility: Random fluctuation level influencing technology price.

- crash-buffer: Determines how far the price can deviate from fundamental value before crashing.

- w-price: Weight agents assign to market signals (price movements) when making investment decisions.

- w-social: Weight agents assign to peer influence (social sentiment) when deciding to invest.

## Monitors

- Tech Price: Current market price of the technology asset.

## Investors: Number of investors currently invested in the technology asset.

- Average Wealth: Mean wealth of all agents.

- Crash?: Indicates whether a market crash has occurred.

## Plots

- Tech Price: Shows the market price over time.

- % Invested: Percentage of agents invested over time.


# THINGS TO NOTICE

- Observe how quickly a financial bubble forms when social influence (w-social) dominates rational analysis (w-price).

- Notice the wealth distribution changes during the bubble growth and after a crash occurs.

- Pay attention to the relationship between the fundamental price (real-growth-rate) and the market price.

# THINGS TO TRY

- Adjust the crash-buffer to explore the sensitivity of the market to speculative bubbles.

- Experiment by setting w-social to 1.0 and w-price to 0.0 (pure herd behavior) and vice versa.

- Increase tech-volatility to examine the effects of market uncertainty.

- Set the real-growth-rate significantly lower or higher than the tech-growth-rate to explore varying degrees of overvaluation.


# EXTENDING THE MODEL

- Include multiple asset classes to model portfolio diversification effects.

- Introduce more sophisticated investor strategies, such as memory or adaptive learning.

- Implement government intervention or market regulation mechanisms to stabilize prices after a crash.

- Add agent demographics such as age, income levels, or distinct investor profiles (institutional vs. retail).


# NETLOGO FEATURES

- Utilizes in-radius to model spatial social influence realistically.

- Implements sliders and monitors extensively to enhance interactivity and scenario testing.


# CREDITS AND REFERENCES

Developed as part of coursework in Agent-Based Modeling.

NetLogo software:
http://ccl.northwestern.edu/netlogo/

Model inspired by financial market behavior theories and the recent growth in interest of AI & Machine Learning sector

This model has been created in June of 2025 by Saliou Cisse
