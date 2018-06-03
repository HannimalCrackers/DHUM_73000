
I made one dashboard with floating containers that looks great in Tableau Public, both on desktop and web, but it looks terrible and everything is crashing together when I embed it into this blog.

{% include parksdash1.html %}


I made a second dashboard, this one with fixed containers. It also looks jacked. 

{% include parksdash2.html %}


I also tried embedding individual sheets from the same uploaded workbook, but I didn't like the tab running along the top. I want only the individual chart to show, without tabs available to toggle between charts. I don't know if that's possible.

Here's an example of what I didn't like, with the tab running along the top.

{% include parkschart-tabfail.html %}


My workaround for this assignment ended up being to load each sheet to Tableau Public individually, which seems inefficient and takes up a lot of space because each sheet carries the whole workbook with it. But that was the only way I could figure out how to get the result I wanted. 


[There's no place like home](./index.md)
