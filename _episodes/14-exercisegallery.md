---
title: "A Gallery of Figures"
teaching: 0
exercises: 0
questions:
- "What great visualizations do our learners come up with?"
objectives:
- "Show off the visualizations learners have made during the exercise."
keypoints:
- "Data visualization is fun!"
---

This is a document where learners can share the data visualizations they've generated. 

To add a visualization:
* Go to the [github repository](https://github.com/dhuppenkothen/data-visualization-tutorial) associated
with this tutorial
* Make sure you are logged into your GitHub account!
* Click the button in the upper right corner labelled "fork". This will generate a copy of the repository 
on your own github account. It should say "forked from dhuppenkothen/data-visualization-tutorial" beneath 
the name of the repository if you click on the newly forked repository on your GitHub home screen.
* Click the green link labelled "clone or download"
* Copy the link shown there, then open a terminal window and navigate to a directory where you want to 
keep this repository (at least temporarily)
* type `git clone [link you just copied]`, where you replace the square brackets and the text within with 
the link you copied on GitHub
* move into the repository directory using `cd`
* now type `git checkout -b myname_dataviz`, where you replace `myname` with your name. This will check 
out a new *branch* (if you're new to version control and branches, take a look at the [git book](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging) for an explanation. Branches are great! No matter what 
you do, which files you delete or add or modify, you *cannot break anything* in the original repository. 
All your work happens essentially in a kind of separate copy. 
* Okay, now copy your data visualization into the `/fig/` folder of the repository
* Modify this document, which you can find under `/_episodes/14-exercisegallery.md`, by copy-pasting the 
template code below, and modifying it with your name, the filename of the visualization, and the location of your 
code (e.g. in your own github repo).
* how use `git add 14-exercisegallery.md` and `git add ../fig/myvizname` to tell git about the changes. Replace
`myvizname` with the file name of your visualization
* Use `git commit -m "an informative message"` to commit your changes with a message that tells a viewer 
what you've just done.
* Type `git push` to push your changes to the copy of the repository on your account on Github.
* Now move back to the [original github repository](https://github.com/dhuppenkothen/data-visualization-tutorial) 
There should be a tab called `pull requests`. Click on that.
* Click the button `New pull request`
* In the tabs called `base` and `compare`, leave `base` unchanged, and change the name in `compare` to 
the name you gave your branch earlier (i.e. whatever you `myname_dataviz` with when you did `git checkout -b`). 
* Click "Create Pull request", and you're done! You've created a pull request!

Here's some sample code for you to use when adding a visualization to this file:

> ## Sample Code for Data Visualization
>
> ### Daniela's fancy new visualization
>
> This is a visualization I made for this exercise. It is awesome!
> ![add your alternative text here]({{ page.root }}/fig/myvizname)
> You can find the code or Jupyter notebook for this figure [at this address](add/your/repository/here).
>
{: .language-markdown}
 
If you copy and paste this code from the website, you should be fine. Replace the placeholder text 
for the alternative text in the square brackets, `myvizname` with the filename of your image file, 
and the dummy `add/your/repository/here` for the link.

If you copy-paste this in the markdown file directly, please remove the `>` that appear before the text 
and the commands, and remove the `{: .source}` marker at the end. These are commands that tell the 
compiler to display the commands on screen, rather interpret them as commands.  

{% include links.md %}
 
