+++
title = '1: Robot'
date = 2024-09-07T23:15:10-07:00
+++

Hello and welcome to the first real content of my blog. This inaugural post will (briefly) document the assembly of my team's robots for the ENPH253 course.

Our challenge this year was unlike any previous one: we had to build not one, but two fully autonomous robots that could cook, assemble, and serve 3d printed food. There were a variety of recipes, ranging from simple salads to deluxe cheeseburgers. 

{{<image src="images/surface.png" caption="Fig. 1. The competition surface.">}}

I took on the role of electrical designer and learned Altium in the first few days of the project. Along with manufacturing some parts for the robots and troubleshooting their behavior with code I iterated through many trial circuits and designed some PCBs.

{{<image src="images/schem.png" caption="Fig. 2. Debouncer circuit by me.">}}

This was one of many circuits used by the robot. Buttons tend to be "bouncy" and provide multiple outputs per press, so this board smoothed out the erratic signal to a single rising edge.

{{<image src="images/board.png" caption="Fig. 3. PCB layout designed by yours truly.">}}

Using my world-class altium expertise I put together this bad boy. The silly graphics are there because our team name was the Krusty Krab. (they should be yellow, as red means wiring... not sure what happened...)

{{<image src="images/render.png" caption="Fig. 4. A stunning render of my immaculate board." >}}

The board looked almost exactly like this in real life. The only issue that arose was the lab running out of the correct size capacitors, so I had to solder two larger ones in series for the same effect. 

{{<image src="images/wiring.jpg" caption="Fig. 5. I wonder who connected this fabulous wiring.">}}

On August 7th, the day before the competition, our robots did not work. So we did what generations of students have done before us and partook in the traditional all-nighter to complete it.

Unfortunately this was my first ever all nighter. The latest I have ever submitted an assignment (and consequently gone to bed) was probably 4 or 5, but until that day I had never witnessed two consecutive sunrises in a row. 

{{<image src="images/ronSunrise.jpg" caption="Fig. 6. It is 5am in this photo.">}}

After testing through the night it was comp day. We had practically rebuilt our robots from scratch and simplified our objective from assembling a burger (which required many steps such as cooking, stacking, and coordinating) to delivering a piece of cheese on a plate. Having once ridiculed the absurdity of this 'recipe' the irony of this was not lost on us.

When it was our turn to shine, we missed the cheese on our first go. On our second, the plate fell through the robot's arms. Then, through frantic last minute adjustments, a miracle happened.

{{<video src="videos/cheese.mp4">}}

This absolute trooper pulled through and served the cheese to the ecstatic audience. Next to our opponents who were cooking up a storm, that may not have looked like much, but I think it was evident in our reaction that the cheese plate was the culmination of hundreds of man-hours of effort, which the audience clearly picked up on. I may be falling victim to self-serving bias, but after experiencing the event and rewatching the stream, I still think our cheese plate got the most vigorous applause of the entire event.
|||
|:-:|:-:|
|![Spongebob](images/spongebob.jpg)|![Squidward](images/squidward.jpg)|
|Spongebob|Squidward|

The keen eyed among you may notice that although the events discussed all occurred during summer, the publishing date is much later. This is because I ~~forgot~~ was very busy and ~~hate microsoft~~ didn't want to set up git in vscode. I tried building the site in codespaces probably at least 20 times using 2 different frameworks, but it would never upload. Today I finally pulled myself together and followed [this tutorial](https://www.youtube.com/watch?v=zrmeOu8DYyw); with some help from chat it actually went quite smoothly. 

Thanks for reading. Rom signing off.