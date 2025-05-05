# CeneoScraper

## Algorithm for extracting opinions about single product from Ceneo.pl
1. send reqest for accessing first webpage with opinious about progect
2. If response is Ok, parse HTML page content into DOW sructure
3. Extract and their components from DOW opinions 
4. Save opinions with their components to complex data structure
5. is there are more pages with opinions, repeat steps 1-5
6. save  data structure with opinions into database

## Structure of single opinion in Ceneo.pl
|Component|Veriable|Selector|
|---------|--------|--------|
|opinion|opinion|div.js_product-review|
|opinion ID|opinion_id|[data-entry-id]|
|opinion’s author|author|span.user-post__author-name|
|author’s recommendation|recommend|span.user-post__author-recomendation > em|
|score expressed in number of stars|stars|span.user-post__score-count|
|opinion’s content|content|div.user-post__text|
|list of product advantages|pros|div.review-feature__title--positives ~ div.review-feature__item|
|list of product disadvantages|cons|div.review-feature__title--negatives ~ div.review-feature__item|
|how many users think that opinion was helpful|up_votes|button.vote-yes span|
|how many users think that opinion was unhelpful|down_votes|button.vote-no span|
|publishing date|published|time[datetime]:nth-of-type(1)|
|purchase date|purchased|time[datetime]:nth-of-type(2)|

84514582
107530595