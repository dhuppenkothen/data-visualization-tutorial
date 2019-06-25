---
title: "Visual Hierarchy and Gestalt Psychology"
teaching: 10
exercises: 0
questions:
- "How can we ensure that a visualization as a whole is consistent and presents information clearly?"
objectives:
- "Familiarize learners with basic principles of Gestalt psychology"
- "Introduce core principles: similarity, proximity, connection, enclosure, interpolation, completion"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---
Gestalt principles were introduced by German psychologists in the 1920s. “Gestalt” itself is a German word 
meaning “shape” or “form”. It encompasses the idea that when you put certain elements together, the 
combination of these elements produces something new (this is where the common saying “the whole is greater 
than the sum of its parts”). You’ve all used Gestalt principles before! 

One common example is the principle of similarity: things that are similar in size, shape or colour 
are perceived as belonging together. 
When you colour data points of one type of data in red, and data points of another type of data in blue, 
viewers tend to implicitly understand that the red points belong together, and are somehow different from 
the blue points. But in design, the principle of similarity extends further than the colour of data points 
to all elements of the page, including font, type size, orientation and white space. 

Here’s a summary of the Gestalt principles as currently known:
* Similarity
* Proximity
* Common fate 
* note that proximity and common fate are special cases of similarity for position + velocity
* continuity, good continuation
* closure
* these principles pervade all perceptual experiences, e.g. camouflage
* generalized common fate: also holds for changes in luminance
* synchrony: elements that change simultaneously are grouped together
* common region: tendency for elements that lie within the same bounded area or region to be grouped together
* element connectedness: tendency for distinct elements that share a common border to be grouped together
* uniform connectedness: where do our individual forms come from? What makes a dot a “dot” and a line a line?
 Uniform connectedness is the principle by which the visual system initially partitions the image into a set 
 of mutually exclusive connected regions having uniform or smoothly changing properties, such as luminance, 
colour, texture, motion and depth.

So what does this mean in practice? Let’s explore these principles. 

Here are some dots. If I space them equally, you’ll probably see them just as a line of dots (although the 
fact that I said “line” is already significant, because it means you already perceive them together by virtue 
of being different from the rest). 

![Four black dots arranged in a row, spaced equidistantly]({{ page.root }}/fig/gestalt1.pdf)

Now if I move the dots closer to one another, but leave some space between them, what do you see? 

![Four black dots arranged in a row, with a larger space between dots 2 and 3 than 1 and 2, 
and 3 and 4]({{ page.root }}/fig/gestalt2.pdf)


Would you still describe the picture above as a line of dots, or rather pairs of dots? I would do the latter, 
and that is an outcome of the principle of *proximity*: elements that are close together are perceived as 
belonging together. One place where this might come in handy is when designing multi-panel figures. Imagine 
you had a number of plots that should be read as a sequence, e.g. from left to right. It might be helpful 
to design your panels such that they form a line, like so:

![Four black rectangles denoting panels in a row, spaced equidistantly]({{ page.root }}/fig/gestalt3.pdf)


But imagine that plots 1 and 2 show result A, and plots 3 and 4 show result B, where they are definitely 
different. You might want to move the plots belonging together closer together, either in a single row 
or in two rows:

![Four black rectangles denoting panels in a row, with panels 1 and 2, and panels 3 and 4 grouped closer 
together]({{ page.root }}/fig/gestalt4.pdf)


![Four black rectangles denoting panels, with panels 1 and 2 stacked above 
panels 3 and 4]({{ page.root }}/fig/gestalt5.pdf)


In this way, the principle of proximity can help you organize your information so that a reader can 
easily figure out what belongs together and what doesn’t. 

We already spoke a little bit about similarity earlier, so let’s go back to our dots. Similarity extends 
to many different properties, including colour, shape and size. Let’s pick colour for now. 
Here’s an example of how similarity by colour works:


![Four dots in a row, spaced equidistantly; dots 1 and 2 are purple, 
dots 3 and 4 are blue]({{ page.root }}/fig/gestalt6.pdf)

Even though the points are equally spaced, they tend to appear to viewers in experiments as two pairs of 
points, distinguished by their colour. We can make a more complex version of the same principle:

![eight dots in blue, eight in purple, forming two wavy patterns]({{ page.root }}/fig/gestalt7.pdf)

Even though the points are scattered throughout one another, there is still some coherent structure due 
to the colour differences. Similarity extends to more complex properties, too, for example parallelism:

![eight dots in blue, eight in purple, eight in orange, forming wavy patterns, with 
orange and blue dots following the same pattern]({{ page.root }}/fig/gestalt8.pdf)

