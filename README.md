This project is a continuation of the [Lazy Prices](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=1658471) paper published by Lauren Cohen of HBS which speculated that a magnitude of changes in the content of a company's quarterly filing would indicate that their stock is likely to drop.

This is based on the theory that companies are reporting the bare minimum required by the SEC, that any changes would more likely than not be to disclose risk to stakeholders and that one could make a profitable trading strategy by shorting companies whose quarterly filings change substantially compared to their typical reporting pattern.

The following steps were taken to generate the data required for testing Cohen's hypothesis: 

`notebook_474_zipline.ipynb` was used for:
- download list of tickers from NASDAQ, NYSE, AMEX and the corresponding ciks (SEC labels for tickers)
- scrape the data from the SEC(only the 10ks were downloaded for this project)
- preprocess: HTMLs to txt
- get cos similarity and jaccard scores

`final_10k_data.ipynb` was used for:
- searching the 10k folders to see which ciks where processed from our stock list
- adding the dates to the to the scores
- generating a list of ciks/tickers/scores/date ranges
- create final_ciks.txt containing ciks worth looking into for further analysis
