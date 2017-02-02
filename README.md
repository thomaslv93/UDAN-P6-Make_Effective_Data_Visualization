# Udacity Data Analyst Nanodegree
# Project 6 - Data Visualization

## Summary

This is a data visualization depicting the total security delays per month at U.S. airports since the founding of the TSA (Transportation Security Administration). The map remains unchanged for about 20 seconds at the beginning since there were no recorded security delays in those months, but the animation is in progress and after the animation is finished, you can use the timeline at the bottom to click through different months and look more closely. Notice the roughly sinusoidal pattern in the timeline (which doubles as a histogram) with peaks in winter and summer months (common vacation periods) and troughs in spring and fall months as well as the extreme delays in August of 2006 related to the 2006 transatlantic aircraft plot which led to the banning of liquids and gels on US aircraft. Also notice that delays are most common at global and regional hubs like Los Angeles, Chicago, New York and Houston.

## Design

I wanted to design a bubble map which would show the flight delays over time at each airport. First I used SQLite3 to manipulate the RITA flights data to give me the total security-related flight delays (in minutes) for each airport for each month (I assumed that all security related flight delays occured at departure and so were related to the airport of origin). I then cross referenced the database of airports, their names and coordinates and cut this down to only the airports relevant to the flights dataset, since apparently there were many airports which were not included in the flight data I had. First I plotted all of the relevant airports onto the map, then I decided to update their size and color to represent the security-related delays in minutes over time. After I received the first feedback I updated the projection to include Alaska, Hawaii, and Puerto Rico with a projection from Mike Bostock's blog. I also adjusted the bubble aesthetics and transition and added a title to each bubble which can be read when hovered over. After the second round of feedback I added a timeline which doubled as a histogram of the total minutes security-delayed across the country. The timeline also kept track of where we are in the animation. After the third round of feedback I used color to differentiate between the different years on the timeline and added interactivity so that after the animation is completed the user can click individual months to see what the map looks like there. I also added hover information to the timeline and added a title to the visualization, including one which updated with the month and year.

## Feedback

- Feedback on Version 1: A better map type which shows Alaska and Hawaii would be ideal. Also the bubbles could transition more smoothly, allow for viewing of overlapping bubbles, and look more aesthetically pleasing. You should also add information for each bubble which you can get when you hover over, like the airport name and the delay in minutes.
- Feedback on Version 2: This would benefit from some kind of timeline which shows where you are in the animation.
- Feedback on Version 3: The timeline is good, but you should differentiate it by years. You should also add some interactivity and add a title to your visualization.

## Revised

In my second submission I have removed references to the TSA and focused only on the months where there is reliable data. I have adjusted the size of the bars so that the seasonal variation is more visible. I have adjusted the color coding so that now the years are differentiated by the color of the text label (red vs black) and the seasons (winter and summer vs fall and spring) are differentiated by bar color. I also added a paragraph at the beginning directing the reader's attention to the interesting parts of the visualization.

## Revised 2.0

In my third submission I have added a simple axis to the timeline which measures the security delay in hours.

## Resources
- [d3Vienno youtube channel](https://www.youtube.com/watch?v=n5NcCoa9dDU&list=PL6il2r9i3BqH9PmbOf5wA5E1wOG3FT22p)
- [Mike Bostock's blog](https://bl.ocks.org/)
- [AlbersUSA + PR](https://bl.ocks.org/mbostock/5629120)
- [d3js.org](https://d3js.org/)
