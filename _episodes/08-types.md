---
title: "Choosing a Type of Visualization"
teaching: 10
exercises: 10
questions:
- "What is the difference between continuous, categorical, nominal, ordinal, and proportional data, and how
do these different data types affect our choice of visualization?"
keypoints:
- "Be careful to tailor your choice of visualization to the type of data and the type of information you
are trying to convey"
- "Pie charts only work for parts-to-whole relationships, i.e. proportional data"
- "If relative differences are important in line charts, including the zero-point can be misleading."
- "In bar charts, the area of the bar is proportional to the value displayed, thus leaving out the zero
point in these types of charts can lead to confusion."
---


In the previous sections, you have learned a lot about the different concepts that help us design good
visualizations, like colour and space, and you have been introduced to the cognitive and psychological
concepts that help us design easy-to-read visualizations, like pre-attentive processes and Gestalt
psychology.

But all of that does not answer one very important question: **How do we pick the right type of 
visualization for our data set?**

Let's explore this question using an example. Below is a plot showing the average long distance
trip length in miles for Thanksgiving (a US holiday), Christmas, and the rest of the year:

![pie chart of trip length, with all three slices approximately equally sized]({{ page.root }}/fig/triplength.png)
Image Source: [WTF Visualizations][wtfviz]

> ## Exercise
>
> Do you think this is a good way to visualize this type of data? Why or why not? What type of
> visualization would you choose?
>
> What would you change to make this more easily readable?
>
{: .challenge}

Much has been written about the use and mis-use of pie charts in the data visualization literature. One line of
argument goes that humans are generally better at estimating lengths and rectangular areas than we are at estimating
angles and arc lengths of a circle, which is how differences in value of different categories are encoded in
pie charts.

Regardless of your thoughts about pie charts in general, this is not a good use of them. Why? Because pie charts generally
describe *parts-to-whole* relationship. For example, you could look around the classroom, and query everyone's
home institution, and then make a pie chart of the percentage of participants coming from each institution.
This makes sense, because it describes a part-to-whole relationship: if three out of ten students are enrolled
at the University of Washington, I can make a pie slice that encompasses 30% of the pie. This will make sense, because
this inherently implies that 70% of students are enrolled somewhere else, which is true.

This no longer becomes true for data sets that do not describe part-to-whole relationships, like in the case above.
Average trip length is just a number, it isn't measured relative to anything whole. A better use for a pie chart would
be, for example, if this chart depicted the fraction of time travelled for Christmas, Thanksgiving, and the rest of the
year, relative to the average *total* time that people spend travelling.

This kind of mistake can also be commonly seen in questionnaires, where people are allowed to check multiple answers.
If you have a survey that says, for example, that 80% of people like ice cream, and 60% of people like cake, and
75% of people like chocolate, then representing this as a pie chart will be confusing, because what does it mean
for the percentages to sum up to 215%? It just means that lots of people like all three!

A better way to represent this data would be a bar chart:

![bar chart of trip length]({{ page.root }}/fig/triplength_bar.png)

You can find the code to generate this visualization [in the corresponding notebook][triplength_notebook].
While the bar chart is much less exciting, it is also much easier to see whether the longest distances are
travelled for Thanksgiving, Christmas, or the rest of the year, something that isn't immediately apparent
in the pie chart without the numbers (especially with the 3D perspective added in!).