Notice the parallelism between the blue and the orange dots? You would probably consider them grouped 
together, and distinctly different from the purple dots. This is also a a good example of how gestalt 
principles work hierarchically to make sense out of images: first, things are grouped together by 
colour, so that we have three distinct wavy groups of dots, and then from there, we can tell that the 
orange and blue groups of dots are similar to one another, and dissimilar from the purple dots. 


Another important Gestalt principle is that of element connectedness: elements that are connected in 
some way are perceived to belong together:

![eight blue dots, eight purple dots, with purple dots connected to each other by a line, and blue 
dots connected to each other by a different line]({{ page.root }}/fig/gestalt9.pdf)



This makes the similarity perceived through colour much stronger, but it also holds if I take away the 
colour differences:

![two sets of eight dots each in purple, with each set interconnected by a 
line]({{ page.root }}/fig/gestalt10.pdf)


This example also explains another Gestalt principle: the principle of continuity. According to this 
principle, continuous lines/borders are perceived to belong together. In the picture above, we tend 
to perceive things as continuous lines that cross one another rather than assuming that the points before 
the first intersection belong to one another, and the points between the intersections belong together, 
and the points after the second intersections belong together. 

The principle of continuity is much stronger, however. Take a look at the following figure:

![left side: a purple rectangle and blue blue round shape partly occluded by the rectangle;
right side: only the outline of the same rectangle is visible, revealing that the occluded shape is of 
a ping-pong bat]({{ page.root }}/fig/gestalt11.pdf)



If I asked you what the shape of the blue object is, what would you say? Most people would assume that the 
full shape is a circle, but that need not be true. In this case, it’s actually a ping pong bat! In general, 
however, people tend to perceive the simplest shape they can.

Let’s go back to our data points again. Another important principle for data visualization is the 
principle of common region or closure: closed lines are often perceived to belong to the same object, 
and objects enclosed in the same bounded region are also often perceived as belonging together. 
Let’s see an example:

![eight blue dots, eight purple dots, blue dots connected by a line, purple dots connected by a line, 
with a single purple and a single blue dot jointly enclosed by a thick black 
rectangle]({{ page.root }}/fig/gestalt12.pdf)


Enclosing those two points in a common rectangle makes them appear to be related. Interestingly, this is 
true despite both colour and the connections telling us differently. *Not all principles are
perceived equally strongly* 
Here, the principle of enclosure supercedes the principles of connectedness and similarity. 

So far, we’ve been talking about groups of dots. But one thing you might ask is: are these dots the 
fundamental unit of perception? Why do we see dots and then apply Gestalt principles to them, and can 
the dots be decomposed into something more elementary? This is where the more recent **principle of 
uniform connectedness** comes in: uniform connectedness is the principle by which the visual system 
initially partitions the image into a set of mutually exclusive connected regions having uniform or 
smoothly changing properties, such as luminance, colour, texture, motion and depth. That is, the our 
brain considers a dot a single coherent unit because it has the same colour throughout, separated 
from other units (e.g. other dots and lines) that for themselves have some form of uniformity 
(here in colour). 

There are a number of Gestalt principles that we haven’t talked about here, because they relate to 
motion. This is less important in static data visualization, but turns out to be important when 
looking at animations or interactive visualization. One important property is that the principle 
of similarity also extends to motion. This was originally called “common fate”, and indicates 
that if certain elements move in the same direction, they are considered to belong together. 
This works not just in physical motion, but also for synchronous changes of the object properties. 
For example, objects that change luminance in a sycnhronized way are also perceived to belong 
together, even when they are stationary. 

So what does this mean for our data visualizations? Much like with pre-attentive processing, 
take care to work *with* your reader’s visual system, rather than against it. Use the principles 
of Gestalt psychology to group things together that actually belong together, and avoid grouping 
dissimilar things in similarity or proximity. Use things like lines and closures judiciously, 
because they can present very strong cues that elements belong together. And finally, use different 
types of Gestalt to help make things clear. For example, employing multiple principles of Gestalt 
in the same direction (as we’ve done with colour and connectedness above) can help make the 
meaning of your visualization clearer.


> ## Exercise
>
> Take a recent visualization, slide, website or other document you’ve created. Do you think 
> there are ways you can use the principles of Gestalt to make it easier for viewers to 
> understand the key points? Which priniciples can you use to organize the relevant information 
> in an easy-to-view way. Write down the key points of your document/visualization/slide/website,
> and then connect them to the Gestalt prinicples you can use to communicate them effectively.
> Draw a sketch of your new design, and label the principles you've used on your sketch.
> Then share with your partner, and share feedback.
>
{: .challenge}



{% include links.md %}


