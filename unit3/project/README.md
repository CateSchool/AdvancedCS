# Final Project

  - [I. Overview](#i-overview)
    - [1. Google Colab Notebook](#1-google-colab-notebook)
    - [2. Visual Data Essay](#2-visual-data-essay)
  - [II. Suggested Timeline](#ii-suggested-timeline)
  - [III. Resources](#iii-resources)
  - [IV. Copying Code](#iv-copying-code)

---
## I. Overview 
Students will analyze and visualize large data sets in the creation of a web-based visual essay. Students will begin by selecting a personally-relevant **theme** (e.g. public health, mass incarceration, climate change, or affordable housing). After amassing related datasets and performing quantitative analysis, students will tell a persuasive, engaging story about the data using code.

The project consists of two parts:

1. [Google CoLab Notebook](#1-google-colab-notebook) - a Python "lab notebook" that documents the process of collecting, cleaning, understanding, and analyzing your data. 
2. [Visual Data Essay](#2-visual-data-essay) - a HTML/JavaScript web-based report that tells a **coherent, unified story** based on your data analysis. This report mixes interactive visualizations with narrative text.

![data viz](assets/data.jpeg)
### 1. Google Colab Notebook
As you're first starting to make sense of your data, your initial ideas and analysis will comprise your Google Colab Notebook. Google Colab allows you to mix text and Python code snippets. 

[Here is a notebook demo](https://colab.research.google.com/drive/1KXW8jxytbLFwOS8diw428mTMqZ-LwBKt?usp=sharing).

Your Google Colab Notebook should loosely resemble a lab notebook that works through the **scientific method** in order to draw conclusions from your data. (Where relevant) your notebook should have the following sections:

1. *Title Block* - name, date, quick overview
2. *Table of Contents* - links to other sections
3. *Dataset Overview* - a link to and overview of (e.g. column names/ data types) the dataset 
4. *Guiding Questions* - questions you intend to explore about the data 
5. *Exploratory Analysis* - explore your data and make observations using simple plots, graphs, etc
6. *Hypotheses* - form some conjectures based on the observations
7. *Quantitative Analysis* - e.g. mean, median, mode, aggregation, linear regression ...
8. *Conclusions* - summarize what you learned about the data
9. *Data Output* - a cleaned dataset ready to be exported / visualized
10. *Citations*
 
### 2. Visual Data Essay
Once you have analyzed your data, you need to present the information and conclusions in a compelling, engaging, and polished web-based report that combines narrative text and interactive data visualizations. 

The report should include:  

* **3 visualizations taking different analytical approaches**  
  * *At least 1* must be creative & **innovative** (i.e. more novel than bar charts, scatter plots, pie charts, histograms, etc.) 
  * *At least 1* of your visualizations must include some form of **interaction**. 
  * *At least 1* must use D3.js
  
* **Written explanations, context, and analysis** to support the visual narrative and make a persuasive argument about your topic (>= 300 words).

* Strongly encouraged to **try additional JavaScript libraries** (e.g. [Leaflet.js](https://www.youtube.com/watch?v=nZaZ2dB6pow&t=2s), [mappa.js](https://mappa.js.org/docs/taxi-routes.html), chart.js, three.js, ...)

Each visualization should include:  

* its own Javascript file but be embedded within the HTML report
* documentation
  * Whenever relevant, include axis labels, units, titles, and legends.
  * Include a link to the data source in a comment in the code, as well as a citation of the source (for example, a label at the bottom of the chart)

---
## II. Suggested Timeline

| **Week** | **Date** |       **Topic**      |
|:--------:|----------|:--------------------:|
|   23-25  |    ...   | Introduction to Unit |
|    26    |   4/11   | CoLab Report         |
|    27    |   4/18   | CoLab Report         |
|    28    |   4/25   | Data Viz 1           |
|    29    |    5/2   | Data Viz 2           |
|    30    |    5/9   | Data Viz 3           |
|    31    |   5/16   | Finalize Reports     |

---
## III. Resources
**Data sets**
* [Kaggle](https://www.kaggle.com/)
* [Google Dataset Search](https://datasetsearch.research.google.com/)
* [Data.gov](https://data.gov/)
* [NASA Earth data](https://earthdata.nasa.gov/)

**Useful sites** 

* [Flowing Data](https://flowingdata.com/)
* [Pudding](https://pudding.cool/)
* [NYT Graphics](https://www.nytimes.com/spotlight/graphics)
* [Information is Beautiful](https://informationisbeautiful.net/)
* [Reddit r/dataisbeautiful](https://www.reddit.com/r/dataisbeautiful/)

**Visual Essay Examples**

* [Chicago's Million Dollar Blocks](https://chicagosmilliondollarblocks.com/#12/41.9093/-87.6872)
* [NYT Tulsa Massacre Visualization](https://www.nytimes.com/interactive/2021/05/24/us/tulsa-race-massacre.html)
* [Women in Headlines](https://pudding.cool/2022/02/women-in-headlines/)
* [The Marshall Project](https://www.themarshallproject.org/2020/12/18/1-in-5-prisoners-in-the-u-s-has-had-covid-19)

---
## IV. Copying Code
For some visualizations, particularly if you're using D3.js, you will want to start with sample code. It is fine to copy/paste the examples **as long as**:

1. There is a comment with a URL documenting the source.
2. You change the code in a meaningful, significant way.