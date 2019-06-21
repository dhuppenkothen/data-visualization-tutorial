---
title: "The Cognition of Visual Information"
teaching: 10
exercises: 10
questions:
- "How does our brain process visual information?"
- "What attributes are pre-attentive, which ones aren't?"
- "How can this knowledge help us design more effective visualizations?"

objectives:
- "Understand the difference between pre-attentive and serial processing of visual information"
- "Understand which attributes are pre-attentive, and which ones aren't"
- "Apply this knowledge to improve a visualization."
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---

Much of what follows is a summary of the excellent review paper "Attention and Visual Memory in 
Visualization and Computer Graphics" by Healey and Enns ([website][healywebsite] or [PDF][healypdf]). 
There is *lots* more to say about visual perception that I can do here. For more detailed information 
on the topic, and some background on the underlying theories of perception, take a look at the 
website and PDF and the references mentioned in both. Another excellent resource is the book 
"Information Visualization: Perception for Design" by Colin Ware. 
Human perception is a fascinating topic! 

How does the human brain perceive visual information? How do we go from ink on a paper, or pixels on 
a screen to an understanding in our minds? 
It might be easy to assume that whatever light falls into our eyes is perceived and stored by our brains.
This is not true, however! Our eyes and brains are not cameras, passively generating more or less faithful 
reconstructions of reality! Healy and Enns liken visual perception to a *"dynamic and ongoing construction 
project, where the products being built are short-lived models of the external world that are specifically 
designed for the current visually guided tasks of the viewer."*

There does not appear to be general-purpose vision! Instead, what we perceive when we are confronted with 
a scene depends on our goals, our expectations, our state of mind, and where our attention is in any 
given moment. There are tasks that we can perform in less than the blink of an eye (quite literally!), and 
there are things that we are equally just entirely blind to without expending a significant amoutn of mental 
effort. Designing a visualization is not simply a matter of choosing shapes and colours: it becomes 
the task of working *with* your viewer's minds to help them make sense of the most important information 
you are trying to convey. The goal is to work with our brains' strengths to guide the viewer's attention, 
and make sure the brain's weaknesses do not impede understanding.

This leads to a number of important questions to think about when designing a visualization:

>
> * How should I represent my data?
> * How can I highlight important values in my visualization?
> * How can I ensure that viewers perceive differences in data accurately?
> * What visual properties draw the eye, and our focus of attention to a particular object?
> * How do we display information without producing visual confusion?
>
{: .callout} 

Thankfully, our brains are pretty amazing, and there are a range of strengths of visual cognition, the 
science of how we perceive things with our eyes, to help viewers understand our visualization.

### Pre-Attentive Processing

There are a number of visual tasks that the brain can perform *incredibly* fast. Initially, researchers 
believed that these tasks happen as soon as the eye takes in an image or a scene, before our attention is 
directed anywhere. More recent work suggests, however, that attention plays a crucial role in all visual 
perception, and that we can miss important elements in a scene when our attention is directed away from 
them (more on that below). 

In this sense, the term "pre-attentive processing" is a bit of a misnomer, but has stuck around for its 
descriptiveness. More generally, researchers consider a task pre-attentive if a viewer can 
perform the task in large, multi-component displays of information in less than 200-250 milliseconds 
(this is really short!).

As an example, consider the two figures below, taking from [Healy & Enns, 2012][healypdf] (Figure 1). 
Which of the two contains a red dot?

![two-panel plot, the left side contains only blue dots, the right panel contains blue dots as well as a single red dot]({{ page.root }}/fig/preattentive1.png)

For most of you, the answer was probably fairly obvious. The red dot (called the "target") "pops out" 
at us from the sea of blue dots (also called "distractor").. 
We don't need to think about it, and we don't need to search each dot until we find the right one. The 
red dot is just *there*. This is pre-attentive processing at work, and colour is a strong pre-attentive 
feature. 

We can repeat the same experiment with shapes (from the same figure). Which of the following two panels 
contains a red dot?

![A plot with two panels, the left one contains red squares, the right one red squares and a single red dot]({{ page.root }}/fig/preattentive2.png)

Again, many people can perform that task reasonably quickly, without having to search through every shape 
until they find the circle. The circle is just there, the eyes drawn instinctively. Shape, or more accurately, 
curvature, is a preattentive task. 

There a whole number of pre-attentive features (see also Figure 2 of [Healy & Enns, 2012][healypdf]), among 
them size, orientation, length, density, hue, luminance, intersections, 3D depth, direction of motion, and 
lighting direction. Encoding information using pre-attentive features helps guide our eyes to the most 
important pieces of information in a visualization. For example, if there's a particular data point in your 
scatter plot that is important, give it a different colour to make it pop out!

What happens if you *combine* pre-attentive features? What happens when you're trying to find a red dot 
in a figure filled with red squares and blue circles?
Let's give it a try. In the figure below, which panel has a red dot?

![]({{ page.root }}/fig/preattentive3.png)

If you're anything like me, this was *much* harder and took *much* longer. The reason is that both the 
shape (circle) and the colour are present in the distractors (though not together). Trying to find two 
separate attributes in an ensemble of distractors that contain the same attributes (even though not together) 
is no longer a pre-attentive task. Instead, we have to search through the elements one by one until we 
find the one that matches our target. This requires a lot more time and mental energy. 

One of the cognitive theories aiming to explain pre-attentive processing suggests that similarity plays a
crucial role in finding patterns. The more similar the target and the distractors are, the harder it is 
to pick out the target. But this theory suggests that the similarity between distractors *also* plays a 
role in pre-attentive processing: the more dissimilar distractors are to *each other*, the harder it 
becomes to pick out the target.

> ## Exercise: Try it yourself!
>
> Healy has a great little online app that lets you try this out yourself: you can find it
> [on his website][healyapp].
>
> The apps hows you images like the ones you've seen above, with circles or squares, where your
> task is to figure out whether there's a red dot in each of them. The image will be shown to you 
> for a very short time, and afterwards it will tell you whether a red dot was present or absent, 
> which allows you to figure out whether you found it or not.
>
> The app allows you to choose whether to display colours, shapes or the conjunction of both. 
> it also allows you to choose the time in milliseconds that a display will be shown to you, 
> the number of distractor elements, and the number of times you'll be shown an image. 
>
> How does your performance for pre-attentive tasks depend on the time the image is shown to you, 
> the number if distractor elements, and the type of task (colour, shape, both)?
> 
> Start out with colour, and systematically vary the exposure time from 500ms to 100ms. 
> Do ten trials per exposure time. How does your accuracy of prediction change?
>
> Now pick the lowest exposure time that gives you good accuracy, and vary the number of elements. 
> Does your performance change significantly>
> 
> Repeat the exposure time experiment with shape and the combined shape and colour versions.
> Is your minimum exposure time signfiicantly different for these cases? 
{: .challenge}

We have seen how some attributes make cognition very fast, and how combinations of attributes 
loose this cognitive advantage. How do we use this knowledge in visualization?

> Pre-Attentive Features
> 
> When encoding the most important information in your visualization, choose features that 
> are pre-attentive, and avoid combinations of attributes that require a serial search to 
> find and undersstand.
>
{: .callout}





[healywebsite]: https://www.csc2.ncsu.edu/faculty/healey/PP/#jscript_search
[healypdf]: https://www.csc2.ncsu.edu/faculty/healey/download/tvcg.12a.pdf 
[healyapp]: https://www.csc2.ncsu.edu/faculty/healey/PP/#jscript_search


{% include links.md %}






