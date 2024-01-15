# Random Forest for Inflation Forecasting

This project has been realized by Victor Francey and Rémi Hurstel for the course of ***Macroeconometrics and Machine Learning*** from Professor Simoni.

## Installation

To install the libraries we use:

```
pip install -r requirements.txt
```

We download the macroeconomic data by using the FRED API ([pyfredapi](https://github.com/gw-moore/pyfredapi)).

### FRED API Key

Before using `pyfredapi` you must have an API key to the FRED API web service. You can apply for one for free on the [FRED website](https://fred.stlouisfed.org/docs/api/api_key.html).

Then create a file named `.env` and write `FRED_API_KEY="your_api_key"`. Now save your file.

You can now use the notebook named `download` !

### pyfredapi documentation

You can find the documentation of pyfredapi on this [link](https://pyfredapi.readthedocs.io/en/latest/).

## Structure

The repository contains:

* a folder `data` which contains the inputs we dowload for the model and the meanings of each of the vairables used as imputs
* a folder `figures` which contains some figures showing interessant results
* a Python notebook `download.ipynb` which download the macroeconomics data from the FRED website using `pyfredapi`
* a R Markdown notebook `inflation_forecasting.Rmd` wich contains our model and the different fit and forecasts with analysis.

If you just want to see our Random Forest model, you don't need to run the `download.ipynb` notebook. You only need to use the `inflation_forecasting.Rmd` file.

## Macroeconomics data

List of the data we use:

|    fred code    | Description                                                                                           |
| :-------------: | ----------------------------------------------------------------------------------------------------- |
|    CPIAUCSL    | Consumer Price Index for All Urban Consumers: All Items in U.S. City Average                          |
|     UNRATE     | Unemployment Rate                                                                                     |
|    FEDFUNDS    | Federal Funds Effective Rate                                                                         |
|      M1SL      | M1                                                                                                    |
| MRTSSM44000USS | Retail Sales: Retail Trade                                                                           |
|     UMCSENT     | University of Michigan: Consumer Sentiment                                                           |
|   PCUOMFGOMFG   | Producer Price Index by Industry: Total Manufacturing Industries                                     |
|     W875RX1     | Real personal income excluding current transfer receipts                                             |
|      M2SL      | M2                                                                                                    |
|    DTCTHFNM    | Total Consumer Loans and Leases Owned and Securitized by Finance Companies, Level                    |
|      AMBSL      | St. Louis Adjusted Monetary Base (DISCONTINUED)                                                      |
|    BUSLOANS    | Commercial and Industrial Loans, All Commercial Banks                                                |
|    PCU311311    | Producer Price Index by Industry: Food Manufacturing                                                 |
|     BOPGSTB     | Trade Balance: Goods and Services, Balance of Payments Basis                                         |
|    TWEXMMTH    | Nominal Major Currencies U.S. Dollar Index (Goods Only) (DISCONTINUED)                               |
|  USASARTMISMEI  | Sales: Retail Trade: Total Retail Trade: Volume for United States                                    |
|       IR       | Import Price Index (End Use): All Commodities                                                        |
|       IQ       | Export Price Index (End Use): All Commodities                                                        |
|      IMPGS      | Imports of Goods and Services                                                                         |
|     NETEXP     | Net Exports of Goods and Services                                                                     |
| OECDCPALTT01GYM | Consumer Price Index: All Items: Total                                                                |
|    CMRMTSPL    | Real Manufacturing and Trade Industries Sales                                                         |
|     INDPRO     | Industrial Production: Total Index                                                                    |
|     PERMIT     | New Privately-Owned Housing Units Authorized in Permit-Issuing Places: Total Units                   |
|     GPDIC1     | Real Gross Private Domestic Investment                                                                |
|   MTSDS133FMS   | Federal Surplus or Deficit                                                                            |
|   POILBREUSDM   | Global price of Brent Crude                                                                           |
|      GS10      | Market Yield on U.S. Treasury Securities at 10-Year Constant Maturity, Quoted on an Investment Basis |
|    NONBORRES    | Reserves of Depository Institutions, Nonborrowed                                                      |
|  CES0600000007  | Average Weekly Hours of Production and Nonsupervisory Employees, Goods-Producing                     |
