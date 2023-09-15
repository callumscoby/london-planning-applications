The 35 planning authorities in London collect, aggregate, and disseminate their applications in different formats. In this project, only 33 of the 35 authorities were scraped, as Brent Borough Council employs stringent reCaptcha security measures, and the London Legacy Development Corporation does not publish application outcomes, rendering such scraping useless. 

Of the 33 portals scraped, many share similar back-end infrastructure. For instance, the Wandsworth, Merton, Islington, and Camden planning authority portals are all developed by Northgate. Similarly, the planning portals of 17 of the 33 planning authorities are all developed by IDOX Solutions. This means that the same code can be used to scrape portals of the same provider. In cases where the infrastructure of a planning portal is unique to the authority, such as Harrow, these portals were scraped individually.

Below are 11 Python files covering the scraping of the 33 planning authorities. At present, the code is lengthy and effectively employs a brute-force strategy (i.e., if an error is encountered, try again and try again). 
In future, it will be refactored to enhance its reproducibility and ease of understanding.
