# gquote
R package for intraday market data download from Google or Yahoo Finance
Download intraday data from Google Finance or Yahoo Finance in xts format

Usage:
getIntradayPrice(ticker, src = "google", period = 1, interval = 5, tz = NULL, auto.assign = FALSE, time.shift = 0)

Arguments:
ticker:	ticker for the data to download, a valid Google Finance or Yahoo Finance ticker, include source (exchange) if required.
src: source, can be either "google" or "yahoo"
period:	time period in integer # of days. There are restrictions on maximum amount of data that can be downloaded imposed by the sites
interval:	time interval in integer # of minutes
tz:	timezone, set to NULL by default
auto.assign:	similar to getSymbols in quantmod, set to false by default
time.shift:	(optional) time shift to apply (in hours) to align the time stamp

Return Value: an xts time series

Examples:

x <- gquote::getIntradayPrice("INDEXSP:.INX",period=5, interval=5)    # S&P 500 from Google Finance
tail(x)
