Problem to be solved

A lot of entrepreneurs think it is difficult to find funding for their startup. This visualisation will solve that problem. Therefore the data visualisation will show:
	-Which category startups are funded annually. 
	-At what place.

	By doing this, a person owning a startup will know where to seek funding. 


Graphs
	
I added a screenshot of a type of graph that I want to make in the doc directory. I also want to make a chloropleth map.
Furthermore I have not yet figured out exactly what visualisations I want to make.


Data
	
The data set I will use is Crunchbase's database. It contains information about venture capital deals from 1999 till now. It is currently in an MS Excel file. I will use python to transform it to JSON. Then I can import it in JavaScript.


Steps

The following steps will be taken to solve the problem	
	-Putting the investments in the right categories.
	-Scraping the data from MS Excel.
	-Transforming it to JSON.
	-Make the graphs mentioned above.



D3 Platform

D3 will facilitate making great interactive graphs. There are a lot of documentation and possibilities in this JS library.


Potential problems 

I might run into the following problems while developing my data visualisation:
	
	-Gettting the startups in to roughly 8 categories might be tricky since there are current 4000 different categories.
	-A problem might also be that certain VC deals are missing from the database. Then the story I am trying to tell is unreliable.
	-Making sure the circles in the graph don't overlap.

Similar Visualisations
	
http://letstalkpayments.com/fintech-companies-around-the-world-raised-almost-a-billion-in-december/

It is the same in the sense that it is also about WHERE venture capitalist funding took place. They have chosen for pie charts and bar charts.