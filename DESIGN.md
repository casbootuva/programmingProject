Introduction

This is the design document for my venture capital funding visualisation. It strives to show where it is the most interesting for an entrepreneur to seek funding for his or startup. This document is divided in three sections. Data will contain all information about where the data comes from, how it will be prepared and how it will be loaded in to the program. The visualisation part will contain information about which graphs are used and how they will be made. Finally the user interface part will show the layout of the pages.


Data

The data will be obtained from the crunchbase database. For now, we will only take data of 2015. Some data do not show which country the VC investor is from or don't show how much dollars were invested. We need to dispose that data, we can do this in Excel, where the data is located currently. Then we need to reorganize the investments into broader categories. At the moment they are too specific which is a problem. We will solve this problem by using if statements in Python. Based on keywords in the category field, when can set it to a new category.  For example, if "bitcoin" is found in the category field, set it to the category "financial technology". Then we will dump it to a JSON file.


Visualisation

We will make two graphs that interact with each other. It is hard to explain what they look like with words, so I would like to refer to the scetches that I made. You can find them in this directory. The first one portrays all investments in certain categories by certain countries. These will be represented by a circle. The circle's color shows which category it represents. If the mouse hovers onto a circle, a field will popup showing:
	
	-Which country it is.
	-The percentage how much of total VC funding in this country goes in to this specific category.
	-The absolute amount of this investment in dollars.

Furthemore the percentage mentioned above is also reflected by the position of the circle on the x-axis. This so that the user can immediatly estimate what the nominal amount of the investment is (by looking at the size of the circle) and if it is in important category of startup investment in that country (by looking at the position of this circle). These are both important. By looking at the nominal amount the entrepreneur can see if there is enough funding available in the country for his or her startup. By looking at the relative amount, the user can see if this category is important in that country. You see, if it is a large investment, the entrepreneur can assume there is a lot of expertise in this country for the particular category. 

I understand that this can be a bit unclear now. Therefore I will give an example. Israel has a small economy compared to the USA. Therefore total VC funding in Israel will be a lot less than the USA. Therefore, most of Israel circles will be smaller than the ones belonging to the USA. However, Israel has in one of the best countries in the world at IT security. Therefore a large number of the total amount of VC funding is in the security category. This means that the circle which represents VC investment in IT-security in the US will be larger, however Israel's circle of VC funding in security will be further to the right (it has a higher x-coordinate). If you are an entrepreneur and want to start a security startup, it can be interesting to try and seek funding in both the US and Israel. This is so because in the US there is more money available, however Israel probably has more expertise since such a large chunk of its total VC funding goes into security.

Challenges in the this graph will be to make sure that the circles will not overlap. This can be done with d3.

The second graph will appear if the user presses a button. The circles is the first graph will "drop" to the second graph. There they will be divided per category. So now the x-axis changes to the relative amount invested by each country to the total amount invested in this category. This is really difficult to explain, so please take a look at the sketches. It is shown this way so the entrepreneur can immediatly see where the biggest investments in his or her field take place.

Challenges in the second graph will be to make sure that the circles from the first graph make a nice transition to this graph by "dropping" to the correct place. Also once again it will be challenge to make sure that the circles don't overlap.


User Interface

The user will start at a homepage, explaining the goal of the visualisation. Also the source of the data will be mentioned. The user will click a button and will then be exposed to the graphs. Under the first graphs several conclusions will be drawn from the data. Furthermore next to the second graph conclusions will be drawn from the data. Then the user will now where to start his startup!

