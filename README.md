# gquote

``NOTE``: Since both Google and Yahoo have severly curtailed their financial data distribution services, this repository is no longer maintained.

The goal of this R package (gquote) is to provide a method to access intraday stock quotes from google or yahoo finance. The frequency and maximum history of data and available tickers depend on the respective data sources. Also note some of them may suspend data access (temporarily) if this function is used many times in quick succession.

## Installation

You can install from github with:

```R
# install.packages("devtools")
devtools::install_github("prodipta/gquote")
```

## Example

This is an example which shows you how to download intraday data. The default source is Google Finance.

```R
?getIntradayPrice
x <- getIntradayPrice("INDEXSP:.INX",period=5, interval=5)
tail(x)
```



