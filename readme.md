## IMDb.com Web Scraper


##### Tom Keith - https://github.com/tomkeith

---

### IMDb URL Structure

IMDb has a great url structure for scraping. Using Star Wars for example: `www.imdb.com/title/tt0076759/`. The IMDb ID - here `tt0076759` - is all that is needed to fetch the page.

IMDb IDs can be sourced from the [IMDb open datasets](https://www.imdb.com/interfaces/ "IMDb open datasets") where these unique IDs are represented in the `tconst` column.

### Why scrape IMDb if there is an open dataset?

IMDb's open dataset was lacking some key features needed for my Movie Genre Prediction project. Most notably it only had 3 genres (the first three alphabetically), where as IMDb.com can have 1-7 genres. Additionally, IMDb's open data does not have any text data (for example plot summary), something I also needed for NLP.

Those reasons are the inspiration behind creating this scraper.

### Movie Posters

The function `imdb_scrape` has an optional second parameter (boolean) to save the movie poster (default location is /posters/ folder).

#### Notes

The main function `imdb_scrape` is meant to be ran in a loop. **The notebook is not meant to be run all at once.** Rather, the main cell (that is not a function) is mean to be manually updated before each running of the cell. See notes before that cell.

---