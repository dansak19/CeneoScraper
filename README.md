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
|opinion’s author|author|span.verified-purchase|
|author’s recommendation|recommend||
|score expressed in number of stars|stars||
|opinion’s content|content||
|list of product advantages|pros||
|list of product disadvantages|cons||
|how many users think that opinion was helpful|up_votes||
|how many users think that opinion was unhelpful|down_votes||
|publishing date|published||
|purchase date|purchased||

