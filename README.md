# MQL4
MQL4 MetaTrader AniTrade

Selected code samples in MQL language for MetaTrader platform

Top Bots - Algo for finding tops and bottoms (valleys) in price series used for support/resistance and entry/exit calculations (MQL language for MetaTrader)

Image shows arrows for tops/bots compared with ZigZag indicator (Welles Wilder Accumulative Swing Index ASI below)
 
Super Smoother Moving Average by John Ehlers implemented in MQL

Image shows comparison of Super Smoother MA and Jurik MA next to Simple MA

By Aharon Zbaida
https://sites.google.com/site/aharonzbaida/home/mql-code/tops-and-bottoms---characterizing-market-swing-price-levels

 Tops and Bottoms - Characterizing Market Swing Price Levels
It is often desirable to characterize market price levels relative to historic price swing levels. Since prices move up with concentration of buyers, and down with concentration of sellers, price levels where reversals occur (up trend making u-turn down, or down-trend making u-turn up), tend to reflect price levels where orders of buyers and sellers have concentrated historically, and have reached an equilibrium, albeit temporary. It is also observed that these levels often continue to act as support and resistance to price movements after the time of reversal. It should be noted that these levels are not a prediction of future price movement, just a comparative scale to historical levels, and can serve as a basis for establishing: Support and Resistance levels, potential order exit levels, trend and market regime changes.

For these reasons, we desire to characterize price swing levels. Though over the years, market technicians have adapted individualized variations on what constitutes a proper swing, here is presented original work based on Highs and Lows:

    That a High that is adjacent on both sides to Highs lower than itself, is considered a potential Top. Likewise, a Low that is adjacent on both sides to Lows that are higher than itself are considered potential Bottoms, or Bots for short. There are bars, that meet the criteria as both potential tops and bots. Bars with potential as tops or bottoms, are classified according to how they measure up to a feature that has occurred just prior  (an immediately prior top or bot).

    A potential top is classified as a top if it is immediately preceded by a bot, or is more extreme (i.e. higher than) an immediately preceding top. If it is more extreme, it overwrites the previous top, and has become the latest feature in the series.

    In a likewise manner, a potential bot is classified as a bot if it is immediately preceded by a top, or is more extreme (i.e. lower than) an immediately preceding low. If it is more extreme, it overwrites the previous bot, and has become the latest feature in the series.

    In the case of bars that meet criteria as both potential tops and bots (call them doubles), if they are more extreme than the previous feature of the same direction (the new potential top is higher than the immediate previous feature that is also a top, or lower than an immediate previous feature that is also a bot), they overwrite that feature and dominate. In case they are not be more extreme, they are classified as opposite the previous feature (i.e. if the previous feature was a top, the double is classified as a bot, and vise versa). Since classification of doubles depends on the prior feature, if a double happens to be the first bar analyzed on the chart, we skip it, and move forward to a non-double potential feature.

    The chart is sequentially scanned from left to right in chronological order of development. A potential feature (top or bot) is thus classified according to the above rules, and a feature array is constructed. Times of feature occurrence, and extreme price levels (lows for bots and highs for tops) are also recorded in arrays of matching indices. 

Code for calculating Tops and Bots is available for download below.

Figure below shows a chart where Tops and Bots are graphically indicated as Red and Blue arrows respectively. It also shows the popular ZigZag indicator (Red line), and J. Welles Wilder, Jr.'s Accumulative Swing Index in a sub-window for comparison.


