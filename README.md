# CollectionBuilder-with-Vegalite-Experiment

I'm trying to create data visualization item type for an child object in CB using [vegalite](https://vega.github.io/vega-lite/) , which is a javascript data visualization library. 
- Specifically, I have a project exploring labor conditions of book scanning workers in the internet archive. Doing data archaeology and analysis, we've found that these working conditions are far worse for book scanning workers employed at business process outsourcing firms in the global South as opposed to their counterparts at academic libraries in the global North. 
- I'm exploring using collection builder to create a website for the project. Each scanning center would be a parent object. It would have multiple child objects serving as data visualizations about working conditions at the scanning center (parent object).

## How I've tried to do it: 
I've created a data-visualization.html layout page which embeds the vegalite-reader.html block. That block turns a vegalite-compatible json file into a data visualization. Each child object has a link to the vegalite-compatible json file in the object_location metadata field. These are stored in a separate github repository for the project (https://github.com/ers6/ia_scanning_labor_data). 

At the moment, each center has 2 child object visualizations associated with it. The first is a bar chart visualizing of the number of books scanned per month over time. The second is a scatter plot showing the ratio of workers working to pages scanned for each month of a center's operation. 

----------

## What Went Wrong? 

Both the bar chart and scatter plot visualizations are not rendering properly in different ways.

The bar chart only shows up after I readjust the size of my browser window (doesn't matter if it's bigger or smaller- it just need to be readjusted to show up at all). The scatter plot doesn't show up at all, but when I copy the json file into vegalite's online editor, it works properly. 

This has led me to believe there's a problem with the sizing of the windows of the vegalite-maker template and the pop-up child window. that's causing the bar chart to not render until the window is readjusted and the scatter plot to fail to render at all. 
