# hepsiburada-webscraper
 Webscrapping code for hepsiburada comments. I made this code for my NLP project, it is also public here <https://github.com/uguratli/Hepsiburada-Sentiment-analysis>. The code might be run faster with lxml parser, but I did not try it. I already got what I want, maybe for other projects I can try lxml parser.

## Requirements

`beautifulsoup4`
`chime`
`numpy`
`pandas`
`progress`
`Requests`

## Usage

* `hepsi.py` is review collecting code, can not work alone, includes bs4 funcions for collecting reviews from Hepsiburada.com, works for category and product. `hepsi.py` can collect almost half of total reviews, I limited for half because I cant reach all pages via url, after some point url retuns just first page and no need to waste time to collect same reviews again and again.
* `comments.py` is review collecting main code, reads product_list.txt and collect reviews (almost half) for given products. Reviews are filtered according to their stars, for nagative 1-2 and for positive 4-5, `comments.py` reads product urls from `product_list.txt` and filters reviews as negative and positive, and collects reviews with comment, rate, seller name and date, and creates dataframe then save them as pickle file with date. 

## Other files

* `requirements.txt`: List of libraries I used for this project.
* `product_list.txt`: List of product I chose to use for my NLP project.