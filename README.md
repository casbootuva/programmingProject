What features will be exposed to the end user, what problem will be solved for the user?

	The data visualisation will show:
		-Which startups are funded by category.
		-At what time did this happened historically.
		-At what place.

	By doing this, a person owning a startup will know where to seek funding. 

A preliminary sketch of what the application will look like?
	
	I added a screenshot of a type of graph that I want to make in the doc directory. I also want to make a chloropleth map.
	Furthermore I have not yet figured out exactly what visualisations I want to make.

What data sets and data sources will you need, how you will get the data into the right form for your app?
	
	The data set I will use is Crunchbase's database. It contains information about venture capital deals from 1999 till now. It is currently in a csv file. I will use python to transform it to JSON. Then I can import it in JavaScript.

What separate parts of the application can be defined (decomposing the problem) and how these should work together?
	
	-Scraping the data from csv.
	-Transforming it to JSON.
	-Make a Choropleth map which transforms over time.
	-Make several other interactive charts.


How the platform will facilitate creating your application, and what external components (APIs) you need to make certain features possible?

	D3 will facilitate making great interactive graphs.

Potential problems that may arise during development and what possibilities you have to overcome these?
	
	-A potential problem might be gettting the startups in to the right category.
	-A problem might also be that certain VC deals are missing from the database. Then the story i am trying to tell is unreliable.

A very short review of similar applications or visualizations in terms of features and possibly technical aspects (what do they offer? how have they implemented it?)
	
	http://letstalkpayments.com/fintech-companies-around-the-world-raised-almost-a-billion-in-december/

	It is the same in the sense that it is also about WHERE venture capitalist funding took place. They have chosen for pie charts and bar charts.