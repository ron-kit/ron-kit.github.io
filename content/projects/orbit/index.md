+++
image = "aleasat.png"
date = "2025-01-23"
title = "FFC for UBC Orbit"
type = "gallery"
+++

As the lead of UBC Orbit's OBC (On-Board Computer) subteam, I made various contributions and improvements to the satellite's electronics.

{{<image src="ffc.png">}}

Above is a custom FFC (Flat Flexible Cable) I designed to interface between the OBC and COMMS subsystems.

I had to take a number of factors into consideration for this design:
- The COMMS board processes and amplifies received RF signals, so I had to design this board with high frequency signals of about 1-2A in mind.
- Vacuum and thermal conditions in space - even in low orbit - are much more hostile than those on Earth, so the materials were chosen carefully.
- Instead of the polyester that most COTS cables are made of, I used a polyimide coverlay to minimize degassing, and a gold surface finish for longevity.
- Also, the connection process of the old cable was convoluted and slow, requiring screw insertion, so I designed a receptacle component and corresponding mating process by researching that of similarly sized Molex cables.

{{<image src="layerstack.png">}}

I tested it by applying RF signals of various frequencies to one pin at a time and measuring adjacent traces for EMI. Due the relatively low voltages and lack of any loop area, I did not detect anything with my oscilloscope.

The cable was well received and implemented successfully, and modified versions were integrated into other subsystems.