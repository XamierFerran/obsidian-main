# Introduction
I've recently been thinking about buying a keyboard since Asli is offering to buy me one for dropping alcohol all over my current one. While I have found plenty of nice 65% keyboards and done research on which key switches I want (Cherry MX Browns), I don't actually think I need it. My current keyboard works well enough to make me think twice about buying a whole other keyboard that would only work slightly better and have a gimmicky retro color scheme. So, instead of doing that, I thought I'd make my own keyboard case!

This project didn't come out of nowhere in my mind. I've been meaning to build a keyboard/macropad for the past maybe three years. I have the key switches, key caps, microcontrollers, solder, soldering iron, wiring, even rough CAD. However, for some reason I can't seem to make this project come to reality. I think there is some sort of "lock-in" event horizon that I haven't reach yet where I can't see what to do next but really the solution is to do something at all. 

Anyways, instead of continuing that project and 3D printing a keyboard case, I'll just completely pivot to a related project but with an entirely different skill set. I'm going to make a **wooden keyboard case!** I'm also going to try a new form of documentation where I let my writing be driven by the questions I ask myself. Here goes nothing

## I want to create a wooden keyboard case! What are the tools at my disposal?
Nolop has a **CNC mill (Tormach 440c)**, an **X-Carve**, a **route**r, **dremel**, and **sandpaper**. Though I've seen a video on someone making a case using sand paper and a router [I Turned This Block of Wood Into a Keyboard](https://www.youtube.com/watch?v=TShpMoFeHvs&ab_channel=JDTechGear), I would like to learn how to use the X-Carve as the skills are transferable to a CNC mill. 

## Does the X-Carve have movement in the Z direction?
Yes, supposedly. I ask this question because I anticipate needing to lift up and drop down the end mill to create the case. This is informed by my training on a manual mill in Bray Lab.

## How do I use the X-Carve, and how could I use it to create a keyboard case?
![[guide-x-carve.pdf]]

## How do I do the electronics!?!?
Honestly, in the video I mentioned above, the creator actually just uses a pre-made pcb board which meant all he had to do was solder and put the key caps in. I'm not sure what he did for software so that is a mystery, but I think i might prefer to buy a pre-made pcb.

I ended up buying one from [Mode Design](https://modedesigns.com/products/envoy-pcb?_pos=1&_psq=65%25+pcb&_ss=e&_v=1.0). I found that this was on the cheaper end of most of the pcb's and it is a 65% keyboard. If I'm being honest I'm not even entirely sure about all of the features of this pcb (how does it power? Can I extend it?), but I will figure it out once I get it in my hands. 

## What kind of wood should I use?
Home Depot is cheap and accessible, that will almost certainly be where I buy from. Unless I find good scrap in Nolop's scrap bin. I found out there is dimensional lumber in Home Depot's selection, which is preferable since I don't want thin ply wood or like a 2x4 or 1x3. I need thicker wood at least for the case.

## Do I need a keyboard plate?
Apparently no, but also it heavily dictates how the keyboard would feel. I feel like it would be interesting to see how my keyboard would feel without a plate, and then when I install a plate. Plates are also usually made of metal or tough plastic like polycarbonate. I don't see a reason for it to need to be so intense, so I'd be down to try acrylic. If that doesn't work well for me then I can also try an aluminum sheet from bray. I will say, I'm not sure if I can actually switch out the plate after soldering the key switches on. [source](https://akkogear.eu/blogs/news/keyboard-plates-a-quick-guide)

# Action Items
- [x] Buy pre-made pcb
- [ ] Buy block of wood big enough to fit pre-made pcb **(Go to home depot in person to see, or nolop scrap bin just to check)**
- [ ] Buy keyswitches and possibly caps
	- [ ] could be a good idea to use see through caps for right now and then custom 3d printed caps for space bar, enter, etc.

# Purchases

| Bought/Not? | Item               | Link                                                                          |
| ----------- | ------------------ | ----------------------------------------------------------------------------- |
| [x]         | 65% Keyboard PCB   | https://modedesigns.com/products/envoy-pcb?_pos=1&_psq=65%25+pcb&_ss=e&_v=1.0 |
| [?]         | Dimensional Lumber | https://www.homedepot.com/b/Lumber-Composites-Dimensional-Lumber/N-5yc1vZc3tc |

# Resources
- [I Turned This Block of Wood Into a Mechanical Keyboard](https://youtu.be/TShpMoFeHvs?si=G0Y-hR9etNxlM8y3)
- https://geekhack.org/index.php?topic=75773.0
- [Nolop X-Carve Documentation](https://nolop.org/training-x-carve-cnc-router/)
- https://www.youtube.com/watch?v=yYcNi9hKxDk&ab_channel=ZackFreedman

## Video Notes: [I Turned This Block of Wood Into a Mechanical Keyboard](https://youtu.be/TShpMoFeHvs?si=G0Y-hR9etNxlM8y3)
- Person made the keyboard out of two pieces of wood. 
- One thinner for the top of the case that will hide the electronics and be shown off with the keycaps. 
- The other Is thicker and is cut at a 7 degree angle, for a typing inclination