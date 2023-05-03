# Data Visualization

## Reading

### [Matplotlib Tutorial](https://www.labri.fr/perso/nrougier/teaching/matplotlib/)

## Bookmark and Review

- [Seaborn Tutorial](https://seaborn.pydata.org/tutorial.html)
- [Bokeh Tutorial](https://mybinder.org/v2/gh/bokeh/bokeh-notebooks/master?filepath=tutorial%2F00%20-%20Introduction%20and%20Setup.ipynb)

### Cheat Sheet

- [Seaborn Cheat Sheet](https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Python_Seaborn_Cheat_Sheet.pdf)

---

### Reading Questions

- What are the key differences between Matplotlib, Seaborn, and Bokeh libraries in terms of their features and use cases? Provide an example of a specific visualization that is more suitable for each library.
  - `Matplotlib` is probably the most common Python library for visualizing data. Everybody who is interested in data science has probably used Matplotlib at least once.
    - Easy to see the property of the data
    - Can plot anything
    - It may be complex to plot non-basic plots or adjust the plots to look nice.
  - `Seaborn` is a Python data visualization library based on Matplotlib. It provides a higher-level wrapper on the library which makes it easier to use.
    - Less code
    - Makes common-used plots prettier (e.g., popular plots such as bar plot, box plot, count plot, histograms, etc.)
    - Is more constrained and does not have as wide a collection as matplotlib
  - `Bokeh` is a flexible interactive visualization library that targets web browsers for representation.
    - Interactive version of Matplotlib
    - Linke between plots
    - Because Bokeh is a library that somewhat has a middle-level interface, it often takes less code than Matplotlib but takes more code to produce the same plot as Seaborn

  - "Matplotlib can create any plot because it is a low-level visualization library. Bokeh can be both used as a high-level or low-level interface; thus, it can create many sophisticated plots that Matplotlib creates but with fewer lines of code and higher resolution" [Top 6 Python Libraries for Visualization: Which one to Use?](https://towardsdatascience.com/top-6-python-libraries-for-visualization-which-one-to-use-fe43381cd658#:~:text=Matplotlib%20can%20create%20any%20plot,of%20code%20and%20higher%20resolution.)

  - "Matplotlib is a library in Python that enables users to generate visualizations like histograms, scatter plots, bar charts, pie charts and much more. Seaborn is a visualization library that is built on top of Matplotlib. It provides data visualizations that are typically more aesthetic and statistically sophisticated." [Python Data Visualization With Seaborn & Matplotlib | Built In](https://builtin.com/data-science/data-visualization-tutorial#:~:text=Matplotlib%20is%20a%20library%20in,more%20aesthetic%20and%20statistically%20sophisticated.)

- In the Seaborn library, what are the main functions to create relational, categorical, and distribution plots? Briefly explain the purpose of each type of plot and provide an example use case.
  - relplot / relational
    - scatterplot
    - lineplot
  - displot / distributions
    - histplot
    - kdeplot
    - ecdfplot
    - rugplot
  - catplot / categorical
    - stripplot
    - swarmplot
    - boxplot
    - violinplot
    - pointplot
    - barplot

- Discuss the role of the Seaborn Cheat Sheet in a Python developer’s workflow. What are some key sections or elements featured in the cheat sheet that can help a developer quickly reference Seaborn functionalities?
  - The DataCamp cheat sheet presents the five basic steps needed to make beautiful statistical graphs in Python.
    - Data
    - Figure Aesthetics
    - Plotting with Seaborn
    - Further Customizations
    - Show or Save Plot
