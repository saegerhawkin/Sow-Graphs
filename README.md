# Exploring Sow Data With Python
During my 2019 summer internship at Johnsonville I explored some functionality of Python. I took some open sourced USDA data from their website: https://www.usda.gov/topics/data I was mostly concerned with looking at sow data because this is what Johnsonville purchases for their sausages. I have included the static CSVs that I used for this analysis.

There are three notebook files in this repository. Each one is for a different feature.

### Bokeh
See the Bokeh_sowdata.ipynb for this work. Bokeh is an interactive graphing library I was interested in exploring. I just made a simple bar chart showing the amount of sows by state. I found Bokeh a little clunky, but I was still able to make a helpful graph. Check out the code on here to see the interactive graphs: https://nbviewer.jupyter.org/github/saegerhawkin/sows_python/blob/master/Bokeh_sow_data.ipynb

### Plotly
Both the sow_geograph and sow_dashboard notebooks use Plotly. I enjoyed working in Plotly more than Bokeh. The graph concepts were easier to me, and I found the integration with other packages like ipywidgets, and Dash really cool. 

The sow_geograph file used the same data as the Bokeh file. I wanted to make a heatmap over the US states, showing the same exact data in a map format. I was happy with how the result turned out, although I have a couple issues I couldn't resolve.
- The legends's ticks were not logarithimic like the color scale.
- I could not get commas in between the thousands on the hover tool

The sow_dashboard used the negotiated sows csv file. There are different ways to buy sows. Negotiated sows are the most common way that companies purchase sows so I chose this dataset. The goal of this project was to show the prices broken down by the different weight classes. I first made a line chart that showed how the prices flucuated over time. Plotly made this really simple, and the hover tool made it really easy to compare the different weight classes. Then I made a chart to show the standard deviation because a coworker asked to see if there was a pattern of prices fluctuating that caused standard deviations. We didn't explore this idea further, but it would be interesting to look into further. Then I made some functions and used ipywidgets to see if I could interactively change the graph. This took some work, but in the end I got it to function. 
