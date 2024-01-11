# Investment Calculator

A simple tool written with LibreOffice Calc to analyze a portfolio of investments in the stock market and in various assets.


## Features

- Handles stocks, ETF, bonds, cryptocurrencies, cash and gold.
- Each asset is given an expected return, an expense ratio, and a monthly investment.
- Computes the portfolio value over time taking into account fees, expected returns and monthly contributions of each asset.
- Analyzes the country repartition of the portfolio, as well as the weight of each asset class.
- Can help build a diversified portfolio and spot over and under-exposures.
- Completely open source. All features are available in the public github repository.


## Installation

Simply download the file ```Calculator.ods``` to your computer.


## Documentation

The tool should be opened with LibreOffice Calc. It could work with Microsoft Excel but this has not been tested.
Unless you want to change the tool's behavior, only cells from ```A4``` to ```BR59``` should be modified.

- Give the asset's alias in column ```A``` (optional).
- Give the asset's ISIN in column ```B```, if relevant (optional).
- Give the asset's expense ratio in column ```C```.
- Give the asset's issuer in column ```D``` (optional).
- Give the amount of the asset you buy monthly in column ```E```.
- Give the amount of the asset you currently own in column ```F```.
- Choose a future expected return for the asset in column ```G```. For a $7$% return, give $1.07$.
- Use columns ```H``` to ```BR``` to indicate the country weight of each asset, when relevant. Gold is treated as a country.

A value of $0$ is assumed for a cell left empty. If your own gold, put it in the stocks/ETF section and write $100$ in column ```AZ``` at the corresponding row. For stocks, bonds, gold and cash, historical average returns can be used to try to infer future returns. For cryptocurrencies, we are all quite blind.
Skip columns ```H``` to ```BR``` if you are uninterested in the geographical distribution of your portfolio.

- Use rows ```4``` to ```26``` for stocks, ETF and gold.
- Use rows ```28``` to ```38``` for bonds.
- Use rows ```40``` to ```48``` for cryptocurrencies.
- Use rows ```50``` to ```59``` for cash.

Once all input cells are filled, you can check out the geographical repartition of your portfolio between rows ```61``` and ```64```. Between rows ```67``` and ```73```, you will find the expected value of your portfolio over time,
as well as the repartition between stocks, bonds, cryptocurrencies and cash. The time evolution of fees is indicated between rows ```74``` and ```76```. Finally, pie charts and graphs of the portfolio are plotted between rows ```81``` and ```162```.


## Contributors

- Jérémy Couturier, <https://jeremycouturier.com>

This tool is open source and you are encouraged to contribute to it. Upon first use, it contains my portfolio. If you wish to criticize my investment strategy or share yours, please reach out.
If you want to start investing in the stock market, I recommend the broker Trade Republic <https://ref.trade.re/c2pwqw9g>. You can use my code C2PWQW9G.


## Weaknesses

The volatility of the different assets is not taken into account, and evolutions over short timespans could drastically deviate from what the tool computes.
This tool should only be used by investors following a passive and long-term strategy (15+ years).
Similarly, the long-term evolution could be affected if the expected returns are too optimistic.


## License

This tool is a free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

It is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this tool.  If not, see <http://www.gnu.org/licenses/>.
